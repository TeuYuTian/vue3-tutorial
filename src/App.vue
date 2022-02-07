<template>
<br/>

  Add 1:<button @click="increase"> +1 </button> <br/>
  Minus 1:<button @click="decrease"> -1 </button> <br/>
  Add 5:<button @click="increasefive"> +5 </button> <br/>
  Minus 1:<button @click="decreasefive"> -5 </button> <br/>
  

  <br/>


 <h2>{{counter}}</h2>

  Name: <input type="text" v-model="name"/> <br/>
  Address1: <input type="text" v-model="address1"/> <br/>
  Address2: <input type="text" v-model="address2"/> <br/>
  Tel: <input type="text" v-model="tel"/> <br/>
  Email: <input type="text" v-model="email"/> <br/>

  <img v-bind:src= "filename"/> <br/>
  <img :src= "picture1"/> <br/>
  <img :src= "picture2"/> <br/>


  <hr/>
  Name: {{name}} <br/>
  Address1: {{address1}} <br/>
  Address2: {{address2}} <br/>
  Tel: {{tel}} <br/>
  Email: {{email}} <br/>

</template>

<script>
export default {
  data(){
    return{
      name:"",
      address1:"",
      address2:"",
      tel:"",
      email:"",
      filename: "logo.png",
      picture1: "download.png",
      picture2: "picture.jpg",
      counter: 0,

    };
  }
  ,
  components: {},
    methods: {
      increase(){
        this.counter = this.counter+1
      },
      decrease(){
        this.counter = this.counter-1
      },
      increasefive(){
        this.counter = this.counter+5
      },
      decreasefive(){
        this.counter = this.counter-5
      },

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
