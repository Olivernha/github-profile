<script setup>
import { onMounted, reactive, ref ,computed ,watch } from "vue";
import TheAccStatus from "./components/TheAccStatus.vue";
import TheAvatar from "./components/TheAvatar.vue";
import TheRepositroy from "./components/TheRepositroy.vue";
import TheSearch from "./components/TheSearch.vue";

const search = ref('github');
const showAllRepos = ref(false);

const result = reactive({
  name:'',
  bio:'',
  avatar_url:'',
  followers:'',
  following:'',
  location:'',
  repo:[],
})


const displayedRepos = computed(() => {
  return showAllRepos.value ? result.repo : result.repo.slice(0, 4);
});

const fetchAllRepo = () => {
  showAllRepos.value = true;
};
const fetchUserData = async (username) => {
  try {
    const response = await fetch(`https://api.github.com/users/${username}`);
    if (!response.ok) throw new Error('User not found');
    const data = await response.json();
    result.name = data.name || 'No name available';
    result.bio = data.bio || 'No bio available';
    result.avatar_url = data.avatar_url;
    result.followers = data.followers;
    result.following = data.following;
    result.location = data.location || 'No location available';
    
    // Fetch repositories
    const repoResponse = await fetch(data.repos_url);
    if (!repoResponse.ok) throw new Error('Repositories not found');
    result.repo = await repoResponse.json();
  } catch (error) {
    console.error(error);
  }
};
watch(search, async (newSearch) => {
  if (newSearch.trim() !== '') {
    await fetchUserData(newSearch);
    showAllRepos.value = false; 
  }
});
onMounted(async () => {
  await fetchUserData(search.value);
});

</script>

<template>
  <main class="min-h-screen bg-[#364153]">
    <header class="flex justify-center h-72">
      <div class="flex flex-col">
        <TheSearch @search="search = $event"/>
        <div v-if="result" class="flex flex-row bg-[#262E40] rounded-lg p-3 space-x-4 mt-3">
          <TheAvatar :width="'w-20'" :avatarUrl=result.avatar_url />

          <div class="flex flex-col space-y-2 mt-2">
            <p class="text-xl font-bold text-white">{{ result.name }}</p>
            <p class="text-[#97A3B6]">{{ result.bio }}</p>
          </div>
        </div>
      </div>
    </header>
    <div class="max-w-7xl mx-auto">
      <section>
        <div class="flex">
          <!--image container-->
          <div class="-mt-12 bg-[#364153] p-3 rounded-lg">
            <TheAvatar :width="'w-40'" :avatarUrl=result.avatar_url />
          </div>
          <!-- account status-->
          <TheAccStatus :followers=result.followers :following=result.following :location=result.location />
        </div>
      </section>
      <section class="pb-5">
        <div class="flex flex-col space-y-10">
          <div class="flex flex-col space-y-2 mt-2">
            <p class="text-4xl font-bold text-white">Github</p>
            <p class="text-white">How people build software</p>
          </div>
          <!-- repo-->
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <TheRepositroy :repo="displayedRepos" />
          </div>

          <div v-if="!showAllRepos && result.repo.length > 4" class="flex justify-center my-5 text-[#CDD5E0]">
            <a href="#" @click.prevent="fetchAllRepo" class="hover:text-white cursor-pointer">View All repositories</a>
          </div>
        </div>
      </section>
    </div>
  </main>
</template>

<style scoped>
header {
  background-image: url("./assets/resources/hero-image-github-profile.jpg");
  background-repeat: no-repeat;
  background-size: contain;
}
</style>