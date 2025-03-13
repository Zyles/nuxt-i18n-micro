<template>
  <div><h1>{{ $t('contact.title') }}</h1></div>
</template>

<script setup>
import { useNuxtApp } from '#imports'

const { $defineI18nRoute } = useNuxtApp()

definePageMeta({ name: 'contact' })

$defineI18nRoute({
  localeRoutes: {
    en: '/contact',
    de: '/kontakt',
  },
})
</script>

<style></style>
