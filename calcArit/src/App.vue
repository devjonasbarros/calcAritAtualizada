<!-- 
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




// http://localhost:5173/

<script >

export default{
  data(){
    return{
      n1:'' ,
      n2:'',
      selected:'', 

      
    }
  },

  methods:{

    
    somar(){
  return this.n1 + this.n2
    },

    subtracao(){
      return this.n1 - n2
    },

    multiplicar(){
      return this.n1 * n2
    },

    dividir(){
      return this.n1 / n2
    },

  limpar(){
    return this.n1,n2 = ''
  },


    
    
  }

}

</script>

<template>  

<div >Selecione: {{ selected }}</div>

<select v-model="selected">
  <option disabled value="">Aritmetica</option>
  <option>somar</option>
  <option > subtrair</option>
  <option>multiplicar</option>
  <option>dividir</option> 

</select>

  <input type="number" v-model.number="n1" placeholder="Primeiro valor">
  <input type="number" v-model.number="n2" placeholder="Segundo valor">

  <h3 >{{ somar() }}</h3>
  

  
  
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
