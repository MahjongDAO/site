<script context="module">
	import backgroud from './mahj-backgroud.svg';
	export const prerender = true;
</script>

<svelte:head>
	<title>Home - Mahjong DAO</title>
</svelte:head>

<section>
	<div class="left-content">
		<div class="welcome">
			<p>Build Mahjong Games</p>
			<p>In The Metaverse</p>
		</div>

		<div class="tokenomics">
			<h2><a href="https://mahj.notion.site/Mahjong-DAO-WHITEPAPER-70c658d2e6284cd7a802dfe1bb96d726" target="_blank">NFTs TOKENOMICS</a></h2>
			<p><b>Total Supply</b>: 148 Mahjong tile NFTs</p>
			<p><b>DAO Members</b>: who owns mahjong tile NFTs</p>
			<p><b>DAO Team</b>: who owns 🀢🀣🀤🀥🀦🀧🀨🀩 NFTs</p>
			<p><b>DAO Treasury</b>: 20% sales revenue</p>
			<p><b>$MAHJ Liquidity</b>: 80% sales revenue</p>
		</div>
		<div class="tokenomics">
			<h2>$MAHJ TOKENOMICS</h2>
			<p><b>Total Supply</b>: 21,000,000,000</p>
			<p><b>Liquidity Pool</b>: 40% of total supply</p>
			<p><b>Stake Rewards</b>: 30% of total supply</p>
			<p><b>DAO Treasury</b>: 20% of total supply</p>
			<p><b>Workgroup Rewards</b>: 10% of total supply</p>
		</div>

		<div class="welcome"></div>
	</div>

	<picture class="right-content">
		<img src={backgroud} alt="Mahjong Games" />
	</picture>
</section>

<section class="roadmap">
	<h2>Road Map</h2>
	<div>
		<h3>2022 Q1</h3>
		<p><a href="https://etherscan.io/address/0x9831F71ed9E5015e62D3412716ffb8aae122eF2a" target="_blank">Contract deployed</a><i class="icon-check">✔</i></p>
		<p>03-08 NFTs listing on <a href="https://looksrare.org/collections/0x9831F71ed9E5015e62D3412716ffb8aae122eF2a" target="_blank">LooksRare</a><i class="icon-check">✔</i></p>
		<p>03-15 NFTs public sales<i class="icon-check">✔</i></p>
	</div>
	<div>
		<h3>2022 Q2</h3>
		<p>Bridging to <a href="https://bridge.avax.network/" target="_blank">Avalanche</a></p>
		<p>05-02 $MAHJ listing on <a href="https://traderjoexyz.com/trade" target="_blank">Trader Joe</a></p>
		<p>NFTs and $MAHJ staking</p>
		<p>Listing on Coingecko / CoinMarketCap</p>
	</div>
	<div>
		<h3>2022 Q3</h3>
		<p>Launching mahjong DAO surrounding souvenirs</p>
	</div>
	<div>
		<h3>2022 Q4</h3>
		<p>Launching a Sub DAO & mahjong game</p>
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: stretch;
		flex: 1;
		width: 100%;
	}

	.left-content {
		display: flex;
		flex-flow: wrap;
    flex-direction: column;
		align-items: flex-start;
    justify-content: space-evenly;
	}

	.welcome {
		width: 100%;
	}

	.welcome p {
		margin: 0;
		font-size: 2em;
		font-weight: bolder;
	}

	.tokenomics {
		max-width: 360px;
		width: calc(100% - 2em);
		margin-top: 1em;
		padding: 1em;
    background-color: var(--weak-black-color);
    border-radius: 0.3em;
	}

	.tokenomics h2 {
		margin: 0;
		font-size: 1.5em;
		font-weight: bolder;
	}

	.roadmap p,
	.tokenomics p {
		margin: 0.5em 0 0 0;
		font-size: 1em;
	}

	picture.right-content {
		display: flex;
		flex-flow: wrap;
		align-items: center;
    align-content: center;
		height: 720px;
	}

	picture.right-content img {
		height: 100%;
		top: 0;
		display: block;
	}

	.roadmap {
		flex-wrap: wrap;
		width: calc(100% - 2em);
		margin: 1em 0 0;
		padding: 1em;
    background-color: var(--weak-black-color);
    border-radius: 0.3em;
	}

	.roadmap h2 {
		width: 100%;
		font-size: 1.5em;
		font-weight: bolder;
		margin: 0;
	}

	.roadmap div {
		width: 50%;
	}

	.roadmap h3 {
		font-size: 1em;
		color: var(--primary-color);
		margin: 2em auto 0;
	}

	.icon-check {
		color: var(--pure-purple);
		padding-left: 1em;
	}

	@media (max-width: 600px) {
		section {
			flex-direction: column;
			justify-content: flex-start;
		}

		picture.right-content {
			height: 600px;
			justify-content: center;
			margin-top: 1em;
		}

		.welcome {
			text-align: center;
		}

		.welcome p {
			font-weight: normal;
		}

		.roadmap div {
			width: 100%;
		}
	}
</style>
