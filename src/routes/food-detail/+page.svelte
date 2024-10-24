<script>
	import TableRow from './table-row.svelte';
	import Foods from '../../data/foods.json';

	let showForm = false;
	let searchTxt = '';
	let searchResult = [];
	let eaten = [
		{ name: 'Chicken', icon: '🐔', calories: 400 },
		{ name: 'Pizza', icon: '🍕', calories: 300 },
		{ name: 'Salad', icon: '🥗', calories: 15 }
	];

	$: total = eaten.reduce((p, cur) => p + cur.calories, 0);

	function doShowForm() {
		showForm = true;
	}

	function hideForm() {
		showForm = false;
	}

	function stopPropagation(event) {
		event.stopPropagation();
	}

	function doSearch() {
		searchResult = Foods.filter((v) => v.name.toLowerCase().includes(searchTxt.toLowerCase()));
	}

	function doAdd(f) {
		eaten = [...eaten, { ...f }];
	}
</script>

<div class="m-5 flex flex-col gap-5">
	<div class="box space-y-1">
		<div class="text-lg font-bold">What did i eat today?</div>

		<div class="relative w-60 h-60 mx-auto">
			<svg class="w-full h-full" viewBox="0 0 100 100">
				<!-- Background circle -->
				<circle
					class="text-light-pink grad stroke-current"
					stroke-width="10"
					cx="50"
					cy="50"
					r="40"
					fill="transparent"
				></circle>
				<!-- Progress circle -->
				<circle
					class="text-gradient-pink progress-ring__circle stroke-current"
					stroke-width="10"
					stroke-linecap="round"
					cx="50"
					cy="50"
					r="40"
					fill="transparent"
					stroke-dasharray="251.2"
					stroke-dashoffset="calc(251.2px - (251.2px * {parseInt((total / 3000) * 100)}) / 100)"
				></circle>

				<!-- Center text -->
				<text
					x="50"
					y="56"
					font-family="Verdana"
					font-size="7"
					text-anchor="middle"
					color="darkgray"
					alignment-baseline="middle">{total} / 3000 kcal</text
				>
			</svg>
		</div>
	</div>

	<div class="box space-y-3">
		<div class="flex justify-between">
			<div>name</div>
			<div>cal</div>
		</div>

		{#each eaten as f}
			<TableRow val={f.calories} emoji={f.icon} name={f.name} />
		{/each}
		<!-- <TableRow val={45} emoji="🍕" name="Pizza" /> -->
		<!-- <TableRow val={88} emoji="🥗" name="Salad" /> -->
	</div>

	<button
		class="cursor-pointer fixed right-10 bottom-10 text-primary bg-base-100 w-8 aspect-square flex justify-center items-center rounded-full"
		on:click={doShowForm}
	>
		<i class="fa fa-plus" />
	</button>
</div>

{#if showForm}
	<button
		class="fixed h-screen w-screen flex justify-center items-center"
		on:click={hideForm}
		style="background-color: rgba(0,0,0,0.5)"
	>
		<button class="card bg-base-100 w-96 shadow-xl" on:click={stopPropagation}>
			<div class="card-body w-full">
				<h2 class="card-title">aDD fOOD</h2>
				<input class="search bg-gray-200" bind:value={searchTxt} />
				<div class="card-actions justify-end">
					<button class="btn btn-primary" on:click={doSearch}>SEARCH</button>
				</div>
				<div class="my-2 flex flex-wrap gap-1">
					{#each searchResult as f}
						<button class="btn btn-xs bg-gray-500 text-sm" on:click={() => doAdd(f)}
							>{f.icon} {f.name}</button
						>
					{/each}
				</div>
			</div>
		</button>
	</button>
{/if}

<style>
	.text-light-orange {
		color: #ffefd6;
	}

	.text-light-pink {
		color: #fee6ed;
	}
</style>
