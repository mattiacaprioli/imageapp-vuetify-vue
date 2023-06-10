<script setup>
  import SideBar from "./components/SideBar.vue";
  import ImageGallary from "./components/ImageGallary.vue";
  import { ref } from "vue"

  const isWithColor = ref(true)

  const onSelectOption = (isColor) => {
    isWithColor.value = isColor
  }
</script>

<template>
  <VApp>
    <SideBar @selectOption="onSelectOption" />
    <VMain>
      <ImageGallary :isWithColor="isWithColor" />
    </VMain>
  </VApp>
</template>
