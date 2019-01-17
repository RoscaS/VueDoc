<template>
  <div class="home">
    <Page :source="mdText">

    </Page>
  </div>
</template>

<script>
  import VueMarkdown from 'vue-markdown/src/VueMarkdown';
  import Page from '../components/Page';


  export default {
    name: 'home',
    components: {Page, VueMarkdown},
    data: () => ({
      source: '',
      mdText: '',
    }),
    mounted() {
    }
  };
</script>
