<script>
  export let selectedWheels = "17 inches";
  const wheels = ["17 inches", "18 inches"];
</script>

<div>
  <h2>Select Wheels</h2>
  {#each wheels as wheel}
    <label>
      <input type="radio" bind:group={selectedWheels} value={wheel} />
      {wheel}
    </label>
  {/each}
</div>

<style>
  div {
    margin-bottom: 1rem;
  }

  label {
    display: block;
    margin: 0.25rem 0;
  }
</style>
