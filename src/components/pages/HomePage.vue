<template>
	<div class="home">
		<main-section></main-section>
		<main-grid></main-grid>
		<mainComponent></mainComponent>
		<mainTeach></mainTeach>
		<main-theme />
	</div>
</template>

<script setup>
import mainGrid from '@/components/Main/mainGrid.vue'
import MainSection from '@/components/Main/mainSection.vue'
import mainTheme from '@/components/Main/mainTheme.vue'
import mainComponent from '../Main/mainComponent.vue'
import mainTeach from '../Main/mainTeach.vue'
</script>

<style scoped></style>
