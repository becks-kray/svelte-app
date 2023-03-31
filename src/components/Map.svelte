<script lang="ts">
	import { onMount } from 'svelte';
	import { Map, MapMouseEvent } from 'maplibre-gl';

	export let width = 'w-full';

    let map: Map;
    const url = 'https://api.opentopodata.org/v1/srtm30m';

    async function onMapClick(event: MapMouseEvent) {
        console.log('event', event);
        const { lat, lng } = event.lngLat;
    }
	onMount(() => {
		map = new Map({
			container: 'map', // container id
			style: 'https://basemaps.cartocdn.com/gl/dark-matter-gl-style/style.json',
			center: [-85, 42], // starting position [lng, lat]
			zoom: 5 // starting zoom
		});
        map.on('click', onMapClick);
	});
</script>

<div id="map" class="absolute top-0 bottom-0 {width}" />
