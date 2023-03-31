<script>
	import Sidebar from '../../components/Sidebar.svelte';
	import Map from '../../components/Map.svelte';
</script>

<div class="grid grid-cols-4 gap-5">
	<div class="col-span-3 h-100">
		<Map width="w-3/4" />
	</div>
	<Sidebar />
</div>

<style lang="postcss">
	:global(html) {
		background-color: theme(colors.gray.800);
	}
</style>
