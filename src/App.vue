<template>
  <MyHeader />
  <MyIntro />
  <MyCode />
  <MyFooter />
</template>

<script setup lang="ts">
import MyHeader from '@/components/MyHeader.vue'
import MyIntro from '@/components/MyIntro.vue'
import MyCode from '@/components/MyCode.vue'
import MyFooter from '@/components/MyFooter.vue'
</script>

<style>
:root {
  --color-yellow: #fee715;
  --color-blue-light: #e9f4ff;
  --color-blue-dark: #1c275d;
  --color-night: #101820;

  --color-text: var(--color-blue-dark);
  --color-background: var(--color-blue-light);

  @media (prefers-color-scheme: dark) {
    --color-text: var(--color-yellow);
    --color-background: var(--color-night);
  }
}

html {
  font-size: 20px;
  scroll-behavior: smooth;
}

body {
  background-color: var(--color-background);
  background-image: linear-gradient(300deg,
      hsl(210deg 100% 96%) 0%,
      hsl(205deg 100% 95%) 29%,
      hsl(201deg 100% 95%) 42%,
      hsl(197deg 100% 94%) 51%,
      hsl(193deg 100% 94%) 58%,
      hsl(191deg 100% 94%) 63%,
      hsl(188deg 100% 93%) 68%,
      hsl(186deg 100% 93%) 72%,
      hsl(182deg 92% 92%) 75%,
      hsl(178deg 90% 92%) 79%,
      hsl(173deg 94% 92%) 83%,
      hsl(168deg 97% 92%) 87%,
      hsl(162deg 100% 93%) 100%);
  color: var(--color-text);
  font-family:
    ui-monospace, 'Cascadia Code', 'Source Code Pro', Menlo, Consolas, 'DejaVu Sans Mono', monospace;
  line-height: 1.3;

  @media (prefers-color-scheme: dark) {
    background-image: none;
  }
}

#app {
  padding: 6vw;
}

section {
  max-width: 680px;
  margin-top: 3rem;
}

a,
a:active,
a:visited {
  color: inherit;
}
</style>
