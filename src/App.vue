<template>
  <component :is="layout"></component>
  <!-- <router-view/> -->
</template>

<script>
import EmptyLayout from '@/layouts/EmptyLayout.vue'
import MainLayout from '@/layouts/MainLayout.vue'
export default {
  computed: {
    layout () { return (this.$route.meta.layout || 'empty') + '-layout' }
  },
  components: { EmptyLayout, MainLayout }
}
</script>

<style lang="scss">
@import '~materialize-css/dist/css/materialize.min.css';
@import 'assets/index.css';
</style>
