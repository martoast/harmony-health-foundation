<template>
  <div class="relative isolate overflow-hidden">
    <!-- Background with gradient overlay -->
    <div class="absolute inset-0">
      <img src="/hero-image.png" alt="" class="h-full w-full object-cover" />
      <div class="absolute inset-0 bg-gradient-to-r from-blue-900/90 to-blue-600/70 mix-blend-multiply"></div>
    </div>
    
    <!-- Logo in header -->
    <div class="relative z-10 px-6 pt-6 lg:px-8">
      <div class="mx-auto max-w-7xl">
        <img src="/harmony-health-logo.svg" alt="Harmony Health Foundation" class="h-12 md:h-16" />
      </div>
    </div>
    
    <!-- Hero content -->
    <div class="relative px-6 py-16 sm:py-24 lg:px-8">
      <div class="mx-auto max-w-7xl grid lg:grid-cols-2 gap-12 items-center">
        <!-- Left column: Text content -->
        <div class="text-center lg:text-left">
          <div class="inline-flex items-center px-4 py-1.5 rounded-full bg-white/10 backdrop-blur-sm mb-6">
            <span class="h-2 w-2 rounded-full bg-blue-400 mr-2"></span>
            <span class="text-sm font-semibold text-white uppercase tracking-wide">501(c)(3) Nonprofit Organization</span>
          </div>
          
          <h1 class="text-4xl font-bold tracking-tight text-white sm:text-5xl lg:text-6xl">
            Empowering Healthcare.<br class="hidden sm:inline" /> Supporting Communities.
          </h1>
          
          <p class="mt-6 text-lg text-blue-100">
            Harmony Health Foundation provides education, employment, and community outreach to build a stronger, more compassionate healthcare workforce and uplift elderly care.
          </p>
          
          <!-- Stats bar -->
          <div class="mt-10 grid grid-cols-2 sm:grid-cols-4 gap-x-8 gap-y-6 text-center lg:text-left">
            <div>
              <p class="text-3xl font-bold text-white">200+</p>
              <p class="mt-1 text-sm text-blue-200">EMTs Trained</p>
            </div>
            <div>
              <p class="text-3xl font-bold text-white">50+</p>
              <p class="mt-1 text-sm text-blue-200">Scholarships Awarded</p>
            </div>
            <div>
              <p class="text-3xl font-bold text-white">8</p>
              <p class="mt-1 text-sm text-blue-200">Facilities Served</p>
            </div>
            <div>
              <p class="text-3xl font-bold text-white">30+</p>
              <p class="mt-1 text-sm text-blue-200">Community Events Hosted</p>
            </div>
          </div>
        </div>
        
        <!-- Right column: Action card -->
        <div class="flex justify-center lg:justify-end">
          <div class="w-full max-w-sm bg-white rounded-2xl shadow-xl overflow-hidden">
            <div class="px-6 py-8">
              <h2 class="text-2xl font-bold text-gray-900 text-center">How can we help you?</h2>
              <p class="mt-2 text-sm text-gray-500 text-center">Get started with one of our services</p>
              
              <form @submit.prevent="scrollToSection" class="mt-6 space-y-6">
                <div>
                  <label for="action" class="block text-sm font-medium text-gray-700">I'd like to:</label>
                  <select 
                    id="action" 
                    name="action" 
                    v-model="selectedSection" 
                    required 
                    class="mt-2 block w-full rounded-md border-gray-300 py-3 pl-3 pr-10 text-base focus:border-blue-500 focus:outline-none focus:ring-blue-500"
                  >
                    <option value="">Select an option</option>
                    <option value="programs">Apply for Scholarships</option>
                    <option value="programs">Request a Safety Presentation</option>
                    <option value="partnerships">Become a Partner</option>
                    <option value="donate">Donate Today</option>
                  </select>
                </div>
                
                <button 
                  type="submit" 
                  class="w-full flex items-center justify-center rounded-md border border-transparent bg-blue-600 py-3 px-4 text-base font-medium text-white shadow-sm hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2"
                >
                  Get Started
                </button>
              </form>
              
              <p class="mt-6 text-xs text-center text-gray-500">
                Have other inquiries?
                <a href="#contact" class="font-medium text-blue-600 hover:text-blue-500">Contact us</a>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const selectedSection = ref('')

const scrollToSection = () => {
  if (!selectedSection.value) return
  
  // Get the element by ID
  const sectionElement = document.getElementById(selectedSection.value)
  
  if (sectionElement) {
    // Smooth scroll to the section
    sectionElement.scrollIntoView({ 
      behavior: 'smooth',
      block: 'start'
    })
  }
}
</script>