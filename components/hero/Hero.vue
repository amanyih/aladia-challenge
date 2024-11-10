<script lang="ts" setup>
import {
  Breadcrumb,
  BreadcrumbEllipsis,
  BreadcrumbItem,
  BreadcrumbLink,
  BreadcrumbList,
  BreadcrumbPage,
  BreadcrumbSeparator,
} from "@/components/ui/breadcrumb";
</script>

<template>
  <div
    class="bg-black flex flex-col items-center justify-between text-white text-2xl gap-4 p-4"
  >
    <div class="flex flex-col lg:flex-row gap-8 w-[80rem] h-80">
      <div>
        <Breadcrumb class="self-start">
          <BreadcrumbList>
            <BreadcrumbItem>
              <BreadcrumbLink href="/"> IT & Software </BreadcrumbLink>
            </BreadcrumbItem>
            <BreadcrumbSeparator />
            <BreadcrumbItem>
              <BreadcrumbLink href="/docs/components/accordion.html">
                IT Certifications
              </BreadcrumbLink>
            </BreadcrumbItem>
            <BreadcrumbSeparator />
            <BreadcrumbItem>
              <BreadcrumbPage>Amazon AWS</BreadcrumbPage>
            </BreadcrumbItem>
          </BreadcrumbList>
        </Breadcrumb>
        <div class="flex-1 mt-5">
          <h1 class="text-3xl font-bold mb-2">
            AWS Certified Solutions Architect Associate (SAA-C03) Course
          </h1>
          <p class="text-md text-gray-300 mb-4">
            2024 AWS Certified Solutions Architect Associate Video Course
            SAA-C03 | Hands-on Exercises + AWS Practice Exam + Slides
          </p>
          <!-- Rating and Student Info -->
          <div class="flex items-center text-yellow-400 mb-4 text-sm">
            <span class="font-semibold">4.6</span>
            <span class="ml-2">★★★★★</span>
            <span class="text-gray-400 ml-2">(19,975 ratings)</span>
            <span class="text-gray-400 ml-2">105,522 students</span>
          </div>
          <!-- Author Information -->
          <div class="text-gray-400 mb-4 text-sm">
            <p>
              Created by
              <a href="#" class="text-blue-400 hover:underline"
                >Neal Davis | AWS Certified Solutions Architect & Developer,
                Digital Cloud Training | AWS Certified Cloud Practitioner AWS
                Certified Solutions Architect, AWS Developer Associate</a
              >
            </p>
            <p>
              Last updated 11/2024 • English, Arabic [Auto],
              <a href="#" class="text-blue-400 hover:underline">26 more</a>
            </p>
          </div>
        </div>
      </div>

      <div class="bg-white shadow-2xl w-full max-w-sm">
        <div class="relative mb-4">
          <img
            src="https://img-c.udemycdn.com/course/750x422/5057824_1b8f_3.jpg"
            alt="Course Preview"
            class="w-full"
          />
          <button
            class="absolute bottom-0 left-1/2 transform -translate-x-1/2 font-bold px-4 py-1 text-base"
          >
            Preview this course
          </button>
        </div>

        <!-- 
        when scrolling , and the following component reaches the top of the viewport, it should stick to the top of the viewport
        it should stop sticking to the top of the viewport when the bottom of the component reaches the bottom of the viewport
        and it should be there for the rest of the scroll.

         -->

        <div
          class="shadow-xl pl-4 pr-4 bg-white pb-4 border-b border-gray-300 z-10 mt-4 w-full max-w-sm sticky top-0"
        >
          <nav class="border-b border-gray-300 mb-4 text-base bg-white">
            <ul class="flex">
              <li
                class="flex-1 text-center py-2 cursor-pointer text-black font-semibold border-b-2 border-black"
              >
                Personal
              </li>
              <li
                class="flex-1 text-center py-2 cursor-pointer text-gray-500 hover:text-black"
              >
                Teams
              </li>
            </ul>
          </nav>

          <div class="mb-4 bg-white shadow-">
            <h2 class="text-xl font-semibold text-black s">
              Subscribe to Udemy’s top courses
            </h2>
            <p class="text-gray-600 text-sm mt-2">
              Get this course, plus 12,000+ of our top-rated courses, with
              Personal Plan.
              <a href="#" class="text-blue-500 underline">Learn more</a>
            </p>
            <button
              class="w-full text-base bg-purple-600 text-white font-semibold py-2 mt-4 hover:bg-purple-700"
            >
              Try Personal Plan for free
            </button>
            <p class="text-gray-500 text-xs mt-2 text-center">
              Starting at $10.00 per month after trial
            </p>
            <p class="text-gray-500 text-xs text-center">Cancel anytime</p>
            <div
              class="flex items-center justify-center my-4 text-gray-500 text-sm"
            >
              <span class="flex-grow border-b border-gray-300"></span>
              <span class="px-2">or</span>
              <span class="flex-grow border-b border-gray-300"></span>
            </div>
          </div>

          <div class="mb-4 text-center">
            <p class="text-xl font-bold text-black text-start">$84.99</p>
            <Button
              class="w-full border border-gray-900 text-gray-900 font-bold text-xl mt-4 hover:bg-gray-100 py-6"
              variant="default"
            >
              Add to cart
            </Button>
            <p class="text-gray-500 text-xs my-2">
              30-Day Money-Back Guarantee
            </p>
            <p class="text-gray-500 text-xs my-2">Full Lifetime Access</p>
          </div>

          <div class="flex justify-around text-sm font-bold text-gray-700 mb-4">
            <button class="underline">Share</button>
            <button>Gift this course</button>
            <button>Apply Coupon</button>
          </div>

          <div class="mb-2">
            <div
              class="border border-gray-300 p-2 flex items-center mb-2 border-dashed"
            >
              <span class="text-gray-700 text-sm font-semibold"
                >LETSLEARNNOW</span
              >
              <span class="ml-1 text-xs text-gray-500">is applied</span>
              <button class="ml-auto text-gray-400 hover:text-gray-600">
                &times;
              </button>
            </div>
            <div class="flex">
              <input
                type="text"
                placeholder="Enter Coupon"
                class="flex-1 border border-gray-300 p-2 text-sm focus:ring"
              />

              <button class="bg-gray-900 text-white font-semibold px-4 text-sm">
                Apply
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
