<template>
    <main class="login-container">
      <form>
        <FieldComponent 
        v-for="(field, index) in data.fields"
        :key="index" 
        :data="field" />
      </form>
    </main>
  </template>
  <script lang="ts" setup>

  import FieldComponent from './FieldComponent.vue'

  interface FormComponentProperties {
    data: {
        fields: Array<{id: string, type?: string, class?: string, placeholder: string}>,
        buttons: {id: string, textContent: string,type: 'submit' | 'reset' | 'button', class?: string}[],
    }
  }

  defineProps<FormComponentProperties>();

</script>