<script setup></script>

<template>
  <main class="min-h-screen bg-[#364153]">
    <header class="flex justify-center h-72">
      <div
        class="flex justify-between bg-[#20293A] px-6 py-3 rounded-lg h-16 mt-10"
      >
        <img src="./assets/resources/Search.svg" alt="logo" class="w-5" />
        <input
          type="text"
          class="ml-3 border-none text-white md:w-100 placeholder:font-normal focus:outline-none"
          placeholder="Username"
        />
      </div>
    </header>
    <div class="max-w-7xl mx-auto">
      <section>
        <div class="flex">
          <!--image container-->
          <div class="-mt-12 bg-[#364153] p-3 rounded-lg">
            <img
              src="./assets/resources/github-mark-white.svg"
              alt="logo"
              class="w-40 p-1 bg-black rounded-lg"
            />
          </div>
          <!-- account status-->
          <div
            class="flex justify-between h-16 items-center space-x-5 ml-10 mt-2"
          >
            <div
              class="flex justify-between p-2 bg-[#111729] space-x-5 rounded-lg p-3 text-[#CDD5E0]"
            >
              <p class="text-md font-semibold pl-3 py-1">Followers</p>
              <p
                class="ext-md font-semibold border-l-2 border-l-[#97A3B6] px-6 py-1"
              >
                27839
              </p>
            </div>
            <div
              class="flex justify-between p-2 bg-[#111729] space-x-5 rounded-lg p-3 text-[#CDD5E0]"
            >
              <p class="inline-block text-md font-semibold pl-3 py-1">
                Following
              </p>
              <p
                class="ext-md font-semibold border-l-2 border-l-[#97A3B6] px-6 py-1"
              >
                0
              </p>
            </div>
            <div
              class="flex justify-between p-2 bg-[#111729] space-x-5 rounded-lg p-3 text-[#CDD5E0]"
            >
              <p class="text-md font-semibold pl-3 py-1">Location</p>
              <p
                class="ext-md font-semibold border-l-2 border-l-[#97A3B6] px-6 py-1"
              >
                San Francisco,CA
              </p>
            </div>
          </div>
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
            <div
              class="flex flex-col space-y-3 bg-gradient-to-br from-[#111729] to-[#1D1B48] text-[#CDD5E0] rounded-lg p-6"
            >
              <p class="font-semibold text-xl">.github</p>
              <p class="font-normal text-[#97A3B6]">
                Community health files for @Github organizations
              </p>
              <div class="flex flex-row items-center space-x-4 text-[#97A3B6]">
                <div class="flex flex-row items-center space-x-2">
                  <img src="./assets/resources/Chield_alt.svg" alt="" />
                  <p>MIT</p>
                </div>
                <div class="flex flex-row items-center space-x-2">
                  <img src="./assets/resources/Nesting.svg" alt="" />
                  <p>2,369</p>
                </div>
                <div class="flex flex-row items-center space-x-2">
                  <img src="./assets/resources/Star.svg" alt="" />
                  <p class="text-sm ml-2">703</p>
                </div>
                <p class="text-sm ml-3">updated 4 days ago</p>
              </div>
            </div>
            <div
              class="flex flex-col space-y-3 bg-gradient-to-br from-[#111729] to-[#1D1B48] text-[#CDD5E0] rounded-lg p-6"
            >
              <p class="font-semibold text-xl">.github</p>
              <p class="font-normal text-[#97A3B6]">
                Community health files for @Github organizations
              </p>
              <div class="flex flex-row items-center space-x-4 text-[#97A3B6]">
                <div class="flex flex-row items-center space-x-2">
                  <img src="./assets/resources/Chield_alt.svg" alt="" />
                  <p>MIT</p>
                </div>
                <div class="flex flex-row items-center space-x-2">
                  <img src="./assets/resources/Nesting.svg" alt="" />
                  <p>2,369</p>
                </div>
                <div class="flex flex-row items-center space-x-2">
                  <img src="./assets/resources/Star.svg" alt="" />
                  <p class="text-sm ml-2">703</p>
                </div>
                <p class="text-sm ml-3">updated 4 days ago</p>
              </div>
            </div>
            <div
              class="flex flex-col space-y-3 bg-gradient-to-br from-[#111729] to-[#1D1B48] text-[#CDD5E0] rounded-lg p-6"
            >
              <p class="font-semibold text-xl">.github</p>
              <p class="font-normal text-[#97A3B6]">
                Community health files for @Github organizations
              </p>
              <div class="flex flex-row items-center space-x-4 text-[#97A3B6]">
                <div class="flex flex-row items-center space-x-2">
                  <img src="./assets/resources/Chield_alt.svg" alt="" />
                  <p>MIT</p>
                </div>
                <div class="flex flex-row items-center space-x-2">
                  <img src="./assets/resources/Nesting.svg" alt="" />
                  <p>2,369</p>
                </div>
                <div class="flex flex-row items-center space-x-2">
                  <img src="./assets/resources/Star.svg" alt="" />
                  <p class="text-sm ml-2">703</p>
                </div>
                <p class="text-sm ml-3">updated 4 days ago</p>
              </div>
            </div>
            <div
              class="flex flex-col space-y-3 bg-gradient-to-br from-[#111729] to-[#1D1B48] text-[#CDD5E0] rounded-lg p-6"
            >
              <p class="font-semibold text-xl">.github</p>
              <p class="font-normal text-[#97A3B6]">
                Community health files for @Github organizations
              </p>
              <div class="flex flex-row items-center space-x-4 text-[#97A3B6]">
                <div class="flex flex-row items-center space-x-2">
                  <img src="./assets/resources/Chield_alt.svg" alt="" />
                  <p>MIT</p>
                </div>
                <div class="flex flex-row items-center space-x-2">
                  <img src="./assets/resources/Nesting.svg" alt="" />
                  <p>2,369</p>
                </div>
                <div class="flex flex-row items-center space-x-2">
                  <img src="./assets/resources/Star.svg" alt="" />
                  <p class="text-sm ml-2">703</p>
                </div>
                <p class="text-sm ml-3">updated 4 days ago</p>
              </div>
            </div>
          </div>

          <div class="flex justify-center my-5 text-[#CDD5E0]">
            <p>View All repositories</p>
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
