<template>
    <h2>Connexion</h2>
        <div class="input-group">
          <label v-bind:for="data.id">Email</label>
          <input
              v-bind:id="data.id"
              v-bind:type="data.type ? data.type : 'text'"
              v-bind:placeholder="data.placeholder"
              v-bind:class="'input' + (data.class ? data.class : '')"
            required
             />
        </div>
  
        <div class="input-group">
          <label for="password">Mot de passe</label>
          <input type="password" id="password" required />
        </div>
  
        <div class="button-group">
          <button type="submit" class="btn-primary">Valider</button>
          <button type="reset" class="btn-secondary">Réinitialiser</button>
        </div>
  
        <p class="register-text">
          Pas encore inscrit(e) ? <a href="/register">Inscrivez-vous</a>
        </p>
</template>

<script setup lang="ts">

interface FieldComponentProperties {
    data: {
        id: string;
        placeholder: string;
        type?: string;
        class?: string;
    }
} 

defineProps<FieldComponentProperties>();

</script>  