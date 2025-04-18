<template>
    <footer class="bg-white">
      <div class="mx-auto max-w-7xl px-6 pt-20 pb-8 sm:pt-24 lg:px-8 lg:pt-32">
        <div class="xl:grid xl:grid-cols-3 xl:gap-8">
          <div class="space-y-8 xl:col-span-1">
            <img class="h-12" src="/harmony-health-logo.svg" alt="Harmony Health Foundation" />
            <p class="text-sm text-gray-600 max-w-xs">
              Strengthening the healthcare ecosystem through education, employment, and community outreach.
            </p>
            <div class="flex space-x-6">
              <a v-for="item in navigation.social" :key="item.name" :href="item.href" class="text-gray-400 hover:text-gray-500">
                <span class="sr-only">{{ item.name }}</span>
                <component :is="item.icon" class="size-6" aria-hidden="true" />
              </a>
            </div>
          </div>
          <div class="mt-16 grid grid-cols-2 gap-8 xl:col-span-2 xl:mt-0">
            <div class="md:grid md:grid-cols-2 md:gap-8">
              <div>
                <h3 class="text-sm font-semibold text-gray-900">Programs</h3>
                <ul role="list" class="mt-6 space-y-4">
                  <li v-for="item in navigation.programs" :key="item.name">
                    <a :href="item.href" class="text-sm text-gray-600 hover:text-blue-600">{{ item.name }}</a>
                  </li>
                </ul>
              </div>
              <div class="mt-10 md:mt-0">
                <h3 class="text-sm font-semibold text-gray-900">Get Involved</h3>
                <ul role="list" class="mt-6 space-y-4">
                  <li v-for="item in navigation.getInvolved" :key="item.name">
                    <a :href="item.href" class="text-sm text-gray-600 hover:text-blue-600">{{ item.name }}</a>
                  </li>
                </ul>
              </div>
            </div>
            <div class="md:grid md:grid-cols-2 md:gap-8">
              <div>
                <h3 class="text-sm font-semibold text-gray-900">About</h3>
                <ul role="list" class="mt-6 space-y-4">
                  <li v-for="item in navigation.about" :key="item.name">
                    <a :href="item.href" class="text-sm text-gray-600 hover:text-blue-600">{{ item.name }}</a>
                  </li>
                </ul>
              </div>
              <div class="mt-10 md:mt-0">
                <h3 class="text-sm font-semibold text-gray-900">Legal</h3>
                <ul role="list" class="mt-6 space-y-4">
                  <li v-for="item in navigation.legal" :key="item.name">
                    <a :href="item.href" class="text-sm text-gray-600 hover:text-blue-600">{{ item.name }}</a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Newsletter -->
        <div class="mt-16 border-t border-gray-200 pt-8">
          <div class="md:flex md:items-center md:justify-between">
            <div>
              <h3 class="text-sm font-semibold text-gray-900">Subscribe to our newsletter</h3>
              <p class="mt-2 text-sm text-gray-600">The latest news about our programs, events, and the healthcare community.</p>
            </div>
            <form class="mt-4 sm:ml-4 sm:mt-0 sm:flex-shrink-0">
              <div class="flex gap-2">
                <label for="email-address" class="sr-only">Email address</label>
                <input type="email" name="email-address" id="email-address" autocomplete="email" required class="w-full min-w-0 rounded-md border-0 bg-white px-3.5 py-2 text-sm text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-blue-600" placeholder="Enter your email" />
                <button type="submit" class="flex-shrink-0 rounded-md bg-blue-600 px-3.5 py-2 text-sm font-semibold text-white shadow-sm hover:bg-blue-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-blue-600">Subscribe</button>
              </div>
            </form>
          </div>
        </div>
        
        <!-- Copyright and certification -->
        <div class="mt-8 border-t border-gray-200 pt-8 md:flex md:items-center md:justify-between">
          <div class="flex flex-col md:flex-row md:items-center gap-4">
            <p class="text-xs text-gray-500">&copy; 2025 Harmony Health Foundation. All rights reserved.</p>
            <p class="text-xs text-gray-500">501(c)(3) Nonprofit</p>
          </div>
          <div class="mt-4 md:mt-0">
            <a href="#accessibility" class="text-xs text-gray-500 hover:text-blue-600">Accessibility</a>
          </div>
        </div>
      </div>
    </footer>
  </template>
  <script setup>
  import { defineComponent, h } from 'vue'
  
  const navigation = {
    programs: [
      { name: 'Workforce Development', href: '#scholarships' },
      { name: 'Healthcare Job Creation', href: '#careers' },
      { name: 'Community Outreach', href: '#outreach' },
      { name: 'Safety Presentations', href: '#presentations' },
    ],
    getInvolved: [
      { name: 'Apply for Scholarships', href: '#scholarships' },
      { name: 'Careers', href: '#careers' },
      { name: 'Become a Partner', href: '#partners' },
      { name: 'Donate', href: '#donate' },
    ],
    about: [
      { name: 'Our Mission', href: '#about' },
      { name: 'Leadership Team', href: '#team' },
      { name: 'Events', href: '#events' },
      { name: 'Success Stories', href: '#success-stories' },
    ],
    legal: [
      { name: 'Privacy Policy', href: '#privacy' },
      { name: 'Terms of Service', href: '#terms' },
      { name: 'Donor Privacy', href: '#donor-privacy' },
    ],
    social: [
      {
        name: 'Facebook',
        href: '#',
        icon: defineComponent({
          render: () =>
            h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
              h('path', {
                'fill-rule': 'evenodd',
                d: 'M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z',
                'clip-rule': 'evenodd',
              }),
            ]),
        }),
      },
      {
        name: 'Instagram',
        href: '#',
        icon: defineComponent({
          render: () =>
            h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
              h('path', {
                'fill-rule': 'evenodd',
                d: 'M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z',
                'clip-rule': 'evenodd',
              }),
            ]),
        }),
      },
      {
        name: 'LinkedIn',
        href: '#',
        icon: defineComponent({
          render: () =>
            h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
              h('path', {
                d: 'M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z',
              }),
            ]),
        }),
      },
    ],
  }
  </script>