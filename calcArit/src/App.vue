


// http://localhost:5173/

<script >

export default{
  data(){
    return{
      n1:'' ,
      n2:'',
      controlador: true,
      

      
    }
  },

  methods:{

    
    somar(){
  return this.n1 + this.n2
    },

    subtracao(){
      return this.n1 - this.n2
    },

    multiplicar(){
      return this.n1 * this.n2
    },

    dividir(){
      return this.n1 / this.n2
    },

  limpar(){
    return this.n2, this.n1 = ''
    
  },

  ativarOperacao(){
    this.controlador = !this.controlador
  }


    
    
  }

}


</script>

<template>  

<div id="app">


<h1>CALCULADORA SIMPLES</h1>

<!-- <div >Selecione: {{ selected }}</div>

<select v-model="selected">
  <option enable value="">Aritmetica</option>
  <option>somar</option>
  <option > subtrair</option>
  <option>multiplicar</option>
  <option>dividir</option> 

</select> -->


<label for="">I</label>
  <input :disabled="controlador" type="number" v-model.number="n1" placeholder="Valor 1">
  <label for=""> II</label>
  <input :disabled="controlador" type="number" v-model.number="n2" placeholder="Valor 2">
  <button class="ligar"@click="ativarOperacao()">Ligar</button>
  <button class="limparCampos" @click="limpar()">Apagar</button>
  <label id="instrucao">Passe o mause sobre o operador ! </label> <br>
  
  <hr> <br>

  <label > Somar </label>
<p>{{ somar() }}</p>
<hr> <br>

  <label > Subtração </label>
<p>{{ subtracao() }}</p>
<hr> <br>


  <label > Multiplicar </label>
  <p>{{ multiplicar() }}</p>
  <hr> <br>


  <label > Divisão </label>
  <p>{{ dividir() }}</p>
  <hr> <br>

</div>
</template>

<style scoped>


input{
  width: 160px;
  height: 30px;
  margin-left: 10px;
  text-align: center;
  font-size: 20px;
  font-family: Arial, Helvetica, sans-serif;
  border-color: blue;
  
}

p{
  color: transparent;
  font-size: 35px;
  cursor: pointer;

}

p:hover{
color: black;
}

.ligar{
  margin-left: 15px;
  height: 36px;
  color: aliceblue;
  cursor: pointer;
  background-color: black;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 20px;
  width: 130px;
  
}

.limparCampos{
  margin-left: 15px;
  height: 36px;
  color: black;
  cursor: pointer;
  background-color: rgb(223, 15, 43);
  font-family: Arial, Helvetica, sans-serif;
  font-size: 20px;
  width: 130px;
  border: none;
  
}

.limparCampos:hover{
color: aliceblue;
background-color: blue;
border: none;
}

.ligar:hover{
color: rgb(209, 16, 122);
background-color: rgb(5, 206, 48);
border: none;
}

#instrucao{
color: black;
font-size: 15px;
font-family: Arial, Helvetica, sans-serif;
margin-left: 10px;
background-color: yellow;
padding: 10px;
}

</style> 




<!-- 

// http://localhost:5173/

<script >
import { reactive } from 'vue';


// let contador = 0;
const estado = reactive({
  contador: 0,
})

function incrementar(){
  estado.contador++
}


function decrementar (){
  estado.contador--
}
export default{
  data(){
    return{
      n1:'' ,
      n2:'',
      resultado: '',
      
    }
  },

  methods:{
    
    somar(){
this.resultado = this.n1 + this.n2
    },    
    
  }

}


</script>

<template>  


  <input type="number" v-model.number="n1" placeholder="Primeiro valor">
  <input type="number" v-model.number="n2" placeholder="Segundo valor">  

  {{ resultado }}
  <button v-on:click="resultado"> Somar</button>

  <br>
  <hr>

  {{ estado.contador }}
  <button @click="incrementar" type="button">+</button>
  <button @click="decrementar" type="button">-</button>
  
</template>

<style scoped>



input{
  width: 130px;
  height: 30px;
  margin: 20px;
  
}

spam{
color: rgb(2, 77, 2);


}

select{
  height: 35px;

}

select, option{
  color: red;
  font-size: 20px;
  font-family: Arial, Helvetica, sans-serif;
  padding-left: 20px;
  border-radius: 30px;
  padding-right: 10px;
}

selected{
  color: red;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 24px;}

  h3{
    font-size: 42px;
    color: red;
    font-family: Arial, Helvetica, sans-serif;
  }


</style> 

<br> -->




<!-- 

Constantes com vue.js

const nome =  'jonas';

Criando objetos

const meuObj = {
nome: "jonas"
livroFavorito = "Economia"
}

function mostrar (){
return `${nome} Bom dia`;
}


// http://localhost:5173/

<script >

new Vue({
  el: "#app",
  data:{
    
      n1:"" ,
      n2:"",
      selected:"", 

  },

methods:{
    somar(){
  return this.n1 + this.n2
    },

    subtracao(){
      return this.n1 - n2
    },
    
  }
}

);

</script>


  <template>  
<div id="app">

  <div v-if="selected==somar">
    <div>Selecione: {{ selected }}</div>

<select v-model="selected">
  <option disabled value="">Aritmetica</option>
  <option>somar</option>
  <option > subtrair</option>
  <option>*</option>
  <option>/</option> 

</select>

  <input type="number" v-model.number="n1" placeholder="Primeiro valor">
  <input type="number" v-model.number="n2" placeholder="Segundo valor">

  <h3>{{ somar() }}</h3>
  </div>



</div>
</template>


<style scoped>

input{
  width: 130px;
  height: 30px;
  margin: 20px;
  
}

spam{
color: rgb(2, 77, 2);


}

select{
  height: 35px;

}

select, option{
  color: red;
  font-size: 20px;
  font-family: Arial, Helvetica, sans-serif;
  padding-left: 20px;
  border-radius: 30px;
  padding-right: 10px;
}

selected{
  color: red;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 24px;}

</style>


 -->
