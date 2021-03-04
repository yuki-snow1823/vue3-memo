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

  <li v-for="memo in memos" :key="memo.id">
    {{ memo.title }}：{{ memo.text }}
  </li>
</template>

<script>
  export default {
    data() {
      return {
        title: "",
        text: "",
        formSize: "600px",
        memos: [],
        memo: {}
      }
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
