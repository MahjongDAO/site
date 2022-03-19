<script>
	import { page } from '$app/stores';
	import logo from './mahj-logo.svg';
</script>

<header>
	<div class="corner">
		<a href="https://www.mahj.vip">
			<img src={logo} alt="Mahjong DAO Home" />
		</a>
	</div>

	<nav>
		<ul>
			<li class:active={$page.url.pathname === '/about'}>
				<a sveltekit:prefetch href="/about">About</a>
			</li>
			<li class:active={$page.url.pathname === '/nfts'}>
				<a sveltekit:prefetch href="https://looksrare.org/collections/0x9831F71ed9E5015e62D3412716ffb8aae122eF2a" target="_blank">NFTs</a>
			</li>
		</ul>
	</nav>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		height: 80px;
	}

	header img {
		height: 100%;
		object-fit: contain;
	}

	nav {
		display: flex;
		justify-content: center;
	}

	ul {
		position: relative;
		padding: 1em 0;
		margin: 0;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
	}

	li {
		position: relative;
		height: 100%;
		margin-left: 2em;
	}

	li.active::before {
		--size: 8px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--pure-white);
	}

	nav a {
		display: flex;
		height: 100%;
		justify-content: center;
		align-items: center;
		font-weight: 700;
		font-size: 1.2rem;
		letter-spacing: 0.05em;
	}

	@media (max-width: 800px) {
		header {
			height: 50px;
		}

		nav a {
			padding-left: 1em;
		}
	}
</style>
