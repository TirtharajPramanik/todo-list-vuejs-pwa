<template>
	<label
		for="emerald-toggle"
		class="inline-flex relative items-center mr-5 cursor-pointer w-max"
	>
		<input
			type="checkbox"
			value=""
			id="emerald-toggle"
			class="sr-only peer"
			v-model="inputVal"
		/>
		<div
			class="w-11 h-6 bg-gray-200 rounded-full peer dark:bg-gray-500 peer-focus:ring-4 peer-focus:ring-emerald-300 dark:peer-focus:ring-emerald-800 peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-0.5 after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all dark:border-gray-600 peer-checked:bg-emerald-500"
		></div>
		<span class="ml-3 text-sm font-medium text-gray-900 dark:text-gray-300">{{
			inputVal ? 'Completed' : 'Incomplete'
		}}</span>
	</label>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
	props: { modelValue: { type: Boolean, required: false, default: false } },
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
