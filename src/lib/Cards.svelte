<script>
  let cards;

  const handleOnMouseMove = e => {
    const { currentTarget: target } = e;
  
    const rect = target.getBoundingClientRect(),
      x = e.clientX - rect.left,
      y = e.clientY - rect.top;
  
    target.style.setProperty("--mouse-x", `${x}px`);
    target.style.setProperty("--mouse-y", `${y}px`);
  }

  const handleCardsOnMouseMove = e => {
    for (const card of Array.from(cards)) {
      const rect = card.getBoundingClientRect(),
            x = e.clientX - rect.left,
            y = e.clientY - rect.top;
  
      card.style.setProperty("--mouse-x", `${x}px`);
      card.style.setProperty("--mouse-y", `${y}px`);
    }
  };

  window.addEventListener("DOMContentLoaded", () => {
    cards = document.querySelectorAll(".card");
    for (const card of Array.from(cards)) {
      card.onmousemove = handleOnMouseMove;
    }
    document.getElementById("cards").onmousemove = handleCardsOnMouseMove;
  });
</script>
  
  

<div id="cards">
    <div class="card">
      <div class="card-content">
        Vi er eksperter på moderne webutvikling
        <img src="https://www.transparentpng.com/thumb/seo-png/seo-free-download-4.png" alt="">

    </div>
    </div>
    <div class="card">
      <div class="card-content">Vi lover gode SEO-løsninger
        <img src="https://www.transparentpng.com/thumb/seo-png/seo-free-download-4.png" alt="">
      </div>
    </div>
    <div class="card">
      <div class="card-content">Vi bygger nordens raskeste nettsider
        <img src="https://www.transparentpng.com/thumb/seo-png/seo-free-download-4.png" alt="">

      </div>
    </div>
  </div>

  <style>
    :root {
    --bg-color: rgb(20, 20, 20);
    --card-color: rgb(46, 41, 71);
  }
  
  #cards {
    display: flex;
    margin: 60px auto;
    flex-wrap: wrap;
    gap: 8px;  
    max-width: 916px;
    width: calc(100% - 20px);
  }
  
  #cards:hover > .card::after {
    opacity: 1;
  }
  
  .card {
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 10px;
    cursor: pointer;
    display: flex;
    height: 260px;
    flex-direction: column;
    position: relative;
    width: 300px;  
  }
  
  .card:hover::before {
    opacity: 1;
  }
  
  .card::before,
  .card::after {
    border-radius: inherit;
    content: "";
    height: 100%;
    left: 0px;
    opacity: 0;
    position: absolute;
    top: 0px;
    transition: opacity 500ms;
    width: 100%;
  }
  
  .card::before {
    background: radial-gradient(
      800px circle at var(--mouse-x) var(--mouse-y), 
      rgba(255, 255, 255, 0.06),
      transparent 40%
    );
    z-index: 3;
  }
  
  .card::after {  
    background: radial-gradient(
      600px circle at var(--mouse-x) var(--mouse-y), 
      rgba(255, 255, 255, 0.4),
      transparent 40%
    );
    z-index: 1;
  }
  
  .card > .card-content {
    background-color: var(--card-color);
    border-radius: inherit;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    inset: 1px;
    padding: 10px;
    position: absolute;
    z-index: 2;
    text-align: center;
    font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;

}

img {
    height: 10em;
    width: 10em;
    margin: 0px auto;
    vertical-align: middle;
}
  </style>
