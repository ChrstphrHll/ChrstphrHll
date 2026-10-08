<script lang="ts">
  import me from "$lib/assets/me.png"

  let colors = [
    
  ]

  function getRadius(color: String) {
    const radius = "8px"
    if (color === "red") {
      return `${radius} 0px 0px ${radius}`
    } else if (color === "purple") {
      return `0px ${radius} ${radius} 0px`
    }
    return "0px"
  }
</script>


<h1 class="lato-black">ChrstphrHll </h1>
<img src={me} alt="christopher as a stick figure sitting at a laptop">
<p>That's me! I make cool stuff and put it on the internet.</p>

<ul>
  <li>
    <a href="https://swu-draft.pages.dev" target="_blank">Starwars Unlimited Multiplayer Draft Simulator</a>
  </li>
  <li>
    <a href="https://pitazines.pages.dev/" target="_blank">Pita Zines</a> a gift I made for my partner
  </li>
  <li>
    <a href="https://chrstphrhll.itch.io/showponystudios" target="_blank">Show Pony Studio</a> a two day game jam game
  </li>
  <li>
    <a href="https://chrstphrhll.itch.io/buylowselleyes" target="_blank">Buy Low; Sell Eyes</a> a four day game jam game
  </li>
  <li>
    <a href="https://chrstphrhll.itch.io/trust-no-one" target="_blank">Trust No. 1</a> another game jam game
  </li>
  <li>
    <a href="https://chrstphrhll.github.io/DukeBotWBingo/" target="_blank">Duke Breath of the Wild Bingo</a>
  </li>
  <li>
    <a href="https://democratichelphub.org/" target="_blank">Durham Help Hub</a> an info website for a mutual aid initiative in Durham
  </li>
  <li>
    <a href="https://chrstphrhll.pages.dev/" target="_blank">ChrstphrHll</a> a portfolio website with no secrets or puzzles; its just normal
  </li>
  <li>
    <a href="https://compcon.app/" target="_blank">COMP/CON</a> a <i>Lancer</i> RGP companion app that I've made community contributions to
  </li>
</ul>

<div style="display: flex; min-width: 100%; margin-block: 16px;">
{#each ["red", "orange", "yellow", "green", "blue", "purple"] as color}
  <div style="height:8px; width: 100%; border-radius: {getRadius(color)}; background-color: var(--{color});"></div>
{/each}
</div>

<p>And here's a micro controller I taught to play <i>Celeste</i> really really fast with a friend</p>
<video controls>
  <source src="/celeste_tas.mov">
</video>


<style>
  @import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap');


  /* Pallet from https://lospec.com/palette-list/fantasy */
  :global(:root) {
    --red: #ca5954;
    --orange: #e39347;
    --yellow: #e8c65b;
    --green: #557d55;
    --blue: #668da9;
    --purple: #7c6da2;
    
    --dark-red: #a94949;
    --dark-orange: #e56f4b;
    --dark-yellow: #eeb551;
    --dark-green: #446350;
    --dark-blue: #5c699f;
    --dark-purple: #5a5888;
  }

  h1 {
    font-family: "Lato", sans-serif;
    font-weight: 900;
    font-style: normal;
  }

  p, ul {
    font-family: "Lato", sans-serif;
  }

  a {
    color: var(--red);
  }

  a:visited {
    color: var(--dark-red);
  }

  :global(body) {
    background-color: antiquewhite;
    color: rgb(101, 15, 15);
  }
  video {
    margin-inline: auto;
    width: min(500px, 90vw)
  }

  @media (width >= 500px) {
    img {
      float: right;
      margin-top: -16px;
    }
  }
</style>