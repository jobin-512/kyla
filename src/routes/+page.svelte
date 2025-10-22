<script lang="ts">
  import { onMount } from "svelte";
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";

  import Hero from '$lib/assets/home/hero.webp';
  import about from '$lib/assets/home/about.webp';
  import property1 from '$lib/assets/home/01.webp';
  import property2 from '$lib/assets/home/02.webp';
  import property3 from '$lib/assets/home/03.webp';
  import property4 from '$lib/assets/home/04.webp';
  import houseDiscount from '$lib/assets/home/choose1.webp';
  import apartmentDiscount from '$lib/assets/home/choose2.webp';
  import cta from "$lib/assets/home/cta.webp";
  import FeatureCard from '$lib/components/FeatureCard.svelte';
  import banner from '$lib/assets/home/banner.mp4';

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    // Hero text animation
    gsap.from(".hero-content", {
      y: 50,
      opacity: 0,
      duration: 1.5,
      ease: "power3.out",
    });

    // Fade up for all sections
    gsap.utils.toArray<HTMLElement>(".fade-up").forEach((el) => {
      gsap.fromTo(
        el,
        { y: 60, opacity: 0 },
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

    // Feature card stagger reveal
    gsap.from(".feature-card", {
      scrollTrigger: {
        trigger: ".feature-card",
        start: "top 90%",
      },
      y: 40,
      opacity: 0,
      duration: 0.8,
      stagger: 0.15,
      ease: "power2.out",
    });

    // Property hover pop-in
    gsap.from(".property-card", {
      scrollTrigger: {
        trigger: ".property-card",
        start: "top 85%",
      },
      y: 50,
      opacity: 0,
      duration: 0.9,
      stagger: 0.2,
      ease: "power2.out",
    });
  });
</script>

  <svelte:head>
    <title>Commercial &amp; Retail Properties for Lease in Castroville, TX</title>
    <meta name="description" content="Discover flexible commercial and retail properties for lease in Castroville, TX. Explore listings that fit your business goals with trusted local support.">
    <meta name="keywords" content="commercial properties for lease castroville tx,commercial property for lease near me,castroville retail space for lease by owner,Retail Space for Lease in Medina County">
  </svelte:head>

<!-- Hero Section -->
<section class="relative h-[80vh] overflow-hidden">
  <video
    class="absolute inset-0 w-full h-full object-cover"
    src={banner}
    autoplay
    loop
    muted
    playsinline
  ></video>
  <div class="absolute inset-0 bg-black opacity-40"></div>
  <div class="relative z-10 flex items-center justify-center h-full hero-content">
    <div class="text-center text-white p-8 bg-[#00000099] rounded-lg max-w-2xl mx-4">
      <h1 class="text-5xl font-bold mb-4">Find the Perfect Commercial Property for Lease Near You</h1>
      <p class="text-xl mb-2">Looking for a retail space for lease in Medina County? Explore exclusive retail space for lease by owner across Texas' Medina County in locations like Castroville, Hondo, etc., and secure your next business location today.</p>
    </div>
  </div>
</section>

<!-- Spotlight Retail Section -->
<section class="py-16 px-8 bg-gray-50 fade-up">
  <div class="max-w-7xl mx-auto text-center">
    <h2 class="text-4xl font-bold text-gray-800 mb-6">Spotlight on Retail Space for Lease in Medina County</h2>
    <p class="text-gray-600 text-lg max-w-3xl mx-auto mb-6">We understand that location is everything, especially in the competitive retail market...</p>
    <div class="flex justify-center gap-6 flex-wrap mt-8">
      <div class="bg-white p-6 rounded-lg shadow-lg hover:scale-105 transform transition">Small Boutique Front</div>
      <div class="bg-white p-6 rounded-lg shadow-lg hover:scale-105 transform transition">Large Service Center</div>
      <div class="bg-white p-6 rounded-lg shadow-lg hover:scale-105 transform transition">High-Visibility Locations</div>
    </div>
  </div>
</section>

<!-- About Section -->
<section class="flex flex-col lg:flex-row items-center justify-center py-16 px-8 gap-8 bg-white max-w-7xl mx-auto fade-up">
  <div class="lg:w-1/2 flex justify-center items-center relative">
    <div class="absolute -bottom-10 -right-10 w-3/4 h-3/4 bg-gray-200 z-0"></div>
    <img src={about} alt="About Us" class="relative z-10 w-full max-w-md rounded-lg shadow-lg" />
  </div>
  <div class="lg:w-1/2 mt-12 lg:mt-0 lg:pl-16 text-center lg:text-left">
    <h2 class="text-4xl font-bold text-gray-800 mb-6">Why Choose Kyla Schuehle Burell?</h2>
    <p class="text-gray-600 mb-8 max-w-md mx-auto lg:mx-0">We're not just leasing properties—we're building partnerships that help your business thrive in the heart of Texas!</p>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <div class="feature-card"><FeatureCard title="Prime Locations" icon="M12 8c..." text="Our commercial properties..." /></div>
      <div class="feature-card"><FeatureCard title="Direct Owner Leasing" icon="M7 12l..." text="No middlemen..." /></div>
      <div class="feature-card"><FeatureCard title="Flexible Solutions" icon="M21 21l..." text="Every business is unique..." /></div>
      <div class="feature-card"><FeatureCard title="Local Expertise" icon="M12 15v..." text="We know Medina County inside and out!" /></div>
    </div>
  </div>
</section>

<!-- Search Ends Here Section -->
<section class="py-16 px-8 bg-white fade-up">
  <div class="max-w-7xl mx-auto text-center">
    <h2 class="text-4xl font-bold text-gray-800 mb-6">Your Search Ends Here</h2>
    <p class="text-gray-600 text-lg max-w-3xl mx-auto mb-6">You've been searching for the ideal commercial property...</p>
    <button class="bg-blue-500 text-white px-6 py-3 rounded-lg hover:bg-blue-600 transition">Explore Listings</button>
  </div>
</section>

<!-- Property for Sale Section -->
<section class="py-16 px-8 bg-gray-100 fade-up">
  <div class="max-w-7xl mx-auto text-center mb-12">
    <h2 class="text-4xl font-bold text-gray-800">Property for Sale</h2>
    <p class="mt-4 text-lg text-gray-600 max-w-2xl mx-auto">Ortiz is one of the most popular real estate companies...</p>
  </div>
  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 max-w-7xl mx-auto">
    {#each [property1, property2, property3, property4] as prop, i}
      <div class="property-card bg-white rounded-lg shadow-lg overflow-hidden group">
        <div class="relative overflow-hidden">
          <img src={prop} alt="Property {i + 1}" class="w-full h-60 object-cover transform group-hover:scale-105 transition-transform duration-300" />
          <span class="absolute top-4 left-4 bg-blue-500 text-white text-xs font-semibold px-3 py-1 rounded-full">{i % 2 === 0 ? 'FOR RENT' : 'FOR SALE'}</span>
        </div>
        <div class="p-6">
          <h3 class="text-xl font-semibold text-gray-800">Property {i + 1}</h3>
          <p class="mt-2 text-gray-600 text-sm">Address goes here</p>
          <p class="text-gray-500 text-xs">Sqft, Beds, Bath, Garage</p>
          <p class="mt-4 text-blue-600 font-bold text-lg">Price $XXX,XXX</p>
        </div>
      </div>
    {/each}
  </div>
</section>


<!-- Discover Diverse Properties Section -->
<section class="fade-up py-16 px-8 bg-gray-50">
  <div class="max-w-7xl mx-auto text-center">
    <h2 class="text-4xl font-bold text-gray-800 mb-6">Discover Diverse Commercial Properties for Lease</h2>
    <p class="text-gray-600 text-lg max-w-3xl mx-auto mb-6">Castroville is booming, and your business needs a space that matches its ambition. Our inventory goes beyond basic retail—we offer flexible commercial properties for lease, including light industrial spaces, professional office suites, and specialized mixed-use buildings. No matter your industry, if you need a strategic location in the "Little Alsace of Texas," we have the perfect fit. Tell us your requirements, and we'll secure the right space for your expansion.</p>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-8">
      <div class="bg-white rounded-lg shadow-lg p-6 hover:scale-105 transform transition">Light Industrial Spaces</div>
      <div class="bg-white rounded-lg shadow-lg p-6 hover:scale-105 transform transition">Professional Office Suites</div>
      <div class="bg-white rounded-lg shadow-lg p-6 hover:scale-105 transform transition">Mixed-Use Buildings</div>
    </div>
  </div>
</section>


<!-- Discount Section -->
<section class="fade-up py-16 px-8 bg-white">
  <div class="max-w-7xl mx-auto flex flex-col lg:flex-row items-center justify-between gap-12">
    <div class="relative w-full lg:w-1/2 flex justify-center items-center h-96">
      <div class="absolute w-2/3 h-4/5 left-0 top-0 bg-gray-200 rounded-lg shadow-lg rotate-3"></div>
      <div class="absolute w-2/3 h-4/5 right-0 bottom-0 bg-gray-300 rounded-lg shadow-lg -rotate-3"></div>
      <div class="relative z-10 w-3/5 h-auto overflow-hidden rounded-lg shadow-xl -rotate-6 transform hover:rotate-0 transition-transform duration-300">
        <img src={houseDiscount} alt="Discounted House" class="w-full h-full object-cover" />
        <div class="absolute top-4 left-4 bg-blue-500 text-white text-xs font-semibold px-3 py-1 rounded-full rotate-45 transform origin-top-left">35% Discount</div>
        <div class="absolute bottom-0 w-full bg-blue-500 text-white text-center py-2 text-lg font-semibold">Price $89,000</div>
      </div>
      <div class="relative z-20 w-3/5 h-auto overflow-hidden rounded-lg shadow-xl rotate-6 -ml-16 mt-32 transform hover:rotate-0 transition-transform duration-300">
        <img src={apartmentDiscount} alt="Discounted Apartment" class="w-full h-full object-cover" />
        <div class="absolute bottom-0 w-full bg-blue-500 text-white text-center py-2 text-lg font-semibold">Price $1,53,000</div>
      </div>
    </div>

    <div class="w-full lg:w-1/2 mt-12 lg:mt-0 lg:pl-16 text-center lg:text-left">
      <h2 class="text-4xl font-bold text-gray-800 mb-6">What Makes Leasing with Kyla Different?</h2>
      <p class="text-gray-600 mb-8 max-w-md mx-auto lg:mx-0">Forget everything you know about traditional landlords. Here, you get a true business ally who's invested in watching you win—from day one to grand opening and beyond!</p>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <FeatureCard title="Strategic Market Positioning" text="We don't just hand you keys—we give you a competitive advantage by placing your business exactly where it needs to be to thrive!" icon="M7 12l3-3 3 3 4-4M18 10V6M6 6h.01M12 6v4.062M16.5 10.5L12 15m0 0l-4.5 4.5"/>
        <FeatureCard title="Zero Red Tape Experience" text="Fast answers, flexible scheduling, and straightforward deals—because your time is money, and bureaucracy shouldn't cost you either!" icon="M3 10v11h18V10M17 10V6a4 4 0 00-4-4H7a4 4 0 00-4 4v4h14z"/>
        <FeatureCard title="Customized Lease Structures" text="Your business has a unique story, and your lease should tell it—with terms that bend to fit your goals, not the other way around!" icon="M12 8c1.657 0 3 .895 3 2s-1.343 2-3 2-3-.895-3-2 1.343-2 3-2zM9 20h6a1 1 0 001-1v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2a1 1 0 001 1h4zm0-10a3 3 0 11-6 0 3 3 0 016 0z"/>
        <FeatureCard title="Community-Connected Advantage" text="Tap into our local network and community ties that transform you from 'new tenant' to 'valued neighbor' the moment you move in!" icon="M9 12l2 2 4-4m5.618-4.276a11.952 11.952 0 01-.001-3.004c-.161-.994-.7-1.785-1.444-2.316a4.958 4.958 0 00-2.327-1.425C14.07 2.008 13.045 2 12 2c-1.045 0-2.07.008-3.046.012a4.958 4.958 0 00-2.327 1.425C5.7 4.939 5.161 5.73 5 6.724a11.952 11.952 0 01-.001 3.004c-.161 1.01-.7 1.785-1.444 2.316a4.958 4.958 0 00-2.327 1.425C2.07 14.008 2 15.045 2 16c0 1.045.008 2.07.012 3.046a4.958 4.958 0 001.425 2.327c.531.744 1.322 1.283 2.316 1.444a11.952 11.952 0 013.004.001c.994.161 1.785.7 2.316 1.444a4.958 4.958 0 001.425 2.327c1.01.008 2.035 0 3.046 0a4.958 4.958 0 002.327-1.425c.744-.531 1.283-1.322 1.444-2.316a11.952 11.952 0 01.001-3.004c.161-1.01.7-1.785 1.444-2.316a4.958 4.958 0 002.327-1.425c.008-1.01 0-2.035 0-3.046a4.958 4.958 0 00-1.425-2.327c-.531-.744-1.322-1.283-2.316-1.444z"/>
      </div>
    </div>
  </div>
</section>

<!-- CTA Image Section -->
<section class="fade-up flex justify-center items-center py-16 px-[5vw]">
  <img src={cta} alt="cta" class="rounded-xl shadow-xl"/>
</section>

<!-- New Interactive Sections -->



<!-- Exclusive Owner Leasing Section -->
<section class="fade-up py-16 px-8 bg-white">
  <div class="max-w-7xl mx-auto text-center">
    <h2 class="text-4xl font-bold text-gray-800 mb-6">Exclusive: Retail Space for Lease by Owner Advantage</h2>
    <p class="text-gray-600 text-lg max-w-3xl mx-auto mb-6">Tired of institutional landlords and frustrating management companies? You're in the right place. Our exclusive portfolio focuses on retail space for lease by the owner. This means faster approvals, greater transparency, and a direct line to the decision-maker (that’s me!). We cut out the unnecessary bureaucracy so you can focus 100% on what matters: running your business. Experience the ease of direct leasing with a local partner who truly cares.</p>
    <div class="flex justify-center gap-6 flex-wrap mt-8">
      <div class="bg-blue-500 text-white p-6 rounded-lg shadow-lg hover:scale-105 transform transition">Direct Owner Contact</div>
      <div class="bg-blue-500 text-white p-6 rounded-lg shadow-lg hover:scale-105 transform transition">Fast Approvals</div>
      <div class="bg-blue-500 text-white p-6 rounded-lg shadow-lg hover:scale-105 transform transition">Transparent Deals</div>
    </div>
  </div>
</section>




<!-- Insider Insights Section -->
<section class="fade-up py-16 px-8 bg-gray-50">
  <div class="max-w-7xl mx-auto text-center">
    <h2 class="text-4xl font-bold text-gray-800 mb-6">Insider Insights & Local Business Tips</h2>
    <p class="text-gray-600 text-lg max-w-3xl mx-auto mb-6">Your go-to resource for everything commercial real estate! From leasing strategies to market trends, we're sharing the knowledge that helps your business win big in Medina County.</p>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-8">
      <div class="bg-white p-6 rounded-lg shadow-lg hover:scale-105 transform transition">Leasing Strategies</div>
      <div class="bg-white p-6 rounded-lg shadow-lg hover:scale-105 transform transition">Market Trends</div>
      <div class="bg-white p-6 rounded-lg shadow-lg hover:scale-105 transform transition">Community Insights</div>
    </div>
  </div>
</section>

<!-- Contact Section -->
<section class="fade-up py-16 px-8 bg-white">
  <div class="max-w-2xl mx-auto text-center">
    <h2 class="text-4xl font-bold text-gray-800 mb-6">Ready to Lease Your Next Space?</h2>
    <p class="text-gray-600 text-lg mb-8">Connect with Kylas Burell now and explore exclusive retail space for lease in Medina County and retail space for lease by owner. Provide your name, email, phone number, and let us know what type of space you’re looking for. Our team will help you find the perfect fit quickly and efficiently.</p>
    <form class="flex flex-col gap-4">
      <input type="text" placeholder="Name" class="border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"/>
      <input type="email" placeholder="Email" class="border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"/>
      <input type="tel" placeholder="Phone Number" class="border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"/>
      <input type="text" placeholder="Type of Space You’re Looking For" class="border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"/>
      <button type="submit" class="bg-blue-500 text-white px-6 py-3 rounded-lg hover:bg-blue-600 transition mt-4">Submit</button>
    </form>
  </div>
</section>
