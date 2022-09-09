<script setup lang="ts">
    import Card from "../components/card.vue"
    import maisons from "../assets/maisons.json"
    
    </script>
    
<template>
    <section>
        <Card v-for="maison in maisons" :key="maison.nom" v-bind="maison"></Card>
    </section>
</template>