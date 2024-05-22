<template>
    <div class="child-component">
      <button class="btn btn-success" @click="sendDataToParent">Kirim Data dari B</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ChildComponentB',
    methods: {
      sendDataToParent() {
        this.$emit('data-from-b', 'Data dari Komponen B');
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
  