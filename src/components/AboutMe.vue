<script setup lang="ts">
import { type Ref, ref } from 'vue';

let displayText: Ref<Boolean> = ref(true);

function changeText(btnName: string) {
	let form = document.getElementById('form') as HTMLElement;
	let exp = document.getElementById('exp') as HTMLElement;
	form.className = form.className.replace(' activeBtn', '');
	exp.className = exp.className.replace(' activeBtn', '');
	if (btnName === 'form') {
		form.className += ' activeBtn';
	}
	if (btnName === 'exp') {
		exp.className += ' activeBtn';
	}
}
</script>

<template>
	<div id="aboutMe">
		<div id="aboutMenu">
			<div id="btnWrapper">
				<button
					id="exp"
					class="btn activeBtn"
					@click.prevent="
						() => {
							if (displayText === false) {
								displayText = !displayText;
								changeText('exp');
							}
						}
					"
				>
					Expériences
				</button>
				<button
					id="form"
					class="btn"
					@click.prevent="
						() => {
							if (displayText === true) {
								displayText = !displayText;
								changeText('form');
							}
						}
					"
				>
					Formation
				</button>
			</div>
		</div>
		<p v-if="displayText" class="text" id="expText">
			Parmi mes expériences, j'ai eu l'occasion, à de nombreuses reprises depuis le lycée, de coder des petits
			programmes, et ce dans différents langages. j'ai également eu l'occasion récemment de participer à un hackaton
			avec mon école : un rush de 2 semaines pour réaliser un projet satisfaisant le client. Je travaille également en
			tant qu'autodidacte afin de compléter mes compétences et mon <strong>autonomie</strong>.
		</p>
		<p v-else-if="!displayText" class="text" id="formText">
			Comprendre comment fonctionnent les outils que j'utilise et pouvoir faire mes propres outils qui correspondent à
			mes besoins. C'est pour cette raison que j'ai immédiatement apprécié programmer, et ce dès mes premiers cours
			d'informatique avec python au lycée. Par la suite, je me suis dirigé vers des cursus en rapport avec la
			programmation, mais la méthodologie ne me convenait pas... jusqu'à mon arrivée à l'ETNA. Ce qui est bien, c'est
			que cette école met l'accent sur <strong>l'alternance et l'autonomie</strong>. On apprend en réalisant des projets
			qui nous permettent de découvrir de nouvelles choses à chaques fois.
		</p>
	</div>
</template>

<style lang="css" src="../style/aboutMe.css" scoped />
