<script lang="ts">
	import Header from '../components/Header.svelte';
	import 'normalize.css';
	// import { theme } from './stores';
	// import { onMount } from 'svelte';

	// onMount(() => {
	// 	if ($theme === 'dark') {
	// 		document.querySelector('html').classList.add('dark');
	// 	}
	// });

	export let segment: string;
</script>

<Header {segment} />
<main>
	<slot />
</main>

<style type="text/scss">
	:global(:root) {
		--red: #900;
		--pinkRed: #ff5470;
		--blue: #369;
		--purpleBlue: #2e2b5e;
		--white: #fffffe;
		--greyWhite: #e6e3e0;
		--grey: #efefef;
		--yellow: #ffc600;
		--light: #fff;
		--black: #1b2d45;
		--dark: #000;
		--seaGreen: #83c6a4;
		--lighterDark: #131415;
		--shellYellow: #ffc850;
		--purple: #7a5a84;
		--lightGrey: #c5c5c5;
		--lightGray: var(--lightGrey);
		--lightShade: #f8f7f5;
		--darkGrey: #272727;

		/* Define Colors intentions */
		--primary: var(--purple);
		--secondary: var(--seaGreen);
		--danger: var(--pinkRed);
		--background: var(--greyWhite);
		--textColor: var(--black);
		--buttonTextColor: var(--black);
		--textAccent: var(--purpleBlue);
		--lineColor: var(--grey);
		--cardBg: var(--secondary);
		--headerBackground: var(--lightShade);
		--footerBackground: var(--darkGrey);
		--linkHover: var(--purpleBlue);
		--lightHairLine: var(--lightGrey);

		/* Toggle Switch */
		--toggleBackgroundColor: var(--lightGray);
		--toggleBackgroundUnchecked: var(--lightGrey);
		--toggleCheckedBackgroundColor: var(--seaGreen);
		--toggleButtonColor: var(--primary);

		/* Styles */
		--line: solid 1px var(--lineColor);

		/* Type */
		--headingFont: 'Fira Sans';
		--bodyFont: 'Merriweather';
		--baseFontSize: 100%;
		--h1: 3.052rem;
		--h2: 2.441rem;
		--h3: 1.953rem;
		--h4: 1.563rem;
		--h5: 1.25rem;
		--h6: 1.8rem;
		--bodyTextSize: 1.8rem;
		--smallText: 1.44rem;
		--lineHeight: 1.75;

		/* Font Sizes */
		--xsFont: 1.2rem;
		--smFont: 1.4rem;
		--mdFont: 1.4rem;
		--lgFont: 1.8rem;
		--xlFont: 2rem;

		/* Radius */
		--xsRadius: 0.2rem;
		--smRadius: 0.4rem;
		--mdRadius: 0.8rem;
		--lgRadius: 1.6rem;
		--xlRadius: 3.2rem;

		/* Spacing */
		--xsSpacing: 1rem;
		--smSpacing: 1.2rem;
		--mdSpacing: 1.6rem;
		--lgSpacing: 2rem;
		--xlSpacing: 2.4rem;

		/* Elevation */
		--level-0: none;
		--level-1: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
		--level-2: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
		--level-3: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
		--level-4: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);

		/* Positioning */
		--containerPadding: 2.5%;
		--headerHeight: 8rem;
		--borderRadius: 10px;
		--buttonRadius: 8px;
		--maxWidth: 1000px;

		/* Color Theme */
		--colorScheme: 'light';
	}

	:global(html) {
		box-sizing: border-box;
		font-size: 10px;
	}

	:global(*) {
		box-sizing: inherit;
	}

	:global(*:before) {
		box-sizing: inherit;
	}

	:global(*:after) {
		box-sizing: inherit;
	}

	:global(figure) {
		margin: 0 auto;
	}

	:global(p) {
		margin: 0 auto;
	}

	:global(a.button) {
		background: var(--shellYellow);
		color: var(--lightShade);
		border: 0;
		padding: 0.6rem 1rem;
		border-radius: 2px;
		cursor: pointer;
		--cast: 2px;
		box-shadow: var(--cast) var(--cast) 0 var(--lightAccent);
		text-shadow: 0.5px 0.5px 0 rgba(0, 0, 0, 0.2);
		transition: all 0.2s;
		text-decoration: none;
		&:hover {
			--cast: 4px;
		}
		&:active {
			--cast: 2px;
		}
	}

	:global(button) {
		background: var(--shellYellow);
		color: var(--lightShade);
		border: 0;
		padding: 0.6rem 1rem;
		border-radius: 2px;
		cursor: pointer;
		--cast: 2px;
		box-shadow: var(--cast) var(--cast) 0 var(--lightAccent);
		text-shadow: 0.5px 0.5px 0 rgba(0, 0, 0, 0.2);
		transition: all 0.2s;
		text-decoration: none;
		&:hover {
			--cast: 4px;
		}
		&:active {
			--cast: 2px;
		}
	}

	:global(.card) {
		padding: 1.5rem;
		background: var(--cardBg);
		box-shadow: var(--level-3);
		border-radius: var(--borderRadius);
		color: var(--textColor);

		*:first-child {
			margin-top: 0;
		}

		*:last-child {
			margin-bottom: 0;
		}
	}

	main {
		// position: relative;
		max-width: var(--maxWidth);
		margin: 0 auto;
		padding: 2rem 0rem;

		p,
		li,
		label {
			word-wrap: normal;
			font-size: 1.8rem;
			color: var(--lightShade);
		}
	}
</style>
