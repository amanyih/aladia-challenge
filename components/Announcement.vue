<template>
  <div
    v-if="showAnnouncement"
    class="text-white text-center p-3 bg-purple-700 text-base"
  >
    <span class="font-bold"> Ready to get with the times? </span>| Get the
    skills with Udemy Business.
  </div>

  <Header />

  <button
    @click="closeAnnouncement"
    class="absolute top-2 right-4 p-2 text-white"
  >
    &times;
  </button>
</template>

<script>
export default {
  data() {
    return {
      showAnnouncement: true,
    };
  },
  methods: {
    closeAnnouncement() {
      this.showAnnouncement = false;
    },
  },
};
</script>
