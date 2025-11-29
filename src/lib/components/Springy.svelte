<script>
    import { spring } from 'svelte/motion';  // Import spring for the animation
    import { cubicOut } from 'svelte/easing'; // Import easing for more natural motion
  
    let isVisible = false;
    
    // Define the spring animation for the X and Y positions
    const springX = spring(0, { stiffness: 0.1, damping: 0.25 });  // Horizontal spring (X axis)
    const springY = spring(0, { stiffness: 0.1, damping: 0.25 });  // Vertical spring (Y axis)
    
    function toggleBox() {
      // Toggle the visibility and update the spring's target positions
      isVisible = !isVisible;
      springX.set(isVisible ? 200 : 0); // Move the box horizontally
      springY.set(isVisible ? 150 : 0); // Move the box vertically
    }
  </script>
  
  <div class="container mx-auto mt-10 text-center">
    <button 
      class="px-6 py-3 bg-indigo-500 text-white rounded-lg hover:bg-indigo-700 transition-all"
      on:click={toggleBox}
    >
      Toggle Spring Animation
    </button>
  
    <!-- The Box with spring motion -->
    <div
      class="mt-8"
      style="transform: translate({$springX}px, {$springY}px);"
    >
      <p class="text-xl font-semibold">Spring Motion Box</p>
    </div>
  </div>
  
  <style>
    /* Optional Custom Styles */
    .container {
      max-width: 600px;
    }
  </style>
  