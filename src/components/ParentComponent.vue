<template>
    <div class="parent-component p-3 mb-2 bg-light border">
      <h2>Komponen Induk</h2>
      <p>Data yang Diterima: {{ receivedData }}</p>
      <ChildComponentA @data-from-a="handleDataFromA"/>
      <ChildComponentB @data-from-b="handleDataFromB"/>
      <NestedComponentC />
      <div class="slot-content mt-3">
        <slot></slot>
      </div>
    </div>
  </template>
  
  <script>
  import ChildComponentA from './ChildComponentA.vue';
  import ChildComponentB from './ChildComponentB.vue';
  import NestedComponentC from './NestedComponentC.vue';
  
  export default {
    name: 'ParentComponent',
    components: {
      ChildComponentA,
      ChildComponentB,
      NestedComponentC
    },
    data() {
      return {
        receivedData: ''
      };
    },
    methods: {
      handleDataFromA(data) {
        this.receivedData = data;
      },
      handleDataFromB(data) {
        this.receivedData = data;
      }
    }
  };
  </script>
  
  <style scoped>
  .parent-component {
    border: 1px solid #ddd;
    border-radius: 5px;
    background-color: #f8f9fa;
    padding: 20px;
  }
  
  .slot-content {
    padding: 10px;
    background-color: #e9ecef;
    border-radius: 5px;
  }
  </style>
  