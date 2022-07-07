<template>
  <v-ons-page>
    <custom-toolbar>Page 1</custom-toolbar>
    <p style="text-align: center">
      This is the first page
      <v-ons-button @click="push">Push Page 2</v-ons-button>
    </p>
  </v-ons-page>
</template>

<script>
  import customToolbar from './CustomToolbar.vue';
  import page2 from './Page2.vue';

  export default {
    methods: {
      pop(){
        this.$emit('update:pageStack', this.pageStack.slice(0, -1));
      },
      push() {
        this.$emit('update:pageStack', [...this.pageStack, page2]);
      }
    },
    props: ['pageStack'],
    components: { customToolbar },
    key: 'key_page1',
    emits: ['update:pageStack']
  }
</script>
