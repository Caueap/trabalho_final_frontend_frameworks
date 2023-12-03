<template>
    <FooterBannerComponent/>
    <NewsletterComponent/>

</template>

<script>
import FooterBannerComponent from './FooterBannerComponent.vue';
import NewsletterComponent from '@/components/NewsletterComponent.vue'
    export default {
        name: 'FooterComponent',
        components: {
            FooterBannerComponent,
            NewsletterComponent
        }
        
    }
</script>

<style lang="scss" scoped>

</style>