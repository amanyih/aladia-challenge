<template>
  <footer class="bg-gray-900 text-gray-400 py-8 px-10 text-sm">
    <div
      class="mx-auto flex items-center justify-between space-y-4 border-b border-gray-700 pb-6"
    >
      <p class="text-center text-gray-300">
        Top companies choose
        <span class="text-purple-400">Udemy Business</span> to build in-demand
        career skills.
      </p>
      <div class="flex justify-center space-x-6">
        <img
          v-for="logo in logos"
          :key="logo.alt"
          :src="logo.src"
          :alt="logo.alt"
          :width="logo.width"
          :height="logo.height"
          class="h-10 object-contain"
        />
      </div>
    </div>

    <div
      class="mx-auto py-8 grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-6 text-gray-300"
    >
      <FooterSection
        v-for="section in footerLinks"
        :key="section.title"
        :section="section"
      />
    </div>

    <div
      class="mx-auto border-t border-gray-700 pt-6 flex flex-col md:flex-row justify-between items-center space-y-4 md:space-y-0"
    >
      <div class="flex space-x-4 text-xs text-gray-400 items-center">
        <img
          src="https://www.udemy.com/staticx/udemy/images/v7/logo-udemy-inverted.svg"
          class="h-6 w-auto"
          alt=""
        />
        <a href="#" class="hover:underline">© 2024 Udemy, Inc.</a>
      </div>
      <div class="flex space-x-4 text-xs text-gray-400">
        <button class="hover:underline">Cookie settings</button>
      </div>

      <div class="flex items-center space-x-4 text-xs text-gray-400">
        <button class="hover:underline">🌐 English</button>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  components: {},
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
      footerLinks: [
        {
          title: "Certifications by Issuer",
          links: [
            { text: "Amazon Web Services (AWS) Certifications", href: "#" },
            { text: "Six Sigma Certifications", href: "#" },
            { text: "Microsoft Certifications", href: "#" },
            { text: "Cisco Certifications", href: "#" },
            { text: "Tableau Certifications", href: "#" },
            { text: "See all Certifications", href: "#" },
          ],
        },
        {
          title: "Certifications by Skill",
          links: [
            { text: "Cybersecurity Certification", href: "#" },
            { text: "Project Management Certification", href: "#" },
            { text: "Cloud Certification", href: "#" },
            { text: "Data Analytics Certification", href: "#" },
            { text: "HR Management Certification", href: "#" },
            { text: "See all Certifications", href: "#" },
          ],
        },
        {
          title: "Web Development",
          links: [
            { text: "Web Development", href: "#" },
            { text: "JavaScript", href: "#" },
            { text: "React JS", href: "#" },
            { text: "Angular", href: "#" },
            { text: "Java", href: "#" },
          ],
        },
        {
          title: "Data Science",
          links: [
            { text: "Data Science", href: "#" },
            { text: "Python", href: "#" },
            { text: "Machine Learning", href: "#" },
            { text: "ChatGPT", href: "#" },
            { text: "Deep Learning", href: "#" },
          ],
        },
        {
          title: "IT Certifications",
          links: [
            { text: "Amazon AWS", href: "#" },
            { text: "AWS Certified Cloud Practitioner", href: "#" },
            { text: "AZ-900: Microsoft Azure Fundamentals", href: "#" },
            {
              text: "AWS Certified Solutions Architect - Associate",
              href: "#",
            },
            { text: "Kubernetes", href: "#" },
          ],
        },
        {
          title: "Leadership",
          links: [
            { text: "Leadership", href: "#" },
            { text: "Management Skills", href: "#" },
            { text: "Project Management", href: "#" },
            { text: "Personal Productivity", href: "#" },
            { text: "Emotional Intelligence", href: "#" },
          ],
        },
        {
          title: "Communication",
          links: [
            { text: "Communication Skills", href: "#" },
            { text: "Presentation Skills", href: "#" },
            { text: "Public Speaking", href: "#" },
            { text: "Writing", href: "#" },
            { text: "PowerPoint", href: "#" },
          ],
        },
        {
          title: "Business Analytics & Intelligence",
          links: [
            { text: "Microsoft Excel", href: "#" },
            { text: "SQL", href: "#" },
            { text: "Microsoft Power BI", href: "#" },
            { text: "Data Analysis", href: "#" },
            { text: "Business Analysis", href: "#" },
          ],
        },
        {
          title: "About",
          links: [
            { text: "About us", href: "#" },
            { text: "Careers", href: "#" },
            { text: "Contact us", href: "#" },
            { text: "Blog", href: "#" },
            { text: "Investors", href: "#" },
          ],
        },
        {
          title: "Discovery Udemy",
          links: [
            { text: "Get the app", href: "#" },
            { text: "Teach on Udemy", href: "#" },
            { text: "Plans and Pricing", href: "#" },
            { text: "Affiliate", href: "#" },
            { text: "Help and Support", href: "#" },
          ],
        },
        {
          title: "Udemy for Business",
          links: [{ text: "Udemy Business", href: "#" }],
        },
        {
          title: "Legal & Accessibility",
          links: [
            { text: "Accessibility statement", href: "#" },
            { text: "Privacy policy", href: "#" },
            { text: "Sitemap", href: "#" },
            { text: "Terms", href: "#" },
          ],
        },
      ],
      footerBottomLinks: [
        { text: "Accessibility statement", href: "#" },
        { text: "Privacy policy", href: "#" },
        { text: "Sitemap", href: "#" },
        { text: "Terms", href: "#" },
      ],
    };
  },
};
</script>
