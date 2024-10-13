<template>
	<div class="absolute top-0 left-0 w-full">
		<div
			data-tauri-drag-region
			class="inline-flex gap-3 px-3 items-center justify-end w-full p-2 bg-gradient-to-l from-violet-600 via-purple-500 to-fuchsia-600"
		>
			<button
				@click="appWindow.minimize()"
				class="rounded w-2 h-2 p-2 bg-yellow-500"
			></button>
			<button
				@click="appWindow.toggleMaximize()"
				class="rounded w-2 h-2 p-2 bg-green-500"
			></button>
			<button
				@click="appWindow.close()"
				class="rounded w-2 h-2 p-2 bg-red-500"
			></button>
		</div>
	</div>
</template>

<script lang="ts" setup>
	import { getCurrentWindow } from "@tauri-apps/api/window";

	const appWindow = getCurrentWindow();
</script>

<style></style>
