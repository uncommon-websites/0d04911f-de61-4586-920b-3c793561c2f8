<script lang="ts">
	// Icons
	import IconArrowRight from "~icons/lucide/arrow-right";
	
	// Props
	type Props = {
		class?: string;
	};
	
	let { class: classes = "" }: Props = $props();
	
	// State
	let phoneNumber = $state("");
	let isSubmitting = $state(false);
	let isSuccess = $state(false);
	
	// Format phone number as user types
	function formatPhoneNumber(value: string) {
		const cleaned = value.replace(/\D/g, "");
		const match = cleaned.match(/^(\d{0,3})(\d{0,3})(\d{0,4})$/);
		
		if (match) {
			const parts = [match[1], match[2], match[3]].filter(Boolean);
			return parts.join("-");
		}
		
		return value;
	}
	
	function handleInput(e: Event) {
		const target = e.target as HTMLInputElement;
		phoneNumber = formatPhoneNumber(target.value);
	}
	
	async function handleSubmit(e: Event) {
		e.preventDefault();
		
		if (phoneNumber.replace(/\D/g, "").length !== 10) {
			return;
		}
		
		isSubmitting = true;
		
		// Simulate API call
		await new Promise(resolve => setTimeout(resolve, 1000));
		
		isSubmitting = false;
		isSuccess = true;
		
		// Reset after 3 seconds
		setTimeout(() => {
			isSuccess = false;
			phoneNumber = "";
		}, 3000);
	}
	
	let isValid = $derived(phoneNumber.replace(/\D/g, "").length === 10);
</script>

<form onsubmit={handleSubmit} class={["flex flex-col gap-3 sm:flex-row", classes]}>
	<div class="relative flex-1">
		<input
			type="tel"
			value={phoneNumber}
			oninput={handleInput}
			placeholder="Enter your phone number"
			maxlength="12"
			disabled={isSubmitting || isSuccess}
			class={[
				"w-full rounded-lg border border-gray-300 px-4 py-3 text-base transition-all duration-200",
				"focus:border-primary focus:outline-none focus:ring-2 focus:ring-primary/20",
				"disabled:bg-gray-100 disabled:cursor-not-allowed",
				isSuccess && "border-green-500 bg-green-50"
			]}
		/>
	</div>
	
	<button
		type="submit"
		disabled={!isValid || isSubmitting || isSuccess}
		class={[
			"inline-flex items-center justify-center gap-2 rounded-lg px-6 py-3 font-semibold transition-all duration-200",
			"bg-primary text-white hover:brightness-110 active:scale-[0.98]",
			"disabled:cursor-not-allowed disabled:opacity-50 disabled:hover:brightness-100",
			"focus:outline-none focus:ring-2 focus:ring-primary/20",
			"whitespace-nowrap"
		]}
	>
		{#if isSubmitting}
			<span class="inline-block size-4 animate-spin rounded-full border-2 border-white border-t-transparent"></span>
			<span>Signing up...</span>
		{:else if isSuccess}
			<span>✓ Success!</span>
		{:else}
			<span>Sign up now</span>
			<IconArrowRight class="size-4" />
		{/if}
	</button>
</form>

{#if isSuccess}
	<p class="mt-2 text-sm text-green-600">
		Thanks! We'll text you shortly to get started.
	</p>
{/if}
