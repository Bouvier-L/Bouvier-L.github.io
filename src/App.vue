<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';
</script>

<template>
	<header>
		<div class="wrapper">
			<nav>
				<RouterLink class="link" to="/">Accueil</RouterLink>
				<RouterLink class="link" to="/projects">Projets</RouterLink>
			</nav>
		</div>
	</header>

	<RouterView />
</template>

<style lang="css" src="./style/global.css" />

<style lang="css" src="./style/hackathon.css" />

<style lang="css" src="./style/header.css" scoped />

