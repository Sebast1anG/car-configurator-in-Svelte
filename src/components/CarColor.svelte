<script>
  export let selectedColor = "Red";
  const colors = ["Red", "Blue", "Black", "White"];
</script>

<div>
  <h2>Select Color</h2>
  {#each colors as color}
    <label>
      <input type="radio" bind:group={selectedColor} value={color} />
      {color}
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
