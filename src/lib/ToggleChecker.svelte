<script>
	let checked = false;
</script>

<button
	class="btn btn-sm {checked ? 'btn-success' : 'btn-ghost'}"
	on:click={() => (checked = !checked)}><i class="fa fa-check" /></button
>
