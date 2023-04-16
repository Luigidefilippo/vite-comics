<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppMerch from './components/AppMerch.vue';
import AppFooter from './components/AppFooter.vue';
export default {
    components: {
        AppHeader,
        AppContent,
        AppMerch,
        AppFooter
    }
}
</script>

<template>
    <AppHeader />
    <AppContent />
    <AppMerch />
    <AppFooter />                                                       
</template>
<style lang="scss">
@use "./components/style/general.scss" as*;
</style>