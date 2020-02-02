<template lang="html">

	<section class="skill-bar">
		<div :class="[classname,'container']">
			<div>{{this.text}}</div>
			<div class="container" :style="container">
				<div class="skill--level" :style="skillLevel">{{this.size + " %"}}</div>
			</div>
		</div>
	</section>

</template>

<script lang="js">

	export default {
		name: 'skillbar',
		props: {
			classname: {
				type: String,
				required: false
			},
			text: {
				type: String,
				required: false
			},
			size: {
				type: Number,
				required: true
			},
			color: {
				type: String,
				required: false
			},
			bgcolor: {
				type: String,
				required: false
			}
		},
		mounted () {

		},
		data () {
			return {

			}
		},
		methods: {

		},
		computed: {
			container: function() {
				return {
					backgroundColor: "#eee",
					width: "100%"
				};
			},
			skillLevel: function() {
				return {
					color: this.color || "#000",
					backgroundColor: this.bgcolor || "#fff",
					width: this.size + "%",
					textAlign: "left",
					padding: "10px 10px"
				};
			}
		}
}


</script>

<style scoped lang="scss">
	.skill-bar {

	}
</style>
