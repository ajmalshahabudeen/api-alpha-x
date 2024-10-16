<template>
	<div class="flex flex-col justify-center items-center h-screen">
		<div class="flex gap-2 px-10 w-full justify-center items-center">
			<UPopover>
				<UButton
					color="violet"
					:label="httpMethod"
					class="rounded-2xl w-36 py-3 px-7 font-extralight inline-flex justify-between"
					trailing-icon="i-heroicons-chevron-down-20-solid"
				/>

				<template #panel>
					<section class="max-h-32 overflow-y-auto">
						<div
							@click="httpMethod = country"
							class="px-4 py-2 cursor-pointer"
							v-for="country in httpMethods"
						>
							<p>{{ country }}</p>
						</div>
					</section>
				</template>
			</UPopover>
			<UInput
				v-model="value"
				variant="none"
				class="w-full max-w-[50%] rounded-2xl bg-transparent border border-primary-500 placeholder:text-violet-500 focus:outline-none"
				size="xl"
				placeholder="URL to fetch"
			/>
			<UButton
				icon="solar:map-arrow-right-broken"
				trailing
				:loading="false"
				@click="handleSubmit"
				label="Submit"
				type="submit"
				class="uppercase rounded-2xl px-7 py-3 flex justify-center"
			/>
		</div>
	</div>
</template>

<script lang="ts" setup>
	const httpMethods = [
		"GET",
		"POST",
		"PUT",
		"DELETE",
		"PATCH",
		"OPTIONS",
		"HEAD",
	];

	const httpMethod = ref(httpMethods[0]);
	const value = ref("");

	const handleSubmit = () => {
		console.log(httpMethod.value, value.value);
	};
</script>

<style></style>
