<template>
    <section class="relative overflow-hidden bg-blue-600 py-32">
      <!-- Background pattern -->
      <div class="absolute inset-0 opacity-10">
        <svg class="absolute inset-0 h-full w-full" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <pattern id="grid-pattern" width="32" height="32" patternUnits="userSpaceOnUse" x="0" y="0">
              <path d="M0 32V0h32" fill="none" stroke="currentColor" stroke-width="1"></path>
            </pattern>
          </defs>
          <rect width="100%" height="100%" fill="url(#grid-pattern)" />
        </svg>
      </div>
      
      <div class="relative mx-auto max-w-7xl px-6 lg:px-8">
        <div class="mx-auto max-w-2xl lg:max-w-none">
          <div class="lg:grid lg:grid-cols-2 lg:gap-24">
            <!-- Left column: Impact information -->
            <div class="lg:self-center">
              <h2 class="text-3xl font-bold tracking-tight text-white sm:text-4xl">Make a Difference</h2>
              <p class="mt-4 text-lg text-blue-100">
                Every dollar helps us fund a student's future, strengthen healthcare delivery, and improve quality of life for our aging population.
              </p>
              
              <!-- Impact stats -->
              <div class="mt-12 grid grid-cols-1 gap-y-8 gap-x-12 sm:grid-cols-2">
                <div>
                  <p class="text-4xl font-bold tracking-tight text-white">100%</p>
                  <p class="mt-1 text-base text-blue-100">Of donations go directly to our programs</p>
                </div>
                <div>
                  <p class="text-4xl font-bold tracking-tight text-white">$2,500</p>
                  <p class="mt-1 text-base text-blue-100">Average scholarship amount</p>
                </div>
                <div>
                  <p class="text-4xl font-bold tracking-tight text-white">50+</p>
                  <p class="mt-1 text-base text-blue-100">Healthcare careers launched</p>
                </div>
                <div>
                  <p class="text-4xl font-bold tracking-tight text-white">8</p>
                  <p class="mt-1 text-base text-blue-100">Communities served</p>
                </div>
              </div>
            </div>
            
            <!-- Right column: Donation card -->
            <div class="mt-16 lg:mt-0">
              <div class="bg-white rounded-2xl shadow-xl overflow-hidden">
                <div class="px-8 py-10 sm:px-10">
                  <h3 class="text-xl font-semibold text-gray-900">Ways to Give</h3>
                  
                  <!-- Donation options -->
                  <div class="mt-8 space-y-6">
                    <!-- One-time donation -->
                    <div class="relative border border-gray-200 rounded-xl p-6 hover:border-blue-200 hover:bg-blue-50 transition-colors duration-300">
                      <div class="flex items-start">
                        <div class="flex h-6 items-center">
                          <input
                            id="one-time"
                            name="donation-type"
                            type="radio"
                            defaultChecked
                            class="h-4 w-4 border-gray-300 text-blue-600 focus:ring-blue-600"
                          />
                        </div>
                        <div class="ml-3">
                          <label for="one-time" class="block text-sm font-medium leading-6 text-gray-900">One-time donation</label>
                          <p class="text-xs text-gray-500 mt-1">Make an immediate impact with a single contribution</p>
                        </div>
                      </div>
                    </div>
                    
                    <!-- Monthly donation -->
                    <div class="relative border border-gray-200 rounded-xl p-6 hover:border-blue-200 hover:bg-blue-50 transition-colors duration-300">
                      <div class="flex items-start">
                        <div class="flex h-6 items-center">
                          <input
                            id="monthly"
                            name="donation-type"
                            type="radio"
                            class="h-4 w-4 border-gray-300 text-blue-600 focus:ring-blue-600"
                          />
                        </div>
                        <div class="ml-3">
                          <label for="monthly" class="block text-sm font-medium leading-6 text-gray-900">Monthly recurring donation</label>
                          <p class="text-xs text-gray-500 mt-1">Provide sustainable support throughout the year</p>
                        </div>
                      </div>
                    </div>
                    
                    <!-- Sponsor a student -->
                    <div class="relative border border-gray-200 rounded-xl p-6 hover:border-blue-200 hover:bg-blue-50 transition-colors duration-300">
                      <div class="flex items-start">
                        <div class="flex h-6 items-center">
                          <input
                            id="sponsor"
                            name="donation-type"
                            type="radio"
                            class="h-4 w-4 border-gray-300 text-blue-600 focus:ring-blue-600"
                          />
                        </div>
                        <div class="ml-3">
                          <label for="sponsor" class="block text-sm font-medium leading-6 text-gray-900">Sponsor a student</label>
                          <p class="text-xs text-gray-500 mt-1">Fund a complete scholarship for a future healthcare professional</p>
                        </div>
                      </div>
                    </div>
                    
                    <!-- In-kind donation -->
                    <div class="relative border border-gray-200 rounded-xl p-6 hover:border-blue-200 hover:bg-blue-50 transition-colors duration-300">
                      <div class="flex items-start">
                        <div class="flex h-6 items-center">
                          <input
                            id="in-kind"
                            name="donation-type"
                            type="radio"
                            class="h-4 w-4 border-gray-300 text-blue-600 focus:ring-blue-600"
                          />
                        </div>
                        <div class="ml-3">
                          <label for="in-kind" class="block text-sm font-medium leading-6 text-gray-900">In-kind donation</label>
                          <p class="text-xs text-gray-500 mt-1">Contribute equipment, training materials, or vehicles</p>
                        </div>
                      </div>
                    </div>
                  </div>
                  
                  <div class="mt-10">
                    <a
                      href="#donate-form"
                      class="block w-full rounded-md bg-blue-600 px-3.5 py-3.5 text-center text-sm font-semibold text-white shadow-sm hover:bg-blue-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-blue-600"
                    >
                      <div class="flex items-center justify-center">
                        <LockClosedIcon class="h-4 w-4 mr-2" />
                        Donate Securely
                      </div>
                    </a>
                  </div>
                  
                  <!-- Trust indicators -->
                  <div class="mt-6 flex items-center justify-center space-x-6">
                    <div class="flex items-center">
                      <ShieldCheckIcon class="h-5 w-5 text-gray-400" />
                      <span class="ml-2 text-xs text-gray-500">Secure Payment</span>
                    </div>
                    <div class="flex items-center">
                      <DocumentTextIcon class="h-5 w-5 text-gray-400" />
                      <span class="ml-2 text-xs text-gray-500">Tax Deductible</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  <script setup>
  import { LockClosedIcon, ShieldCheckIcon, DocumentTextIcon } from '@heroicons/vue/20/solid'
  </script>