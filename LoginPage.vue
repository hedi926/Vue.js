<template>
    <main class="login-container">
        <FormComponent />
    </main>
  </template>
  <script setup lang="ts">
    import FormComponent from '../components/FormComponent.vue';
    import { reactive } from 'vue';

    const formData = reactive({
      fields: [
        { id: 'email', type: 'email', placeholder: 'Entrez votre email' },
        { id: 'password', type: 'password', placeholder: 'Entrez votre mot de passe' },
      ],
      buttons: [
        { id: 'submit-btn', textContent: 'Valider', type: 'submit', class: 'btn-primary' },
        { id: 'reset-btn', textContent: 'Réinitialiser', type: 'reset', class: 'btn-secondary' },
      ],
    });

  </script>
  
  <style lang="scss">
  .login-container {
    max-width: 400px;
    margin: 50px auto;
    padding: 20px;
    background: #fff;
    border-radius: 8px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    text-align: center;
  
    h2 {
      margin-bottom: 20px;
      font-size: 24px;
    }
  
    .input-group {
      margin-bottom: 15px;
      text-align: left;
  
      label {
        display: block;
        font-weight: bold;
        margin-bottom: 5px;
      }
  
      input {
        width: 100%;
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 5px;
        font-size: 16px;
      }
    }
  
    .button-group {
      display: flex;
      justify-content: space-between;
      margin-top: 20px;
  
      .btn-primary {
        background-color: #007bff;
        color: white;
        padding: 10px 15px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        font-size: 16px;
  
        &:hover {
          background-color: #0056b3;
        }
      }
  
      .btn-secondary {
        background-color: #6c757d;
        color: white;
        padding: 10px 15px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        font-size: 16px;
  
        &:hover {
          background-color: #545b62;
        }
      }
    }
  
    .register-text {
      margin-top: 20px;
      font-size: 14px;
  
      a {
        color: #007bff;
        text-decoration: none;
  
        &:hover {
          text-decoration: underline;
        }
      }
    }
  }
  </style>
  