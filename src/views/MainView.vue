<template>
    <HeaderComponent />
    <MainBodyComponent />
    <FooterComponent />
</template>

<script>
import HeaderComponent from '@/components/HeaderComponent.vue';

import MainBodyComponent from '@/components/MainBodyComponent.vue';
import FooterComponent from '@/components/FooterComponent.vue';

export default {
    name: 'MainView',
    components: {
        HeaderComponent,
        MainBodyComponent,
        FooterComponent
    }

}
</script>

<style lang="scss" scoped></style>