<template>
  <div class="mx-auto border border-gray-500 p-4">
    <h3 class="text-lg font-semibold mb-4">Featured review</h3>

    <div class="flex items-start space-x-4">
      <div class="flex-1">
        <div class="flex items-start space-x-4">
          <img
            src="https://img-c.udemycdn.com/user/200_H/63776246_ac8b_3.jpg"
            alt="User Avatar"
            class="w-12 h-12 rounded-full"
          />
          <div>
            <div class="mb-2">
              <span class="font-semibold">Shreyas</span>
              <p class="text-sm text-gray-500">423 courses</p>
              <p class="text-sm text-gray-500">20 reviews</p>
            </div>
          </div>
        </div>
        <div class="flex items-center space-x-2 text-sm text-gray-500 mb-2">
          <span class="text-yellow-500">★★★★★</span>
          <span>5 years ago</span>
        </div>

        <p class="text-gray-700 mb-4">
          Neal Davis' AWS Solutions Architect Associate course is in depth and
          advanced concepts hands-on concepts are also shown which is not found
          in any other Udemy courses. After a long time, the best AWS Solutions
          Architect course has arrived on Udemy. Congrats to all. Happy learning
          and earning.
        </p>

        <div class="flex items-center space-x-4 text-gray-500 text-sm">
          <span>Was this review helpful?</span>
          <div class="flex space-x-2">
            <button class="flex items-center hover:text-gray-700">
              <i class="fas fa-thumbs-up"></i>
            </button>
            <button class="flex items-center hover:text-gray-700">
              <i class="fas fa-thumbs-down"></i>
            </button>
          </div>
        </div>
        <a href="#" class="hover:underline">Report</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FeaturedReview",
};
</script>
