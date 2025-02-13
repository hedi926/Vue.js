<template>
    <button
     :type="data.type"
     :id="data.id"
     :class="data.class">
    </button>
  </template>
<script setup lang="ts">

interface ButtonComponentProperties {
    data: {
        id: string;
        type?: "button" | "submit" | "reset";
        class?: string;
    }
} 

defineProps<ButtonComponentProperties>();

</script>

