<template>
  <img
    :src=props.avatarUrl
    alt="logo"
    :class="props.width"
    class="p-1 bg-black rounded-lg"
  />
</template>
<script setup>
const props = defineProps({
  width: {
    type: String,
    required: false,
  },
  avatarUrl:{
    type:String,
    required:false
  }
});
</script>
