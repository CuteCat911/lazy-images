<template>
    <img class="lazyload" :data-src="src" src="" alt="">
</template>

<script>

import 'lazysizes';

export default {
    name: 'LazyImage',
    props: {
        src: {
            type: String,
            required: true
        }
    }
}

</script>
