<script>
export default {

data() {
	return {
		arr: ['x', 'y', 'z'],
        arr1: [1, 2, 3],
	}
}

};
</script>


<template>
	<p>{{ arr[0] }}</p>
	<p>{{ arr[1] }}</p>
	<p>{{ arr[2] }}</p>
    <p>{{ arr1[0] + arr1[1] + arr1[2]}}</p>
</template>
