<script setup lang="ts">
useMeta({
  title: "Primdev",
  link: [
    {
      rel: "icon",
      href: "../assets/images/favicon.png",
    },
  ],
});
</script>

<template>
  <div>
    <HeaderApp />
    <slot />
  </div>
</template>
