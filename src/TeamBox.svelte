<script>
  export let team = "";
  export let point = 2;
  function addPoint() {
    point++;
  }
  function minusPoint() {
    point--;
  }
  function resetGame() {
    point = 20;
  }
</script>

<div class="col-6 p-5" style="border: 2px dashed {team};">
  <h3 style="color:{team}">Team {team}: {point}</h3>
  <button on:click={addPoint} class="bg-success">+</button>
  <button on:click={minusPoint} class="bg-danger">-</button>
</div>
<!-- 
{#if point === 0}
  <h3>{team} Won</h3>
  <button on:click={resetGame}>New Game</button>
{/if} -->
