<template>
    <img loading="lazy" :src="src" alt="">
</template>

<script>

export default {
    name: 'NativeLazyImage',
    props: {
        src: {
            type: String,
            required: true
        }
    }
}

</script>
