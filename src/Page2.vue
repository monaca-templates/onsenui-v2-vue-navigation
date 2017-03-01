<template id="page2">
  <v-ons-page>
    <custom-toolbar :pop="pop" :back-label="'Page 1'">Page 2</custom-toolbar>
    <p style="text-align: center">This is the second page</p>
  </v-ons-page>
</template>

<script>
  import customToolbar from 'customToolbar';
  export default {
    methods: {
      pop() {
        this.pageStack.pop();
      } 
    },
    props: ['pageStack'],
    components: { customToolbar }
  }
</script>
