<template>
  <h1>{{ $t('navigation.title') }}</h1>
  <ul class="space-y-0 rounded-xl p-4">
    <li v-for="(link, index) in navLinks" :key="index">
      <NuxtLink :to="link.to">
        <span>
          {{ link.label }}
        </span>
      </NuxtLink>
    </li>
  </ul>
</template>

<script setup lang="ts">
const { localeRoute, $t } = useI18n()

const navLinks = [
  {
    to: localeRoute({ name: 'index' }),
    label: $t('navigation.home'),
  },
  {
    to: localeRoute({ name: 'contact' }),
    label: $t('navigation.contact'),
  },
];
</script>

<style scoped>
</style>
