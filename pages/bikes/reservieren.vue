<template>
  <section class="bg-white px-3 py-3">
    <h2 class="font-bold text-lg mb-3">
      Bike reservieren
    </h2>
    <section class="preview pb-3">
      <RentalCard :reserve="false"/>
    </section>
    <form @submit.prevent="reserve()" class="mt-3">
      <label class="floating-label mb-3 mt-3">
        <span>Your Phone</span>
        <input v-model="form.phone" type="email" class="input w-full validator" required/>
        <div class="validator-hint block text-center">Enter valid email address</div>
      </label>
      <label class="floating-label mb-3 mt-3">
        <span>Your Email</span>
        <input v-model="form.email" type="email" class="input w-full validator" required/>
        <div class="validator-hint block text-center">Enter valid email address</div>
      </label>
      <label class="floating-label mb-3">
        <span>Your Week</span>
        <input v-model="form.week" type="number" class="input w-full validator" required>
        <div class="validator-hint block text-center">Enter valid email address</div>
      </label>
      <label class="floating-label">
        <span>Your Type</span>
        <select v-model="form.typ" class="select w-full validator" required>
          <option disabled selected>Pick a Type</option>
          <option>Wochenende</option>
          <option>Werktage</option>
          <option>Werktage + Wochenende</option>
        </select>
        <div class="validator-hint block text-center">Enter valid email address</div>
      </label>
      <section class="actions flex justify-end mt-3">
        <button type="submit" class="btn btn-secondary">
          speichern
        </button>
      </section>
    </form>
  </section>
</template>

<script setup lang="ts">
import {addBreadcrumb} from "~/utils/breadcrumb";

const route = useRoute();
const router = useRouter();
const form = ref({
  email: '',
  phone: '',
  week: '',
  typ: ''
});

onMounted(() => {
  if (!route.query.id) {
    router.push('/de/bikes');
  }
  addBreadcrumb({
    id: 'abc123',
    label: 'test123',
    icon: '',
    link: '',
  })
})

const reserve = () => {

}
</script>