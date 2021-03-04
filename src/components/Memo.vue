<template>
  <h1>{{ pageTitle}}</h1>
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
</template>

<script>
  export default {
    data() {
      return {
        title: "memoのタイトル",
        text: "memoの本文",
        formSize: "600px",
      }
    },
    props: {
      pageTitle: String
    },
    methods: {
      submit() {
        console.log("hoge");
      },
    }
  }

</script>

<style scoped>


</style>
