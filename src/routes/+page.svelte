<script lang="ts">
   import Hero from '$lib/assets/home/hero.webp';
   import about from '$lib/assets/home/about.webp';
   import property1 from '$lib/assets/home/01.webp';
   import property2 from '$lib/assets/home/02.webp';
   import property3 from '$lib/assets/home/03.webp';
   import property4 from '$lib/assets/home/04.webp';
   import houseDiscount from '$lib/assets/home/choose1.webp';
   import apartmentDiscount from '$lib/assets/home/choose2.webp';
   import cta from "$lib/assets/home/cta.webp"
   import agent1 from '$lib/assets/home/agent1.webp';
   import agent2 from '$lib/assets/home/agent1.webp';
   import agent3 from '$lib/assets/home/agent1.webp';
   import agent4 from '$lib/assets/home/agent1.webp';
</script>



 <section class="relative h-[80vh] bg-cover bg-center" style="background-image: url('{Hero}');">
   <div class="absolute inset-0 bg-black opacity-40"></div>
   <div class="relative z-10 flex items-center justify-center h-full">
     <div class="text-center text-white p-8 bg-[#00000099] rounded-lg max-w-lg mx-4">
       <h1 class="text-5xl font-bold mb-4">Desilva De Villa</h1>
       <p class="text-xl mb-2">24 North Street, California, USA</p>
       <p class="text-lg mb-4">3520 sqft, 5 Bed, 3 Bath, 2 Garage</p>
       <p class="text-3xl font-semibold">For Sale $54,000</p>
     </div>
   </div>
 </section>


<section class="flex flex-col lg:flex-row items-center justify-center py-16 px-8 gap-8 bg-white max-w-7xl mx-auto">
  <div class="lg:w-1/2 flex justify-center items-center relative">
    <div class="absolute -bottom-10 -right-10 w-3/4 h-3/4 bg-gray-200 z-0"></div>
    <img src={about} alt="About Us" class="relative z-10 w-full max-w-md rounded-lg shadow-lg" />
  </div>
  <div class="lg:w-1/2 mt-12 lg:mt-0 lg:pl-16 text-center lg:text-left">
    <h2 class="text-4xl font-bold text-gray-800 mb-6">We never compromise with quality work...</h2>
    <p class="text-gray-600 mb-8 max-w-md mx-auto lg:mx-0">Ortiz is one of the most popular real estate company all around USA. You can find your dream property or build property</p>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <div class="flex items-start">
        <div class="flex-shrink-0 mr-4 text-blue-500">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 8c1.657 0 3 .895 3 2s-1.343 2-3 2-3-.895-3-2 1.343-2 3-2zM9 20h6a1 1 0 001-1v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2a1 1 0 001 1h4zm0-10a3 3 0 11-6 0 3 3 0 016 0z" />
          </svg>
        </div>
        <div>
          <h3 class="text-xl font-semibold text-gray-800">Minimum Cost</h3>
          <p class="text-gray-600">Provide low cost that help all more build real estate</p>
        </div>
      </div>
      <div class="flex items-start">
        <div class="flex-shrink-0 mr-4 text-blue-500">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M7 12l3-3 3 3 4-4M18 10V6M6 6h.01M12 6v4.062M16.5 10.5L12 15m0 0l-4.5 4.5" />
          </svg>
        </div>
        <div>
          <h3 class="text-xl font-semibold text-gray-800">Best Marketing</h3>
          <p class="text-gray-600">Provide low cost that help all more build real estate</p>
        </div>
      </div>
      <div class="flex items-start">
        <div class="flex-shrink-0 mr-4 text-blue-500">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
          </svg>
        </div>
        <div>
          <h3 class="text-xl font-semibold text-gray-800">Easy to Search</h3>
          <p class="text-gray-600">You can find your property to simply and easy way</p>
        </div>
      </div>
      <div class="flex items-start">
        <div class="flex-shrink-0 mr-4 text-blue-500">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v3h8z" />
          </svg>
        </div>
        <div>
          <h3 class="text-xl font-semibold text-gray-800">Secure</h3>
          <p class="text-gray-600">You can find your property to simply and easy way</p>
        </div>
      </div>
    </div>
  </div>
</section>

  <section class="py-16 px-8 bg-gray-100">
    <div class="max-w-7xl mx-auto text-center mb-12">
      <h2 class="text-4xl font-bold text-gray-800">Property for Sale</h2>
      <p class="mt-4 text-lg text-gray-600 max-w-2xl mx-auto">
        Ortiz is one of the most popular real estate company all around USA. You can find your dream property or build property with us
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 max-w-7xl mx-auto">
      <!-- Property Card 1 -->
      <div class="bg-white rounded-lg shadow-lg overflow-hidden group">
        <div class="relative overflow-hidden">
          <img src={property1} alt="Modern House" class="w-full h-60 object-cover transform group-hover:scale-105 transition-transform duration-300" />
          <span class="absolute top-4 left-4 bg-blue-500 text-white text-xs font-semibold px-3 py-1 rounded-full">FOR RENT</span>
        </div>
        <div class="p-6">
          <h3 class="text-xl font-semibold text-gray-800">Mariyasa de Casel</h3>
          <p class="mt-2 text-gray-600 text-sm">22 First street, Chicago, USA 1200</p>
          <p class="text-gray-500 text-xs">Sqft, 3 Bed, 2 Bath, 1 Garage</p>
          <p class="mt-4 text-blue-600 font-bold text-lg">Price $1,25,000</p>
        </div>
      </div>

      <!-- Property Card 2 -->
      <div class="bg-white rounded-lg shadow-lg overflow-hidden group">
        <div class="relative overflow-hidden">
          <img src={property2} alt="White Modern House" class="w-full h-60 object-cover transform group-hover:scale-105 transition-transform duration-300" />
          <span class="absolute top-4 left-4 bg-blue-500 text-white text-xs font-semibold px-3 py-1 rounded-full">FOR SALE</span>
        </div>
        <div class="p-6">
          <h3 class="text-xl font-semibold text-gray-800">Rose de Alfanez</h3>
          <p class="mt-2 text-gray-600 text-sm">132 Future Street, Boston, USA 1600</p>
          <p class="text-gray-500 text-xs">Sqft, 4 Bed, 2 Bath, 2 Garage</p>
          <p class="mt-4 text-blue-600 font-bold text-lg">Price $70,250</p>
        </div>
      </div>

      <!-- Property Card 3 -->
      <div class="bg-white rounded-lg shadow-lg overflow-hidden group">
        <div class="relative overflow-hidden">
          <img src={property3} alt="Luxury Villa" class="w-full h-60 object-cover transform group-hover:scale-105 transition-transform duration-300" />
          <span class="absolute top-4 left-4 bg-blue-500 text-white text-xs font-semibold px-3 py-1 rounded-full">FOR RENT</span>
        </div>
        <div class="p-6">
          <h3 class="text-xl font-semibold text-gray-800">La Casanda Villa</h3>
          <p class="mt-2 text-gray-600 text-sm">1 DE Silicon Tower, Denver 1800</p>
          <p class="text-gray-500 text-xs">Sqft, 5 Bed, 4 Bath, 2 Garage</p>
          <p class="mt-4 text-blue-600 font-bold text-lg">Price $3,45,000</p>
        </div>
      </div>

      <!-- Property Card 4 -->
      <div class="bg-white rounded-lg shadow-lg overflow-hidden group">
        <div class="relative overflow-hidden">
          <img src={property4} alt="Modern Glass House" class="w-full h-60 object-cover transform group-hover:scale-105 transition-transform duration-300" />
          <span class="absolute top-4 left-4 bg-blue-500 text-white text-xs font-semibold px-3 py-1 rounded-full">FOR SALE</span>
        </div>
        <div class="p-6">
          <h3 class="text-xl font-semibold text-gray-800">Glass House Delux</h3>
          <p class="mt-2 text-gray-600 text-sm">24 North Street, California, USA</p>
          <p class="text-gray-500 text-xs">Sqft, 3 Bed, 2 Bath, 1 Garage</p>
          <p class="mt-4 text-blue-600 font-bold text-lg">Price $9,99,000</p>
        </div>
      </div>
    </div>
  </section>
    

<section class="py-16 px-8 bg-white">
  <div class="max-w-7xl mx-auto flex flex-col lg:flex-row items-center justify-between gap-12">
    <!-- Image Section -->
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

    <!-- Content Section -->
    <div class="w-full lg:w-1/2 mt-12 lg:mt-0 lg:pl-16 text-center lg:text-left">
      <h2 class="text-4xl font-bold text-gray-800 mb-6">We never compromise with quality work...</h2>
      <p class="text-gray-600 mb-8 max-w-md mx-auto lg:mx-0">Ortiz is one of the most popular real estate company all around USA. You can find your dream property or build property</p>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div class="flex items-start">
          <div class="flex-shrink-0 mr-4 text-blue-500">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M7 12l3-3 3 3 4-4M18 10V6M6 6h.01M12 6v4.062M16.5 10.5L12 15m0 0l-4.5 4.5" />
            </svg>
          </div>
          <div>
            <h3 class="text-xl font-semibold text-gray-800">Royel touch paint</h3>
            <p class="text-gray-600">Paint is the mirron of beautifull house build property with us</p>
          </div>
        </div>
        <div class="flex items-start">
          <div class="flex-shrink-0 mr-4 text-blue-500">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3 10v11h18V10M17 10V6a4 4 0 00-4-4H7a4 4 0 00-4 4v4h14z" />
            </svg>
          </div>
          <div>
            <h3 class="text-xl font-semibold text-gray-800">Fully Furnished</h3>
            <p class="text-gray-600">Well decorated and fully tuhed properties is available for all</p>
          </div>
        </div>
        <div class="flex items-start">
          <div class="flex-shrink-0 mr-4 text-blue-500">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 8c1.657 0 3 .895 3 2s-1.343 2-3 2-3-.895-3-2 1.343-2 3-2zM9 20h6a1 1 0 001-1v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2a1 1 0 001 1h4zm0-10a3 3 0 11-6 0 3 3 0 016 0z" />
            </svg>
          </div>
          <div>
            <h3 class="text-xl font-semibold text-gray-800">Latest Interior design</h3>
            <p class="text-gray-600">All interior are latest and luxus mirron of beauty dreem</p>
          </div>
        </div>
        <div class="flex items-start">
          <div class="flex-shrink-0 mr-4 text-blue-500">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m5.618-4.276a11.952 11.952 0 01-.001-3.004c-.161-.994-.7-1.785-1.444-2.316a4.958 4.958 0 00-2.327-1.425C14.07 2.008 13.045 2 12 2c-1.045 0-2.07.008-3.046.012a4.958 4.958 0 00-2.327 1.425C5.7 4.939 5.161 5.73 5 6.724a11.952 11.952 0 01-.001 3.004c-.161 1.01-.7 1.785-1.444 2.316a4.958 4.958 0 00-2.327 1.425C2.07 14.008 2 15.045 2 16c0 1.045.008 2.07.012 3.046a4.958 4.958 0 001.425 2.327c.531.744 1.322 1.283 2.316 1.444a11.952 11.952 0 013.004.001c.994.161 1.785.7 2.316 1.444a4.958 4.958 0 001.425 2.327c1.01.008 2.035 0 3.046 0a4.958 4.958 0 002.327-1.425c.744-.531 1.283-1.322 1.444-2.316a11.952 11.952 0 01.001-3.004c.161-1.01.7-1.785 1.444-2.316a4.958 4.958 0 002.327-1.425c.008-1.01 0-2.035 0-3.046a4.958 4.958 0 00-1.425-2.327c-.531-.744-1.322-1.283-2.316-1.444z" />
            </svg>
          </div>
          <div>
            <h3 class="text-xl font-semibold text-gray-800">Non stop security</h3>
            <p class="text-gray-600">Security in our property area is the main priority for our all</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section class=" flex justify-center items-center py-16 px-[5vw]">
  <img src={cta} alt="cta">
</section>


<section class="py-16 px-8 bg-gray-100">
  <div class="max-w-7xl mx-auto text-center mb-12">
    <h2 class="text-4xl font-bold text-gray-800">Our Agents</h2>
    <p class="mt-4 text-lg text-gray-600 max-w-2xl mx-auto">
      one of the most popular real estate company all around USA. You can find your dream property or build property with us
    </p>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 max-w-7xl mx-auto">
    <!-- Agent Card 1 -->
    <div class="bg-white rounded-lg shadow-lg overflow-hidden flex flex-col items-center p-6 text-center">
      <img src={agent1} alt="Jassica Thomson" class="w-40   object-cover mb-4" />
      <h3 class="text-xl font-semibold text-gray-800">Jassica Thomson</h3>
      <p class="text-gray-600">Real Estate Agent</p>
    </div>

    <!-- Agent Card 2 -->
    <div class="bg-white rounded-lg shadow-lg overflow-hidden flex flex-col items-center p-6 text-center">
      <img src={agent2} alt="Thomas Eilliams" class="w-40 object-cover mb-4" />
      <h3 class="text-xl font-semibold text-gray-800">Thomas Eilliams</h3>
      <p class="text-gray-600">Real Estate Agent</p>
    </div>

    <!-- Agent Card 3 -->
    <div class="bg-white rounded-lg shadow-lg overflow-hidden flex flex-col items-center p-6 text-center">
      <img src={agent3} alt="Sayana Sarlin" class="w-40 object-cover mb-4" />
      <h3 class="text-xl font-semibold text-gray-800">Sayana Sarlin</h3>
      <p class="text-gray-600">Real Estate Agent</p>
    </div>

    <!-- Agent Card 4 -->
    <div class="bg-white rounded-lg shadow-lg overflow-hidden flex flex-col items-center p-6 text-center">
      <img src={agent4} alt="Kuddus Boyati" class="w-40  object-cover mb-4" />
      <h3 class="text-xl font-semibold text-gray-800">Kuddus Boyati</h3>
      <p class="text-gray-600">Real Estate Agent</p>
    </div>
  </div>
</section>
