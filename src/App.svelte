<script>
  import logo from './assets/svelte.png'
  import Range from './lib/Range.svelte'
  import Exercises from './lib/Exercises.svelte'
  Range.value = 3;
</script>

<main>
  <h1>Ejercicios Algrebra</h1>

  <label for="basic-range">Dificultad</label>
  <Range on:change={(e) => Exercises.value = Range.value} />
  <Exercises />
  <p>
    Encuentra ejercicios de todo tipos en esta pagina web!
  </p>
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 1rem auto;
    line-height: 1.35;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
</style>
