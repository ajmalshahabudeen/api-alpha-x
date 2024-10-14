<template>
  <div class="flex flex-col justify-center items-center h-screen">
    <form @submit.prevent="handleSubmit" class="flex flex-col gap-2 w-[30%] lg:w-[15%]">
      <UInput required icon="solar:shield-user-broken" type="text" placeholder="username" class="rounded-xl bg-transparent text-violet-500 border border-primary-500 focus:outline-none" size="xl" variant="none" />
      <UInput required icon="solar:lock-password-broken" type="password" placeholder="password" class="rounded-xl bg-transparent text-violet-500 border border-primary-500 placeholder:text-violet-500 focus:outline-none" size="xl" variant="none" />
      <UButton :loading="loading" icon="solar:map-arrow-right-broken" :trailing="true" type="submit" class="uppercase rounded-xl p-2 flex justify-center" variant="soft" size="xl" >Login</UButton>
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

const loading = ref(false)

const handleSubmit = (e:any) => {
  console.log(e.target[0].value, e.target[1].value)

  loading.value = true

  setTimeout(() => {
    loading.value = false
  }, 3000)

}

</script>

<style>

</style>