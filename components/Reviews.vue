<template>
  <div class="mx-auto my-8">
    <h3 class="text-xl font-semibold mb-4 flex items-center">
      <span class="text-yellow-500">★</span> {{ averageRating }} course rating •
      {{ totalRatings }} ratings
    </h3>

    <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
      <div
        v-for="review in reviews"
        :key="review.id"
        class="border-t-2 border-gray-400 p-4 space-y-2"
      >
        <div class="flex items-center justify-between">
          <div class="flex items-center space-x-2">
            <div
              class="w-8 h-8 bg-black rounded-full flex items-center justify-center text-white font-semibold"
            >
              {{ review.initials }}
            </div>
            <div>
              <p class="font-semibold text-sm">{{ review.name }}</p>
              <div class="flex items-center space-x-1 text-xs text-gray-500">
                <span class="text-yellow-500">★★★★★</span>
                <span>{{ review.timeAgo }}</span>
              </div>
            </div>
          </div>

          <button class="text-gray-500 hover:text-gray-700">
            <i class="fas fa-ellipsis-v"></i>
          </button>
        </div>

        <p class="text-gray-700 text-sm">{{ review.content }}</p>

        <a
          href="#"
          class="text-purple-600 text-sm font-semibold hover:underline"
          >Show more</a
        >

        <div class="flex items-center space-x-2 text-xs text-gray-500 mt-2">
          <span>Helpful?</span>
          <button class="flex items-center hover:text-gray-700">
            <i class="fas fa-thumbs-up"></i>
          </button>
          <button class="flex items-center hover:text-gray-700">
            <i class="fas fa-thumbs-down"></i>
          </button>
          <button class="ml-auto hover:text-gray-700">Report</button>
        </div>
      </div>
    </div>

    <div class="mt-6 text-center align-start">
      <button
        class="border border-gray-300 py-2 px-4 font-semibold text-gray-700 hover:bg-gray-100"
      >
        Show all reviews
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ReviewsSection",
  data() {
    return {
      averageRating: "4.6",
      totalRatings: "20K",
      reviews: [
        {
          id: 1,
          initials: "DV",
          name: "Darwin V.",
          timeAgo: "a month ago",
          content:
            "It's a good course because it provides a route through a ton of documentation that is available in AWS.",
        },
        {
          id: 2,
          initials: "FB",
          name: "Francis Jeff B.",
          timeAgo: "a month ago",
          content:
            "This course really helped me to pass my exam! The SAA-C03 tests how the exam taker would assess and think on scenario based questions and I highly appreciate the effort Neal has put in to build this module especially the hands-on...",
        },
        {
          id: 3,
          initials: "AB",
          name: "Arijit B.",
          timeAgo: "a month ago",
          content:
            "I took this training from Neal, and I really liked the way the topics were structured and presented. I also liked Neal's calm and composed way of presenting. I completed my AWS Certified Solutions Architect Associate...",
        },
        {
          id: 4,
          initials: "FJ",
          name: "Franklin J.",
          timeAgo: "4 months ago",
          content:
            "I passed my AWS SAA-C03 certification exam yesterday and this course really helped me to pass the exam. The way each concept was explained with diagrams was very helpful. Thank you Neal for this great course! Kudos !",
        },
      ],
    };
  },
};
</script>
