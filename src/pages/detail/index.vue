<template>
	<div>这是一个详情页{{id}}</div>
</template>

<script>
export default{
	data () {
		return {
			id: 0
		}
	},

	onLoad (options) {
		console.log(options);
		this.id = options['id'];
	}
}
</script>

<style>
</style>