<script>
	import BottomGraph from './bottom-graph.svelte';
</script>

<div class="p-5">
	<div class="grid grid-cols-2 gap-2 theGrid">
		<a href="/food-detail">
			<div>breakfast</div>
			<div>+</div>
		</a>

		<a href="/food-detail">
			<div>lunch</div>
			<div>+</div>
		</a>

		<a href="/food-detail">
			<div>dinner</div>
			<div>+</div>
		</a>

		<a href="/water-timer">
			<div>water</div>
			<div>+</div>
		</a>
	</div>

	<div class="h-8"></div>

	<BottomGraph />
</div>

<div class="fixed bottom-4 left-1/2 transform -translate-x-1/2">
	<button class="text-blue-500 border border-blue-500 rounded-full px-2 py-1 text-sm"> + </button>
</div>

<!-- <div class="fixed h-screen w-screen flex justify-center items-center">
	<div class="card bg-base-100 w-96 h-96 shadow-xl">
		<div class="card-body">
			<h2 class="card-title">fOOD</h2>
			<input class="search" />
			<div class="card-actions justify-end">
				<button class="btn btn-primary">SEARCH</button>
			</div>
		</div>
	</div>
</div> -->

<style>
	.theGrid > a {
		background: lightgray;
		display: flex;
		flex-direction: column;
		padding: 10px;
		border-radius: 20px;
	}

	.theGrid > a > div:nth-child(2) {
		color: darkblue;
		font-size: 80px;
		line-height: 80px;
		text-align: center;
	}

	.search {
		border: 1px solid black;
	}
</style>
