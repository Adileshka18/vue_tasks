<script>
export default {
  data() {
	return {
		text: 'page',
		href: 'page.html',
	}
}
};
</script>


<template>
  <a :href="href">{{ text }}</a>
</template>
