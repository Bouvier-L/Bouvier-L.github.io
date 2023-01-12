<template>
	<img class="wave" src="../assets/waves/up.svg" />
	<div id="hackathon">
		<div id="incluInfo">
			<div class="band">
				<h3>Inclukathon</h3>
				<p id="reward">Récompense : Coup de Coeur</p>
				<p>Défi lancé par l'entreprise :</p>
				<a id="inclulink" href="https://inclusionconseil.fr" target="_blank"
					>Inclusion Conseil <img id="arrow" src="../assets/icons/arrow_top_right.png" alt="top right arrow"
				/></a>
				<p id="resume">
					Site utilisant Vue.js(JavaScript) composé d'un calendrier pour les événements, d'un chat pour échanger avec
					les autres participants, etc. L'API est faite avec Nest.js(TypeScript) et l'ORM Prisma.
				</p>
			</div>
			<div class="blockWrapperRight">
				<div class="block" style="height: 6vh; width: 40%" />
				<div class="block" style="height: 10vh; width: 20%" />
				<div class="block" style="height: 4vh; width: 40%" />
			</div>
		</div>
		<div id="incluImg">
			<div class="incluScreen" id="firstScreen">
				<div class="blockWrapperLeft">
					<div class="block" style="height: 6vh; width: 40%" />
					<div class="block" style="height: 10vh; width: 20%" />
					<div class="block" style="height: 4vh; width: 40%" />
				</div>
				<div class="band">
					<div class="bob">
						<img src="../assets/screenshots/Inclukhaton/chat.png" alt="screenshot of the project's chat service" />
						<p>
							Le chat permet aux participants d'échanger des messages avec ceux du même groupe. Des options pour
							modifier ou supprimer ses messages sont présentes, et tous les messages sont stockées dans la base de
							données. Les administrateurs ayant accès à tous les groupes.
						</p>
					</div>
				</div>
			</div>
			<div class="incluScreen" id="secondScreen">
				<div class="band">
					<div class="bob">
						<p>
							Le calendrier permet de voir tous les événements qui sont stockés dans la base de données. Les
							administrateurs peuvent rajouter des événements et choisir le nom, la date, l'heure et la couleur du tag.
							Il leur est également possible de supprimer un événement en cliquant dessus.
						</p>
						<img
							src="../assets/screenshots/Inclukhaton/calendar.png"
							alt="screenshot of the project's calendar service"
						/>
					</div>
				</div>
				<div class="blockWrapperRight">
					<div class="block" style="height: 6vh; width: 40%" />
					<div class="block" style="height: 10vh; width: 20%" />
					<div class="block" style="height: 4vh; width: 40%" />
				</div>
			</div>
		</div>
	</div>
	<img class="wave" src="../assets/waves/down.svg" />
</template>
