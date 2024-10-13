<template>
  <div class="flex flex-col justify-center items-center h-screen">
    <form @submit.prevent class="flex flex-col gap-2 w-[30%] lg:w-[15%]">
      <UInput type="text" placeholder="username" class="rounded-xl bg-gray-100 text-black focus:outline-none" size="xl" variant="none" />
      <UInput type="password" placeholder="password" class="rounded-xl bg-gray-100 text-black placeholder:text-violet-500 focus:outline-none" size="xl" variant="none" />
      <UButton type="submit" class="rounded-xl p-2 flex justify-center" variant="soft" size="xl" >Login</UButton>
    </form>
    <div class="absolute bottom-16 inline-flex gap-8">
      <NuxtLink to="/register">
        <Icon name="solar:user-plus-broken" class="text-violet-500" size="30" />
      </NuxtLink>
      <NuxtLink to="/register">
        <Icon name="solar:key-minimalistic-square-2-linear" class="text-violet-500" size="30" />
      </NuxtLink>
      <NuxtLink to="/register">
        <Icon name="solar:home-2-linear" class="text-violet-500" size="30" />
      </NuxtLink>
      <ThemeSwitch />
    </div>
  </div>
</template>

<script lang="ts" setup>

</script>

<style>

</style>