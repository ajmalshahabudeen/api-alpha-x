<template>
	<div class="flex flex-col gap-5 justify-center items-center min-h-screen">
		<p class="text-4xl text-fuchsia-400 transition-colors duration-500 ease-in-out tracking-widest font-poppins font-extralight hover:text-violet-500 uppercase">
      Login to Continue
    </p>
    <div class="flex gap-5">
			<NuxtLink
				to="/login"
				class="bg-gradient-to-r uppercase from-violet-500 to-fuchsia-500 hover:rounded-xl rounded-none transition-all duration-500 ease-in-out p-2 px-7 font-extralight"
				>login</NuxtLink
			>
			<NuxtLink
				to="/register"
				class="bg-gradient-to-r uppercase from-fuchsia-500 to-violet-500 hover:rounded-xl rounded-none transition-all duration-500 ease-in-out p-2 px-7 font-extralight"
				>register</NuxtLink
			>
		</div>
	</div>
</template>

<script lang="ts" setup></script>

<style></style>
