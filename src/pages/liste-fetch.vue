<script setup lang="ts">
import Card from "../components/card.vue"
const res = await fetch("src/assets/Maison.json")
const Maison = await res.json()
</script>
    
<template>
    <Card v-for="Maison in Maison" :key="Maison.nom" v-bind="Maison"></Card>
</template>