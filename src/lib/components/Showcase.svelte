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

    let showcaseContainer

    const handleScroll = () => {
        const scrollTop = showcaseContainer.scrollTop
        const delta = scrollTop - (showcaseContainer.dataset.prevScrollTop || 0)
        showcaseContainer.scrollLeft += delta
        showcaseContainer.dataset.prevScrollTop = scrollTop
    }
   
</script>

<div id="showcase-container" class="container">
  <div id="showcase" class="flex flex-row overflow-x-auto">
    {#each showcaseItems as {title, link, image, description}}
      <div class="flex-shrink-0 min-w-min variant-ghost-surface block w-48 h-64 lg:w-72 lg:h-96 bg-contain rounded-md mx-4" style="background-image: url('{image}')">
      </div>
    {/each}
  </div>
</div>

