<template>
  <div class="login">
    <h1>Login</h1>
    <form @submit.prevent="login" id ="login-form">
      <input v-model="username" placeholder="Username" />
      <input v-model="password" type="password" placeholder="Password" />
      <button type="submit">Login</button>
    </form>
    <p v-if="error">{{ error }}</p>
  </div>
</template>


<script setup>
import { ref } from 'vue'
import { useRouter } from 'vue-router'

const username = ref('')
const password = ref('')
const error = ref('')
const router = useRouter()

const login = () => {
  if (username.value === 'admin' && password.value === '1234') {
    localStorage.setItem('auth', 'true')
    router.push('/about')
  } else {
    error.value = 'Invalid credentials'
  }
}
</script>

<style scoped>

.login {
  max-width: 300px;
  margin: auto;
  padding: 1em;
  border: 1px solid #ccc;
  border-radius: 1em;
}

.login input, button {
  margin: 1rem;
}

#login-form {
  display: flex;
  flex-direction: column;
  align-items: center;
}

button {
  background-color: #275FDA;
  color: white;
  border: none;
  padding: 0.5em 1em;
  border-radius: 0.3em;
  cursor: pointer;
}

</style>
