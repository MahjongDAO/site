<script context="module">
	import backgroud from './mahj-backgroud.svg';
	export const prerender = true;
</script>

<svelte:head>
	<title>Home - Mahjong DAO</title>
</svelte:head>

<section>
	<div class="welcome">
		<p>Build Mahjong Games</p>
		<p>In The Metaverse</p>
	</div>

	<picture>
		<img src={backgroud} alt="Mahjong Games" />
	</picture>
</section>

<style>
	section {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: stretch;
		flex: 1;
	}

	.welcome {
		display: flex;
		flex-flow: wrap;
    flex-direction: column;
		align-items: flex-start;
    justify-content: center;
	}

	.welcome p {
		margin: 0;
		font-size: 3em;
		font-weight: bolder;
	}

	picture {
		display: flex;
		flex-flow: wrap;
		align-items: center;
    align-content: center;
		height: 720px;
	}

	picture img {
		height: 100%;
		top: 0;
		display: block;
	}

	@media (max-width: 600px) {
		section {
			flex-direction: column;
			justify-content: flex-start;
		}

		picture {
			height: 600px;
			justify-content: center;
		}

		.welcome {
			margin: 1em auto;
			justify-content: center;
		}

		.welcome p {
			font-size: 2em;
			font-weight: normal;
		}
	}
</style>
