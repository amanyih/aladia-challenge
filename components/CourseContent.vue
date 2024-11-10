<template>
  <div class="mx-auto my-8">
    <h2 class="text-2xl font-semibold mb-2">Course content</h2>
    <p class="text-gray-600 mb-4">
      19 sections • 291 lectures • 22h 56m total length
    </p>
    <a
      href="#"
      class="text-purple-600 font-semibold hover:underline mb-4 inline-block"
      >Expand all sections</a
    >

    <Accordion
      class="border border-gray-200 divide-y divide-gray-200"
      type="single"
    >
      <AccordionItem
        v-for="section in sections"
        :key="section.id"
        :value="section.id"
      >
        <AccordionTrigger
          class="flex justify-between items-center py-4 px-6 cursor-pointer"
        >
          <span class="font-semibold text-gray-800">{{ section.title }}</span>
          <span class="text-gray-500">{{ section.details }}</span>
        </AccordionTrigger>
        <AccordionContent>
          <div class="py-4 px-6 text-gray-700 space-y-3">
            <div
              v-for="lecture in section.lectures"
              :key="lecture.id"
              class="flex justify-between items-center"
            >
              <div class="flex items-center space-x-2">
                <i :class="lecture.icon" class="text-gray-500"></i>
                <a href="#" class="text-sm text-purple-600 hover:underline">
                  {{ lecture.title }}
                </a>
                <span
                  v-if="lecture.preview"
                  class="text-xs text-purple-600 hover:underline cursor-pointer"
                  >Preview</span
                >
              </div>
              <span class="text-xs text-gray-500">{{ lecture.duration }}</span>
            </div>
          </div>
        </AccordionContent>
      </AccordionItem>
    </Accordion>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sections: [
        {
          id: 1,
          title: "Let's Get Started!",
          details: "9 lectures • 33min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
            {
              id: 2,
              title: "The SAA-C03 Exam",
              duration: "05:07",
              preview: true,
              icon: "fas fa-play-circle",
            },
            {
              id: 3,
              title: "Hands-On Practice: Free Tier vs Sandbox",
              duration: "03:20",
              icon: "fas fa-play-circle",
            },
            {
              id: 4,
              title: "AWS Account Overview",
              duration: "03:59",
              preview: true,
              icon: "fas fa-play-circle",
            },
            {
              id: 5,
              title: "[HOL] Create Your AWS Free Tier Account",
              duration: "04:33",
              preview: true,
              icon: "fas fa-play-circle",
            },
            {
              id: 6,
              title: "[HOL] Configure Account and Create a Budget and Alarm",
              duration: "05:23",
              icon: "fas fa-play-circle",
            },
            {
              id: 7,
              title: "[HOL] Setup Multi-Factor Authentication (MFA)",
              duration: "02:09",
              icon: "fas fa-play-circle",
            },
            {
              id: 8,
              title: "[HOL] Install Tools and Configure AWS CLI",
              duration: "04:29",
              icon: "fas fa-play-circle",
            },
            {
              id: 9,
              title: "Course Download",
              duration: "00:11",
              icon: "fas fa-file-alt",
            },
          ],
        },
        {
          id: 2,
          title: "AWS Identity and Access Management (IAM)",
          details: "14 lectures • 1hr",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
            {
              id: 2,
              title: "The SAA-C03 Exam",
              duration: "05:07",
              preview: true,
              icon: "fas fa-play-circle",
            },
            {
              id: 3,
              title: "Hands-On Practice: Free Tier vs Sandbox",
              duration: "03:20",
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 3,
          title: "Amazon Elastic Compute Cloud (EC2)",
          details: "26 lectures • 2hr 19min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 4,
          title: "Elastic Load Balancing and Auto Scaling",
          details: "18 lectures • 1hr 45min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 5,
          title: "AWS Organizations and Control Tower",
          details: "9 lectures • 34min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 6,
          title: "Amazon Virtual Private Cloud (VPC)",
          details: "23 lectures • 2hr 14min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 7,
          title: "Amazon Simple Storage Service (S3)",
          details: "23 lectures • 1hr 46min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 8,
          title: "DNS, Caching, and Performance Optimization",
          details: "17 lectures • 1hr 18min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 9,
          title: "Block and File Storage",
          details: "16 lectures • 1hr 23min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 10,
          title: "Docker Containers and ECS",
          details: "13 lectures • 1hr 5min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 11,
          title: "Serverless Applications",
          details: "17 lectures • 1hr 29min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 12,
          title: "Databases and Analytics",
          details: "32 lectures • 2hr 42min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 13,
          title: "Deployment and Management",
          details: "16 lectures • 1hr 18min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 14,
          title: "Monitoring, Logging, and Auditing",
          details: "13 lectures • 46min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 15,
          title: "Security in the Cloud",
          details: "20 lectures • 1hr 27min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 16,
          title: "Migration and Transfer",
          details: "11 lectures • 36min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
        {
          id: 17,
          title: "Web, Mobile, ML, and Cost Management",
          details: "12 lectures • 40min",
          lectures: [
            {
              id: 1,
              title: "Welcome and How to Use this Course",
              duration: "03:56",
              preview: true,
              icon: "fas fa-play-circle",
            },
          ],
        },
      ],
    };
  },
};
</script>
