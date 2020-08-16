<script>
  import Combine from "./components/logic/Combine.svelte";
  import Spread from "./components/logic/Spread.svelte";
  import ThemeToggle from "./components/logic/ThemeToggle.svelte";
</script>

<style>
  main,
  footer {
    max-width: 240px;
    margin: 0 auto;
  }
  footer {
    min-width: 240px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  h1 {
    color: var(--accent-color);
    font-size: 3em;
    font-weight: 300;
  }
  h1 span {
    font-weight: 500;
    transition: color 0.15s;
  }
  h1 span:hover {
    color: var(--action-color);
  }
  /* responsive layout */
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }

  /* color theme */
  :global(body) {
    background-color: var(--light-background);
    color: var(--light-color);
    transition: background-color 0.3s;
  }
  :global(body.dark-mode) {
    background-color: var(--dark-background);
    color: var(--dark-color);
  }
</style>

<main>
  <header>
    <h1>
      Welcome to the
      <span>Emoji Factory</span>
    </h1>
    <p>Here discover how emojis are built 🧱🔧</p>
    <p>Play around and find secrets 🔎</p>
  </header>

  <section>
    <h3>Break an emoji into its components 🧨</h3>
    <Spread />

    <h3>Combine simple emojis into more complex ones 🧩</h3>
    <Combine />
  </section>
</main>

<footer>
  <h4>
    By
    <a href="https://github.com/moreirathomas">moreirathomas</a>
    ✌️
  </h4>
  <ThemeToggle />
</footer>
