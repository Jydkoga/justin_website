<script>
  import { onMount } from "svelte";

  // State for each dropdown
  let isPhotographicOpen = false;
  let isEtcOpen = false;

  // Event handlers for Photographic Projects dropdown
  function togglePhotographic() {
    isPhotographicOpen = true;
  }

  function closePhotographic() {
    isPhotographicOpen = false;
  }

  // Event handlers for Etc dropdown
  function toggleEtc() {
    isEtcOpen = true;
  }

  function closeEtc() {
    isEtcOpen = false;
  }
</script>

<nav class="navbar">
  <ul>
    <li><a href="/">Home</a></li>
    <li
      class="dropdown"
      on:mouseenter={togglePhotographic}
      on:mouseleave={closePhotographic}
    >
      <span style="cursor: pointer;">Photographic Projects ▾</span>
      {#if isPhotographicOpen}
        <div class="dropdown-content">
          <a href="/newyorkcity">New York City</a>
          <a href="/portraits">Portraits</a>
          <a href="/family">Family</a>
        </div>
      {/if}
    </li>
    <li class="dropdown" on:mouseenter={toggleEtc} on:mouseleave={closeEtc}>
      <span style="cursor: pointer;">Epic Things ▾</span>
      {#if isEtcOpen}
        <div class="dropdown-content">
          <a href="/broadway_bomb">Broadway Bomb</a>
          <a href="/articles">Articles</a>
        </div>
      {/if}
    </li>
    <li><a href="/about">About & Contact</a></li>
  </ul>
</nav>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500&display=swap");
  :global(*) {
    font-family: "Montserrat", sans-serif;
  }
  :global(.navbar) {
    color: black;
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-weight: bold;
  }

  :global(a) {
    color: black;
    text-decoration: none;
  }

  :global(a:hover) {
    text-decoration: underline;
  }

  ul {
    list-style: none;
    display: flex;
    gap: 1rem;
    margin: 0;
    padding: 0;
  }

  .dropdown {
    position: relative;
  }

  .dropdown-content {
    position: absolute;
    top: 100%;
    left: 0;
    border: 1px solid #444;
    padding: 0.5rem 0;
    display: flex;
    flex-direction: column;
    z-index: 10;
    background-color: white;
  }

  .dropdown-content a {
    padding: 0.5rem 1rem;
  }

  .dropdown-content a:hover {
  }
</style>
