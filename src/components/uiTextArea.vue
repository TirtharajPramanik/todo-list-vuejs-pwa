<template>
	<div class="relative">
		<textarea
			type="text"
			:id="name"
			class="block px-2.5 pb-2.5 pt-4 w-full text-sm text-gray-900 bg-transparent rounded-lg border-1 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-emerald-500 focus:outline-none focus:ring-0 focus:border-emerald-600 peer transition duration-500"
			placeholder=" "
			v-model="inputVal"
		/>
		<label
			:for="name"
			class="absolute text-sm text-gray-500 dark:text-gray-200 duration-300 transform -translate-y-4 scale-75 top-2 z-10 origin-[0] bg-white rounded-md dark:bg-slate-700 px-2 peer-focus:px-2 peer-focus:text-emerald-600 dark:peer-focus:text-emerald-200 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-95 peer-focus:-translate-y-4 left-1"
		>
			<slot />
		</label>
	</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
	props: {
		name: { type: String, required: true },
		autofocus: { type: Boolean, required: false, default: false },
		modelValue: { type: String, required: false, default: '' },
	},
	computed: {
		inputVal: {
			get() {
				return this.modelValue;
			},
			set(val: string) {
				return this.$emit('update:modelValue', val);
			},
		},
	},
});
</script>
