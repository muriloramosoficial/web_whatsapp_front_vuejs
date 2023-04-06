<script setup>
import ContentSelector from '../components/Content/ContentSelector.vue';
import SidebarLeft from '../components/SidebarLeft/SidebarLeft.vue'

</script>

<template>
  <main>
    <div class="sidebarLeft">
      <SidebarLeft/>
    </div>
    <div class="content">
      <ContentSelector/>
    </div>
  </main>
</template>

<style>
main{
  display: flex;
  justify-content: left;
  flex-direction: row;
}
</style>
