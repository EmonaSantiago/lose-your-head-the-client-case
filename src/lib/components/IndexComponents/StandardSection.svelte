<script>
	import { cursor } from "$lib/stores/cursor";
</script>

<section
	on:mouseenter={() =>
		cursor.set({
			scale: "1",
			color: "rgba(0, 0, 0, 0.15)",
		})}
	on:mouseleave={() =>
		cursor.set({
			scale: "1",
			color: "rgba(255, 240, 33, 0.5)",
			border: "none",
		})}
>
	<slot />
</section>

<style>
	section {
		background-color: var(--color-cmd-yellow);
		display: flex;
		flex-direction: column;
		gap: 1rem;
		padding: 2rem 2rem;
	}

	@media (min-width: 40rem) {
		section {
			padding: 2rem 3rem;
		}
	}

	@media (min-width: 45rem) {
		section {
			display: grid;
			grid-template-columns: 1fr 1fr;
		}
	}
</style>
