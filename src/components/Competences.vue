<script setup lang="ts">
import { type Ref, ref } from 'vue';

let displayCards: Ref<Boolean> = ref(true);

function changeCards(btnName: string) {
	let lang = document.getElementById('lang') as HTMLElement
	let frame = document.getElementById('frame') as HTMLElement
	lang.className = lang.className.replace(' activeBtn', '')
	frame.className = frame.className.replace(' activeBtn', '')
	if (btnName === 'frame') {
		frame.className += ' activeBtn'
	}
	if (btnName === 'lang') {
		lang.className += ' activeBtn'
	}
}
</script>

<template>
  <div id="competences">
			<div id="compMenu">
				<div id="btnWrapper">
					<button id="lang" class="btn activeBtn"
						@click.prevent="
							() => {
								if (displayCards === false) {
									displayCards = !displayCards
									changeCards('lang')
								}
							}
						"
					>
						Langages
					</button>
					<button id="frame" class="btn"
						@click.prevent="
							() => {
								if (displayCards === true) {
									displayCards = !displayCards
									changeCards('frame')
								}
							}
						"
					>
						Frameworks
					</button>
				</div>
			</div>
			<div v-if="displayCards" id="languages" class="cardsWin">
				<div class="card" id="python">
					<img src="../assets/icons/python.png" alt="Python icon" sizes="64x64" />
					<h3>Python</h3>
				</div>
				<div class="card" id="typescript">
					<img src="../assets/icons/typescript.png" alt="TypeScript icon" sizes="64x64" />
					<h3>TypeScript</h3>
				</div>
				<div class="card" id="sql">
					<img src="../assets/icons/sql.png" alt="SQL icon" sizes="64x64" />
					<h3>SQL</h3>
				</div>
				<div class="card" id="bash">
					<img src="../assets/icons/bash.png" alt="Bash icon" sizes="64x64" />
					<h3>Bash</h3>
				</div>
			</div>
			<div v-else-if="!displayCards" id="framework" class="cardsWin">
				<div class="card" id="vue">
					<img src="../assets/icons/vuejs.png" alt="Vue.JS icon" sizes="64x64" />
					<h3>Vue.JS</h3>
				</div>
				<div class="card" id="next">
					<img src="../assets/icons/nextjs.png" alt="Next.JS icon" sizes="64x64" />
					<h3>Next.JS</h3>
				</div>
				<div class="card" id="react">
					<img src="../assets/icons/react.png" alt="React.JS icon" sizes="64x64" />
					<h3>React.JS</h3>
				</div>
				<div class="card" id="nest">
					<img src="../assets/icons/nestjs.png" alt="Nest.JS icon" sizes="64x64" />
					<h3>Nest.JS</h3>
				</div>
			</div>
		</div>
</template>

<style lang="css" src="../style/competences.css" scoped />