<template >
 <div id="app">
   <h2>STUDENT DETAILS</h2>
   FIRSTNAME <input type="text" v-model="fname"><br><br>
   LASTNAME <input type="text" v-model="lname"><br><br>
   PASSWORD<input type ="password" v-model="psw"><br><br>
   COURSE <input type="text" v-model="course"><br><br>
    FEMALE<input type="radio" v-model="gender">
    MALE<input type="radio" v-model="gender">
   <h2>{{name}} {{psw}} {{course}} {{gender}}</h2>
   <h2 >{{student_details}}</h2>
   <div class="details">
   <button  @click="login">LOGIN</button>
   <p v-if="login">Successful login</p>
   <button v-else>SIGN IN</button>
   </div>
 </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return{
      fname:'',
      lname:'',
        psw:'',
      course:'',
      gender:'',
      login:false
    }
  },
  computed: {
    student_details(){
      return `${this.fname} ${this.lname} ${this.psw} ${this.course} ${this.gender} `


    }
  }
}
</script>

<style>
*{
  background-color: palegreen;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.details{
  color: rebeccapurple;
}
.details :hover{
  color: darkred;
  background-color: black;
  cursor: pointer;
  font-size: 17px;
}
</style>
