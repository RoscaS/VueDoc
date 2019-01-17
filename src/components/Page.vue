<template>

  <div class="container content">


    <div class="text-body">
      <div id="Toc"></div>
      <vue-markdown :source="mdSource" toc toc-id="Toc"></vue-markdown>
    </div>
  </div>


</template>

<script>
  import VueMarkdown from 'vue-markdown/src/VueMarkdown';
  import mdSource from 'raw-loader!../markdown/page.md';

  export default {
    name: 'Page',

    props: {source: {default: ''}},

    components: {VueMarkdown},

    data: () => ({
      mdSource: mdSource,
    }),

  };
</script>

<style lang="scss" scoped>

  .print-preview {
    margin: 60px auto 60px auto;
    height: 297mm;
    width: 210mm;
    border: 1px solid black;
    box-shadow: 10px 10px 43px -1px rgba(0, 0, 0, 0.38);

    @media print {
      margin: unset;
      box-shadow: unset;
      border: unset;
    }
  }

  .text-body {
    margin: 25.4mm;

  }


</style>
