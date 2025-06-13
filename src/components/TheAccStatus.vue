<template>
  <div class="flex justify-between h-16 items-center space-x-5 ml-10 mt-2">
    <div
      class="flex justify-between p-2 bg-[#111729] space-x-5 rounded-lg p-3 text-[#CDD5E0]"
    >
      <p class="text-md font-semibold pl-3 py-1">Followers</p>
      <p class="ext-md font-semibold border-l-2 border-l-[#97A3B6] px-6 py-1">
        {{ followers }}
      </p>
    </div>
    <div
      class="flex justify-between p-2 bg-[#111729] space-x-5 rounded-lg p-3 text-[#CDD5E0]"
    >
      <p class="inline-block text-md font-semibold pl-3 py-1">Following</p>
      <p class="ext-md font-semibold border-l-2 border-l-[#97A3B6] px-6 py-1">
       {{ following }}
      </p>
    </div>
    <div
      class="flex justify-between p-2 bg-[#111729] space-x-5 rounded-lg p-3 text-[#CDD5E0]"
    >
      <p class="text-md font-semibold pl-3 py-1">Location</p>
      <p class="ext-md font-semibold border-l-2 border-l-[#97A3B6] px-6 py-1">
        {{ location }}
      </p>
    </div>
  </div>
</template>

<script setup>
defineProps({
    followers: Number,
    following: Number,
    location:String
})
</script>

