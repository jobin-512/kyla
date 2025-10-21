<script lang="ts">
  // Optional: You can define quick links or popular posts as arrays if you want to dynamically render them
  const quickLinks = ["Services", "Agent", "Properties", "Features", "From Blog", "Contact"];
  const popularPosts = [
    { title: "Duplex Villa Design", desc: "Lorem ipsum dolor sit amet, tur acinglit sed do eius" },
    { title: "Duplex Villa Design", desc: "Lorem ipsum dolor sit amet, tur acinglit sed do eius" }
  ];
</script>

<footer class="bg-[#0b3550] text-white relative pt-16">
  <div class="max-w-7xl mx-auto px-8 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 relative z-10">
    <!-- About -->
    <div>
      <h3 class="text-xl font-bold mb-4">About</h3>
      <p class="text-gray-300 mb-4 text-sm">
        Ortiz is the best and popular real estate to you how all this mistaoltcing pleasure and praising ained wasnad pain was prexplain
      </p>
    </div>

    <!-- Popular Post -->
    <div>
      <h3 class="text-xl font-bold mb-4">Popular Post</h3>
      {#each popularPosts as post}
        <div class="mb-4 text-sm">
          <p class="font-semibold">{post.title}</p>
          <p class="text-gray-300">{post.desc}</p>
        </div>
      {/each}
    </div>

    <!-- Quick Links -->
    <div>
      <h3 class="text-xl font-bold mb-4">Quick Link</h3>
      <ul class="text-gray-300 text-sm space-y-2">
        {#each quickLinks as link}
          <li class="hover:text-white cursor-pointer">{link}</li>
        {/each}
      </ul>
    </div>

    <!-- Contact Us -->
    <div>
      <h3 class="text-xl font-bold mb-4">Contact Us</h3>
      <p class="text-gray-300 text-sm mb-2"><strong>Address:</strong> 256, 1st AVE, Manchester, 125, North England</p>
      <p class="text-gray-300 text-sm mb-2"><strong>Telephone:</strong> +88 (012) 356 958 45</p>
      <p class="text-gray-300 text-sm mb-2"><strong>Email:</strong> info@example.com</p>
      <p class="text-gray-300 text-sm"><strong>Web:</strong> www.example.com</p>
    </div>
  </div>

  <!-- Footer Bottom -->
  <div class="bg-[#1a92dc] text-white text-center py-4 mt-12">
    © 2025 Copyright Kylas Burell. All rights reserved.
  </div>
</footer>
