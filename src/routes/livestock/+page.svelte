<script lang="ts">
  import { onMount } from "svelte";
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";
  gsap.registerPlugin(ScrollTrigger);

  import p1 from "$lib/assets/livestock/1.jpeg";
  import p2 from "$lib/assets/livestock/2.jpeg";
  import p3 from "$lib/assets/livestock/3.jpeg";
  import p4 from "$lib/assets/livestock/4.jpeg";

  let heroSection: HTMLElement;
  let contentBlocks: HTMLElement[];

  onMount(() => {
    // Hero animation
    gsap.from(".hero-stagger", {
      opacity: 0,
      y: 40,
      duration: 1,
      stagger: 0.2,
      ease: "power3.out",
    });

    // Fade-in content sections
    gsap.utils.toArray(".fade-section").forEach((el: any) => {
      gsap.from(el, {
        scrollTrigger: {
          trigger: el,
          start: "top 85%",
        },
        opacity: 0,
        y: 30,
        duration: 0.9,
        ease: "power2.out",
      });
    });

    // Floating gradient shapes
    gsap.to(".float", {
      y: -15,
      duration: 3,
      repeat: -1,
      yoyo: true,
      ease: "sine.inOut",
      stagger: 0.5,
    });
  });
</script>

<div class="font-sans text-gray-900 overflow-hidden bg-gradient-to-b from-white via-indigo-50 to-teal-50">

  <!-- Hero -->
  <section bind:this={heroSection} class="relative py-24 md:py-32 overflow-hidden">
    <div class="container mx-auto px-6 md:px-12 lg:px-20 grid grid-cols-1 md:grid-cols-2 items-center gap-12">
      <div>
        <h1 class="hero-stagger text-4xl md:text-5xl font-serif text-indigo-900 leading-tight">
          About the Livestock Operation
        </h1>
        <p class="hero-stagger mt-6 text-gray-700 leading-relaxed">
          Raising Quality — Living the Ranching Life
        </p>
        <p class="hero-stagger mt-4 text-gray-600 max-w-lg">
          My connection to real estate and livestock runs deep. I don’t just work in agriculture — I live it every day. Having spent my life on ranches and caring for animals, I understand the dedication, patience, and hard work that go into maintaining a thriving operation.
        </p>
      </div>

      <!-- Gradient photo frame -->
      <div class="relative flex justify-center md:justify-end">
        <div class="float absolute -top-10 -left-10 w-32 h-32 bg-teal-300/60 rounded-full blur-xl"></div>
        <div class="float absolute bottom-0 -right-10 w-40 h-40 bg-indigo-300/70 rounded-full blur-xl"></div>
        <div class="relative rounded-[2rem] p-[6px] bg-gradient-to-tr from-indigo-400 via-teal-400 to-pink-400 shadow-xl">
          <img src={p1} alt="Ranch" class="rounded-[1.8rem] w-full h-full object-cover" />
        </div>
      </div>
    </div>
  </section>

  <!-- Mission -->
  <section class="fade-section py-20 bg-white">
    <div class="container mx-auto px-6 md:px-12 lg:px-20 text-center md:text-left grid md:grid-cols-2 gap-12 items-center">
      <div>
        <h2 class="text-3xl font-serif text-indigo-900 mb-6">My Mission: Quality, Care & Commitment</h2>
        <p class="text-gray-600 leading-relaxed mb-6">
          Ranching is more than a profession — it’s a lifestyle rooted in stewardship, responsibility, and authenticity. Each animal represents generations of selective breeding, attention to health, and respect for the land.
        </p>
        <ul class="text-gray-700 space-y-2">
          <li>✅ Dedicated to premium livestock quality</li>
          <li>🌿 Sustainable, Living Soil Organic (LSO) Practices</li>
          <li>🤝 Ethical breeding and herd management</li>
          <li>🐮 Trusted relationships with buyers and fellow ranchers</li>
        </ul>
      </div>

      <div class="relative flex justify-center">
        <div class="relative rounded-[2rem] p-[6px] bg-gradient-to-tr from-teal-400 via-indigo-400 to-purple-400 shadow-lg">
          <img src={p3} alt="Livestock Mission" class="rounded-[1.8rem] object-cover h-[420px] w-full" />
        </div>
      </div>
    </div>
  </section>

  <!-- Livestock Offerings -->
  <section class="fade-section py-20 bg-gradient-to-b from-teal-50 to-white">
    <div class="container mx-auto px-6 md:px-12 lg:px-20">
      <h2 class="text-3xl font-serif text-indigo-900 mb-10 text-center">What I Offer: Livestock Sales & Support</h2>

      <div class="grid md:grid-cols-3 gap-8">
        <div class="bg-white rounded-2xl shadow-md p-6 transition hover:-translate-y-2 hover:shadow-xl">
          <img src={p2} alt="British White Park Cattle" class="rounded-xl mb-4 object-cover h-48 w-full" />
          <h3 class="text-xl font-semibold text-indigo-800 mb-2">British White Park Cattle</h3>
          <p class="text-gray-600 text-sm">Renowned for calm temperament, feed efficiency, and exceptional beef quality. We offer reliable British White Park Cattle breeders in Texas.</p>
        </div>

        <div class="bg-white rounded-2xl shadow-md p-6 transition hover:-translate-y-2 hover:shadow-xl">
          <img src={p3} alt="Black Angus" class="rounded-xl mb-4 object-cover h-48 w-full" />
          <h3 class="text-xl font-semibold text-indigo-800 mb-2">Black Angus Cattle</h3>
          <p class="text-gray-600 text-sm">Industry-standard genetics known for consistency, marbling, and performance. Specialized Black Angus breeding stock available for sale.</p>
        </div>

        <div class="bg-white rounded-2xl shadow-md p-6 transition hover:-translate-y-2 hover:shadow-xl">
          <img src={p4} alt="Spotted Boer Goats" class="rounded-xl mb-4 object-cover h-48 w-full" />
          <h3 class="text-xl font-semibold text-indigo-800 mb-2">Spotted Boer Goats</h3>
          <p class="text-gray-600 text-sm">Hardy, fast-growing, and ideal for breeding or meat production. Raised with care for long-term value and quality.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Location -->
  <section class="fade-section py-20 bg-white">
    <div class="container mx-auto px-6 md:px-12 lg:px-20 grid md:grid-cols-2 items-center gap-12">
      <div>
        <h2 class="text-3xl font-serif text-indigo-900 mb-4">Where We’re Rooted</h2>
        <p class="text-gray-600 mb-4">
          Our operation is based in Castroville, Texas, serving both local and regional buyers across Medina County. From small hobby farms to large-scale operations, we connect high-quality livestock with people who value integrity, sustainability, and care.
        </p>
        <p class="text-gray-700 mb-2"><strong>📍 Location:</strong> 2439 Hwy 90 West, Suite 101, Castroville, TX 78009</p>
        <p class="text-gray-700 mb-2"><strong>📞 Phone:</strong>1-210-416-0980</p>
        <p class="text-gray-700"><strong>📧 Email:</strong> kylaburell@gmail.com</p>
      </div>

      <div class="rounded-[2rem] p-[6px] bg-gradient-to-tr from-indigo-400 via-teal-400 to-pink-400 shadow-lg">
        <img src={p4} alt="Castroville Map" class="rounded-[1.8rem] object-cover w-full h-[400px]" />
      </div>
    </div>
  </section>

  <!-- Approach -->
  <section class="fade-section py-20 bg-teal-50">
    <div class="container mx-auto px-6 md:px-12 lg:px-20 text-center">
      <h2 class="text-3xl font-serif text-indigo-900 mb-6">My Approach: Honest, Hands-On & Experienced</h2>
      <p class="text-gray-600 max-w-3xl mx-auto leading-relaxed">
        Every day on the ranch brings new challenges and rewards — and that experience shapes everything I do. I believe in transparency, hands-on care, and long-term relationships built on trust.
      </p>

      <div class="mt-10 grid md:grid-cols-2 lg:grid-cols-4 gap-8">
        <div class="bg-white p-6 rounded-2xl shadow hover:shadow-lg transition">
          <h3 class="font-semibold text-indigo-800 mb-2">Experience You Can Trust</h3>
          <p class="text-gray-600 text-sm">A lifetime spent working with animals and managing herds.</p>
        </div>

        <div class="bg-white p-6 rounded-2xl shadow hover:shadow-lg transition">
          <h3 class="font-semibold text-indigo-800 mb-2">Quality Genetics</h3>
          <p class="text-gray-600 text-sm">Selective breeding focused on health, strength, and temperament.</p>
        </div>

        <div class="bg-white p-6 rounded-2xl shadow hover:shadow-lg transition">
          <h3 class="font-semibold text-indigo-800 mb-2">Sustainable Practices</h3>
          <p class="text-gray-600 text-sm">Living Soil Organic (LSO) methods and responsible stewardship.</p>
        </div>

        <div class="bg-white p-6 rounded-2xl shadow hover:shadow-lg transition">
          <h3 class="font-semibold text-indigo-800 mb-2">Personalized Support</h3>
          <p class="text-gray-600 text-sm">From selection to transport, ensuring a seamless experience.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Call to Action -->
  <section class="fade-section py-24 bg-gradient-to-r from-indigo-600 via-teal-600 to-indigo-700 text-white text-center">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl md:text-4xl font-serif mb-6">Let’s Build Something Great Together</h2>
      <p class="text-lg mb-8 max-w-3xl mx-auto opacity-90">
        Whether you’re growing your herd, starting a new venture, or searching for quality breeding stock, I’d love to help you find the right fit.
      </p>
      <a href="/contact" class="bg-white text-indigo-700 font-semibold px-8 py-3 rounded-full shadow hover:bg-indigo-50 transition">
        Get in Touch
      </a>
    </div>
  </section>
</div>

<style>
  :global(.container) {
    max-width: 1200px;
  }
</style>
