<template>
  <FontAwesomeIcon :icon="iconName" />
</template>

<script setup lang="ts">
import { defineProps, computed } from 'vue';
import { library } from '@fortawesome/fontawesome-svg-core';
import { faTwitter, faYoutube, faTiktok, faInstagram, faDiscord } from '@fortawesome/free-brands-svg-icons';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

library.add(faTwitter, faYoutube, faTiktok, faInstagram, faDiscord);

const props = defineProps({
  icon: String
});

const iconName = computed(() => {
  return props.icon;
});
</script>
