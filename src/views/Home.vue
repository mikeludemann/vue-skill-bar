<template>
	<div class="home">
		<img alt="Vue logo" src="../assets/logo.png">
		<HelloWorld msg="Welcome to Your Vue.js App"/>
    <skillbar text="IT" color="#ddd" bgcolor="#080" :size="80"/>
	</div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import skillbar from '@/components/skill-bar.vue'

export default {
	name: 'home',
	components: {
		HelloWorld,
		skillbar
	}
}
</script>
