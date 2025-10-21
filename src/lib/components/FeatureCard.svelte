<script lang="ts">
  export let title: string;
  export let text: string;
  export let icon: string;
</script>

<div class="flex items-start">
  <div class="flex-shrink-0 mr-4 text-blue-500">
    <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
      <path stroke-linecap="round" stroke-linejoin="round" d={icon}/>
    </svg>
  </div>
  <div>
    <h3 class="text-xl font-semibold text-gray-800">{title}</h3>
    <p class="text-gray-600">{text}</p>
  </div>
</div>
