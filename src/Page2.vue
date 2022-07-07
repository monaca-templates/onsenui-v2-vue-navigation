<template>
  <v-ons-page>
    <custom-toolbar :back-label="'Page 1'">Page 2</custom-toolbar>
    <p style="text-align: center">This is the second page</p>
  </v-ons-page>
</template>

<script>
  import customToolbar from './CustomToolbar.vue';

  export default {
    methods: {
      pop() {
        this.$emit('update:pageStack', this.pageStack.slice(0, -1));
      }
    },
    props: ['pageStack'],
    components: { customToolbar },
    key: 'key_page2',
    emits: ['update:pageStack']
  }
</script>
