<script>
	export let standardUID;
	export let chapterUID;
	export let chapterTitle;

	import { cursor } from "$lib/stores/cursor";

	const path = standardUID.toLowerCase().split(' ').join('-');
</script>

<li>
	<a
		on:mouseenter={() =>
			cursor.set({
				scale: "1.1",
				color: "rgba(0, 0, 0, 0.15)",
				border: "2px dashed #000",
			})}
		on:mouseleave={() =>
			cursor.set({
				scale: "1",
				color: "rgba(0, 0, 0, 0.15)",
				border: "none",
			})}
		href="{path}#{chapterUID}">{chapterTitle}</a
	>
</li>

<style>
	a {
		padding: 0.5rem 0;
		color: var(--color-black);
		max-width: 20rem;
	}
</style>
