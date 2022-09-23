<script setup lang="ts">
import Card from "../components/card.vue"
import Maison from "../assets/Maison.json"

    defineProps({
        nbr: String,
    })

</script>
    
<template>
  <Card v-bind="Maison[nbr]"></Card>
</template>

<route>
{
  name: 'offre-nbr'
}
</route>