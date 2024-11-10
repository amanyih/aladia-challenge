<script setup lang="ts">
import {
  NavigationMenu,
  NavigationMenuContent,
  NavigationMenuItem,
  NavigationMenuLink,
  NavigationMenuList,
  NavigationMenuTrigger,
  navigationMenuTriggerStyle,
} from "@/components/ui/navigation-menu";
import { Button } from "@/components/ui/button";
import {
  HoverCard,
  HoverCardContent,
  HoverCardTrigger,
} from "@/components/ui/hover-card";

const components: { title: string; href: string; description: string }[] = [
  {
    title: "Alert Dialog",
    href: "/docs/components/alert-dialog",
    description:
      "A modal dialog that interrupts the user with important content and expects a response.",
  },
  {
    title: "Hover Card",
    href: "/docs/components/hover-card",
    description:
      "For sighted users to preview content available behind a link.",
  },
  {
    title: "Progress",
    href: "/docs/components/progress",
    description:
      "Displays an indicator showing the completion progress of a task, typically displayed as a progress bar.",
  },
  {
    title: "Scroll-area",
    href: "/docs/components/scroll-area",
    description: "Visually or semantically separates content.",
  },
  {
    title: "Tabs",
    href: "/docs/components/tabs",
    description:
      "A set of layered sections of content—known as tab panels—that are displayed one at a time.",
  },
  {
    title: "Tooltip",
    href: "/docs/components/tooltip",
    description:
      "A popup that displays information related to an element when the element receives keyboard focus or the mouse hovers over it.",
  },
];
</script>

<template>
  <div class="flex items-center justify-between px-2">
    <img
      src="https://www.udemy.com/staticx/udemy/images/v7/logo-udemy.svg"
      class="h-6 w-auto"
      alt=""
    />
    <NavigationMenu class="p-4 items-center justify-between">
      <NavigationMenuList>
        <NavigationMenuItem>
          <NavigationMenuTrigger>Categories</NavigationMenuTrigger>
          <NavigationMenuContent>
            <ul
              class="grid w-[400px] gap-3 p-4 md:w-[500px] md:grid-cols-2 lg:w-[600px]"
            >
              <li v-for="component in components" :key="component.title">
                <NavigationMenuLink as-child>
                  <a
                    :href="component.href"
                    class="block select-none space-y-1 rounded-md p-3 leading-none no-underline outline-none transition-colors hover:bg-accent hover:text-accent-foreground focus:bg-accent focus:text-accent-foreground"
                  >
                    <div class="text-sm font-medium leading-none">
                      {{ component.title }}
                    </div>
                    <p
                      class="line-clamp-2 text-sm leading-snug text-muted-foreground"
                    >
                      {{ component.description }}
                    </p>
                  </a>
                </NavigationMenuLink>
              </li>
            </ul>
          </NavigationMenuContent>
        </NavigationMenuItem>
        <NavigationMenuItem>
          <span class="flex items-center rounded-full p-2 relative">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6 text-gray-500 absolute left-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M21 21l-5-5m2-5a9 9 0 11-18 0 9 9 0 0118 0z"
              />
            </svg>
            <input
              type="text"
              placeholder="Search for anything"
              class="rounded-full w-[70rem] pl-12 pr-4 py-2 border border-gray-300 focus:outline-none focus:ring-2 focus:ring-accent focus:ring-opacity-50"
            />
          </span>
        </NavigationMenuItem>
        <NavigationMenuItem>
          <HoverCard>
            <HoverCardTrigger as-child>
              <Button variant="link"> Udemy Business </Button>
            </HoverCardTrigger>
            <HoverCardContent class="w-80">
              <div class="text-center rounded-md">
                <p class="text-lg font-medium mb-2">
                  Get your team access to over
                  <span class="font-bold">27,000</span> top Udemy courses,
                  anytime, anywhere.
                </p>
                <button
                  class="bg-black text-white font-semibold py-2 px-4 mt-4 w-full"
                >
                  Try Udemy Business
                </button>
              </div>
            </HoverCardContent>
          </HoverCard>
        </NavigationMenuItem>
        <NavigationMenuItem>
          <HoverCard>
            <HoverCardTrigger as-child>
              <Button variant="link"> Teach on Udemy </Button>
            </HoverCardTrigger>
            <HoverCardContent class="w-80">
              <div class="text-center rounded-md">
                <p class="text-lg font-medium mb-2">
                  Turn what you know into an opportunity and reach millions
                  around the world. Get your team access to over
                </p>
                <button
                  class="bg-black text-white font-semibold py-2 px-4 mt-4 w-full"
                >
                  Learn More
                </button>
              </div>
            </HoverCardContent>
          </HoverCard>
        </NavigationMenuItem>
        <NavigationMenuItem>
          <HoverCard>
            <HoverCardTrigger as-child>
              <Button variant="link">
                <Icon
                  name="clarity:shopping-cart-line"
                  class="h-6 w-6 text-gray-500"
                />
              </Button>
            </HoverCardTrigger>
            <HoverCardContent class="w-80">
              <div class="text-center p-4">
                <p class="text-gray-700 mb-2">Your cart is empty.</p>
                <a href="#" class="text-purple-700 font-semibold"
                  >Keep shopping</a
                >
              </div>
            </HoverCardContent>
          </HoverCard>
        </NavigationMenuItem>
        <Button variant="default"> Login </Button>
        <Button variant="secondary"> Sign Up </Button>
        <Button variant="default">
          <Icon name="clarity:world-line" class="h-6 w-6 text-gray-500" />
        </Button>
      </NavigationMenuList>
    </NavigationMenu>
  </div>
</template>
