<template>
  <div>
    <h4 class="font-semibold text-white mb-2">{{ section.title }}</h4>
    <ul>
      <li v-for="link in section.links" :key="link.text">
        <a :href="link.href" class="text-gray-400 hover:underline">{{
          link.text
        }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "FooterSection",
  props: {
    section: Object,
  },
};
</script>
