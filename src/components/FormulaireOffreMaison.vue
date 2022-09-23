<script setup lang="ts">
import { ref } from "@vue/reactivity"
import Card from "@/components/card.vue"
import { supabase } from "@/supabase";
async function upsertMaison(dataForm, node) {
 const { data, error } = await supabase.from("Maison").upsert(dataForm);
 if (error) node.setErrors([error.message])
}
const maison = ref({})
</script>
<template>
    <div>
        <div class="p-2">
            <h2 class="text-2xl">Résultat ( Prévisualisation )</h2>
            <Card v-bind="maison"/>
        </div>
        <div class="p-2">
            <FormKit type="form" @submit="upsertMaison" 
                v-model="maison"
                submit-label="Submit"
                :submit-attrs="{ classes: { input: 'bg-blue-300 p-1 rounded mt-5 flex justify-center w-20' } }">
                <div class="flex justify-around">
                    <FormKit name="nom" label="Nom"
                    :config="{
                        classes: {
                            input: 'p-1 rounded border-gray-300 shadow-sm border-2',
                            label: 'text-gray-600',
                        },
                    }"/>
                    <FormKit name="prix" label="Prix" type="number"
                    :config="{
                        classes: {
                            input: 'p-1 rounded border-b-blue-500 shadow-sm border-2',
                            label: 'text-gray-600',
                        },
                    }"/>
                </div>
                <FormKit name="favori" label="Favori" type="checkbox" wrapper-class="flex"
                :config="{
                        classes: {
                            label: 'ml-5 mt-10',
                            input:'content-center w-12 mt-12'
                        },
                    }"/>
            </FormKit>
        </div>
    </div>
</template>