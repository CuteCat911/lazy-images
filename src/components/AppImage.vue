<template>
    <NativeLazyImage v-if="nativeLazy" :src="src"/>
    <LazyImage v-else :src="src"/>
</template>

<script>

export default {
    name: 'AppImage',
    props: {
        src: {
            type: String,
            required: true
        },
        nativeLazy: Boolean
    },
    components: {
        NativeLazyImage: () => import('@/components/NativeLazyImage.vue'),
        LazyImage: () => import('@/components/LazyImage.vue')
    }
}

</script>

<style>
    img {
        display: block;
    }
</style>
