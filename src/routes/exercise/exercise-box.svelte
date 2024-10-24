<script>
	import RandomChecker from '$lib/RandomChecker.svelte';
	import ToggleChecker from '$lib/ToggleChecker.svelte';

	export let name;
	export let fav;
</script>

<tr>
	<th>{name}</th>
	<!-- weekly -->
	<td class="w-6"><RandomChecker /></td>
	<td class="w-6"><RandomChecker /></td>
	<td class="w-6"><RandomChecker /></td>
	<td class="w-6"><RandomChecker /></td>
	<td class="w-6"><RandomChecker /></td>
	<td class="w-6"><RandomChecker /></td>
	<td class="w-6"><RandomChecker /></td>
	<!-- checkmark -->
	<td class="w-6">
		<ToggleChecker />
	</td>
</tr>

<style>
	td {
		text-align: center;
	}

	.box {
		background: lightgray;
		border-radius: 10px;
		padding: 3px 10px;
	}
</style>
