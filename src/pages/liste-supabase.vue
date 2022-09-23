<script setup lang="ts">
import Card from "../components/card.vue"
import { supabase } from "../supabase";
console.log("supabase :", supabase);

let { data: Maison, error } = await supabase
  .from('Maison')
  .select('*')

const maisons = Maison;
console.log("test", Maison)
</script>
    
<template>
    <Card v-for="maison in Maison" :key="maison.nom" v-bind="maison"/>
</template>