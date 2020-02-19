<template>
  <div>
    <AppImage v-for="i in imagesCount"
              :key="i"
              :src="`./images/cat-${i}.jpg`"
              :nativeLazy="nativeLazy"
    />
  </div>
</template>

<script>

import AppImage from '@/components/AppImage'

export default {
  name: 'App',
  data () {
    return {
      imagesCount: 48
    }
  },
  created () {
    this.nativeLazy = 'loading' in HTMLImageElement.prototype
  },
  components: {
    AppImage
  }
}
</script>
