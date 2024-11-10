<template>
  <div class="mx-auto my-8 border border-gray-200 p-6 bg-white">
    <h3 class="text-xl font-semibold mb-4">Frequently Bought Together</h3>

    <div
      v-for="(course, index) in courses"
      :key="course.id"
      class="flex items-center space-x-4 py-4 border-b last:border-b-0"
    >
      <img :src="course.image" alt="Course Image" class="w-20 h-20" />

      <div class="flex-1">
        <h4 class="text-gray-800 font-semibold text-sm mb-1">
          {{ course.title }}
        </h4>
        <p class="text-xs text-gray-500 mb-1">{{ course.instructor }}</p>
        <div class="flex items-center space-x-1 text-xs text-gray-700">
          <span class="text-yellow-500">★ {{ course.rating }}</span>
          <span class="text-gray-500">({{ course.reviews }})</span>
        </div>
      </div>

      <span class="text-gray-800 font-semibold">{{ course.price }}</span>
    </div>

    <div class="flex items-center justify-between pt-4">
      <span class="text-lg font-semibold"
        >Total: <span class="text-gray-800">{{ totalPrice }}</span></span
      >
      <button
        class="bg-purple-600 text-white font-semibold py-2 px-4 hover:bg-purple-700"
      >
        Add all to cart
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "FrequentlyBoughtTogether",
  data() {
    return {
      courses: [
        {
          id: 1,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "AWS Certified Solutions Architect Associate (SAA-C03) Course",
          instructor:
            "Neal Davis | AWS Certified Solutions Architect & Developer,...",
          rating: "4.6",
          reviews: "19,965",
          price: "$84.99",
        },
        {
          id: 2,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "AWS Certified Cloud Practitioner (CLF-C02) Exam Training",
          instructor:
            "Neal Davis | AWS Certified Solutions Architect & Developer,...",
          rating: "4.7",
          reviews: "36,181",
          price: "$84.99",
        },
        {
          id: 3,
          image: "https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg",
          title: "AWS Certified Developer Associate Exam Training DVA-C02",
          instructor:
            "Neal Davis | AWS Certified Solutions Architect & Developer,...",
          rating: "4.7",
          reviews: "4,042",
          price: "$84.99",
        },
      ],
      totalPrice: "$254.97",
    };
  },
};
</script>
