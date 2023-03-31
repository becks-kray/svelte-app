<script>
	import { onMount } from 'svelte';
	import maplibre from 'maplibre-gl';

	onMount(() => {
		new maplibre.Map({
			container: 'map', // container id
			style: 'https://demotiles.maplibre.org/style.json', // style URL
			center: [0, 0], // starting position [lng, lat]
			zoom: 1 // starting zoom
		});
	});
</script>

<div class="p-0 m-0">
    <div class="absolute top-0 bottom-0 w-full" id="map"></div>
</div>