<script setup lang="ts">
console.log("sike")
import Card from "../components/card.vue"
import { supabase } from "../supabase";
console.log("supabase :", supabase);
const Maison = [];
let { data: Maisons, error } = await supabase
  .from('Maison')
  .select('*')
</script>
    
<template>
    <Card v-for="Maison in Maison" :key="Maison.nom" v-bind="Maison"></Card>
</template>