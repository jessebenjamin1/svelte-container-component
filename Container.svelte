<script>
	export let sm = false;
	export let md = false;
	export let lg = false;
	export let xl = false;
	export let xxl = false;
	export let xxxl = false;
	export let stack = false;
	export let w = '100%';
	export let maxW = '48rem';
	export let klass = '';
	let classes = `${klass} container`;
</script>

<div
	class={classes}
	class:maxW
	class:sm
	class:md
	class:lg
	class:xl
	class:xxl
	class:xxxl
	class:stack
>
	<slot />
</div>

<style>
	.container {
		margin: auto;
		width: var(--w);
	}

	.maxW {
		max-width: var(--maxW);
	}

	.sm {
		max-width: 36rem;
	}

	.md {
		max-width: 48rem;
	}

	.lg {
		max-width: 64rem;
	}

	.xl {
		max-width: 80rem;
	}

	.xxl {
		max-width: 96rem;
	}

	.xxxl {
		max-width: 120rem;
	}

	.stack {
		display: grid;
		gap: var(--spacing);
	}
</style>
