<script context="module" lang="ts">
	import { ROUTES } from './routes'
	import Input from '../components/common/Input/Input.svelte'
	import IconButton from '../components/common/IconButton/IconButton.svelte'
	import Button from '../components/common/Button/Button.svelte'
	import HomeIcon from '../icons/HomeIcon.svelte'
	import PropertyIcon from '../icons/Property.svelte'
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<main>
	<!-- {#each Object.entries(ROUTES) as [name, route]}
		<a class="mx-2 text-blue-400 underline" href={route}>{name}</a>
	{/each} -->

	<div class="grid lg:grid-cols-2 gap-20 grid-cols-1">
		<div>
			<h1
				class="text-4xl font-amplitudeWide font-normal text-dark-gray text-shadow-md"
			>
				Property Details
			</h1>
			<p
				class="text-dark-gray text-lg font-normal leading-6 font-amplitudeWide max-w-md mt-2"
			>
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
				tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
				veniam.
			</p>

			<form class="mt-[45px]">
				<Input label="Property Name" />
				<Input
					placeholder="21 Jump Street, Los Angeles, California"
					label="Address"
				/>
			</form>
		</div>

		<div>
			<img
				src="/images/house.svg"
				class="min-w-[340px] min-h-[220px]"
				alt="house"
			/>
		</div>
	</div>

	<div class="mt-6">
		<h3 class="font-amplitudeWide mb-6 font-semibold text-dark-gray">
			Property Type
		</h3>
		<div class="grid grid-cols-4 gap-5">
			<IconButton icon={HomeIcon} label="Single-Family" />
			<IconButton icon={PropertyIcon} label="Multi-Family" />
			<IconButton icon={HomeIcon} label="Townhome" />
			<IconButton icon={PropertyIcon} label="Condo" />
		</div>
	</div>

	<div class="my-6">
		<h3 class="font-amplitudeWide mb-6 font-semibold text-dark-gray">
			Unit info
		</h3>
	</div>

	<footer class="flex justify-between mt-[54px]">
		<Button variant="primary">back</Button>
		<Button variant="secondary">continue</Button>
	</footer>
</main>
