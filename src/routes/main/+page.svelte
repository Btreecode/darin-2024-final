<script>
	import Exercise from './exercise.svelte';
	import Food from './food.svelte';
	import Calendar from './calendar.svelte';
</script>

<div class="flex-1 flex flex-col p-5 gap-5">
	<a href="/food-detail" class="box center flex-1">
		<img src="/burger-food.png" class="h-24" alt="burger" />
	</a>
	<a href="/exercise" class="box center flex-1">
		<img src="/running-Exercise.png" class="h-24" alt="burger" />
	</a>
</div>

<style>
	.box:hover {
		background: skyblue;
	}

	.box:active {
		background: rgb(0, 0, 0);
		text-decoration: white;
	}
</style>
