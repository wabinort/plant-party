<script>
	// import PlantCard from './Modules/Plant-card.svelte';
	import {
		Card,
		Button,
		Image
	} from 'smelte';
	import "smelte/src/tailwind.css";
	import {plants} from './plants.json';

	const daes = {
		'name': 'cursedcat',
		'photo': '/avatars/cursedcat.jpg',
	}

</script>

<main>
	<p style="color: var(--color-secondary-50)">Wowowowow look at  the plaaaaants</p>
	<p style="color: var(--color-secondary-200)">Wowowowow look at  the plaaaaants</p>
	<p style="color: var(--color-secondary-300)">Wowowowow look at  the plaaaaants</p>
	<p style="color: var(--color-secondary-400)">Wowowowow look at  the plaaaaants</p>
	<p style="color: var(--color-secondary-500)">Wowowowow look at  the plaaaaants</p>


	{#each plants as plant}
		<div style="margin: 1rem; display: inline-block; color: var(--color-primary-200);">
			<Card.Card hover=true classes="rounded">
				<div slot="title">
					<Card.Title
						title={plant.name}
						subheader={plant.genus}
						avatar={daes.photo}
					/>
				</div>
				<div slot="media">
					<div class="card-image">
					<Image
						class="w-full"
						src={plant.photo}
						alt="{plant.name} photo"
					/>
					</div>
				</div>
				<div slot="actions">
					<div class="p-2">
						<Button href="{plant.reference}" block classes="bg-info-500">ok learn</Button>
					</div>
				</div>
			</Card.Card>
		</div>
	 {/each}
	 
	 
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		height: 100vh;
	}

	h1 {
		text-transform: uppercase;
		font-size: 2.5rem;
		font-weight: 100;
	}
	
	.card-image {
		max-width: 20rem;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>