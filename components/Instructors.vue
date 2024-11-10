<template>
  <div class="mx-auto my-8 space-y-8">
    <h3 class="text-2xl font-semibold mb-6">Instructors</h3>

    <div
      v-for="instructor in instructors"
      :key="instructor.id"
      class="border-b border-gray-200 pb-6 mb-6"
    >
      <a
        :href="instructor.profileLink"
        class="text-lg font-semibold text-purple-600 underline"
      >
        {{ instructor.name }}
      </a>
      <p class="text-sm text-gray-500">{{ instructor.title }}</p>

      <div class="flex items-start space-x-4 mt-4">
        <img
          :src="instructor.image"
          alt="Instructor Avatar"
          class="w-16 h-16 rounded-full"
        />

        <div class="flex-1 space-y-1 text-sm text-gray-600">
          <div class="flex items-center space-x-2">
            <span class="text-gray-700"
              >⭐ {{ instructor.rating }} Instructor Rating</span
            >
          </div>
          <p>{{ instructor.reviews }} Reviews</p>
          <p>{{ instructor.students }} Students</p>
          <p>{{ instructor.courses }} Courses</p>
        </div>
      </div>

      <p class="text-gray-700 mt-4">{{ instructor.description }}</p>
      <p v-if="instructor.additionalDescription" class="text-gray-700 mt-2">
        {{ instructor.additionalDescription }}
      </p>

      <a
        href="#"
        class="text-purple-600 text-sm font-semibold mt-2 inline-block hover:underline"
      >
        Show more <span>&#9662;</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "InstructorsSection",
  data() {
    return {
      instructors: [
        {
          id: 1,
          name: "Neal Davis | AWS Certified Solutions Architect & Developer",
          profileLink: "#",
          title: "AWS Solutions Architect & AWS Certified Instructor",
          image: "https://img-b.udemycdn.com/user/200_H/23565832_b988_5.jpg",
          rating: "4.6",
          reviews: "161,680",
          students: "742,940",
          courses: "24",
          description:
            "Hi, my name's Neal. I am the founder of Digital Cloud Training, a highly experienced AWS Cloud Solutions Architect and a successful IT instructor. I've been working in IT for over 20 years in a variety of roles ranging from support to architecture. Over the last 15 years, I have mainly worked as a Solutions Architect in the systems integration space designing solutions for enterprise organizations.",
          additionalDescription:
            "My experience in IT has included working with virtualization and cloud computing since its inception. In my most recent consulting role I worked as an Enterprise Architect designing Hybrid IT and Digital Transformation solutions.",
        },
        {
          id: 2,
          name: "Digital Cloud Training | AWS Certified Cloud Practitioner AWS Certified Solutions Architect, AWS Developer Associate",
          profileLink: "#",
          title: "Highest Quality AWS Certification Exam Preparation Resources",
          image: "https://img-b.udemycdn.com/user/200_H/23565832_b988_5.jpg",
          rating: "4.6",
          reviews: "161,840",
          students: "742,879",
          courses: "25",
          description:
            "Digital Cloud Training provides AWS Certification exam preparation resources including instructor-led Video Courses, guided Hands-on Labs, in-depth Training Notes, Exam-Cram lessons for quick revision, Quizzes to test your knowledge and exam-difficulty Practice Exams to assess your exam readiness.",
          additionalDescription:
            "We strive to provide the highest quality AWS Training Resources that ensure our students are best prepared to pass their AWS exams first time, every time! With Digital Cloud Training, you get access to highly experienced staff who support you on your AWS Certification journey and help you elevate your career through achieving highly valuable certifications.",
        },
      ],
    };
  },
};
</script>
