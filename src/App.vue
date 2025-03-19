<script>
export default {
  data() {
	return {
		isAdmin: true,
	};
},
};
</script>

<template>
	<p v-if="isAdmin">+++</p>
	<p v-else>---</p>
</template>