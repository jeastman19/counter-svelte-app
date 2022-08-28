<script lang="ts">
  let counter: number = 0;

  const modifyCounter = (value: number): number => (counter += value);
</script>

<main>
  <h1>Counter App</h1>

  <hr />

  <h2 class={counter < 0 ? "negative" : "positive"}>Counter: {counter}</h2>

  <button class="btn add" on:click={() => modifyCounter(1)}>+1</button>
  <button class="btn diminish" on:click={() => modifyCounter(-1)}>-1</button>
  <button class="btn reset" on:click={() => modifyCounter(-counter)}
    >Reset</button
  >
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  h2 {
    font-size: 2rem;
  }

  .btn {
    font-size: 2rem;
    margin: 0 0.4rem;
    border-radius: 9px;
    width: 110px;
  }

  .btn:hover {
    cursor: pointer;
  }

  .add {
    background-color: #26b231;
  }

  .add:active {
    background-color: #128d12;
  }

  .diminish {
    background-color: #3a9aea;
  }

  .diminish:active {
    background-color: #165486;
  }

  .reset {
    background-color: tomato;
  }

  .reset:active {
    background-color: rgb(128, 35, 19);
  }

  .negative {
    color: red;
  }

  .positive {
    color: blue;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
