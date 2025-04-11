<template>
    <div>
      <button @click="function1">Call Function 1</button>
      <button @click="function2">Call Function 2</button>
    </div>
  </template>
  
  <script>
  export default {
    props: ['function1', 'function2']
  };
  </script>