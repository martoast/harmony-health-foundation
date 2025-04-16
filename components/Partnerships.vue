<template>
    <section class="py-32 bg-white">
      <div class="max-w-7xl mx-auto px-6 lg:px-8">
        <!-- Minimal header with subtle animation -->
        <div class="text-center mb-24">
          <h2 class="text-sm font-semibold uppercase tracking-widest text-blue-600 mb-3">Stronger Together</h2>
          <h3 class="text-4xl font-bold text-gray-900 tracking-tight">Partnerships</h3>
        </div>
        
        <!-- Clean, minimal grid layout -->
        <div class="grid lg:grid-cols-2 gap-24">
          <!-- Left column: Partner types -->
          <div class="space-y-16">
            <!-- Educational institutions -->
            <div class="group">
              <div class="flex items-center">
                <div class="h-px w-12 bg-gray-200 mr-6"></div>
                <h4 class="text-xl font-semibold text-gray-900">Educational Institutions</h4>
              </div>
              <p class="mt-6 text-gray-500 leading-relaxed">
                We collaborate with colleges and training programs to offer tuition sponsorships and guaranteed employment for graduates.
              </p>
              <div class="mt-8 overflow-hidden">
                <img 
                  src="/partnership-education.png" 
                  alt="Educational partnership" 
                  class="w-full h-72 object-cover rounded-lg shadow-sm transition-transform duration-500 group-hover:scale-105"
                />
              </div>
            </div>
            
            <!-- Healthcare facilities -->
            <div class="group">
              <div class="flex items-center">
                <div class="h-px w-12 bg-gray-200 mr-6"></div>
                <h4 class="text-xl font-semibold text-gray-900">Healthcare Facilities</h4>
              </div>
              <p class="mt-6 text-gray-500 leading-relaxed">
                We partner with nursing homes, hospitals, and assisted living centers to bring education, response readiness, and long-term staffing solutions.
              </p>
              <div class="mt-8 overflow-hidden">
                <img 
                  src="/partnership-healthcare.png" 
                  alt="Healthcare facility partnership" 
                  class="w-full h-72 object-cover rounded-lg shadow-sm transition-transform duration-500 group-hover:scale-105"
                />
              </div>
            </div>
          </div>
          
          <!-- Right column: How to partner and testimonial -->
          <div class="lg:px-8 lg:border-l border-gray-100 lg:pl-16">
            <div class="sticky top-8">
              <!-- Clean, minimal partner info card -->
              <div class="bg-gray-50 rounded-2xl p-10">
                <h4 class="text-xl font-semibold text-gray-900">How to Partner</h4>
                <p class="mt-4 text-gray-500 leading-relaxed">
                  Want to sponsor students, host training events, or receive healthcare staffing support? Our partnership team will guide you through the process.
                </p>
                
                <!-- Clean partnership benefits -->
                <ul class="mt-8 space-y-4">
                  <li class="flex">
                    <CheckCircleIcon class="h-6 w-6 text-blue-600 flex-shrink-0" />
                    <span class="ml-3 text-gray-500">Scholarship sponsorship opportunities</span>
                  </li>
                  <li class="flex">
                    <CheckCircleIcon class="h-6 w-6 text-blue-600 flex-shrink-0" />
                    <span class="ml-3 text-gray-500">Co-branded training events</span>
                  </li>
                  <li class="flex">
                    <CheckCircleIcon class="h-6 w-6 text-blue-600 flex-shrink-0" />
                    <span class="ml-3 text-gray-500">Healthcare staffing solutions</span>
                  </li>
                  <li class="flex">
                    <CheckCircleIcon class="h-6 w-6 text-blue-600 flex-shrink-0" />
                    <span class="ml-3 text-gray-500">Community outreach collaboration</span>
                  </li>
                </ul>
                
                <!-- Minimal, focused CTA -->
                <div class="mt-10">
                  <a 
                    href="mailto:partners@harmonyhealthfoundation.org" 
                    class="block w-full text-center bg-blue-600 text-white py-4 px-6 rounded-xl hover:bg-blue-700 transition-colors duration-300 text-sm font-medium tracking-wide"
                  >
                    Contact Our Partnership Team
                  </a>
                </div>
              </div>
              
              <!-- Testimonial -->
              <div class="mt-12 bg-white border border-gray-100 rounded-2xl p-10">
                <div class="flex items-center mb-6">
                  <div class="h-10 w-10 rounded-full bg-blue-100 flex items-center justify-center">
                    <BuildingOffice2Icon class="h-5 w-5 text-blue-600" />
                  </div>
                  <div class="ml-4">
                    <h5 class="text-sm font-semibold text-gray-900">Central Medical College</h5>
                    <p class="text-xs text-gray-500">Educational Partner</p>
                  </div>
                </div>
                <p class="text-gray-500 italic leading-relaxed">
                  "Our partnership with Harmony Health Foundation has transformed our EMT program. Students now have clear career paths and meaningful employment opportunities after graduation."
                </p>
              </div>
            </div>
          </div>
        </div>
        
       
      </div>
    </section>
  </template>
  <script setup>
  import { CheckCircleIcon, BuildingOffice2Icon } from '@heroicons/vue/24/solid'
  </script>