<template>
  <h1>{{ pageTitle}}</h1>
  <!-- formサイズが変わらない -->
  <div>
    <input type="text" v-model="title" :width="formSize" placeholder="タイトルを入力してください。">
  </div>
  <div>
    <input type="text" v-model="text" :width="formSize" placeholder="本文を入力してください。">
  </div>

</template>

<script>
  export default {
    title: "memoのタイトル",
    text: "memoの本文",
    formSize: "300",
    props: {
      pageTitle: String
    }
  }

</script>

<style scoped>


</style>
