<template>
  <!-- CSS only -->
  <Users />
</template>

<script lang="ts">
import Vue from 'vue'
import Users from '~/components/Users.vue';

export default Vue.extend({
    name: "IndexPage",
    components: { Users }
})
</script>
