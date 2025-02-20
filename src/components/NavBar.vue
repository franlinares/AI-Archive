<template>
  <nav class="nav-bar">
    <div class="nav-bar__left">
      <router-link to="/" class="nav-bar__link">Home</router-link>
      <router-link to="/about" class="nav-bar__link">About</router-link>
      <router-link to="/begin" class="nav-bar__link">Begin</router-link>
    </div>
    <div class="nav-bar__right">
      <button class="nav-bar__button" @click="handleRegister">Register</button>
      <button class="nav-bar__button" @click="handleLogin">Login</button>
      <i class="nav-bar__icon-user"></i>
    </div>
  </nav>
</template>

<script lang="ts" setup>
import { useRouter } from 'vue-router'

const router = useRouter()

// Función para manejar el registro
const handleRegister = (): void => {
  console.log('Redirecting to register...')
  // Lógica para redirigir o mostrar un formulario de registro
  router.push('/register')
}

// Función para manejar el inicio de sesión
const handleLogin = (): void => {
  console.log('Redirecting to login...')
  // Lógica para redirigir o mostrar un formulario de login
  router.push('/login')
}
</script>

<style lang="less" scoped>
.nav-bar {
  display: flex;
  justify-content: space-between;
  padding: 24px;
  background-color: #333;
  color: white;

  &__left,
  &__right {
    display: flex;
    align-items: center;
  }

  &__link {
    margin-right: 20px;
    text-decoration: none;
    color: white;
    font-size: 1.1rem;

    &:hover {
      color: #ff6347; /* Color hover */
    }
  }

  &__button {
    background-color: transparent;
    border: 1px solid white;
    color: white;
    padding: 0.5rem 1rem;
    margin-left: 10px;
    cursor: pointer;
    font-size: 1rem;

    &:hover {
      background-color: white;
      color: #333;
    }
  }

  &__icon-user {
    font-size: 1.5rem;
    margin-left: 20px;
    cursor: pointer;
  }
}
</style>
