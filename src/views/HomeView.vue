<script setup lang="ts">
import AboutMe from '../components/AboutMe.vue';
import Competences from '../components/Competences.vue';
import Footer from '../components/Footer.vue';
import Hackhaton from '../components/Hackhaton.vue';
</script>

<template>
	<main>
		<div id="firstStep">
			<div id="cvLink">
				<h1>Loïc BOUVIER</h1>
				<a href="/CV-Bouvier_Loic.pdf" download>Téléchargez mon CV</a>
			</div>
			<p>
				Je suis une personne passionnée et déterminée, toujours prête à apprendre de nouvelles choses. Je suis persuadé
				que je pourrais être un atout pour votre entreprise grâce à ma polyvalence et ma capacité à m'adapter à
				différentes situations.
			</p>
		</div>
		<AboutMe />
		<Competences />
		<Hackhaton />
		<Footer />
	</main>
</template>

<style lang="css" src="../style/firstStep.css" scoped />

<style lang="css" src="../style/footer.css" scoped />
