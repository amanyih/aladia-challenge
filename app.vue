<template>
  <title>AWS Certified Solutions Architect Associate (SAA-C03) Course</title>

  <Announcement />

  <main class="min-h-screen">
    <NavBar />
    <Hero />
    <div class="flex justify-center p-8 bg-gray-50">
      <div class="flex flex-col lg:flex-row gap-8 max-w-7xl w-full">
        <div class="flex-1 space-y-6">
          <div class="border border-gray-300 p-4">
            <div class="flex justify-between items-center mb-4">
              <p class="text-gray-800 font-semibold">
                Prepare for your certification with this course.
                <a
                  href="#"
                  class="text-purple-600 underline hover:text-purple-800"
                  >Learn more</a
                >
              </p>
            </div>

            <div class="flex items-center space-x-4">
              <img
                src="https://d1.awsstatic.com/certification/badges/AWS-Certified-Solutions-Architect-Associate_badge_150x150.e359ae4a6d4d82c3e31d4f9104c8d389b56a2423.png"
                alt="AWS Certified Solutions Architect Badge"
                class="w-16 h-16"
              />

              <div>
                <p class="text-purple-700 font-semibold">
                  AWS Certified Solutions Architect – Associate
                </p>
                <p class="text-gray-500 text-xs">
                  Issued by Amazon Web Services Training and Certification
                </p>
              </div>
            </div>
          </div>

          <!-- What You'll Learn Section -->
          <div class="border border-gray-300 p-6 bg-white">
            <h2 class="text-2xl font-semibold mb-4">What you'll learn</h2>
            <div
              class="grid grid-cols-1 md:grid-cols-2 gap-4 text-sm text-gray-800"
            >
              <ul class="space-y-2">
                <li>
                  ✓ 24 HOURS OF INSTRUCTOR-GUIDED LECTURES: With our practical
                  exercises, you’ll learn how to architect and build
                  applications on Amazon Web Services
                </li>
                <li>
                  ✓ FULL-LENGTH PRACTICE TEST: Get familiar with the real AWS
                  exam format, style and difficulty with a complimentary
                  practice exam that is timed and scored
                </li>
                <li>
                  ✓ ALL CODE FILES AND SLIDES: Available for download (.zip file
                  / PDF format)
                </li>
                <li>
                  ✓ PRESENTED IN A PROFESSIONAL WAY: Focused and to the point,
                  clear language with professional subtitles
                </li>
                <li>
                  ✓ ACTIVE Q&A FORUM: Our discussion board provides a platform
                  for students to ask questions, share their recent exam
                  experiences, and offer feedback on exam topics
                </li>
              </ul>

              <ul class="space-y-2">
                <li>
                  ✓ EXAM CRAM LECTURES: These fast-paced lectures are perfect
                  for quick revision of the most important facts before sitting
                  your exam
                </li>
                <li>
                  ✓ QUIZ QUESTIONS: Review your knowledge with quiz questions
                  that test your understanding and measure your progress
                </li>
                <li>
                  ✓ ALWAYS UP TO DATE: Our teachings reflect the latest SAA-C03
                  exam. Students have lifetime access to all future updates
                </li>
                <li>
                  ✓ THE ULTIMATE EXAM PREP: We’ll teach you everything you need
                  to know to ace your exam AND master the cloud in the real
                  world
                </li>
                <li>
                  ✓ RESPONSIVE SUPPORT: Our team of AWS experts respond to all
                  of your questions, concerns, or feedback
                </li>
              </ul>
            </div>

            <div class="text-purple-600 font-semibold mt-4 cursor-pointer">
              Show less ▲
            </div>
          </div>

          <div class="text-2xl font-bold mb-12">
            <h3 class="mb-4">Explore related topics</h3>
            <div class="flex flex-wrap gap-3">
              <span
                class="border border-gray-400 text-gray-800 px-4 py-1 rounded-full text-base"
                >Amazon AWS</span
              >
              <span
                class="border border-gray-400 text-gray-800 px-4 py-1 rounded-full text-base"
                >AWS Certified Solutions Architect - Associate</span
              >
              <span
                class="border border-gray-400 text-gray-800 px-4 py-1 rounded-full text-base"
                >IT Certifications</span
              >
              <span
                class="border border-gray-400 text-gray-800 px-4 py-1 rounded-full text-base"
                >IT & Software</span
              >
            </div>
          </div>

          <div>
            <h3 class="text-2xl mb-4 font-bold">This course includes:</h3>
            <div
              class="grid grid-cols-1 sm:grid-cols-2 gap-y-2 gap-x-4 text-gray-800"
            >
              <div class="flex items-center space-x-2">
                <i class="fas fa-video text-xl"></i>
                <span class="text-sm">23 hours on-demand video</span>
              </div>
              <div class="flex items-center space-x-2">
                <i class="fas fa-question-circle text-xl"></i>
                <span class="text-sm">1 practice test</span>
              </div>
              <div class="flex items-center space-x-2">
                <i class="fas fa-file-alt text-xl"></i>
                <span class="text-sm">18 articles</span>
              </div>
              <div class="flex items-center space-x-2">
                <i class="fas fa-mobile-alt text-xl"></i>
                <span class="text-sm">Access on mobile and TV</span>
              </div>
              <div class="flex items-center space-x-2">
                <i class="fas fa-trophy text-xl"></i>
                <span class="text-sm">Certificate of completion</span>
              </div>
            </div>
          </div>

          <div class="border border-gray-300 p-6">
            <div class="mb-4">
              <h3 class="text-lg font-semibold text-gray-800">
                Top companies offer this course to their employees
              </h3>
              <p class="text-sm text-gray-600">
                This course was selected for our collection of top-rated courses
                trusted by businesses worldwide.
                <a href="#" class="text-purple-600 hover:underline"
                  >Learn more</a
                >
              </p>
            </div>

            <div class="flex justify-between items-center">
              <img
                v-for="logo in logos"
                :key="logo.alt"
                :src="logo.src"
                :alt="logo.alt"
                :height="logo.height"
                :width="logo.width"
                loading="lazy"
              />
            </div>
          </div>

          <CourseContent />
          <RequirementsDescription />
          <FeaturedReview />
          <StudentsAlsoBought />
          <FrequentlyBought />
          <Instructors />
          <Reviews />
          <MoreCourses />
        </div>

        <div class="min-w-96"></div>
      </div>
    </div>
  </main>

  <Footer />
</template>

<script>
export default {
  data() {
    return {
      logos: [
        {
          src: "https://s.udemycdn.com/partner-logos/v4/nasdaq-light.svg",
          alt: "Nasdaq",
          height: 44,
          width: 115,
        },
        {
          src: "https://s.udemycdn.com/partner-logos/v4/volkswagen-light.svg",
          alt: "Volkswagen",
          height: 44,
          width: 44,
        },
        {
          src: "https://s.udemycdn.com/partner-logos/v4/box-light.svg",
          alt: "Box",
          height: 44,
          width: 67,
        },
        {
          src: "https://s.udemycdn.com/partner-logos/v4/netapp-light.svg",
          alt: "NetApp",
          height: 44,
          width: 115,
        },
        {
          src: "https://s.udemycdn.com/partner-logos/v4/eventbrite-light.svg",
          alt: "Eventbrite",
          height: 44,
          width: 115,
        },
      ],
    };
  },
};
</script>
