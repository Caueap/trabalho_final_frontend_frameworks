<template>
    <BannerComponent/>
    <InfoComponent/>
    <CategoriesComponent/>
    <ProductsComponent/>
</template>

<script>
import BannerComponent from './BannerComponent.vue';
import InfoComponent from './InfoComponent.vue';
import CategoriesComponent from './CategoriesComponent.vue';
import ProductsComponent from './ProductsComponent.vue';

export default {
    name: 'MainBodyComponent',
    components: {
        BannerComponent,
        InfoComponent,
        CategoriesComponent,
        ProductsComponent
    }
}
</script>

<style lang="scss" scoped>

</style>