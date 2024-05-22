<template>
    <div class="child-component">
      <button class="btn btn-primary" @click="sendDataToParent">Kirim Data dari A</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ChildComponentA',
    methods: {
      sendDataToParent() {
        this.$emit('data-from-a', 'Data dari Komponen A');
      }
    }
  };
  </script>
  
  <style scoped>
  .child-component {
    margin: 10px;
    padding: 10px;
    background-color: #f1f1f1;
    border-radius: 5px;
  }
  </style>
  