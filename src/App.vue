<template>
  <div id="app" class="container mt-5">
    <ParentComponent>
      <template v-slot>
        <p>Sloot</p>
      </template>
    </ParentComponent>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  name: 'App',
  components: {
    ParentComponent
  }
};
</script>
