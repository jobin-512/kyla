<script lang="ts">
  import { onMount } from "svelte";
  import gsap from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";

  onMount(() => {
    gsap.utils.toArray<HTMLElement>(".fade-up").forEach((el) => {
      gsap.fromTo(
        el,
        { y: 40, opacity: 0 },
        {
          y: 0,
          opacity: 1,
          duration: 1,
          ease: "power2.out",
          scrollTrigger: {
            trigger: el,
            start: "top 85%",
          },
        }
      );
    });
  });
</script>

<!-- Hero Section -->
<section
  class="relative bg-cover bg-center h-[60vh] flex items-center justify-center"
  style="background-image: url('/images/contact-bg.jpg')"
>
  <div class="absolute inset-0 bg-black bg-opacity-60"></div>
  <div class="relative text-center text-white px-6 fade-up">
    <h1 class="text-4xl md:text-5xl font-bold mb-4">
      Contact Kyla Schuehle Burell
    </h1>
    <p class="text-lg max-w-3xl mx-auto">
      Let’s Bring Your Commercial Real Estate Vision to Life
    </p>
  </div>
</section>

<!-- Main Contact Section -->
<section class="py-20 px-8 bg-gray-50">
  <div class="max-w-7xl mx-auto grid grid-cols-1 lg:grid-cols-2 gap-12 items-start">
    <!-- Left Content -->
    <div class="fade-up">
      <h2 class="text-3xl font-bold text-gray-800 mb-6">
        Let’s Build Your Future in Medina County
      </h2>
      <p class="text-gray-700 leading-relaxed mb-4">
        Looking for the right space for lease in Medina County? Whether you’re a growing business, an investor, or a first-time entrepreneur, finding the right property is about more than square footage—it’s about location, opportunity, and long-term potential.
      </p>
      <p class="text-gray-700 leading-relaxed mb-4">
        I’m <strong>Kyla Schuehle Burell</strong>, your trusted local expert for Castroville, TX office space for lease and surrounding commercial properties. My goal is to make your next move simple, strategic, and successful by pairing you with a space that truly fits your business goals and growth plans.
      </p>
      <p class="text-gray-700 leading-relaxed mb-4">
        At <strong>Kyla Schuehle Burell Real Estate</strong>, I do more than list properties—I provide personalized guidance, deep market insight, and proven marketing strategies to help your investment stand out. From one-on-one consultations to full-scale property management support, every step of your journey is designed to be informed, confident, and rewarding.
      </p>
      <p class="text-gray-700 leading-relaxed mb-4">
        If you’re exploring commercial real estate for lease or seeking professional advice on how to position your property for maximum visibility and return, I’m here to help you every step of the way.
      </p>

      <div class="mt-8 space-y-3 text-gray-700">
        <div class="flex items-center gap-3">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-blue-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 12.414a4 4 0 10-5.657 5.657l4.243 4.243a8 8 0 111.414-1.414z" />
          </svg>
          <span><strong>Office Location:</strong> 2439 Hwy 90 West, Suite 101, Castroville, TX 78009</span>
        </div>
        <div class="flex items-center gap-3">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-blue-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8m-9 4v8m0-8l-7.89 5.26a2 2 0 01-2.22 0L3 12z" />
          </svg>
          <span><strong>Email:</strong> <a href="mailto:kylaburell@gmail.com" class="text-blue-600 hover:underline">kylaburell@gmail.com</a></span>
        </div>
        <div class="flex items-center gap-3">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-blue-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.95.684l1.518 4.55a1 1 0 01-.21.972L9.4 10.6a11.042 11.042 0 005 5l1.393-1.138a1 1 0 01.973-.21l4.55 1.518A1 1 0 0122 16.72V20a2 2 0 01-2 2h-1C9.716 22 2 14.284 2 5V4a1 1 0 011-1z" />
          </svg>
          <span><strong>Phone:</strong> <a href="tel:+12104160980" class="text-blue-600 hover:underline">1-210-416-0980</a></span>
        </div>
      </div>
    </div>

    <!-- Right: Contact Form -->
    <div class="bg-white rounded-2xl shadow-lg p-8 fade-up">
      <h3 class="text-2xl font-semibold mb-6 text-gray-800">Get In Touch</h3>
      <form class="space-y-4">
        <div>
          <label class="block text-gray-600 mb-1 text-sm">Full Name</label>
          <input type="text" class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500" />
        </div>
        <div>
          <label class="block text-gray-600 mb-1 text-sm">Email</label>
          <input type="email" class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500" />
        </div>
        <div>
          <label class="block text-gray-600 mb-1 text-sm">Phone Number</label>
          <input type="tel" class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500" />
        </div>
        <div>
          <label class="block text-gray-600 mb-1 text-sm">Message</label>
          <textarea rows="4" class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"></textarea>
        </div>
        <button type="submit" class="bg-blue-600 text-white px-6 py-3 rounded-lg hover:bg-blue-700 transition w-full">
          Send Message
        </button>
      </form>
    </div>
  </div>
</section>

<!-- CTA Section -->
<section class="bg-blue-600 text-white text-center py-12 fade-up">
  <h2 class="text-3xl font-bold mb-4">Let’s Connect Today</h2>
  <p class="max-w-2xl mx-auto text-lg mb-6">
    Turn your real estate goals into reality — because in this business, timing, trust, and the right partnership make all the difference.
  </p>
  <button class="bg-white text-blue-600 px-6 py-3 rounded-lg font-semibold hover:bg-gray-100 transition">
    Schedule a Consultation
  </button>
</section>
