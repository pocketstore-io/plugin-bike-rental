<template>
  <!-- Headline -->
  <section class="headline flex justify-between bg-white">
    <h2 class="font-bold text-lg my-3 mx-3">
      Bikes zum mieten
    </h2>
    <section class="actions my-3 mx-3 space-x-3 flex">
      <a href="/de/admin/bike/rental" class="btn btn-primary btn-sm">verwalten</a>
    </section>
  </section>
  <RentalGrid />
  <!-- Pagination -->
</template>
<script setup lang="ts">
import RentalGrid from "@/components/rental/Grid.vue";
import {usePocketBase} from "~/util/pocketbase";
const pb = usePocketBase()
</script>