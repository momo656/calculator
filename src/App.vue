<template>
  <body>
    <div class="container ">
      <div class="display">
        <form action="" @submit.prevent="calculate">
          <input type="text" v-model="input">
          <input id="eq" type="submit" value="=">
          
        </form>
      </div>
      <div class="buttons">
        <div class="row">
          <div class="col-auto">
            <button id="clc" @click="updateDis('+')" class="btn">+</button>
            <button id="clc" @click="updateDis('-')" class="btn">-</button>
            <button id="clc" @click="updateDis('*')" class="btn">*</button>
            <button id="clc" @click="updateDis('/')" class="btn">/</button>
            
          </div>
        </div>

        <div class="row">
          <div class="col-auto">
            <button @click="updateDis('1')" class="btn">1</button>
            <button @click="updateDis('2')" class="btn">2</button>
            <button @click="updateDis('3')" class="btn">3</button>
            <button  id="del" @click="clear()" class="btn">C</button>
          </div>
        </div>
      
        <div class="row">
          <div class="col-auto">
            <button @click="updateDis('4')" class="btn">4</button>
            <button @click="updateDis('5')" class="btn">5</button>
            <button @click="updateDis('6')" class="btn">6</button>
            <button @click="updateDis('.')" class="btn">.</button>
          </div>
        </div>
      
        <div class="row">
          <div class="col-auto">
            <button @click="updateDis('7')" class="btn">7</button>
            <button @click="updateDis('8')" class="btn">8</button>
            <button @click="updateDis('9')" class="btn">9</button>
            <button @click="updateDis('0')" class="btn">0</button>
          </div>
        </div>
      </div>
      
    </div>

  </body>
</template>

<script>

export default {
  name: 'App',
  components: {
    
  },
  data() {
    return {
      input: '',
      result: ''
    }
  },
  methods: {
    updateDis(value) {
      this.input += value
    },
    calculate() {
      this.result = eval(this.input)
      this.input = this.result
    },
    clear() {
      this.input = ''
      this.result = ''
    }
  }
}
</script>

<style>
body {
  
 
  font-family: Arial, sans-serif;
  background-color: #2b2828;
}
.container {
  margin: 8% auto;
  padding: 10px;
  height: 80%;
  width: 29%;
  background-color: #cac9c9;
  border-radius: 15px;
}
input{
 width: 70%;
  font-size: 20px;
  margin: 10px 0;
  padding: 10px;
  border-style: none;
  border-radius: 8px;
}
#eq{
  background-color: #4CAF50;
  color: white;
  width: 15%;
  font-size: 20px;
  padding: 10px;
  margin: 10px 10px;
  border-style: none;
  border-radius: 8px;
}

.btn{
  text-align: center;
  background-color: #f37209;
  color: white;
  width: 20%;
  height:20% ;
  font-size: 25px;
  padding: 20px;
  margin: 5px ; 
  border-style: none;
  border-radius: 8px;
}
#clc{
  background-color: #0e97af;
  color: white;
  width: 20%;
  height:20% ;
  font-size: 25px;
  padding: 20px;
  margin: 5px ; 
  border-style: none;
  border-radius: 8px;
}
#del{
  background-color: #f31109;
  color: white;
  width: 20%;
  height:20% ;
  font-size: 20px;
  padding: 20px;
  margin: 5px ; 
  border-style: none;
  border-radius: 8px;
}
@media only screen and (max-width: 768px) {

  .container {
  margin: 15% auto;
  padding: 10px;
  height: 100%;
  width: 50%;
  background-color: #cac9c9;
}
input{
 
  font-size: 20px;
  margin: 10px 0;
  padding: 10px;
  border-style: none;
  border-radius: 8px;
}
#eq{
  background-color: #4CAF50;
  color: white;
  width: 15%;
  font-size: 20px;
  padding: 10px;
  margin: 10px 10px;
  border-style: none;
  border-radius: 8px;
}
  
}
@media only screen and (max-width: 420px) {

.container {
margin: 15% auto;
padding: 10px;
height: 100%;
width: 50%;
background-color: #cac9c9;
}
input{

font-size: 20px;
margin: 10px 0;
padding: 8px;
border-style: none;
border-radius: 8px;
}
#eq{
background-color: #4CAF50;
color: white;
width: 15%;
font-size: 20px;
padding: 8px;
margin: 10px 5px;
border-style: none;
border-radius: 8px;
}
.btn{
  text-align: center;
  background-color: #f37209;
  color: white;
  width: 20%;
  height:20% ;
  font-size: 25px;
  padding: 10px;
  margin: 4px ; 
  border-style: none;
  border-radius: 8px;
}
#clc{
  background-color: #0e97af;
  color: white;
  width: 20%;
  height:20% ;
  font-size: 25px;
  padding: 10px;
  margin: 4px ; 
  border-style: none;
  border-radius: 8px;
}
#del{
  background-color: #f31109;
  color: white;
  width: 20%;
  height:20% ;
  font-size: 25px;
  padding: 10px;
  margin: 4px ; 
  border-style: none;
  border-radius: 8px;
}

}

</style>
