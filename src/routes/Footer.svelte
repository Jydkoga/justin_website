<footer>
  <img
    class="footer-image"
    src="src/photos/instagram.png"
    alt="New York City"
    width="100%"
    height="auto"
    style="margin-top: 20px"
    on:click={() => {
      window.open("https://www.instagram.com/photosbykoga/", "_blank");
    }}
  />
</footer>

<style>
  footer {
    display: flex;
    justify-content: flex-end;
    padding-left: 73%;
  }
  .footer-image:hover {
    cursor: pointer;
  }
</style>
