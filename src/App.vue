<template>
  <div>
    <ChildComponent 
      :function1="function1" 
      :function2="function2" 
    />
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';

export default {
  components: {
    ChildComponent
  },
  methods: {
    function1() {
      alert("Function 1 called!");
    },
    function2() {
      alert("Function 2 called!");
    }
  }
};
</script>