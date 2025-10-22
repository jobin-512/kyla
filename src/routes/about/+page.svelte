<script lang="ts">
  import { onMount } from "svelte";
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";
  import aboutHero from "$lib/assets/home/hero.webp"; // optional hero illustration

  onMount(() => {
    gsap.utils.toArray<HTMLElement>(".fade-up").forEach((el) => {
      gsap.fromTo(
        el,
        { y: 60, opacity: 0 },
        {
          y: 0,
          opacity: 1,
          duration: 1.1,
          ease: "power2.out",
          scrollTrigger: { trigger: el, start: "top 85%" },
        }
      );
    });
  });
</script>

  <svelte:head>
    <title>Trusted Commercial Leasing Expert in Medina County</title>
    <meta name="description" content="Explore high-traffic commercial space for lease in Castroville TX, including office space in Medina County. Secure your ideal property today with expert lease real estate guidance.">
    <meta name="keywords" content="commercial space for lease hondo,castroville office space for lease,office space for lease medina county,Commercial space for lease castroville texas,Office Space For Lease in Castroville TX,lease real estate medina county">
  </svelte:head>

<!-- Hero -->
<section class="relative h-[70vh] bg-center bg-cover" style="background-image:url('{aboutHero}')">
  <div class="absolute inset-0 bg-black/50"></div>
  <div class="relative z-10 flex items-center justify-center h-full text-center text-white px-4 fade-up">
    <div class="max-w-3xl">
      <h1 class="text-5xl font-bold mb-3">About Kyla Schuehle Burell</h1>
      <p class="text-xl font-light">Connecting People, Properties, and Possibilities</p>
    </div>
  </div>
</section>

<!-- Intro -->
<section class="py-16 px-6 bg-white fade-up">
  <div class="max-w-5xl mx-auto text-center">
    <p class="text-lg text-gray-700 leading-relaxed">
      Welcome to my website—your one-stop destination for finding the perfect commercial property
      and discovering what’s possible when passion meets real estate expertise.
    </p>
    <p class="mt-6 text-gray-600">
      I’m <strong>Kyla Schuehle Burell</strong>, proud to help individuals, business owners, and investors
      find the right space for lease in Castroville and beyond.
    </p>
  </div>
</section>

<!-- Mission -->
<section class="py-20 px-8 bg-gray-50 fade-up">
  <div class="max-w-6xl mx-auto grid lg:grid-cols-2 gap-12 items-center">
    <div>
      <h2 class="text-3xl font-bold text-gray-800 mb-4">My Mission: Turning Property Goals into Real-World Success</h2>
      <p class="text-gray-600 leading-relaxed mb-4">
        Real estate is more than a profession for me—it’s a passion rooted in community, connection,
        and possibility. Every client deserves personalized attention, honest communication, and a
        strategy built for long-term success.
      </p>
      <p class="text-gray-600 leading-relaxed">
        When you work with me, you’re gaining a partner who listens to your goals, anticipates your needs,
        and guides you confidently through every step of your leasing or buying journey.
      </p>
    </div>
    <div class="bg-white shadow-lg rounded-2xl p-8">
      <ul class="space-y-3 text-gray-700">
        <li>✓ Personalized attention and strategic planning</li>
        <li>✓ Deep local expertise in Castroville and Medina County</li>
        <li>✓ Proven marketing and negotiation strategies</li>
        <li>✓ End-to-end support for buyers, tenants, and investors</li>
      </ul>
    </div>
  </div>
</section>

<!-- What I Offer -->
<section class="py-20 px-6 bg-white fade-up">
  <div class="max-w-6xl mx-auto text-center mb-12">
    <h2 class="text-3xl font-bold text-gray-800 mb-4">What I Offer: Commercial Real Estate That Fits You</h2>
    <p class="text-gray-600 max-w-3xl mx-auto">
      I specialize in helping clients lease or purchase a wide range of commercial properties across Castroville and surrounding areas.
    </p>
  </div>
  <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8 max-w-6xl mx-auto">
    <div class="bg-gray-50 rounded-xl p-6 shadow hover:shadow-md transition">
      <h3 class="text-xl font-semibold text-gray-800 mb-2">Office Spaces</h3>
      <p class="text-gray-600">Professional environments for growing teams and established businesses.</p>
    </div>
    <div class="bg-gray-50 rounded-xl p-6 shadow hover:shadow-md transition">
      <h3 class="text-xl font-semibold text-gray-800 mb-2">Retail Spaces</h3>
      <p class="text-gray-600">High-visibility locations designed to attract foot traffic and boost your brand.</p>
    </div>
    <div class="bg-gray-50 rounded-xl p-6 shadow hover:shadow-md transition">
      <h3 class="text-xl font-semibold text-gray-800 mb-2">Warehouses &amp; Industrial Units</h3>
      <p class="text-gray-600">Adaptable spaces for logistics, storage, or production.</p>
    </div>
    <div class="bg-gray-50 rounded-xl p-6 shadow hover:shadow-md transition">
      <h3 class="text-xl font-semibold text-gray-800 mb-2">Farms &amp; Ranches</h3>
      <p class="text-gray-600">Rural listings for land, lifestyle, or agricultural opportunity.</p>
    </div>
  </div>
</section>

<!-- Where I Work -->
<section class="py-20 px-6 bg-gray-100 fade-up">
  <div class="max-w-6xl mx-auto grid lg:grid-cols-2 gap-12 items-center">
    <div>
      <h2 class="text-3xl font-bold text-gray-800 mb-4">Where I Work: Rooted in Castroville</h2>
      <p class="text-gray-600 leading-relaxed">
        Castroville, TX, blends small-town charm with business opportunity. I also serve clients
        throughout Medina County and across Highway 90—from Castroville to Hondo—connecting
        entrepreneurs and investors with commercial spaces and investment opportunities.
      </p>
    </div>
    <div class="bg-white shadow rounded-2xl p-8 text-gray-700">
      <h3 class="text-xl font-semibold mb-4 text-blue-700">Office Location</h3>
      <p>2439 Hwy 90 West, Suite 101<br />Castroville, TX 78009</p>
      <p class="mt-4">📞 1-210-416-0980<br />✉️ kylaburell@gmail.com</p>
    </div>
  </div>
</section>

<!-- Approach -->
<section class="py-20 px-6 bg-white fade-up">
  <div class="max-w-6xl mx-auto text-center">
    <h2 class="text-3xl font-bold text-gray-800 mb-6">My Approach: Personalized, Professional &amp; Proven</h2>
    <p class="text-gray-600 max-w-3xl mx-auto">
      Every client relationship begins with a conversation. I take time to understand your vision—
      your goals, business model, and growth plan—then craft a strategy to match.
    </p>
    <p class="mt-6 text-gray-600 max-w-3xl mx-auto">
      Expect clear communication, creative solutions, and a supportive experience from start to finish.
    </p>
  </div>
</section>

<!-- Why Clients Choose Me -->
<section class="py-20 px-6 bg-gray-50 fade-up">
  <div class="max-w-6xl mx-auto text-center mb-12">
    <h2 class="text-3xl font-bold text-gray-800 mb-4">Why Clients Choose Me</h2>
    <p class="text-gray-600">Trusted guidance, transparent communication, and long-term partnership.</p>
  </div>
  <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto">
    {#each [
      ["Local Expertise", "Deep knowledge of the Castroville market and surrounding regions."],
      ["Full-Service Support", "From searches to negotiations, every step handled with care."],
      ["Tailored Solutions", "Your business is unique—your space should be too."],
      ["Transparency &amp; Trust", "Integrity and honesty guide every transaction."],
      ["Long-Term Vision", "Building relationships that last well beyond closing."],
      ["Community Connection", "Dedicated to Medina County’s growth and success."]
    ] as [title, text]}
      <div class="bg-white p-8 rounded-2xl shadow hover:shadow-lg transition">
        <h3 class="text-xl font-semibold text-gray-800 mb-2">{title}</h3>
        <p class="text-gray-600">{@html text}</p>
      </div>
    {/each}
  </div>
</section>

<!-- CTA -->
<section class="py-20 px-6 bg-blue-600 text-white text-center fade-up">
  <div class="max-w-4xl mx-auto">
    <h2 class="text-4xl font-bold mb-4">Let’s Build Your Next Chapter Together</h2>
    <p class="text-lg mb-8">
      Whether you’re expanding your company, launching a new venture, or finding your ideal space for lease in Castroville,
      I’d love to help you reach your goals.
    </p>
    <a href="/contact" class="inline-block bg-white text-blue-700 font-semibold px-8 py-3 rounded-lg hover:bg-gray-100 transition">
      Get in Touch
    </a>
  </div>
</section>
