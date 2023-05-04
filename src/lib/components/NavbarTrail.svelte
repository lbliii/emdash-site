<script>
    import { scrollY } from '$lib/stores';

    let scrollTransform = 0
    $: y = $scrollY 
    $: scrollShowcaseItems(y)

    function scrollShowcaseItems(y){
        scrollTransform = y / 10

        console.log(scrollTransform)
    }
</script>

<button type="button" class="btn btn-sm rounded-3xl variant-ghost-tertiary px-20 border-b-4 border-tertiary-700 font-black {y > 1200 ? 'hidden' :''}">Contact</button>