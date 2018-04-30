<template>
  <div id="home">
    <h1>{{msg}}</h1>
    <button @click="googleLogin">Googleアカウントでログイン</button>
  </div>
</template>

<script>
  export default {
    name: "Home",
    data() {
      return {
        msg: 'Welcome to MyMarkdown'
      }
    },
    methods: {
      googleLogin: function () {
        const provider = new firebase.auth.GoogleAuthProvider();
        firebase.auth().signInWithRedirect(provider);
      }
    }
  }
</script>

<style scoped lang="scss">

</style>
