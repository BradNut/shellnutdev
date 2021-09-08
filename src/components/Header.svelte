<script lang="ts">
	import Logo from './Logo.svelte';
	import Nav from './Nav.svelte';

	export let segment: string;
</script>

<header>
	<Logo />
	<Nav {segment} />
</header>

<style lang="scss">
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		background-color: var(--lightGrey);
		background: var(--headerBackground);
		box-shadow: var(--level-2);
		padding: 0 var(--containerPadding);
		font-size: 1.6rem;

		@media (max-width: 1000px) {
			padding-top: 3rem;
		}

		@media (max-width: 650px) {
			display: grid;
			align-content: center;
			justify-items: center;
			grid-template-columns: 1fr;
		}
	}
</style>
