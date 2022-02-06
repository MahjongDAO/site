<script>
	import Header from '$lib/header/Header.svelte';
	import twitter from './twitter.svg';
	import telegram from './telegram.svg';
	import github from './github.svg';
	import '../app.css';
</script>

<Header />

<main>
	<slot />
</main>

<footer>
	<div>
		<p>© 2022 Mahjong Dao, All Rights Reserved.</p>
	</div>
	<nav>
		<ul>
			<li>
				<a href="https://twitter.com/MahjongDAO" target="_blank">
					<img src={twitter} alt="twitter" />
				</a>
			</li>
			<li>
				<a  href="https://t.me/MahjongDAO" target="_blank">
					<img src={telegram} alt="telegram" />
				</a>
			</li>
			<li>
				<a href="https://github.com/MahjongDAO" target="_blank">
					<img src={github} alt="github" />
				</a>
			</li>
		</ul>
	</nav>
</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100%;
		min-height: 720px;
		margin: 1em auto 0;
		box-sizing: border-box;
	}

	footer {
		display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
		margin: 1em auto 0;
		border-top: 1px solid var(--weak-white-color);
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
		padding-left: 1em;
	}

	footer p {
		color: var(--secondary-color);
		font-size: 0.9em;
		text-decoration: none;
	}

	li img {
		background-color: var(--pure-purple);
    border-radius: 50%;
    background-clip: border-box;
    padding: 8px;
	}

	@media (max-width: 600px) {
		footer {
			flex-direction: column;
			align-items: flex-end;
		}
	}
</style>
