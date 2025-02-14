<template>
    <Header />
    <CarForm />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import CarForm from "@/components/CarForm.vue";
import Header from "@/components/Header.vue";

@Options({
  components: {
    Header,
    CarForm,
  },
})
export default class CadastroVue extends Vue {}
</script>