<script>
	import { onMount } from 'svelte';
	import maplibre from 'maplibre-gl';

	export let width = 'w-full';

	onMount(() => {
		new maplibre.Map({
			container: 'map', // container id
			style: 'https://basemaps.cartocdn.com/gl/dark-matter-gl-style/style.json',
			center: [0, 0], // starting position [lng, lat]
			zoom: 1 // starting zoom
		});
	});
</script>

<div id="map" class="absolute top-0 bottom-0 {width}" />
