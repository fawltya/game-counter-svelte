<script>
  import TeamBox from "./TeamBox.svelte";
  let redTeam = 2;
  let blueTeam = 2;
  function resetGame() {
    redTeam = 2;
    blueTeam = 2;
  }
  let result = "";
</script>

<container class="container-xl justify-center">
  <h1>MTG Counter App</h1>
  <div class="d-flex flex-row justify-content-center my-5 row">
    <TeamBox team="red" bind:point={redTeam} />
    <TeamBox team="blue" bind:point={blueTeam} />
  </div>
  {#if redTeam === 0}
    <h3>Red Won</h3>
    <button on:click={resetGame}>New Game</button>
  {:else if blueTeam === 0}
    <h3>Blue Won</h3>
    <button on:click={resetGame}>New Game</button>
  {/if}
  {#if redTeam > 0 && blueTeam > 0}
    <button on:click={resetGame}>Reset Game</button>
  {/if}
</container>
