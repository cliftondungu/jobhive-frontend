<template>
    <header class="header">
      <div class="logo">
        <h1>{{ appTitle }}</h1>
      </div>
    </header>
  </template>
  
  <script>
  export default {
    data() {
      return {
        appTitle: 'JobHive'
      }
    }
  }
  </script>
  
  <style>
  .header {
    display: grid;
    grid-template-columns: auto;
    align-items: center;
    padding: 20px;
    background-color: #fff;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .logo h1 {
    margin: 0;
    font-size: 24px;
    font-weight: bold;
  }
  </style>
  