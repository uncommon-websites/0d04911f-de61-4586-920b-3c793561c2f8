<script lang="ts">
	// Types
	type Props = {
		value?: string;
		placeholder?: string;
		onsubmit?: (phone: string) => void;
		class?: string;
	};

	let { value = $bindable(''), placeholder = 'Enter your phone number', onsubmit, class: classes = '' }: Props = $props();

	// Components
	import Button from './Button.svelte';

	function handleSubmit(e: Event) {
		e.preventDefault();
		if (onsubmit && value) {
			onsubmit(value);
		}
	}

	function formatPhoneNumber(input: string): string {
		// Remove all non-numeric characters
		const cleaned = input.replace(/\D/g, '');
		
		// Format as (XXX) XXX-XXXX
		if (cleaned.length <= 3) {
			return cleaned;
		} else if (cleaned.length <= 6) {
			return `(${cleaned.slice(0, 3)}) ${cleaned.slice(3)}`;
		} else {
			return `(${cleaned.slice(0, 3)}) ${cleaned.slice(3, 6)}-${cleaned.slice(6, 10)}`;
		}
	}

	function handleInput(e: Event) {
		const target = e.target as HTMLInputElement;
		const formatted = formatPhoneNumber(target.value);
		value = formatted;
	}
</script>

<form onsubmit={handleSubmit} class={['flex gap-3 w-full max-w-md', classes]}>
	<input
		type="tel"
		bind:value
		oninput={handleInput}
		placeholder={placeholder}
		class="flex-1 rounded-lg border border-gray-300 px-4 py-2.5 text-base focus:outline-none focus:ring-2 focus:ring-primary-500 focus:border-transparent"
		maxlength="14"
		required
	/>
	<Button type="submit" variant="primary" size="lg">
		Sign up now
	</Button>
</form>
