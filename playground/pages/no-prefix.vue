<template>
  <div class="container">
    <h1>No Prefix Strategy Test</h1>
    <p>Current locale: <span id="content">{{ $getLocale() }}</span></p>
    <p>Select locale: <i18n-switcher /></p>
    <p>Contact page link: <a :href="contactRoute">Contact</a></p>
    <p>Contact route debug: {{ contactRoute }}</p>
    <p>Contact route obj:</p> <pre>{{ contactRouteObj }}</pre>
  </div>
</template>

<script setup>
import { useNuxtApp } from '#imports'

const { $getLocale, $localeRoute } = useNuxtApp()

const locale = computed(() => $getLocale())
const contactRoute = computed(() => $localeRoute({ name: 'contact' }).path)
const contactRouteObj = computed(() => $localeRoute({ name: 'contact' }, locale.value))
</script>
