<script>
    import { scrollY } from '$lib/stores';

    let scrollTransform = 0
    $: y = $scrollY 
    $: scrollShowcaseItems(y)

    function scrollShowcaseItems(y){
        scrollTransform = y / 10
    }
</script>

<div class="emdash text-md {y > 1550 ? 'hidden' :''} -mr-4">
{#if y > 100}
     =
    {/if}
    {#if y > 300}
    =
    {/if}
    {#if y > 500}
    =
    {/if}
    {#if y > 700}
    =
    {/if}
    {#if y > 900}
    =
    {/if}
    {#if y > 1100}
    =
{/if}
</div>

<a class="emdash text-md {y > 1550 ? 'hidden' :''} hover:text-primary-500" alt="" href="/contact">
    ▶︎ Contact
</a>