<script setup lang="ts">
/*
 * Emits
 */
const emit = defineEmits(["selectOption"]);

/*
 * Change the color of the images
 */
const selectOption = (isColor: boolean) => {
  emit("selectOption", isColor);
};
</script>

<template>
  <VNavigationDrawer
    expand-on-hover
    rail>
    <VList>
      <VListItem
        prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
        title="Kevin Campbell"
        subtitle="kevn@tcmsvc.com"></VListItem>
    </VList>
    <VDivider></VDivider>
    <VList
      density="compact"
      nav>
      <VListItem
        prepend-icon="mdi-image"
        title="Color Gallery"
        value="color"
        @click="selectOption(true)" />
      <VListItem
        prepend-icon="mdi-palette"
        title="Grayspace Gallery"
        value="color"
        @click="selectOption(false)" />
    </VList>
  </VNavigationDrawer>
</template>
