<script>
	import ExerciseBox from './exercise-box.svelte';
</script>

<div class="m-5">
	<div class="box">
		<h1>Exercises</h1>

		<table class="w-full table">
			<tr>
				<td></td>
				<td>10/2</td>
				<td>10/3</td>
				<td>10/4</td>
				<td>10/5</td>
				<td>10/6</td>
				<td>10/7</td>
				<td>10/8</td>
			</tr>
			<ExerciseBox fav={false} name="Shoulder" />
			<ExerciseBox fav={true} name="Arm" />
			<ExerciseBox fav={true} name="Chest" />
			<ExerciseBox fav={false} name="Back" />
			<ExerciseBox fav={true} name="Core" />
		</table>
	</div>
</div>

<style>
	td {
		font-size: 9px;
		padding: 10px;
	}
</style>
