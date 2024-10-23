<script>
  import CarModel from './components/CarModel.svelte';
  import CarColor from './components/CarColor.svelte';
  import CarWheels from './components/CarWheels.svelte';
  import Summary from './components/Summary.svelte';
  
  let selectedModel = "Sedan";
  let selectedColor = "White";
  let selectedWheels = "17 inches";
  
  const basePrice = {
    "Sedan": 100000,
    "SUV": 125000,
    "Coupe": 110000
  };
  
  const colorPrice = {
    "White": 0,
    "Red": 100,
    "Blue": 1200,
    "Black": 1500
  };
  
  $: totalPrice = basePrice[selectedModel] + (selectedWheels === "18 inches" ? 1000 : 0) + (colorPrice[selectedColor] || 0); ;
  $: formattedPrice = totalPrice.toLocaleString('pl-PL');
</script>

<main>
  <h1>Car Configurator</h1>
  
  <CarModel bind:selectedModel />
  <CarColor bind:selectedColor />
  <CarWheels bind:selectedWheels />
  <Summary {selectedModel} {selectedColor} {selectedWheels} totalPrice={formattedPrice} />
</main>

<style>
  main {
    font-family: Arial, sans-serif;
    padding: 2rem;
    max-width: 800px;
    margin: 0 auto;
  }

  h1 {
    text-align: center;
    margin-bottom: 2rem;
  }
</style>
