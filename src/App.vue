<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppProducts from './components/AppProducts.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  name: 'App',
  components: {
    AppHeader,
    AppContent,
    AppProducts,
    AppFooter,
  }
}
</script>

<template>
  <AppHeader />
  <AppContent />
  <AppProducts />
  <AppFooter />
</template>

<style lang="scss">
@use './styles/partials/variables' as *;
@use './styles/general.scss' as *;
</style>
