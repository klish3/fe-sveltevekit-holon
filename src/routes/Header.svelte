<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';
	import holonLogo from '$lib/images/logo.png';
</script>

<header>
	<div class="logo-corner">
		<a href="https://kit.svelte.dev">
			<img src={holonLogo} alt="SvelteKit" />
		</a>
	</div>

	<nav>
		<svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
		</svg>
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li aria-current={$page.url.pathname.startsWith('/business-analysis') ? 'page' : undefined}>
				<a href="/business-analysis">Business Analysis</a>
			</li>
			<li
				aria-current={$page.url.pathname.startsWith('/business-process-management')
					? 'page'
					: undefined}
			>
				<a href="/business-process-management">Business Process Management</a>
			</li>
			<li aria-current={$page.url.pathname.startsWith('/executive-coaching') ? 'page' : undefined}>
				<a href="/executive-coaching">Executive Coaching</a>
			</li>
			<li aria-current={$page.url.pathname.startsWith('/strategy-consulting') ? 'page' : undefined}>
				<a href="/strategy-consulting">Strategy Consulting</a>
			</li>
			<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">About</a>
			</li>

			<li aria-current={$page.url.pathname.startsWith('/contact') ? 'page' : undefined}>
				<a href="/contact">Contact</a>
			</li>
		</ul>

		<svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z" />
		</svg>
	</nav>

	<div class="corner"></div>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
	}

	.logo-corner {
		width: 10em;
		height: 4em;
		padding-left: 1em;
		margin-right: -1em;
	}
	.corner {
		width: 3em;
		height: em;
	}
	.corner a,
	.logo-corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		width: 2em;
		height: 2em;
		object-fit: contain;
	}

	nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}

	svg {
		width: 2em;
		height: 3em;
		display: block;
	}

	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page']::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>
