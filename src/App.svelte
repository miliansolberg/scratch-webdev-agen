<script>
  import Navbar from './lib/Navbar.svelte';
  import Cards from './lib/Cards.svelte';
  import Testimonials from './lib/Testimonials.svelte';
</script>

<main>

<div class="navbar__container">
  <div class="navbar">
    <Navbar />
n  </div>
</div>

<div id="header__container">
  <h1>Nordens største Webutvikler-byrå</h1>

  <h2>Vi bygger moderne webløsninger for deg.</h2>
</div>

<div class="cards__container">
  <div class="cards">
  <Cards />
</div>
</div>


<div class="testimonials__container">
  <div class="testimonials">
    <Testimonials />
  </div>
</div>

</main>

<style>


  h1 {
    text-align: center;
  }

  #header__container {
    text-align: center;
  }

  .cards__container {
    align-items: center;
    margin: 0px auto;
  }

  .cards {
    align-items: center;
    justify-content: center;
    margin: 0px auto;
  }

</style>
