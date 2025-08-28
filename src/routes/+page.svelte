<script>
    import Hero from "$lib/components/Hero.svelte";
    import Slider from "$lib/components/Slider.svelte";
    import SvgAnimation from "$lib/components/SvgAnimation.svelte";
    import TxtHero from "$lib/components/TxtHero.svelte";
    import ScrollCardsContainer from "$lib/components/ScrollCardsContainer.svelte";
</script>

<Hero />
<TxtHero />
<SvgAnimation />

<!-- Scroll Cards Section -->
<ScrollCardsContainer />

<style>
    :global(body) {
        margin: 0;
        padding: 0;
        overflow-x: hidden;
    }
</style>
