<template>
  <Designer />
</template>

<script setup>
import { onMounted } from 'vue';
import { useStore } from 'vuex';
import Designer from './views/designer/Designer.vue';

// use Vuex store
const store = useStore();

// Set backend current user in the store on mount
onMounted(() => {
  store.commit('user/setUser', {
    name: 'Stagiaire Mobilosoft',
    email: 'stagiaire.mobilosoft@gmail.com',
  });
});

</script>

<style scoped>
/* Styles for designer page */
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:ital,wght@0,100;0,200;0,300;0,400;0,500;1,100;1,200;1,300;1,400&family=Raleway:ital,wght@0,100;0,200;0,300;0,400;0,500;1,100;1,200;1,300;1,400&display=swap');

/* Additional custom styles for your component */
</style>
