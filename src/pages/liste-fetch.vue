<script setup>
const res = await fetch("src/assets/maisons.json")
const maisons = await res.json()
import Card from "../components/card.vue"
</script>
    
<template>
    <Card v-for="maison in maisons" :key="maison.nom" v-bind="maison"></Card>
</template>