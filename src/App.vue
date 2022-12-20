<script setup lang="ts">
/*
 * Imports
 */
import SideBar from "@/components/SideBar.vue";
import ImageGallery from "@/components/ImageGallery.vue";
import { ref } from "vue";

/*
 * Gallery color
 */
const isWithColor = ref(true);
const onSelectedOption = (isColor: boolean) => {
  isWithColor.value = isColor;
};
</script>
<template>
  <VApp>
    <SideBar @selectOption="onSelectedOption" />
    <VMain>
      <ImageGallery :isWithColor="isWithColor" />
    </VMain>
  </VApp>
</template>
