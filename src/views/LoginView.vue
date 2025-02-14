<template>
    <Header />
    <LoginForm />
  </template>
  
  <script lang="ts">
  import { Options, Vue } from "vue-class-component";
  import LoginForm from "@/components/LoginForm.vue";
  import Header from "@/components/Header.vue";
  
  @Options({
    components: {
      Header,
      LoginForm,
    },
  })
  export default class LoginVue extends Vue {}
  </script>