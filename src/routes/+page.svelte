<script>
	import Counter from './Counter.svelte';
	import hall from '$lib/images/hall.jpg';
	import julie from '$lib/images/julie.jpg';
	import machine from '$lib/images/machine.jpg';
	import terrace from '$lib/images/terrace.jpg';
	import kaka from '$lib/images/kaka.jpg';
</script>

<svelte:head>
	<title>4th Floolr, Sundaram PG | Home</title>
	<meta name="description" content="T1, 4th Floolr" />
</svelte:head>

<section>
	<h1>
		<span class="welcome-text">The password is</span><br />sundarbois
	</h1>

	<div class="angry-grid">
		<div id="item-0">
			<picture>
				<img class="landscape" src={julie} alt="Julie, our dog" />
				<caption class="caption"
					>Our best friend</caption
				>
			</picture>
		</div>
		<div id="item-1">
			<picture>
				<img class="portrait" src={machine} alt="Julie, our dog" />
				<caption class="caption"
					>Can I wash my clothes today?</caption
				>
			</picture>
		</div>
		<div id="item-2">
			<picture>
				<img class="portrait" src={hall} alt="Julie, our dog" />
				<caption class="caption"
					>The sovereign republic</caption
				>
			</picture>
		</div>
		<div id="item-3">
			<picture>
				<img class="portrait" src={kaka} alt="Julie, our dog" />
				<caption class="caption"
					>
					A superhero, if there was one
					</caption
				>
			</picture>
		</div>
		<div id="item-4">
			<picture>
				<img class="landscape" src={terrace} alt="Julie, our dog" />
				<caption class="caption"
					>Home</caption
				>
			</picture>
		</div>
	</div>

	<h2>
		<a href="https://t14f.com">t14f</a>
	</h2>
</section>

<style>
	.angry-grid {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		align-content: center;
		gap: 10px;
	}

	#item-0 {
		flex: 1 0 100%;
	}

	#item-1,
	#item-2,
	#item-3 {
		flex: 0 0 calc(33.33% - 10px); /* Adjust the width as needed with proper spacing */
		margin-top: 50rem;
	}

	#item-4 {
		flex: 1 0 100%;
	}

	#item-1 {
		margin-top: 90rem;
	}

	#item-3 {
		margin-top: 120rem;
	}
	.portrait {
		max-width: 100%;
	}

	.landscape {
		max-width: 100%;
		margin-top: 50rem;
	}

	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
		font-size: 5rem;
		line-height: 1.1;
		margin-top: 20rem;
	}

	h2 {
		font-size: 1.5rem;
		text-transform: uppercase;
		font-weight: 600;
		letter-spacing: 0.7rem;
	}

	span.welcome-text {
		font-weight: 300;
		font-style: italic;
	}

	/* Media query for screens smaller than 768px (typical mobile screens) */
	@media screen and (max-width: 768px) {
		h1 {
			font-size: 3rem; /* Decrease the font size for better mobile readability */
		}

		h2 {
			font-size: 1.2rem; /* Decrease the font size for better mobile readability */
			letter-spacing: 0.3rem;
			width: 60%;
			text-align: center;
		}

		.angry-grid {
			flex-direction: column;
		}
	}
</style>
