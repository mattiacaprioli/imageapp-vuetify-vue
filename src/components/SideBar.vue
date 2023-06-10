<script setup>
  import { defineEmits } from 'vue'

  const emits = defineEmits(['selectOption'])

  const selectOption = (isColor) => {
    emits("selectOption", isColor)
  }
</script>

<template>
    <VNavigationDrawer
      expand-on-hover
      rail
    >
    <VList>
        <VListItem
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            title="Lily Dhata"
            subtitle="lily@gmailcom"
            @click="selectOption(true)"
        ></VListItem>
    </VList>

    <VDivider/>

    <VList density="compact" nav>
        <VListItem
          prepend-icon="mdi-image"
          title="Color Gallery"
          value="color"
        />
        <VListItem
          prepend-icon="mdi-dialpad"
          title="Grayspace Gallery"
          value="color"
          @click="selectOption(false)"
        />


    </VList>
    </VNavigationDrawer>
</template>