<template>
    <v-ons-navigator>
      <div :is="page" v-for="page in pageStack" :page-stack="pageStack"></div>
    </v-ons-navigator>
</template>

<script>
  import page1 from 'Page1';
  import page2 from 'Page2';
  export default {
    methods: {},
    data() {
      return {
        pageStack: [page1]
      }
    },
    components:{page1, page2} 
  }
</script>
