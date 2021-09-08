<script lang="ts">
	// import ToggleTheme from '../util/ToggleTheme.svelte';

	export let segment: string;
</script>

<nav aria-label="header navigation">
	<a aria-current={segment === undefined ? 'page' : undefined} href=".">Home</a>
	<a aria-current={segment === 'about' ? 'page' : undefined} href="about">About</a>
	<!-- <a rel="prefetch" aria-current={segment === 'apology' ? 'page' : undefined} href="apology"
		>Apologies</a
	> -->
	<!-- <ToggleTheme /> -->
	<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
				the blog data when we hover over the link or tap it on a touchscreen -->
	<!-- <li><a rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">blog</a></li> -->
</nav>

<style type="text/scss">
	nav {
		position: sticky;
		top: 0;
		z-index: 5;
		display: grid;
		grid-template-columns: repeat(4, auto);
		justify-content: right;
		align-content: center;
		color: var(--lightGrey);

		@media (max-width: 650px) {
			justify-content: center;
		}

		margin: 0.5rem;
		padding: 2rem;

		a + a {
			margin-left: 25px;
		}

		a::after {
			content: '';
			position: absolute;
			width: 100%;
			height: 2px;
			bottom: 0px;
			left: 0px;
			background: var(--linkHover);
			transition: transform 0.3s ease 0s;
			transform: scale(0);
		}

		a {
			position: relative;
			font-size: 2rem;
			text-decoration: none;

			&[aria-current='page'] {
				&:after {
					transform: scale(1);
				}
			}

			&:hover {
				&:after {
					transform: scale(1);
				}
			}
		}
	}
</style>
