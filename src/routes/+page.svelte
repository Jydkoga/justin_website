<script>
  import Footer from "./Footer.svelte";
  import Navbar from "./Navbar.svelte";
</script>

<main>
  <h1>Justin Koga: Photographs and Works on Paper</h1>
  <h2>Photographer.Creative.Adventurer</h2>
  <Navbar class="nav" />
  <img
    class="home-image"
    src="src/photos/justin_skiing_photo.jpg"
    alt="New York City"
    width="100%"
    height="auto"
    style="margin-top: 20px"
  />
  <Footer />
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500&display=swap");

  :global(*) {
    font-family: "Montserrat", sans-serif;
  }
  h1 {
    text-align: center;
    padding: 50px 0 0 0;
  }
  h2 {
    text-align: center;
    font-weight: normal;
  }
  :global(.navbar) {
    justify-content: center;
    padding-top: 20px;
  }
  img {
    max-width: 75%;
  }

  main {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>
