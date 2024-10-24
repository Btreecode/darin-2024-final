<script>
	import '@fortawesome/fontawesome-free/css/all.min.css';
	import './styles.css';
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Knewave&family=Noto+Sans:ital,wght@0,100..900;1,100..900&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<div class="min-h-screen flex flex-col bg-light-blue">
	<nav class="bg-white p-2 space-x-4">
		<!-- <a href="/">Login</a> -->
		<a href="/main" class="text-gradient-pink font-bold text-3xl">daRin</a>
		<!-- <a href="/calendar">Calendar</a> -->
		<!-- <a href="/exercise">Exercise</a> -->
		<!-- <a href="/streaks">streaks</a> -->
	</nav>

	<slot />
</div>

<style>
	nav {
		font-family: 'Knewave';
	}
</style>
