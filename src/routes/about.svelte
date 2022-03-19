<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<svelte:head>
	<title>About</title>
</svelte:head>

<div class="content">
	<h1>About Team</h1>
	<div class="team">
		<div class="team-member">
			<img src="https://cdn.mahj.vip/site/team/Jacky_Lin.jpeg" alt="Jacky Lin"/>
			<div>
				<h1>Jacky Lin</h1>
				<p>Twitter: <a href="https://twitter.com/Zitian_Lin" target="_blank">@Zitian_Lin</a></p>
				<p>Product designer to create good digital products for people.</p>
			</div>
		</div>
		<div class="team-member">
			<img src="https://cdn.mahj.vip/site/team/0xZens.jpeg" alt="0xZens"/>
			<div>
				<h1>0xZens</h1>
				<p>Twitter: <a href="https://twitter.com/0xzens" target="_blank">@0xzens</a></p>
				<p>Web engineer programming with Node.js, Golang, Rust and Solidity.</p>
			</div>
		</div>
	</div>
</div>

<style>
	.content {
		width: 100%;
		margin: 0;
	}
	.team {
		display: flex;
    flex-direction: row;
		justify-content: space-around;
		align-items: center;
	}
	.team-member {
		margin: 0 0 2em 2em;
		width: 400px;
	}
	.team-member:first-child {
		margin-left: 0;
	}
	.team-member img {
		display: block;
		width: 400px;
		height: 400px;
		border-radius: 0.3em;
	}

	.team p {
		margin: 0;
	}

	@media (max-width: 900px) {
		.team {
			flex-direction: column;
			justify-content: space-around;
		}
		.team-member {
			margin-left: 0;
		}
	}
</style>
