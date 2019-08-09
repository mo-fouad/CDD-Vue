<template>
  <div class="login-page" id="app">
    <LangSwitch></LangSwitch>
    <Notifications></Notifications>
    <Login></Login>
  </div>
</template>

<script>
  import Login from './components/Login.vue'
  import Notifications from './helpers/Notifications.vue'
  import LangSwitch from './helpers/LangSwitch.vue'

  export default {
    name: 'app',
    components: {
      Login,
      Notifications,
      LangSwitch
    },
    mounted() {
    },
    methods: {
      NotificationIsSucess: function () {
      }
    }

  }
</script>

<style lang="scss">
  @import "../src/scss/vars";
  @import "../src/scss/app";

</style>
