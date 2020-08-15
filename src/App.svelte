<script>
  import Combine from "./components/Combine.svelte";
  import Spread from "./components/Spread.svelte";
</script>

<style>
  main,
  footer {
    /* padding: 1em; */
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    font-size: 3em;
    font-weight: 300;
  }
  h1 span {
    font-weight: 500;
  }
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>

  <header>
    <h1>
      Welcome to the
      <span>Emoji Factory</span>
    </h1>
    <p>Here you can play with emojis and discover how they're built 🔥</p>
    <p>Play around and find secrets 🔭</p>
  </header>

  <h3>Combine simple emojis into more complex ones 🧩</h3>
  <Spread />

  <h3>Break emojis into their components 🧨</h3>
  <Combine />

</main>

<footer>
  <h4>
    By
    <a href="https://github.com/moreirathomas">moreirathomas</a>
  </h4>
</footer>
