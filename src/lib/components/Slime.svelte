<script>
    import { scrollY } from '$lib/stores';

    let scrollTransform = 0

    let slime1rate, slime2rate, slime3rate, slime4rate, slime5rate = 0

    $: y = $scrollY
    $: scrollShowcaseItems(y)

    function scrollShowcaseItems(y){
        scrollTransform = y

        slime1rate = (scrollTransform * .02)
        slime2rate = (scrollTransform * .07)
        slime3rate = (scrollTransform * .04)
        slime4rate = (scrollTransform * .12)
        slime5rate = (scrollTransform * .08)

    }
</script>

<div class="flex flex-row mb-4">
    <div id="slime-1" class="bg-secondary-800 w-1/5" style="height: {slime1rate}px"></div>
    <div id="slime-2" class="bg-secondary-800 w-1/5" style="height: {slime2rate}px"></div>
    <div id="slime-3" class="bg-secondary-800 w-1/5" style="height: {slime3rate}px"></div>
    <div id="slime-4" class="bg-secondary-800 w-1/5" style="height: {slime4rate}px"></div>
    <div id="slime-5" class="bg-secondary-800 w-1/5" style="height: {slime5rate}px"></div>
</div>
