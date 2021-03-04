<template>
  <h1>{{ pageTitle }}</h1>
  <!-- formサイズが変わらない -->
  <div>
    <input type="text" v-model="title" :width="formSize" placeholder="タイトルを入力してください。">
  </div>
  <div>
    <input type="text" v-model="text" :width="formSize" placeholder="本文を入力してください。">
  </div>
  <div>
    <input @click="submit" type="submit" value="送信！">
  </div>

  <vue-markdown-it :source='source' />


  <li v-for="memo in memos" :key="memo.id">
    {{ memo.title }}：{{ memo.text }}
  </li>
</template>

<script>
import VueMarkdownIt from 'vue3-markdown-it';
// 今読み込めない
// import 'markdown-it-latex/dist/index.css';
// import 'highlight.js/styles/monokai.css';

  export default {
    data() {
      return {
        title: "",
        text: "",
        value: "hoge",
        formSize: "600px",
        memos: [],
        memo: {},
        source: '# Hello World!'
      }
    },
    components: {
      VueMarkdownIt 
    },
    props: {
      pageTitle: String
    },
    methods: {
      submit() {
        let memo = {
          title: this.title,
          text: this.text
        }
        this.memos.push(memo);
      },
    }
  }

</script>

<style scoped>


</style>
