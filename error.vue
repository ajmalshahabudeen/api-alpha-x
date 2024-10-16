<script setup lang="ts">
	import type { NuxtError } from "#app";

	const props = defineProps({
		error: Object as () => NuxtError,
	});
</script>

<template>
	<div class="flex flex-col gap-5 justify-center items-center min-h-screen">
		<h1 class="text-4xl font-extrabold text-red-400 uppercase">
			Application error: {{ (error as NuxtError).statusCode }}
		</h1>
		<NuxtLink to="/" class="bg-gradient-to-r from-violet-500 to-fuchsia-500 rounded-xl p-2 px-7 font-extralight"
			>Fix it</NuxtLink
		>
	</div>
</template>
