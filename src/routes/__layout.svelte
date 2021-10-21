<script>
	import Icon from '../components/icon.svelte';
	let darkMode = true;

	const toggleDarkMode = () => {
		darkMode = !darkMode;
		const body = document.querySelector('body');
		body.className = darkMode ? 'dark-mode' : '';
	};
</script>

<nav class="topnav">
	<div class="leftside">
		<a href="/">Home</a>
		<a href="/contact">Contact</a>
	</div>
	<button on:click={toggleDarkMode}>
		<Icon name="lamp" class={darkMode ? 'light-fill' : 'dark-fill'} />
	</button>
</nav>

<slot />

<footer>
	<p>
		This website was made using <a href="https://kit.svelte.dev/" target="_blank">SvelteKit</a>, a
		highly performant, minimalist, production-ready frontend framework. I'm a big fan.
	</p>
</footer>

<style lang="scss">
	@import 'src/styles/layout.scss';
</style>
