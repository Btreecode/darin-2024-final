<!-- <script>
	import { Line } from 'svelte-chartjs';
	import { data } from './data.js';

	import {
		Chart as ChartJS,
		Title,
		Tooltip,
		Legend,
		LineElement,
		LinearScale,
		PointElement,
		CategoryScale
	} from 'chart.js';

	ChartJS.register(Title, Tooltip, Legend, LineElement, LinearScale, PointElement, CategoryScale);
</script> -->

<div>
	<div class="flex">
		<div class="bg-gray-300 rounded-full flex items-center justify-center p-0.5">
			<i class="fa-dumbbell fa-solid"></i>
		</div>
		<div class="flex-1">Gym</div>
		<div>...</div>
	</div>
	<div class="flex items-end space-x-1">
		<div class="text-2xl font-bold">1200</div>
		<div class="text-gray-500">minute</div>
	</div>
	<div class="flex items-end space-x-0.5">
		<!-- <Line {data} options={{ responsive: true }} /> -->
		<div class="w-1 h-10 bg-green-500"></div>
		<div class="w-1 h-2 bg-green-500"></div>
		<div class="w-1 h-6 bg-green-500"></div>
		<div class="w-1 h-12 bg-green-500"></div>
		<div class="w-1 h-10 bg-green-500"></div>
		<div class="w-1 h-2 bg-green-500"></div>
		<div class="w-1 h-6 bg-green-500"></div>
		<div class="w-1 h-12 bg-green-500"></div>
	</div>
</div>
