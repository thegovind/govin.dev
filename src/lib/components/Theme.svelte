<script>
	import { browser } from '$app/env';
	import { writable } from 'svelte/store';
	import Button from './Button.svelte';
	export const theme = writable((browser && localStorage.getItem('theme')) || 'dark');
	let dark = $theme == 'dark';

	theme.subscribe((value) => {
		if (browser) {
			localStorage.setItem('theme', value);
			document.documentElement.setAttribute('theme', value);
		}
	});

	$: $theme = dark ? 'dark' : 'light';
</script>

<Button icon={dark ? 'moon' : 'sun'} on:click={() => (dark = !dark)} />
