<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<script setup>
useHead({
  titleTemplate: (titleChunk) => {
    return titleChunk ? `${titleChunk}` : 'Threezero Renting';
  }
})

onMounted(() => {
  // set session from localStorage
  useSetSession(JSON.parse(localStorage.getItem("session")));
  });

</script>

