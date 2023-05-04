<script>

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
 
</script>

<style>
    .item:hover {
        transform: scale(1.3);
    }
</style>

<div id="showcase-container" class="container ">
  <div id="showcase" class="flex flex-row">
    {#each showcaseItems as {title, link, image, description}}
      <div class="flex-shrink-0 min-w-min variant-ghost-surface block w-48 h-64 lg:w-72 lg:h-96 bg-contain rounded-md mx-4 item" style="background-image: url('{image}')">
      </div>
    {/each}
  </div>
</div>

