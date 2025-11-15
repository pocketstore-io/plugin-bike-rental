<template>
  <div class="card bg-gray-400 shadow-sm">
    <figure>
      <img
          src="/unsplash/harley-davidson-aiBYhrzsQw4-unsplash.jpg"
          alt="Shoes"/>
    </figure>
    <div class="card-body">
      <h2 class="card-title">
        <span>Rental Vehicle</span>
        <span class="badge badge-secondary">NEW</span>
      </h2>
      <p>A card component has a figure, a body part, and inside body there are title and actions parts</p>
      <div class="card-actions justify-end">
        <div class="badge badge-primary badge-outline">Gummersbach</div>
        <div class="badge badge-outline">Rental</div>
        <div class="badge badge-outline">Bikes</div>
      </div>
      <div class="card-actions">
        <a v-if="props.reserve" :href="'/de/bikes/reservieren?id='+props.identifier" class="btn btn-primary">
          reservieren
        </a>
      </div>
    </div>
  </div>
  <!-- MODAL for booking -->
</template>

<script setup lang="ts">
const props = defineProps({
  reserve: {type:Boolean, default: true},
  identifier: {type:String, default: ''},
})
</script>