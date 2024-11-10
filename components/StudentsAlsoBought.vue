<template>
  <div class="mx-auto my-8 space-y-4">
    <h3 class="text-xl font-semibold mb-4">Students also bought</h3>

    <div
      v-for="course in courses"
      :key="course.id"
      class="flex items-center space-x-4 border-b border-gray-200 py-4"
    >
      <img :src="course.image" alt="Course Image" class="w-16 h-16" />

      <div class="flex-1">
        <h4 class="text-gray-800 font-semibold text-sm mb-1">
          {{ course.title }}
        </h4>
        <div class="flex items-center space-x-2 text-xs text-gray-500">
          <span
            v-if="course.bestseller"
            class="text-black bg-yellow-400 px-2 py-0.5 text-xs"
            >Bestseller</span
          >
          <span class="text-gray-800 font-semibold">{{ course.hours }}</span>
          <span>• Updated {{ course.updated }}</span>
        </div>
      </div>

      <div class="flex items-center space-x-2 text-sm text-gray-700">
        <span class="text-yellow-500">★ {{ course.rating }}</span>
        <span class="text-xs text-gray-500">({{ course.students }})</span>
      </div>

      <div class="flex items-center space-x-4">
        <span class="text-gray-800 font-semibold">{{ course.price }}</span>
        <button class="text-gray-500 hover:text-gray-700">
          <i class="fas fa-heart"></i>
        </button>
      </div>
    </div>

    <button
      class="w-full text-center py-2 border border-gray-300 text-sm font-semibold text-gray-700 hover:bg-gray-100"
    >
      Show more
    </button>
  </div>
</template>

<script>
export default {
  name: "StudentsAlsoBought",
  data() {
    return {
      courses: [
        {
          id: 1,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "Ultimate AWS Certified Solutions Architect Associate SAA-C03",
          bestseller: true,
          hours: "27.5 total hours",
          updated: "11/2024",
          rating: "4.7",
          students: "1,041,203",
          price: "$84.99",
        },
        {
          id: 2,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "Ultimate AWS Certified Solutions Architect Professional 2024",
          bestseller: true,
          hours: "17 total hours",
          updated: "11/2024",
          rating: "4.7",
          students: "183,185",
          price: "$84.99",
        },
        {
          id: 3,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "AWS Certified Solutions Architect Associate - SAA C03",
          hours: "29 total hours",
          updated: "11/2024",
          rating: "4.7",
          students: "59,347",
          price: "$84.99",
        },
        {
          id: 4,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "AWS Certified Solutions Architect - Professional 2024",
          hours: "41.5 total hours",
          updated: "3/2024",
          rating: "4.6",
          students: "18,944",
          price: "$22.99",
        },
        {
          id: 5,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "AWS Certified Solutions Architect - Associate exam-SAA-C03",
          hours: "26.5 total hours",
          updated: "10/2024",
          rating: "4.6",
          students: "25,551",
          price: "$79.99",
        },
        {
          id: 6,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "AWS Certified Solutions Architect Professional SAP-C02",
          hours: "21 total hours",
          updated: "11/2024",
          rating: "4.7",
          students: "64,404",
          price: "$84.99",
        },
      ],
    };
  },
};
</script>
