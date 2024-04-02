<script>
  let numbers = [10, 25, 33, 62, 75, 100];
  
  function range(n) {
    return Array.from({length: n}, (_, i) => i + 1);
  }
</script>

<!-- Título fuera del contenedor de monedas para asegurar su posición en la parte superior -->
<h1 id='titulo'>Representación de Magnitudes con Monedas</h1>

<div class="monedas-container">
  {#each numbers as number}
  <div class="moneda-wrapper">
    {#each range(number) as _, index}
    <img class="moneda" src="./images/moneeda.png" alt="">
    {/each}
    <h2>{number}</h2>
  </div>
  {/each}
</div>

<style>
  #titulo {
    font-family: 'Helvetica';
    font-size: 30px;
    text-align: center; /* Alinea el texto del título en el centro */
    padding: -10px; /* Reduce el padding para acercar el título al borde superior */
    margin-top: 0; /* Se mantiene el margen superior reducido */
    margin-bottom: 10px; /* Reduce el espacio entre el título y los contenedores de monedas */
  }
  .moneda-wrapper  {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 5px; /* Reduce el margen para acercar los contenedores de monedas entre sí y hacia arriba */
    margin-top: -20;
  }
  .moneda-wrapper h2{
    font-family: Arial;
    font-size: 35px;  
  }
  .monedas-container {
    display: flex;
    flex-direction: row;
    align-items: flex-end;
    justify-content: center;
    flex-wrap: wrap;
    padding: 5px; /* Se mantiene el padding, pero se puede ajustar si se desea reducir el espacio aún más */
    margin-top: -10px; /* Nuevo: Reduce el espacio en la parte superior del contenedor principal */
  }
  .moneda {
    width: 30px;
    height: 30px;
    margin: 2px 0;
    margin-bottom: -25px; /* Ajuste para la sobreposición de las monedas */
  }

  
</style>
