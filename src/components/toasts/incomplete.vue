<template>
	<div
		class="inline-flex flex-shrink-0 justify-center items-center w-8 h-8 text-orange-500 bg-orange-100 rounded-lg dark:bg-orange-700 dark:text-orange-200"
	>
		<svg
			aria-hidden="true"
			class="w-5 h-5"
			fill="currentColor"
			viewBox="0 0 20 20"
			xmlns="http://www.w3.org/2000/svg"
		>
			<path
				fill-rule="evenodd"
				d="M8.257 3.099c.765-1.36 2.722-1.36 3.486 0l5.58 9.92c.75 1.334-.213 2.98-1.742 2.98H4.42c-1.53 0-2.493-1.646-1.743-2.98l5.58-9.92zM11 13a1 1 0 11-2 0 1 1 0 012 0zm-1-8a1 1 0 00-1 1v3a1 1 0 002 0V6a1 1 0 00-1-1z"
				clip-rule="evenodd"
			></path>
		</svg>
		<span class="sr-only">Warning icon</span>
	</div>
	<div class="ml-3 text-sm font-normal">Confirm Incompletion</div>
	<span
		class="ml-auto text-sm font-medium text-amber-600 p-1.5 hover:bg-amber-100 rounded-lg dark:text-amber-500 dark:hover:bg-gray-700"
		@click="$emit('incomplete')"
		>Incomplete</span
	>
</template>

<script lang="ts">
export default {};
</script>

<style lang="css" scoped></style>
