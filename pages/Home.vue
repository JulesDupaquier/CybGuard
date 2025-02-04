<template>
    <div class="text-white min-h-screen">
  
      <!-- Hero Section -->
      <section class="container mx-auto px-6 py-20 text-center">
        <h1 class="text-5xl font-bold mb-6">Protect Your Digital World</h1>
        <p class="text-xl mb-8">Advanced cybersecurity solutions for individuals and businesses.</p>
        <div class="space-x-4">
          <button class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-full">Get Started</button>
          <button class="bg-transparent border border-white hover:bg-white hover:text-gray-900 text-white px-6 py-3 rounded-full">Learn More</button>
        </div>
      </section>
  
      <!-- Features Section -->
      <section class="bg-gray-800 py-20">
        <div class="container mx-auto px-6">
          <h2 class="text-3xl font-bold text-center mb-12">Our Features</h2>
          <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="bg-gray-700 p-8 rounded-lg text-center">
              <h3 class="text-xl font-bold mb-4">Real-Time Monitoring</h3>
              <p class="text-gray-400">Monitor your systems in real-time for any threats.</p>
            </div>
            <div class="bg-gray-700 p-8 rounded-lg text-center">
              <h3 class="text-xl font-bold mb-4">Advanced Encryption</h3>
              <p class="text-gray-400">Secure your data with state-of-the-art encryption.</p>
            </div>
            <div class="bg-gray-700 p-8 rounded-lg text-center">
              <h3 class="text-xl font-bold mb-4">24/7 Support</h3>
              <p class="text-gray-400">Our team is available around the clock to assist you.</p>
            </div>
          </div>
        </div>
      </section>
  
      <!-- Pricing Section -->
      <section class="py-20">
        <div class="container mx-auto px-6">
          <h2 class="text-3xl font-bold text-center mb-12">Pricing Plans</h2>
          <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="bg-gray-800 p-8 rounded-lg text-center">
              <h3 class="text-xl font-bold mb-4">Basic</h3>
              <p class="text-4xl font-bold mb-6">$9.99<span class="text-gray-400 text-lg">/mo</span></p>
              <ul class="text-gray-400 mb-8">
                <li>Real-Time Monitoring</li>
                <li>Basic Encryption</li>
                <li>Email Support</li>
              </ul>
              <button class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-full w-full">Choose Plan</button>
            </div>
            <div class="bg-gray-800 p-8 rounded-lg text-center">
              <h3 class="text-xl font-bold mb-4">Pro</h3>
              <p class="text-4xl font-bold mb-6">$29.99<span class="text-gray-400 text-lg">/mo</span></p>
              <ul class="text-gray-400 mb-8">
                <li>Advanced Monitoring</li>
                <li>Advanced Encryption</li>
                <li>24/7 Support</li>
              </ul>
              <button class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-full w-full">Choose Plan</button>
            </div>
            <div class="bg-gray-800 p-8 rounded-lg text-center">
              <h3 class="text-xl font-bold mb-4">Enterprise</h3>
              <p class="text-4xl font-bold mb-6">$99.99<span class="text-gray-400 text-lg">/mo</span></p>
              <ul class="text-gray-400 mb-8">
                <li>Custom Solutions</li>
                <li>Dedicated Support</li>
                <li>Tailored Encryption</li>
              </ul>
              <button class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-full w-full">Choose Plan</button>
            </div>
          </div>
        </div>
      </section>
  
      <!-- Footer -->
      <footer class="bg-gray-800 py-12">
        <div class="container mx-auto px-6 text-center">
          <p class="text-gray-400">&copy; 2023 CyberSec. All rights reserved.</p>
        </div>
      </footer>
    </div>
  </template>
  
  <script>
  export default {
    name: 'IndexPage',
  }
  </script>
  
  <style>
  /* Add custom styles here if needed */
  </style>