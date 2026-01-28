<template>
  <section>
    <code>
      <pre>{
  <span class="key">"name"</span>: "Alex Berneau",
  <span class="key">"age"</span>: "{{ getAge }}",
  <span class="key">"languages"</span>: ["French", "English"],
  <span class="key">"expertise"</span>: "Front-End Engineer",
  <span class="key">"skills"</span>: [
    "Vue", "Nuxt", "React", "Next", "NodeJS", "TypeScript",
    "Supabase", "Algolia", "ElasticSearch", "Vercel", "Auth0"
  ],
  <span class="key">"workExperiences"</span>: [
    {
      <span class="key">"company"</span>: "AKQA",
      <span class="key">"contract"</span>: "Full time",
      <span class="key">"location"</span>: "Paris, France",
      <span class="key">"period"</span>: "May 2019 - August 2024",
      <span class="key">"link"</span>: "<a href="https://akqa.com" target="_blank">https://akqa.com</a>"
    },
    {
      <span class="key">"company"</span>: "Mo Works",
      <span class="key">"contract"</span>: "Internship",
      <span class="key">"location"</span>: "Melbourne, Australia",
      <span class="key">"period"</span>: "July 2018 - November 2018",
      <span class="key">"link"</span>: "<a href="https://moworks.com.au" target="_blank">https://moworks.com.au</a>"
    },
    {
      <span class="key">"company"</span>: "Wait & See Agency",
      <span class="key">"contract"</span>: "Internship",
      <span class="key">"location"</span>: "Paris, France",
      <span class="key">"period"</span>: "July 2017 - September 2017"
    },
    {
      <span class="key">"company"</span>: "Ohwee",
      <span class="key">"contract"</span>: "Internship",
      <span class="key">"location"</span>: "Paris, France",
      <span class="key">"period"</span>: "July 2016 - September 2017"
    }
  ],
  <span class="key">"formations"</span>: {
    <span class="key">"school"</span>: "HETIC",
    <span class="key">"courses"</span>: [
      "web development",
      "project management",
      "business management",
      "digital creation",
      "entrepreneurship"
    ],
    <span class="key">"period"</span>: "September 2014 - December 2019",
    <span class="key">"link"</span>: "<a href="https://hetic.net" target="_blank">https://hetic.net</a>"
  }
}</pre>
    </code>
  </section>
</template>

<script setup lang="ts">
import { computed } from 'vue'

const getAge = computed((): number => {
  const birthDate = new Date(1994, 3, 24)
  const diff_ms = Date.now() - birthDate.getTime()
  const age_dt = new Date(diff_ms)

  return Math.abs(age_dt.getUTCFullYear() - 1970)
})
</script>

<style scoped>
code {
  width: 100%;
}

pre {
  background-color: #223545;
  color: var(--color-blue-light);
  padding: 1em;
  font-size: 0.7rem;
  letter-spacing: 0.2px;
  overflow-x: auto;

  a {
    color: inherit;
  }
}

.key {
  color: var(--color-yellow);
  font-weight: 600;
}
</style>
