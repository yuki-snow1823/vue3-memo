<template>
  <h1>{{ pageTitle}}</h1>
  
</template>

<script>
  export default {
    title: "memoのタイトル",
    text: "memoの本文",
    props: {
      pageTitle: String
    }
  }

</script>

<style scoped>


</style>
