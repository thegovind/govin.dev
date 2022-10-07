<script>
	import Link from './Link.svelte';
</script>

<footer>
	<div class="social">
		<Link class="button" href="https://github.com/thegovind" icon="github" />
		<Link class="button" href="/rss.xml" icon="rss" />
	</div>
</footer>

<style>
	footer {
		width: 100%;
		padding: 0.5rem 1rem 1rem;
		border-top: 1px solid var(--border);
		background: var(--background-secondary);
		color: #a8a8a8;
	}
	footer .social {
		display: flex;
		justify-content: end;
	}
</style>
