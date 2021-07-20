<script>
	import Controls from "./Controls.svelte";
	import PlayArea from "./PlayArea.svelte";

	export let name;
</script>

<div class="nes-container is-dark with-title root-container">
	<p class="title">Shortest Path Finder.js</p>
	<div class="row">
		<PlayArea />
		<Controls />
	</div>
</div>

<style>
	.root-container {
		height: inherit;
		width: inherit;
		margin: 0px;
	}
	.row {
		display: flex;
		height: 100%;
		width: inherit;
	}
</style>
