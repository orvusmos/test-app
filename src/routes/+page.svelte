<script>
	import Button from '$lib/components/ui/button/button.svelte';
	import * as Card from '$lib/components/ui/card';

	
</script>

<main class="w-full space-y-4">
	<section
		class="relative flex h-[70vh] items-center justify-start gap-12 bg-[url(https://images.unsplash.com/photo-1476950648868-16c7dca9499c?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)] bg-cover p-8"
	>
		<Card.Root class="flex flex-col items-start justify-start gap-4 p-4">
			<h1 class="max-w-xs text-3xl font-bold">
				Give your child the help they deserves, with Heal & Grow.
			</h1>
			<div class="flex items-center justify-start gap-4">
				<Button href="/" variant="outline">Our Services</Button>
				<Button href="/">Request Appointment</Button>
			</div>
		</Card.Root>
	</section>
	<section class="relative grid h-fit grid-rows-3 md:grid-cols-3 md:grid-rows-1 gap-12 p-8">
		<Card.Root class="flex h-full flex-col items-start justify-between gap-4 p-4">
			<h1 class="max-w-xs text-xl font-semibold">Hours</h1>
			<div class="flex w-full flex-col items-start justify-start gap-4">
				<div class="flex w-full items-center justify-between gap-4">
					<h1 class=" text-base font-semibold">Monday - Friday</h1>
					<h1 class=" font-regular text-base">8:30am - 7:00pm</h1>
				</div>
				<div class="flex w-full items-center justify-between gap-4">
					<h1 class=" text-base font-semibold">Saturday</h1>
					<h1 class=" font-regular text-base">9:00am - 2:00pm</h1>
				</div>
				<div class="flex w-full items-center justify-between gap-4">
					<h1 class=" text-base font-semibold">Sunday</h1>
					<h1 class=" font-regular text-base">Closed</h1>
				</div>
			</div>
			<Button href="/" variant="link" class="p-0 text-base font-bold">Download contact card</Button>
		</Card.Root>
		<Card.Root class="flex h-full flex-col items-start justify-between gap-4 p-4">
			<div class="flex w-full flex-col items-start justify-start gap-4">
				<h1 class="max-w-xs text-xl font-semibold">Appointments</h1>
				<p class="text-sm">
					For inquires about already booked appointments call +234 809 354 0899. To request a new
					appointment, please follow the link below.
				</p>
			</div>

			<Button href="/" variant="link" class="p-0 text-base font-bold">Request Appointment</Button>
		</Card.Root>
		<Card.Root class="flex h-full flex-col items-start justify-between gap-4 p-4">
			<div class="flex w-full flex-col items-start justify-start gap-4">
				<h1 class="max-w-xs text-xl font-semibold">Location</h1>
				<p class="text-sm">25 Raymond Njoku Street, Off Awolowo Road, Ikoyi, Lagos</p>
			</div>

			<Button href="/" variant="link" class="p-0 text-base font-bold">Check Location</Button>
		</Card.Root>
	</section>
	<section class="relative flex h-[90vh] flex-col items-start justify-start gap-12 p-8">
		<h1 class="max-w-xs text-3xl font-bold">Our Services</h1>
		<div class="grid grid-cols-4 grid-rows-2 gap-4 w-full h-full">
			<Card.Root class="col-span-1 row-span-1">
				<h1>test</h1>
			</Card.Root>
			<Card.Root class="col-span-1 row-span-1">
				<h1>test</h1>
			</Card.Root>
			<Card.Root class="col-span-2 row-span-1">
				<h1>test</h1>
			</Card.Root>
			<Card.Root class="col-span-1 row-span-1">
				<h1>test</h1>
			</Card.Root>
			<Card.Root class="col-span-1 row-span-1">
				<h1>test</h1>
			</Card.Root>
			<Card.Root class="col-span-2 row-span-1">
				<h1>test</h1>
			</Card.Root>
		</div>
	</section>
		<section
		class="relative flex h-fit items-center justify-center gap-12 bg-muted-foreground p-8"
	>
		<Card.Root class="flex flex-col items-center justify-center gap-4 p-4">
			<h1 class="max-w-xs text-xl font-bold">
				Best healing is just one call away.
			</h1>
			<div class="flex items-center justify-start gap-4">
				<Button href="/">Request Appointment</Button>
			</div>
		</Card.Root>
	</section>
	<section>footer</section>
</main>
