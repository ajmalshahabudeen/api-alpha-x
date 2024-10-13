<template>
	<div>
		<ClientOnly>
			<Icon
				:name="isDark ? 'solar:moon-broken' : 'solar:sun-broken'"
				aria-label="Theme"
				class="text-violet-500 cursor-pointer"
				size="30"
				@click="isDark = !isDark"
			/>
			<template #fallback>
				<div class="w-8 h-8" />
			</template>
		</ClientOnly>
	</div>
</template>

<script lang="ts" setup>
	const colorMode = useColorMode();
	const isDark = computed({
		get() {
			return colorMode.value === "dark";
		},
		set() {
			colorMode.preference =
				colorMode.value === "dark" ? "light" : "dark";
		},
	});
</script>

<style></style>
