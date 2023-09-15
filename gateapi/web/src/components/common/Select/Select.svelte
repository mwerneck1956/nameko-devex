<script lang="ts">
	import type { LabeledInputProps } from './index'

	export let {
		label,
		icon,
		options = [],
		placeholder = '',
		value = '',
		type = 'text',
		readonly = false,
	}: Partial<LabeledInputProps> = {}
</script>

<select
	style="appearance: none; background-image: url('/images/chevron-down-icon.svg'); background-position: right center; background-repeat: no-repeat; padding-right: 2rem;"
	class="cursor-pointer w-full !outline-none text-base font-amplitudeWideBook"
>
	<option value="" disabled selected>Select</option>
	{#each options as option}
		<option class="text-darkViolet" value={option.value}>{option.label}</option>
	{/each}
</select>
