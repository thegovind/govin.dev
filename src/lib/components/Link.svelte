<script>
	import Icon from './Icon.svelte';
	export let disabled = false;
	export let href;
	export let icon;
	export let target;

	let className;
	// required for export of `class`
	export { className as class };
</script>

<a on:click class={className} {href} {disabled} {target}>
	<slot />
	{#if icon}
		<Icon name={icon} />
	{/if}
</a>
