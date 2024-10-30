<template>
  <section id="contact" class="bg-black text-white py-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-5xl mx-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <!-- Left Side: Contact Information -->
        <div class="space-y-6">
          <h2 class="text-4xl font-bold text-yellow-400">Contact Us</h2>
          <div class="space-y-4">
            <p class="flex items-start">
              <MapPinIcon class="h-6 w-6 text-white-400 mr-2 flex-shrink-0" />
              <span>123 Tech Street, Innovation City, 12345</span>
            </p>
            <p class="flex items-start">
              <PhoneIcon class="h-6 w-6 text-white-400 mr-2 flex-shrink-0" />
              <span>+1 (555) 123-4567</span>
            </p>
            <p class="flex items-start">
              <MailIcon class="h-6 w-6 text-white-400 mr-2 flex-shrink-0" />
              <span>info@techcompany.com</span>
            </p>
          </div>
        </div>

        <!-- Right Side: Contact Form -->
        <div>
          <form @submit.prevent="submitForm" class="space-y-8">
            <div>
              <input placeholder="Company name*" id="company" v-model="form.company" required
                class="mt-1 block w-full h-14 bg-white border border-gray-700 rounded-lg shadow-sm py-2 px-3 text-black focus:outline-none focus:ring-2 focus:ring-purple-500 focus:border-transparent">
            </div>
            <div>
              <input placeholder="Full name*" type="text" id="name" v-model="form.name" required
                class="mt-1 block w-full h-14 bg-white border border-gray-700 rounded-lg shadow-sm py-2 px-3 text-black focus:outline-none focus:ring-2 focus:ring-purple-500 focus:border-transparent">
            </div>
            <div>
              <input placeholder="Email*"  type="email" id="email" v-model="form.email" required
                class="mt-1 block w-full h-14 bg-white border border-gray-700 rounded-lg shadow-sm py-2 px-3 text-black focus:outline-none focus:ring-2 focus:ring-purple-500 focus:border-transparent">
            </div>
            <div>
              <textarea placeholder="Message*"  id="message" v-model="form.message" rows="4" required
                class="mt-1 block w-full  bg-white border border-gray-700 rounded-lg shadow-sm py-2 px-3 text-white focus:outline-none focus:ring-2 focus:ring-purple-500 focus:border-transparent resize-y"></textarea>
            </div>
            <div>
              <button type="submit" id="submitBtn"
                class="w-full h-12 bg-purple-600 hover:bg-purple-700 text-white font-bold py-2 px-4 rounded-2xl focus:outline-none focus:ring-2 focus:ring-purple-500 focus:ring-offset-2 focus:ring-offset-gray-900 transition duration-150 ease-in-out">
                Send Message
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import { MapPinIcon, PhoneIcon, MailIcon } from 'lucide-vue-next'

const form = ref({
  company: '',
  name: '',
  email: '',
  message: ''
})

const submitForm = () => {
  // Here you would typically send the form data to your backend
  console.log('Form submitted:', form.value)
  // Reset form after submission
  form.value = { company: '', name: '', email: '', message: '' }
}
</script>