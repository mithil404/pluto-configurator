<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';
	async function connectToDevice() {
		chrome.sockets.tcp.create({}, (createInfo) => {
			chrome.sockets.tcp.connect(createInfo.socketId, '192.168.4.1', 23, (result) => {
				if (result < 0) {
					errorMessage = `Error: ${result}`;
					console.error(errorMessage);
					return;
				}
				usbDevice = createInfo.socketId;
				console.log('Connected to device');
			});
		});
	}
</script>

<header>
	<div class="corner">
		<a href="/">
			<img src={logo} alt="SvelteKit" />
		</a>
	</div>
	<ul id="usb"></ul>
	<div>
		<button
			on:click={(e) => {
				connectToDevice();
			}}>Connect</button
		>
	</div>
</header>

<style>
	header {
		background-color: white;
		display: flex;
		justify-content: space-between;
		align-items: center;
		text-align: center;
		padding-right: 1em;
	}

	.corner {
		width: 3em;
		height: 3em;
	}

	.corner a {
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

	a:hover {
		color: var(--color-theme-1);
	}
</style>
