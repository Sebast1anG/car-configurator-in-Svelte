<script>
  export let selectedModel = "Sedan";
  const models = ["Sedan", "SUV", "Coupe"];
</script>

<div>
  <h2>Select Model</h2>
  {#each models as model}
    <label>
      <input type="radio" bind:group={selectedModel} value={model} />
      {model}
    </label>
  {/each}
</div>

<style>
  div {
    margin-bottom: 1rem;
  }
  
  h2 {
    margin-bottom: 0.5rem;
  }

  label {
    display: block;
    margin: 0.25rem 0;
  }
</style>
