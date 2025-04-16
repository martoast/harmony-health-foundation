<template>
    <div class="relative overflow-hidden bg-white py-24 sm:py-32">
      <div ref="rootElement" class="relative mx-auto max-w-7xl px-6 lg:px-8">
        <h2 class="text-center text-3xl font-bold leading-8 tracking-tight text-gray-900 sm:text-4xl">Programs & Initiatives</h2>
        <p class="mx-auto mt-4 max-w-3xl text-center text-xl text-gray-500">
          Harmony Health Foundation is dedicated to strengthening the healthcare ecosystem by empowering EMTs, medics, and RNs with training, career opportunities, and purpose-driven work.
        </p>
      </div>
      <div v-for="(program, index) in programs" :key="index" :class="{ 'relative mt-12 lg:mt-24': index !== 1, 'mt-24': index === 1 }">
        <div class="lg:mx-auto lg:grid lg:max-w-7xl lg:grid-flow-col-dense lg:grid-cols-2 lg:gap-24 lg:px-8">
          <div :class="{
            'mx-auto max-w-xl px-6 lg:mx-0 lg:max-w-none lg:px-0 lg:py-16': index !== 1,
            'mx-auto max-w-xl px-6 lg:col-start-2 lg:mx-0 lg:max-w-none lg:px-0 lg:py-32': index === 1
          }">
            <div>
              <div>
                <span class="flex h-12 w-12 items-center justify-center rounded-xl bg-blue-600">
                  <component :is="program.icon" class="h-8 w-8 text-white" aria-hidden="true" />
                </span>
              </div>
              <div class="mt-6">
                <h2 class="text-3xl font-bold tracking-tight text-gray-900">{{ program.title }}</h2>
                <p class="mt-4 text-lg text-gray-500">{{ program.description }}</p>
                <div class="mt-6">
                  <a :href="program.ctaLink" class="relative inline-flex items-center gap-x-1.5 rounded-md bg-blue-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-blue-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-blue-600">
                      <component :is="program.ctaIcon" class="-ml-0.5 h-5 w-5" aria-hidden="true"></component>
                      {{ program.ctaText }}
                  </a>
                </div>
              </div>
            </div>
          </div>
          <div :class="{
            'mt-12 sm:mt-16 lg:mt-0': index !== 1,
            'mt-12 sm:mt-16 lg:col-start-1 lg:mt-0': index === 1
          }">
            <div :class="{
              '-mr-48 pl-6 md:-mr-16 lg:relative lg:m-0 lg:h-full lg:px-0': index !== 1,
              '-ml-48 pr-6 md:-ml-16 lg:relative lg:m-0 lg:h-full lg:px-0': index === 1
            }">
              <img 
                class="w-full rounded-xl shadow-xl ring-1 ring-black ring-opacity-5 lg:absolute lg:h-full lg:w-auto lg:max-w-none" 
                :class="{ 'lg:left-0': index !== 1, 'lg:right-0': index === 1 }"
                :src="program.imageSrc" 
                :alt="program.imageAlt" 
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  <script setup>
  import { ref } from 'vue'
  import { AcademicCapIcon, BriefcaseIcon, UserGroupIcon } from '@heroicons/vue/24/outline'
  import { PhoneIcon } from '@heroicons/vue/20/solid'
  import { StarIcon } from '@heroicons/vue/24/solid'
  
  const rootElement = ref(null)
  
  const programs = [
    {
      icon: AcademicCapIcon,
      title: 'Workforce Development',
      description: 'We fund scholarships and tuition for EMT, medic, and RN students. Through partnerships with local schools, we provide job placement, mentorship, and paid internships through Harmony Staffing Solutions.',
      imageSrc: '/feature-image.png',
      imageAlt: 'EMT students in training',
      ctaIcon: AcademicCapIcon,
      ctaText: 'Apply for Scholarship',
      ctaLink: '#scholarships',
      
    },
    {
      icon: BriefcaseIcon,
      title: 'Healthcare Job Creation',
      description: 'As Harmony Ambulance expands, we recruit newly certified professionals into real-world roles—helping them gain field experience while providing vital services to our region.',
      imageSrc: '/feature-image3.png',
      imageAlt: 'Healthcare professionals at work',
      ctaIcon: BriefcaseIcon,
      ctaText: 'Explore Careers',
      ctaLink: '#careers'
    },
    {
      icon: UserGroupIcon,
      title: 'Community Outreach',
      description: 'We lead safety presentations, health awareness campaigns, and emergency preparedness workshops in local nursing homes and senior living facilities.',
      imageSrc: '/feature-image2.png',
      imageAlt: 'Community health workshop',
      ctaIcon: PhoneIcon,
      ctaText: 'Request a Presentation',
      ctaLink: '#presentations'
    }
  ]
  </script>