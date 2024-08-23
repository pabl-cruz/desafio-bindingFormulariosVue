<script>
    export default{
        name: "Card",
        data(){
            return{
                tarjeta: {
                    titulo: '',
                    chip: '',
                    numero: '',
                    fechaExp: '',
                    propietario: '',
                    tipoTarjeta: '',
                }
        }
    }
}
</script>

<template>
    <form>
        <div>
          <label>Título de la tarjeta: </label>
          <input type="text" v-model="tarjeta.titulo" placeholder="Ingrese tipo de tarjeta"/>
        </div>

        <div>
          <label>Chip SRC: </label>
          <input type="text" v-model="tarjeta.chip" placeholder="Ruta del chip, como /chip.png"/>
        </div>

        <div>
          <label>Número: </label>
          <input type="text" v-model="tarjeta.numero" placeholder="000 000 000 000"/>
        </div>

        <div>
          <label>Fecha de expiración: </label>
          <input type="text" v-model="tarjeta.fechaExp" placeholder="00/00"/>
        </div>

        <div>
          <label>Propietario: </label>
          <input type="text" v-model="tarjeta.propietario" placeholder="Ingrese el nombre del propietario"/>
        </div>

        <div>
          <label>Tipo de tarjeta SRC: </label>
          <input type="text" v-model="tarjeta.tipoTarjeta" placeholder="Ruta de logo de tarjeta, como /visa.png"/>
        </div>
      </form>
      
      <div class="carnet">
        <h3>{{ tarjeta.titulo }}</h3>
        <img width="40" :src="tarjeta.chip" alt="chip" />
        <div>
          <h2>{{ tarjeta.numero }}</h2>
          <span>Fecha Exp: <b>{{ tarjeta.fechaExp }}</b></span>
        </div>
        <footer>
          <span>{{ tarjeta.propietario }}</span>
          <img :src="tarjeta.tipoTarjeta" width="60" />
        </footer>
      </div>
</template>

<style scoped>
form {
        padding: 18px;
        border-radius: 20px;
        border: ridge 1px;
        box-shadow: 1px 1px 1px 1px gray;
        font-weight: bold;
        display: flex;
        flex-direction: column;
        gap: 15px;
        justify-content: center;
      }

      form div {
        display: grid;
        grid-template-columns: 100px 200px;
        align-items: center;
        gap: 5px;
      }

      form div label {
        text-align: right;
      }

      .carnet {
        width: 400px;
        height: 230px;
        background: #1c1a1e;
        color: white;
        border-radius: 20px;
        padding: 20px;
        box-shadow: 0px 0px 10px 2px black;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
      }

</style>
