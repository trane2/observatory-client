
<template>
    <LayoutView :collection="collection"/>
</template>

<!-- // // // //  -->

<script>

import LayoutView from './components/layout.vue'
import store from '@/store'

export default {
  components: {
    LayoutView
  },
  metaInfo: {
    title: 'Projects' // title is now "RCOS - Projects"
  },
  computed: {
    collection () {
      return store.getters['project/collection']
    }
  },
  mounted () {
    return store.dispatch('project/fetchCollection')
  }
}
</script>


