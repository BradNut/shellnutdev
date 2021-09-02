<script lang="ts">
  import Header from "../components/Header.svelte";
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
