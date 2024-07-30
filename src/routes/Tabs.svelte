<script>
	import { page } from '$app/stores';
</script>

<section>
	<ul>
		<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
			<a href="/">Home</a>
		</li>
		<li aria-current={$page.url.pathname === '/setup' ? 'page' : undefined}>
			<a href="/basics">About</a>
		</li>
		<li aria-current={$page.url.pathname.startsWith('/configuration') ? 'page' : undefined}>
			<a href="/configuration">Configuration</a>
		</li>
		<li aria-current={$page.url.pathname.startsWith('/pid') ? 'page' : undefined}>
			<a href="/pid">PID</a>
		</li>
		<li aria-current={$page.url.pathname.startsWith('/receiver') ? 'page' : undefined}>
			<a href="/receiver">Receiver</a>
		</li>
		<li aria-current={$page.url.pathname.startsWith('/modes') ? 'page' : undefined}>
			<a href="/modes">Modes</a>
		</li>
		<li aria-current={$page.url.pathname.startsWith('/gps') ? 'page' : undefined}>
			<a href="/gps">GPS</a>
		</li>
		<li aria-current={$page.url.pathname.startsWith('/motors') ? 'page' : undefined}>
			<a href="/motors">Motors</a>
		</li>
		<li aria-current={$page.url.pathname.startsWith('/sensors') ? 'page' : undefined}>
			<a href="/sensors">Sensors</a>
		</li>
		<li aria-current={$page.url.pathname.startsWith('/tetheredlogging') ? 'page' : undefined}>
			<a href="/tetheredlogging">Tethered Logging</a>
		</li>
		<li aria-current={$page.url.pathname.startsWith('/cli') ? 'page' : undefined}>
			<a href="/cli">CLI</a>
		</li>
	</ul>
</section>

<style>
	section {
		background: white;
	}

	ul {
		padding-inline: 1rem;
		margin: 0;
		height: 3em;
		justify-content: center;
		align-items: center;
		list-style: none;
	}

	li {
		width: 10rem;
		position: relative;
		height: 100%;
		margin: 0.5rem 0;
	}

	li[aria-current='page']::before {
		color: var(--color-theme-1);
	}

	li[aria-current='page'] a {
		color: var(--color-theme-1);
	}

	li a {
		background-color: var(--color-bg-1);
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
		border-radius: 5px;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>
