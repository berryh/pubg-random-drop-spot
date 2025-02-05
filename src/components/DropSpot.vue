<script setup lang="ts">
import {ref} from "vue";

const {places} = defineProps(['places'])

const dropSpot = ref(null);

function randomSpot() {
  dropSpot.value = places[Math.floor(Math.random() * places.length)];
}

randomSpot();
</script>

<template>
  <h2 class="text-2xl tracking-tight sm:text-2xl md:text-2xl p-2">Your drop location will be:</h2>
  <br>
  <h1 class="text-2xl font-bold tracking-tight sm:text-2xl md:text-2xl p-2">{{ dropSpot }}</h1>
  <br>
  <Button @click="randomSpot"><span class="pi pi-refresh"/>Pick Random Spot</Button>
  <br><br>
  <p class="text-1xl">We have {{ places.length }} possible {{ places.length > 1 ? "spots" : "spot" }}.</p>
</template>