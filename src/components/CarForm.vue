<template>
    <div class="container mt-4">
      <h2>Cadastro de Carros</h2>
      <form @submit.prevent="addCar">
        <div class="mb-3">
          <label class="form-label">Modelo</label>
          <input v-model="car.model" type="text" class="form-control" required />
        </div>
        <div class="mb-3">
          <label class="form-label">Marca</label>
          <input v-model="car.brand" type="text" class="form-control" required />
        </div>
        <div class="mb-3">
          <label class="form-label">Cor</label>
          <input v-model="car.color" type="text" class="form-control" required />
        </div>
        <div class="mb-3">
          <label class="form-label">Ano</label>
          <input v-model="car.year" type="number" class="form-control" required />
        </div>
        <div class="mb-3">
          <label class="form-label">Status</label>
          <select v-model="car.status" class="form-select">
            <option value="reservado">Reservado</option>
            <option value="vendido">Vendido</option>
            <option value="sob encomenda">Sob Encomenda</option>
            <option value="disponível">Disponível</option>
            <option value="removido">Removido</option>
          </select>
        </div>
        <button type="submit" class="btn btn-primary">Cadastrar</button>
      </form>
      <hr />
      <h3>Carros Cadastrados</h3>
      <table class="table table-striped">
        <thead>
          <tr>
            <th>Modelo</th>
            <th>Marca</th>
            <th>Cor</th>
            <th>Ano</th>
            <th>Status</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(c, index) in cars" :key="index">
            <td>{{ c.model }}</td>
            <td>{{ c.brand }}</td>
            <td>{{ c.color }}</td>
            <td>{{ c.year }}</td>
            <td>{{ c.status }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
<script setup>
import { ref } from 'vue'
const car = ref({ model: '', brand: '', color: '', year: '', status: 'disponível' })
const cars = ref([])
const addCar = () => {
    cars.value.push({ ...car.value })
    car.value = { model: '', brand: '', color: '', year: '', status: 'disponível' }
  }
  </script>
  
  <style scoped>
  .container {
    max-width: 600px;
  }
  </style>