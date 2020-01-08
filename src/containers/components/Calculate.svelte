<script>
  let altura = '';
  let peso = '';
  let resultado = '';

  const calculate = () => {
    resultado = peso / (altura * 2);
  }
</script>

<form class="form" on:submit|preventDefault={calculate}>
    <label for="altura">Altura</label>
    <input bind:value={altura} id="altura" class="form__field" type="text">

    <label for="peso">Peso</label>
    <input bind:value={peso} id="peso" class="form__field" type="text">

    <button class="form__button">Calcular</button>

    <label for="resultado">Resultado</label>
    <input bind:value={resultado} id="resultado" class="form__field" type="text">
</form>

<style>
  .form {
    width: 500px;
    height: 500px;
    background: #eee;
    box-sizing: border-box;
    padding: 20px;
    display: flex;
    flex-direction: column;
  }

  .form__button {
    cursor: pointer;
  }
</style>