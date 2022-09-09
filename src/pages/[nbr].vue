<script setup lang="ts">
const res = await fetch("src/assets/maisons.json")
const maisons = await res.json()
import Card from "../components/card.vue"

    defineProps({
        nbr: String,
    })

</script>
    
    <template>
      <Card v-for="maison in maisons" :key="maison.nom" v-bind="maison"></Card>
    </template>
    
    <route>
    {
      name: 'offre-nbr'
    }
    </route>