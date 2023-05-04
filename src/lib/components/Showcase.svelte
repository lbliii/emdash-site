<script>
    import { scrollY } from '$lib/stores';

    const showcaseItems = [
        {
            title: "title",
            link: "/",
            image: "https://images.pexels.com/photos/16128360/pexels-photo-16128360.jpeg",
            description: "",
        }, 
        {
            title: "title",
            link: "/",
            image: "https://images.pexels.com/photos/16128360/pexels-photo-16128360.jpeg",
            description: "",
        }, 
        {
            title: "title",
            link: "/",
            image: "https://images.pexels.com/photos/16128360/pexels-photo-16128360.jpeg",
            description: "",
        }, 
        {
            title: "title",
            link: "/",
            image: "https://images.pexels.com/photos/16128360/pexels-photo-16128360.jpeg",
            description: "",
        }, 
        {
            title: "title",
            link: "/",
            image: "https://images.pexels.com/photos/16128360/pexels-photo-16128360.jpeg",
            description: "",
        }, 
        {
            title: "title",
            link: "/",
            image: "https://images.pexels.com/photos/16128360/pexels-photo-16128360.jpeg",
            description: "",
        }, 
        
    ]

    let scrollTransform = 0
    $: y = $scrollY - 2000
    $: scrollShowcaseItems(y)

    function scrollShowcaseItems(y){
        scrollTransform = y / 10
    }
    
</script>

<style>
    .item:hover {
        transform: scale(1.3);
        transition: transform 0.3s ease;

    }
</style>

<div id="showcase-container" class="container max-w-lg">
  <div id="showcase" class="flex flex-row" style="transform: translateX({scrollTransform}px)">
    {#each showcaseItems as {title, link, image, description}, index}
      <div id="showcase-{index}" class="flex-shrink-0 min-w-min variant-ghost-tertiary block w-48 h-64 lg:w-72 lg:h-96 bg-contain rounded-md mx-4 item" 
      style="background-image: url('{image}');" on:mouseenter={() => scaleItemIn(event.target)}
      on:mouseleave={() => scaleItemOut(event.target)}>
      </div>
    {/each}
  </div>
</div>

