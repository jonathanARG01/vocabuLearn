<script setup lang="ts">
	import Person from './components/Person.vue';
	import List from './components/List.vue';
</script>



<template>
	<main>
		<Person name="Jonathan Rojas" :age="30" :isAlive="true" />
		<!-- <List /> -->
	</main>
</template>



<style scoped>
	@media (min-width: 1024px) {
		
	}
</style>
