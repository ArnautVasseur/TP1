<script setup lang="ts">
import Card from "../components/card.vue"
import maisons from "../assets/maisons.json"

    defineProps({
        nbr: String,
    })

</script>
    
<template>
  <Card v-bind="maisons[nbr]"></Card>
</template>

<route>
{
  name: 'offre-nbr'
}
</route>