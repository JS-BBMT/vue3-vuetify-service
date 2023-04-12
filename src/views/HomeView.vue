<template>
  <v-row>
    <v-col class="d-flex flex-column text-center">
      <div class="text-center">Starter Vue-3 Service</div>
      <v-btn @click="handlefetch" color="primary" class="mt-3"
        >Get Random User</v-btn
      >
      <div>{{ getFetch || "-" }}</div>
    </v-col>
  </v-row>
</template>

<script setup>
import { computed, onMounted } from "vue-demi";
import { useFetchStore } from "../stores/fetch";

const fetchStore = useFetchStore();

const getFetch = computed(() => fetchStore.getFetch);

const handlefetch = () => {
  fetchStore.getFetchServices();
};
</script>