<script>
  import Timer from "./Timer.svelte";
  import HowTo from "./HowTo.svelte";
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color:darkslategray;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <h1>Handwashing App</h1>
  <Timer />
  <HowTo />
  <h6>
    <a href="https://www.who.int/gpsc/media/how_to_handwash_lge.gif">
      Picture Source
    </a>
  </h6>

</main>
