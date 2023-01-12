<script setup lang="ts">
import { onMounted } from 'vue';

let cardIndex = 1;

onMounted(() => {
	showCards(cardIndex);
});

// Next/previous controls
function plusCards(n: number) {
	showCards((cardIndex += n));
}

// Thumbnail image controls
function currentCard(n: number) {
	showCards((cardIndex = n));
}

function showCards(n: number) {
	let i: number;
	let cards = Array.from(document.getElementsByClassName('card') as HTMLCollectionOf<HTMLElement>);
	let dots = document.getElementsByClassName('dot');
	if (n > cards.length) {
		cardIndex = 1;
	}
	if (n < 1) {
		cardIndex = cards.length;
	}
	for (i = 0; i < cards.length; i++) {
		cards[i].style.display = 'none';
	}
	for (i = 0; i < dots.length; i++) {
		dots[i].className = dots[i].className.replace(' active', '');
	}
	cards[cardIndex - 1].style.display = 'flex';
	dots[cardIndex - 1].className += ' active';
}
</script>

<template>
	<div id="projects">
		<div id="cardShow">
			<div class="card fade">
				<div class="imgWrapper">
					<img
						src="../assets/screenshots/Inclukhaton/chat.png"
						alt="screenshot for hyrule project's start menu"
					/>
					<img
						src="../assets/screenshots/Inclukhaton/calendar.png"
						alt="screenshot for hyrule project's fight menu"
					/>
				</div>
				<div class="description">
					<h1>Inclukathon</h1>
				<p id="reward">Récompense : Coup de Coeur</p>
				<p>Défi lancé par l'entreprise :</p>
				<a id="inclulink" href="https://inclusionconseil.fr" target="_blank"
					>Inclusion Conseil <img id="arrow" src="../assets/icons/arrow_top_right.png" alt="top right arrow"
				/></a>
				<p>
					Site utilisant Vue.js(JavaScript) composé d'un calendrier pour les événements, d'un chat pour échanger avec
					les autres participants, etc. L'API est faite avec Nest.js(TypeScript) et l'ORM Prisma.
				</p>
				</div>
			</div>
			<div class="card fade">
				<div class="imgWrapper">
					<img
						src="../assets/screenshots/hyrule-piscine/hyrule_start.png"
						alt="screenshot for hyrule project's start menu"
					/>
					<img
						src="../assets/screenshots/hyrule-piscine/hyrule_fight.png"
						alt="screenshot for hyrule project's fight menu"
					/>
				</div>
				<div class="description">
					<h1>Hyrule Castle</h1>
					<p>
						Mini-jeu RPG basé sur des combats au tour par tour en TypeScript. Le joueur peut choisir le nombre d'étages
						à franchir, ainsi que la difficulté et le personnage qu'il jouera. Les enemis sont aléatoires et il est
						possible de vérifier les forces et faiblesses de chaque héros et enemis.
					</p>
				</div>
			</div>
			<div class="card fade">
				<div class="imgWrapper">
					<img
						src="../assets/screenshots/animalplayground/AP-history.png"
						alt="screenshot for animal playground project's order's history page"
					/>
					<img
						src="../assets/screenshots/animalplayground/AP-admin.png"
						alt="screenshot for animal playground project's admin page"
					/>
				</div>
				<div class="description">
					<h1>Animal Playground</h1>
					<p>
						Site d'e-commerce codé en TypeScript et utilisant React. Le site est relié à une base de données et l'API
						utilise l'ORM Sequelize. Les utilisateurs peuvent passer une commande ou voir leur historique d'achats. Il
						est également possible, en tant qu'administrateur, d'ajouter ou de supprimer un produit.
					</p>
				</div>
			</div>
			<div class="card fade">
				<div class="imgWrapper">
					<img
						src="../assets/screenshots/ia-gradient_descent/cost.png"
						alt="screenshot for ia-gradient_decent project's cost function visualization"
					/>
					<img
						src="../assets/screenshots/ia-gradient_descent/model.png"
						alt="screenshot for ia-gradient_decent project's model visualization"
					/>
				</div>
				<div class="description">
					<h1>IA - Gradient Descent</h1>
					<p>
						IA qui optimise un modèle linéaire pour qu'il corresponde le plus possible aux données reçues. L'algorithme
						utilisé est la descente de gradient, et le projet est en Python.
					</p>
				</div>
			</div>
		</div>
		<a class="prev" @click.prevent="() => plusCards(-1)">&#10094;</a>
		<a class="next" @click.prevent="() => plusCards(1)">&#10095;</a>
		<div id="dots">
			<span class="dot" @click.prevent="() => currentCard(1)"></span>
			<span class="dot" @click.prevent="() => currentCard(2)"></span>
			<span class="dot" @click.prevent="() => currentCard(3)"></span>
			<span class="dot" @click.prevent="() => currentCard(4)"></span>
		</div>
	</div>
</template>

<style lang="css" src="../style/projectsPage.css" scoped />