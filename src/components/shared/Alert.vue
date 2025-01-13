<template><div class="alert-notification">  
  <v-alert
  class="animate__animated animate__pulse"
    :text="alertStore.text"
    :type="alertStore.type"
    closable
  ></v-alert>
</div>
</template>

<script setup>
import 'animate.css'
import { useAlertStore } from '@/stores/alert.js';
const alertStore = useAlertStore();

</script>

<style scoped>
.alert-notification{
  bottom: 5vh;
  padding: 0 35% 0 40%;
  position: fixed;  
  width: 100%;
  z-index: 1;
}
</style>