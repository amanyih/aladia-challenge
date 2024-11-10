<template>
  <div class="mx-auto my-8 space-y-10">
    <div>
      <h3 class="text-xl font-semibold mb-4">
        More Courses by
        <a href="#" class="hover:underline text-purple-600"
          >Neal Davis | AWS Certified Solutions Architect & Developer</a
        >
      </h3>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
        <div
          v-for="course in nealCourses"
          :key="course.id"
          class="border border-gray-200 p-4 bg-white"
        >
          <img
            :src="course.image"
            alt="Course Image"
            class="w-full h-36 object-cover mb-4"
          />
          <h4 class="text-sm font-semibold text-gray-800 mb-1">
            {{ course.title }}
          </h4>
          <p class="text-xs text-gray-500 mb-2">{{ course.instructor }}</p>
          <div class="flex items-center space-x-1 text-xs text-gray-700">
            <span class="text-yellow-500">★ {{ course.rating }}</span>
            <span class="text-gray-500">({{ course.reviews }})</span>
          </div>
          <p class="text-xs text-gray-500">{{ course.details }}</p>
          <p class="text-gray-800 font-semibold mt-2">{{ course.price }}</p>
        </div>
      </div>
    </div>

    <div>
      <h3 class="text-xl font-semibold mb-4">
        More Courses by
        <a href="#" class="hover:underline text-purple-600"
          >Digital Cloud Training | AWS Certified Cloud Practitioner AWS
          Certified Solutions Architect, AWS Developer Associate</a
        >
      </h3>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
        <div
          v-for="course in digitalCloudCourses"
          :key="course.id"
          class="border border-gray-200 p-4 bg-white"
        >
          <img
            :src="course.image"
            alt="Course Image"
            class="w-full h-36 object-cover mb-4"
          />
          <h4 class="text-sm font-semibold text-gray-800 mb-1">
            {{ course.title }}
          </h4>
          <p class="text-xs text-gray-500 mb-2">{{ course.instructor }}</p>
          <div class="flex items-center space-x-1 text-xs text-gray-700">
            <span class="text-yellow-500">★ {{ course.rating }}</span>
            <span class="text-gray-500">({{ course.reviews }})</span>
          </div>
          <p class="text-xs text-gray-500">{{ course.details }}</p>
          <p class="text-gray-800 font-semibold mt-2">{{ course.price }}</p>
        </div>
      </div>
    </div>

    <div
      class="border border-gray-600 py-2 px-4 font-semibold text-gray-700 hover:bg-gray-100 text-center"
    >
      Report abuse
    </div>
  </div>
</template>

<script>
export default {
  name: "MoreCourses",
  data() {
    return {
      nealCourses: [
        {
          id: 1,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "Introduction to Cloud Computing on AWS for...",
          instructor: "Neal Davis | AWS Certified Solutions...",
          rating: "4.5",
          reviews: "30,818",
          details: "9.5 total hours • 97 lectures • Beginner",
          price: "$74.99",
        },
        {
          id: 2,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "AWS Certified Cloud Practitioner (CLF-C02) Exam Training",
          instructor: "Neal Davis | AWS Certified Solutions...",
          rating: "4.7",
          reviews: "36,191",
          details: "14 total hours • 203 lectures • Beginner",
          price: "$84.99",
        },
        {
          id: 3,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "AWS Certified Cloud Practitioner Practice Exam...",
          instructor: "Neal Davis | AWS Certified Solutions...",
          rating: "4.6",
          reviews: "24,974",
          details: "390 questions • All Levels",
          price: "$74.99",
        },
      ],
      digitalCloudCourses: [
        {
          id: 4,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "Introduction to Cloud Computing on AWS for...",
          instructor: "Digital Cloud Training | AWS Certified...",
          rating: "4.5",
          reviews: "30,818",
          details: "9.5 total hours • 97 lectures • Beginner",
          price: "$74.99",
        },
        {
          id: 5,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "AWS Certified Cloud Practitioner (CLF-C02) Exam Training",
          instructor: "Digital Cloud Training | AWS Certified...",
          rating: "4.7",
          reviews: "36,191",
          details: "14 total hours • 203 lectures • Beginner",
          price: "$84.99",
        },
        {
          id: 6,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "AWS Certified Cloud Practitioner Practice Exam...",
          instructor: "Digital Cloud Training | AWS Certified...",
          rating: "4.6",
          reviews: "24,974",
          details: "390 questions • All Levels",
          price: "$74.99",
        },
      ],
    };
  },
};
</script>
