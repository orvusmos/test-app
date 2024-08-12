<script>
	import '../app.css';
	import Button from '$lib/components/ui/button/button.svelte';
	import { HamburgerMenu } from 'svelte-radix';
</script>

<div class="flex min-h-screen h-fit w-screen flex-col items-center justify-start bg-secondary">
	<div class="flex h-fit w-screen max-w-[1200px] flex-col items-center justify-start bg-background">
		<nav class="flex w-full items-center justify-between p-4">
			<div class="flex items-center justify-center gap-4">
				<Button class="p-0" variant="link">
					<HamburgerMenu class="block h-4 w-4 md:hidden" />
				</Button>
				<Button href="/" variant="link" class="p-0 text-base font-bold">Heal & Grow</Button>
			</div>
			<div class="hidden items-center justify-center gap-8 md:flex">
				<Button href="/about" variant="link" class="p-0 text-base font-bold">About Us</Button>
				<Button href="/" variant="link" class="p-0 text-base font-bold">Location</Button>
				<Button href="/" variant="link" class="p-0 text-base font-bold">Services</Button>
			</div>
			<Button href="/contact">Contact Us</Button>
		</nav>
		<slot></slot>
	</div>
</div>
