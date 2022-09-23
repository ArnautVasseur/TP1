<script setup lang="ts">
    import Card from "../components/card.vue"
    const maisons = [
        {
            nom:"Beverly Hills",
            prix:12000,
            favori:true,
            nbrSDB:3,
            image:"src/assets/house.jpg"
        },
        {
            nom:"test",
            prix:1,
            favori:false,
            nbrSDB:4,
            image:"src/assets/house2.jpg"
        }
    ];
    
    </script>
    
<template>
    <section>
        <Card v-for="Maison in Maison" :key="Maison.nom" v-bind="Maison"></Card>
    </section>
</template>
