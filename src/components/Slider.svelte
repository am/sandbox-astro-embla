<script>
  import emblaCarouselSvelte from "embla-carousel-svelte";

  let emblaApi;
  let options = { loop: false };

  function onInit(event) {
    emblaApi = event.detail;
    console.log(emblaApi.slideNodes()); // Access API
  }
</script>

<div class="embla" use:emblaCarouselSvelte={{ options }} onemblaInit={onInit}>
  <div class="embla__container">
    <div class="embla__slide">Slide 1</div>
    <div class="embla__slide">Slide 2</div>
    <div class="embla__slide">Slide 3</div>
  </div>
</div>

<style>
  .embla {
    overflow: hidden;
  }
  .embla__container {
    display: flex;
  }
  .embla__slide {
    flex: 0 0 100%;
    min-width: 200px;
    min-height: 200px;
    background-color: black;
    color: white;
  }
</style>
