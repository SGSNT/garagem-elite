<template>
  <Header />
  <div class="home container">
    <h1 class="mt-3 text-start">Estoque</h1>

    <div class="row">
      <div class="col-12">
        <table class="table table-striped table-bordered">
          <thead class="table-dark text-center">
            <tr>
              <th scope="col">#</th>
              <th scope="col">Marca</th>
              <th scope="col">Modelo</th>
              <th scope="col">Cor</th>
              <th scope="col">Ano</th>
              <th scope="col">Status</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>1</td>
              <td>Fiat</td>
              <td>Uno</td>
              <td>Vermelho</td>
              <td>2022</td>
              <td>Em estoque</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Header from "@/components/Header.vue";

@Options({
  components: {
    Header,
  },
})
export default class HomeView extends Vue {}
</script>
