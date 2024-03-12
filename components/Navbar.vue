<template>
  <div class="card">
    <Menubar :model="items" />
    <Toast />
  </div>
</template>

<script setup>
import { ref } from "vue";

const items = ref([
  {
    label: "File",
    icon: "pi pi-file",
    items: [
      {
        label: "New",
        icon: "pi pi-plus",
      },
      {
        label: "Print",
        icon: "pi pi-print",
      },
    ],
  },
  {
    label: "Search",
    icon: "pi pi-search",
  },
  {
    separator: true,
  },
  {
    label: "Sync",
    icon: "pi pi-cloud",
    items: [
      {
        label: "Import",
        icon: "pi pi-cloud-download",
      },
      {
        label: "Export",
        icon: "pi pi-cloud-upload",
      },
    ],
  },
]);

var $main_menuEN = "https://icr.univ-amu.fr/wp-json/custom/menu/15";
var $main_menuFR = "https://icr.univ-amu.fr/wp-json/custom/menu/16";
var $top_menuEN = "https://icr.univ-amu.fr/wp-json/custom/menu/17";
var $top_menuFR = "https://icr.univ-amu.fr/wp-json/custom/menu/18";

const { data: menuEN } = await useFetch($main_menuEN);
import { usePrimeVue } from "primevue/config";
</script>
