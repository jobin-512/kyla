<script lang="ts">
  // Optional: You can define quick links or popular posts as arrays if you want to dynamically render them
  const quickLinks = 
  [
    {title: "Services",
      href: "/services"
    }, 
    {title: "Properties",
      href: "/properties"
    }, 
    {title: "Livestock",
      href: "/livestock"
    }, 
    {title: "From Blog",
      href: "/blog"
    }, 
    {title: "Contact",
      href: "/contact"
    }
  ];
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
          <li><a href={link.href} class="hover:text-white cursor-pointer">{link.title}</a></li>
        {/each}
      </ul>
    </div>

    <!-- Contact Us -->
    <div>
      <h3 class="text-xl font-bold mb-4">Contact Us</h3>
      <p class="text-gray-300 text-sm mb-2"><strong>Address:</strong> 2439 Hwy 90 West, Suite 101, Castroville, TX 78009</p>
      <p class="text-gray-300 text-sm mb-2"><strong>Telephone:</strong> 1-210-416-0980</p>
      <p class="text-gray-300 text-sm mb-2"><strong>Email:</strong> kylaburell@gmail.com</p>
    </div>
  </div>

  <!-- Footer Bottom -->
  <div class="bg-[#1a92dc] text-white text-center py-4 mt-12">
    © 2025 Copyright Kylas Burell. All rights reserved.
  </div>
</footer>
