<template>
    <div class="login-form">
      <h2>Login</h2>
      <form @submit.prevent="handleLogin">
        <div>
          <label for="email">E-mail:</label>
          <input type="email" id="email" v-model="email" required />
        </div>
        <div>
          <label for="password">Senha:</label>
          <input type="password" id="password" v-model="password" required />
        </div>
        <button type="submit">
            <a
            href="/"
            class="link-offset-2 link-underline link-underline-opacity-0 text-reset"
            >
            Entrar
            </a>
        </button>
      </form>
    </div>
  </template>
  
  <script lang="ts">
  import { Options, Vue } from "vue-class-component";
  
  @Options({})
  export default class LoginForm extends Vue {
    email: string = '';
    password: string = '';
  
    handleLogin() {
      // Lógica para autenticar o usuário
      console.log('Usuário:', this.email);
      console.log('Senha:', this.password);
    }
  }
  </script>
  
  <style scoped>
.login-form {
  max-width: 400px; 
  margin: auto; 
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #f9f9f9;
  position: absolute; 
  top: 50%; 
  left: 50%; 
  transform: translate(-50%, -50%); 
}

h2 {
  text-align: center;
}

form div {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input {
  width: 100%;
  padding: 8px;
  box-sizing: border-box;
}

button {
  width: 100%;
  padding: 10px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}
</style>