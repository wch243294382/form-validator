<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
const a = '1'
console.log(a)
</script>

<template>
  <main class="container">
    <form id="form" class="form">
      <h2>Register With Us</h2>
      <div class="form-control">
        <label for="username">Username</label>
        <input type="text" id="username" placeholder="Enter username" />
        <small>Error Message</small>
      </div>
      <div class="form-control">
        <label for="email">Email</label>
        <input type="text" id="email" placeholder="Enter email" />
        <small>Error Message</small>
      </div>
      <div class="form-control">
        <label for="password">Password</label>
        <input type="password" id="password" placeholder="Enter password" />
        <small>Error Message</small>
      </div>
      <div class="form-control">
        <label for="password2">Confirm Password</label>
        <input type="password" id="password2" placeholder="Enter password2" />
        <small>Error Message</small>
      </div>
      <button>Submit</button>
    </form>
  </main>
</template>

<style scoped lang="scss">
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background-color: #f5f5f5;
}

.form {
  background-color: #fff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  max-width: 400px;
  width: 100%;
  label {
    display: block;
    margin-bottom: 5px;
  }

  h2 {
    text-align: center;
    margin-bottom: 20px;
  }
  .form-control {
    margin-bottom: 10px;

    input {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 16px;

      &:focus {
        outline: 0;
        border-color: black;
        box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);
      }
      &.success {
        border-color: var(--success-color);
      }

      &.error {
        border-color: var(--error-color);
      }
    }
    small {
      color: var(--error-color);
      // color: red;
      display: block;
      visibility: hidden;
      margin-top: 5px;

      &.error {
        visibility: visible;
      }
    }
  }
  button {
    width: 100%;
    padding: 10px;
    background-color: #5482c5;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
}
</style>
