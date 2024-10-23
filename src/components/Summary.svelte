<script>
  export let selectedModel;
  export let selectedColor;
  export let selectedWheels;
  export let totalPrice;
</script>

<div>
  <h2>Summary</h2>
  <p><strong>Model:</strong> {selectedModel}</p>
  <p><strong>Color:</strong> {selectedColor}</p>
  <p><strong>Wheels:</strong> {selectedWheels}</p>
  <p><strong>Total Price:</strong> {totalPrice} zł</p>
</div>

<style>
  div {
    border-top: 1px solid #ccc;
    padding-top: 1rem;
    margin-top: 1rem;
  }

  p {
    margin: 0.5rem 0;
  }

  h2 {
    margin-bottom: 1rem;
  }
</style>
