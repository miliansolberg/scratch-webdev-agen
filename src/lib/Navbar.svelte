<script>
    import svelteLogo from '../assets/svelte.svg'
</script>

<nav>
    <div>
        <a href="/"> 
          <img src={svelteLogo} class="logo svelte" alt="Svelte Logo" />
        </a>
      </div>
  <ul>
    <li><a href="/">Ferdigheter</a></li>
    <li><a href="/">Kunder</a></li>
    <li><a href="/">Om oss</a></li>
  </ul>
</nav>

<style>

* {
  margin: 0;
  padding: 0;
}

html {
    scroll-behavior: smooth;
}

.logo {
    height: 4em;
}

nav {
  height: 8vh;
  width: 100%;
  border-bottom: 1px solid #fff;
}

nav ul {
display: flex;
justify-content: space-between;
max-width: 30%;
margin: 0 auto;
}

nav ul li {
list-style-type: none;
font-weight: 600;
cursor: pointer;
margin-top: -4vh
}

nav ul li a {
color: #fff;
text-decoration: none;
opacity: 0.8;
}

nav ul li a:active {
    opacity: 1;
}

a {
    
}

.logo {
    height: 6vh;
    will-change: filter;
    transition: filter 300ms;
    padding-left: 6vh;
}


</style>