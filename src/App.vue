<template>
  <v-ons-navigator v-model:page-stack="pageStack">
    <component :is="page" v-for="page in pageStack" :key="page.key" v-model:page-stack="pageStack"></component>
  </v-ons-navigator>
</template>

<script>
  import page1 from './Page1.vue';

  export default {
    data() {
      return {
        pageStack: [page1]
      }
    }
  }
</script>
