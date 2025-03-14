<script>
export default {
  data() {
	return {
		num: 5,
        num1: 1,
		num2: 2,
		num3: 3,
	}
}
};
</script>


<template>
	<p>{{ num * num }}</p>
    <p>{{ num1 + num2 + num3 }}</p>
</template>
