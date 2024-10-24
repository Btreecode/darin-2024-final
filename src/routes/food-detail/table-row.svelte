<script>
	export let name;
	export let emoji;
	export let val;
</script>

<div class="flex">
	<div class="flex items-center">
		<div class="text-lg mx-2 w-5 h-5 flex justify-center items-center rounded-full">
			{emoji}
		</div>
	</div>
	<div class="flex-1">
		<div class="flex justify-between">
			<div class="font-bold">{name}</div>
			<div>{val}</div>
		</div>

		<div>
			<progress class="progress progress-warning h-4" value={val} max="500"></progress>
		</div>
	</div>
</div>
