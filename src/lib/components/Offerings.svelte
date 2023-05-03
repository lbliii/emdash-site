<script lang="ts">

    let rate = 4993
    function calcRate(rate, discount) {
        return rate - (rate * discount)
    }
    function calcSavings(rate, discount) {
        return rate * discount
    }

let offerings = [
    {
        title: "Monthly",
        link: "/",
        description: "Our most flexible plan; pay as you go & cancel at any time.",
        cta: "Subscribe",
        cta_color: "success",
        rate: calcRate(rate, 0),
        savings: calcSavings(rate, 0)
    },
     {
        title: "Quarterly",
        link: "/",
        description: "<b>Save 10%</b>. Great for large projects (~3-6 sprints).",
        cta: "Subscribe",
        cta_color: "primary",
        rate: calcRate(rate, .10),
        savings: calcSavings(rate, .10)
    },
     {
        title: "Yearly",
        link: "/",
        description: "<b>Save 20%.</b> Supercharge your design output without the cost of a full-time designer.",
        cta: "Subscribe",
        cta_color: "tertiary",
        rate: calcRate(rate, .20),
        savings: calcSavings(rate, .20)
    },
     {
        title: "Book a Call",
        link: "/",
        description: "Learn more about how Emdash works and how we can help you.",
        cta: "Book",
        cta_color: "primary"
    }

]


</script>


<div class="flex flex-col lg:flex-row ">
    {#each offerings as {title, link, description, cta, cta_color, rate}, index}
        <a class="card card-hover flex flex-col variant-ghost-surface m-2 lg:-mt-28 lg:w-3/12" href="{link}">
        <div class="card-header flex justify-center p-4">
            <h2>{title}</h2>
        </div>
        <div class="card-body p-4">
            <div class="text-lg">{@html description} </div>
            
        </div>
        <div class="card-footer flex flex-col flex-grow justify-end p-4 space-y-4">
            <div class="flex flex-row justify-center  items-end space-x-1">
                {#if rate}
                <div class="text-4xl font-black mt-4">
                    {rate}
                </div>
                 <div>
                    /m
                </div>
                {/if}
            </div>
            <button type="button" class="btn border-b-4 border-{cta_color}-700 variant-filled-{cta_color} rounded-none font-black"> {cta}</button>
        </div>
        </a>
    {/each}
</div>