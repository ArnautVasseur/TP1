<script setup lang="ts">
import Card from "../components/card.vue"
const unObjet = {
    nom:"Beverly Hills",
    prix:12000,
    favori:true,
    nbrSDB:3,
    image:"src/assets/house.jpg",
    nbr:2
};

</script>

<template>
    <section>
        <Card v-bind="unObjet"></Card>
    </section>
</template>
