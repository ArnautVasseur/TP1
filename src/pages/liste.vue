<script setup lang="ts">
    import Card from "../components/card.vue"
    const maisons = [
        {
            nom:"Beverly Hills",
            prix:12000,
            favori:true,
            nbrSDB:3
        },
        {
            nom:"test",
            prix:1,
            favori:false,
            nbrSDB:4
        }
    ];
    
    </script>
    
<template>
    <section>
        <Card v-for="maison in maisons" :key="maison.nom" v-bind="maison"></Card>
    </section>
</template>
