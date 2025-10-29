<script lang="ts">
  import { onMount } from "svelte";
  import gsap from "gsap";
  import p1 from "$lib/assets/prop/A-Personalized-Approach-to-Commercial-Real-Estate.jpg";
  import p2 from "$lib/assets/prop/Office-Spaces.jpg";
  import p3 from "$lib/assets/prop/Retail-Locations.jpg";
  import p4 from "$lib/assets/prop/Warehouses-&-Industrial.jpg";
  import p5 from "$lib/assets/prop/Commercial-Properties-for-Lease-in-Hondo,-TX.jpg";
  import p6 from "$lib/assets/prop/Castroville,-TX-Commercial-Real-Estate.jpg";


  onMount(() => {
    gsap.from(".fade-up", {
      y: 50,
      opacity: 0,
      duration: 0.8,
      stagger: 0.2,
      ease: "power2.out",
    });
  });
</script>

  <svelte:head>
    <title>Commercial Lease in Medina County – Hondo & Castroville TX</title>
    <meta name="description" content="Discover available commercial properties in Hondo and Castroville TX. Lease prime office and retail spaces in Medina County with trusted real estate support.">
    <meta name="keywords" content="commercial lease medina county,Commercial Properties for Lease in Hondo tx,Castroville, TX Commercial Real Estate Properties for Lease">
  </svelte:head>

<section class="relative overflow-hidden bg-white text-gray-800">
  <!-- Hero Section -->
  <div class="relative py-20 px-6 md:px-20 text-center bg-gradient-to-br from-blue-900 via-blue-700 to-blue-500 text-white">
    <div class="max-w-3xl mx-auto fade-up">
      <h1 class="text-4xl md:text-5xl font-bold mb-4">
        Discover Commercial Spaces Designed to Help Your Business Grow
      </h1>
      <p class="text-lg opacity-90">
        Welcome to the heart of my real estate work — where vision meets opportunity.  
        Whether you’re looking for an office, retail space, or industrial property,  
        let’s find a space that fuels your growth.
      </p>
    </div>
  </div>

  <!-- Intro Section -->
  <div class="max-w-6xl mx-auto py-16 px-6 md:px-12 grid md:grid-cols-2 gap-12 items-center">
    <div class="space-y-6 fade-up">
      <h2 class="text-3xl font-bold text-blue-900">A Personalized Approach to Commercial Real Estate</h2>
      <p class="text-gray-700 leading-relaxed">
        Finding the right property is about more than just browsing listings.  
        It’s about understanding your goals — the why behind your next move —  
        and tailoring a plan that gets you there confidently.
      </p>
      <p class="text-gray-700">
        With deep local knowledge and hands-on experience, I’ll guide you through  
        every step — from discovery and negotiation to lease signing and beyond.
      </p>
    </div>

    <!-- Image Placeholder -->
    <div class="fade-up rounded-2xl  h-80 flex items-center justify-center shadow-inner">
      <img src={p1} alt="A Personalized Approach to Commercial Real Estate" class="h-full w-full object-cover rounded-lg">
    </div>
  </div>

  <!-- Featured Areas -->
  <div class="bg-gray-50 py-20 px-6 md:px-16 text-center">
    <h2 class="text-3xl font-bold text-blue-900 mb-10 fade-up">Explore Commercial Lease Opportunities in Medina County</h2>
    <p class="max-w-3xl mx-auto text-gray-700 fade-up">
      Medina County blends small-town warmth with big-market opportunity.  
      From Castroville to Hondo, discover commercial properties that match your goals.
    </p>

    <div class="grid md:grid-cols-3 gap-10 mt-14">
      <!-- Office -->
      <div class="bg-white rounded-2xl shadow-lg p-8 fade-up">
        <div class="h-48 mb-6 rounded-lg flex items-center justify-center">
          <img src={p2} alt="Office Spaces" class="h-full w-full object-cover rounded-lg">
        </div>
        <h3 class="text-xl font-semibold text-blue-900 mb-2">Office Spaces</h3>
        <p class="text-gray-600">Professional environments for startups and established businesses alike.</p>
      </div>

      <!-- Retail -->
      <div class="bg-white rounded-2xl shadow-lg p-8 fade-up">
        <div class="h-48 mb-6 rounded-lg flex items-center justify-center">
          <img src={p3} alt="Retail Locations" class="h-full w-full object-cover rounded-lg">
        </div>
        <h3 class="text-xl font-semibold text-blue-900 mb-2">Retail Locations</h3>
        <p class="text-gray-600">High-visibility spaces to attract customers and boost brand presence.</p>
      </div>

      <!-- Warehouse -->
      <div class="bg-white rounded-2xl shadow-lg p-8 fade-up">
        <div class="h-48 mb-6 rounded-lg flex items-center justify-center">
          <img src={p4} alt="Warehouses & Industrial" class="h-full w-full object-cover rounded-lg">
        </div>
        <h3 class="text-xl font-semibold text-blue-900 mb-2">Warehouses & Industrial</h3>
        <p class="text-gray-600">Adaptable spaces for logistics, storage, or light manufacturing.</p>
      </div>
    </div>
  </div>

  <!-- Local Market Sections -->
  <div class="max-w-6xl mx-auto py-20 px-6 md:px-12 space-y-20">
    <!-- Hondo -->
    <div class="grid md:grid-cols-2 gap-10 items-center fade-up">
      <div class="rounded-2xl h-72 flex items-center justify-center">
        <img src={p5} alt="Commercial Properties for Lease in Hondo, TX" class="h-full w-full object-cover rounded-lg">
      </div>
      <div>
        <h2 class="text-2xl font-bold text-blue-900 mb-4">Commercial Properties for Lease in Hondo, TX</h2>
        <p class="text-gray-700 leading-relaxed">
          Hondo offers a thriving business community and smart investment opportunities.  
          From affordable leases to prime commercial spaces, I’ll help you find a property  
          that fits your vision and supports your growth.
        </p>
      </div>
    </div>

    <!-- Castroville -->
    <div class="grid md:grid-cols-2 gap-10 items-center fade-up md:flex-row-reverse">
      <div class="rounded-2xl h-72 flex items-center justify-center">
        <img src={p6} alt="Commercial Properties for Lease in Castroville, TX" class="h-full w-full object-cover rounded-lg">
      </div>
      <div>
        <h2 class="text-2xl font-bold text-blue-900 mb-4">Castroville, TX Commercial Real Estate</h2>
        <p class="text-gray-700 leading-relaxed">
          Castroville blends historic charm with modern business potential.  
          I’ll help you explore listings that align with your goals — from boutique retail  
          to professional office spaces — and negotiate the right terms for your success.
        </p>
      </div>
    </div>
  </div>

  <!-- Why Work With Kyla -->
  <div class="bg-gradient-to-r from-blue-900 to-blue-700 text-white py-20 px-6 md:px-16 text-center fade-up">
    <h2 class="text-3xl font-bold mb-8">Why Work With Kyla Schuehle Burell?</h2>
    <div class="max-w-4xl mx-auto grid md:grid-cols-2 gap-8 text-left">
      <ul class="space-y-4">
        <li>✅ Personalized attention — every client and every property is unique.</li>
        <li>✅ Local expertise — deep knowledge of the Medina County market.</li>
        <li>✅ Comprehensive service — from marketing to negotiations.</li>
      </ul>
      <ul class="space-y-4">
        <li>✅ Honesty & transparency — built on trust, not transactions.</li>
        <li>✅ Long-term vision — partnerships that grow with your business.</li>
      </ul>
    </div>
  </div>

  <!-- CTA Section -->
  <div class="py-20 px-6 md:px-16 text-center fade-up">
    <h2 class="text-3xl font-bold text-blue-900 mb-6">Ready to Explore? Let’s Talk.</h2>
    <p class="max-w-2xl mx-auto text-gray-700 mb-10">
      Let’s discuss your goals, review available listings, and find the perfect space to take your business forward.
    </p>
    <div class="flex flex-wrap justify-center gap-6">
      <button class="bg-blue-700 text-white px-8 py-3 rounded-full font-semibold hover:bg-blue-800 transition-all">
        View Available Properties
      </button>
      <button class="border-2 border-blue-700 text-blue-700 px-8 py-3 rounded-full font-semibold hover:bg-blue-700 hover:text-white transition-all">
        Schedule a Consultation
      </button>
    </div>
  </div>
</section>

<style>
  section {
    font-family: 'Inter', sans-serif;
  }
</style>
