<script setup>
import { ref } from 'vue'

const mostrar= ref(true)
const mostrar2= ref(false)
const mostrar3= ref (false)
const mostrar4=ref (false)


const bot2= ref(false)
const bot3=ref (false)


const custom= ref(false)

const online= ref (false)

const large= ref (false)



const number1= ref(true)
const number1Next= ref(false)


const number2= ref(false)
const number2Next= ref (true)



const number3= ref (false)

const priceY=ref (false)

const priceM= ref (false)

const mo= ref(true)
const year= ref(false)

const primaryPrice= ref(true)
const primary= ref (true)
const arc= ref (false)
const pr= ref (false)


const name = ref('')
const gmail = ref('')

const phone = ref('')

const number3Next = ref (true)
const mont= ref(true)
const ys=ref(false)
const adv= ref (false)


function prox() {

  if( name.value === ''  
  ){
    mostrar.value=true
    nm.style.border = '2px solid red'
    nm.placeholder = 'Campo obrigatório!' 
  }
  else if (gmail.value===''){
  mostrar.value=true
  gm.style.border = '2px solid red'
    gm.placeholder = 'Campo obrigatório!' 
  }
  else if(phone.value===''){
    mostrar.value=true
    tl.style.border = '2px solid red'
    tl.placeholder = 'Campo obrigatório!' 
  }




  else{
    mostrar.value=false
    mostrar2.value=true
    number1Next.value=true
    number1.value=false
    number2.value=true
    number2Next.value=false
    bot2.value=false
    bot3.value=true
  }
}



function swit(){
  if(mo.value===true){
    mo.value=false
    year.value=true
    ys.value=true
    mont.value=false
    priceY.value=true
    primaryPrice.value=false
    priceM.value=false

  }
  else if(mo.value===false){
    mo.value=true
    year.value=false
    ys.value=false
    mont.value=true
    priceY.value=false
    primaryPrice.value=true



    
    
  }
}

function back (){
  mostrar.value=true
  mostrar2.value=false
  number1Next.value=false
  number1.value=true
  number2.value=false
  number2Next.value=true
}



function back2 (){
  mostrar3.value=false
  mostrar2.value=true

}

const disab= ref (true)



function prox2 (){



  mostrar.value=false
  mostrar2.value=false
  mostrar3.value=true
  number2.value=false
  number1.value=false
  number2Next.value=true
  number3.value=true
  number3Next.value=false
  
  
}


function arcade (){
  primary.value=false
  arc.value=true
  adv.value=false
  pr.value=false
  disab.value=false
  bot3.value=true

}
function advenced (){
  primary.value=false
  adv.value=true
  arc.value=false
  pr.value=false
  disab.value=false
  bot3.value=true
  
  

}





function pro  (){
  primary.value=false
  adv.value=false
  arc.value=false
  pr.value=true
  disab.value=false
  bot3.value=true

}


function serv (){
  if(online.value===false){
    online.value=true
  }
  else{
    online.value=false
  }
}
function serv2(){
  if(large.value===false){
    large.value=true
  }
  else{
    large.value=false
  }
}
function serv3(){
  if(custom.value===false){
    custom.value=true
  }
  else{
    custom.value=false
  }
}

function select (){
  if (disab.value=true){
  alert("Select a plan!")
}

}








</script>

<template>
  
    <div class="container-main">
      <section class="section-step">
      <div class="container-steps">
        <div class="step1">
          <div class="number"><i v-show="number1" class="bi bi-1-circle-fill"></i>
          <i v-show="number1Next" class="bi bi-1-circle"></i></div>
          <div class="text-step">
            <p class="step-out">Step 1</p>
            <p class="step-down">YOUR INFO</p>
          </div>

        </div>
        <div class="step1">
          <div class="number"><i v-show="number2" class="bi bi-2-circle-fill"></i> <i v-show="number2Next" class="bi bi-2-circle"></i>

          </div>
          <div class="text-step">
            <p class="step-out">Step 2</p>
            <p class="step-down">YOUR INFO</p>
          </div>

        </div>
        <div class="step1">
          <div class="number"><i v-show="number3" class="bi bi-3-circle-fill"></i> <i v-show="number3Next" class="bi bi-3-circle"></i>

          </div>
          <div class="text-step">
            <p class="step-out">Step 3</p>
            <p class="step-down">YOUR INFO</p>
          </div>

        </div>

        
      </div>

      


      </section>


      <section v-show="mostrar" class="main">

        <h2 class="title">Personal info</h2>
        <p class="parag"> Please provide your name, email address, and phone number. </p>

        <form>
        
          <input id="nm" v-model="name"  required type="text" placeholder="Name">
          <input id="gm" v-model="gmail" type="email" placeholder="Email Address">
          <input id="tl" v-model="phone" type="tel"  placeholder="Phone">
        </form>
        

      </section>
      <section v-show="mostrar2" class="main">
        <h2 class="title">Select your plan</h2>
          <p class="parag"> You have the option of monthly or yearly billing.</p>


          <div class="container-itens">

            <div @click="arcade" class="item">
              <div class="img"><img src="./assets/images/icon-arcade.svg" alt=""></div>
              <div class="text">
                <p class="theme">Arcade</p>
                <p v-show="mo" class="monthly">$15/mo</p>
                <p v-show="year" class="monthly">$35/year</p>
              </div>

            </div>

            <div @click="advenced" class="item">
              
              <div  class="img"><img src="./assets/images/icon-advanced.svg" alt=""></div>
              <div class="text">
              <p class="theme">Advenced</p>
              <p v-show="mo" class="monthly">$15/mo</p>
              <p v-show="year" class="monthly">$35/year</p>
              </div>
            </div>

            <div id="prop" @click="pro" class="item">
              <div class="img"><img src="./assets/images/icon-pro.svg" alt=""></div>
              <div class="text">
              <p class="theme">Pro</p>
              <p v-show="mo" class="monthly">$15/mo</p>

              <p v-show="year" class="monthly">$35/year</p>
              </div>

              

              
            </div>
            
            
            
          </div>
          <p v-show="arc" class="title-mon">Arcade <span v-show="mont">(Monthly)</span> <span v-show="ys">(Yearly)</span></p>

          <p v-show="adv" class="title-mon">Advenced <span v-show="mont">(Monthly)</span> <span v-show="ys">(Yearly)</span></p>

          <p v-show="pr" class="title-mon">Pro <span v-show="mont">(Monthly)</span> <span v-show="ys">(Yearly)</span></p>
          <button  class="month">
            <p class="options">Monthly</p>

            
            
            <div class="form-check form-switch">
              
          <input @click="swit" class="form-check-input" type="checkbox" value="true" id="checkNativeSwitch" switch>
          
          
          </div>
          <p class="options">Yearly</p>
          </button>


          <button @click="back" class="back">Go Back</button>
          
          
      </section>


      <section v-show="mostrar3" class="main">
        <h2 class="title">Pick add-ons</h2>
        <p class="parag">Add-ons help enhance your gaming experience</p>

        <div class="container-iten">

          <div class="item-service">
            <div @click="serv" class="check">
              <input class="check" type="checkbox" name="" id="">
            </div>
            <div class="texts">
              <p class="title-service">Online service</p>
              <p class="parag">Acess to multiplayer games</p>
            </div>

          </div>

          <div class="item-service">
            <div @click="serv2" class="check">
              <input class="check" type="checkbox" name="" id="">
            </div>
            <div class="texts">
              <p class="title-service">Larger storage</p>
              <p class="parag">Extra 1TB of cloud save</p>
            </div>

          </div>

          <div class="item-service">
            <div @click="serv3" class="check">
              <input class="check" type="checkbox" name="" id="">
            </div>
            <div class="texts">
              <p class="title-service">Customizable profile</p>
              <p class="parag">Custom theme on your profile</p>
            </div>

          </div>


        </div>

        <button @click="back2" class="back">Go Back</button>





      </section>


      <section v-show="mostrar4" class="main">

        <h2 class="title">Finishing up</h2>

        <p class="parag">double-check everything looks OK before confirming.</p>

        <div class="container-confirm">
          <div class="select">
          <p v-show="primary" class="title-mon">
            SELECT A PLAN 
          </p>

          <p v-show="arc" class="title-mon">Arcade <span v-show="mont">(Monthly)</span> <span v-show="ys">(Yearly)</span></p>

          <p v-show="adv" class="title-mon">Advenced <span v-show="mont">(Monthly)</span> <span v-show="ys">(Yearly)</span></p>

          <p v-show="pr" class="title-mon">Pro <span v-show="mont">(Monthly)</span> <span v-show="ys">(Yearly)</span></p>



          <p v-show="primaryPrice" class="title-mon">$15</p> <p v-show="priceY" class="title-mon">$35</p> <p v-show="priceM" class="title-mon">$35</p>
          </div>
          <a href="#">Change</a>
          <hr>

          <div v-show="online" class="select">
            <p class="services">Online service</p>
            <p class="precing">FREE/mo</p>


          </div>
          <div v-show="large" class="select">
            <p class="services">Large storage</p>
            <p class="precing">FREE/mo</p>


          </div>


          <div v-show="custom" class="select">
            <p class="services">Customizable profile</p>
            <p class="precing">FREE/mo</p>


          </div>

          



        </div>

      </section>


      <button v-show="bot2" type="submit" @click="prox" class="submit-step">Next Step</button>


      <button v-show="bot3" type="submit" @click="prox2" class="submit-step">Next Step</button>

      <button @click="select" v-show="disab"  class="submit-step" > Select a plan</button>
      
      



    </div>
    


  
  
</template>

<style >

.precing{
  color:hsl(213, 96%, 18%);
  
}
.services{
  color: hsl(231, 11%, 63%);
}


.select{
  display: flex;
  justify-content: space-between;
}

.container-confirm{
  background-color: hsl(218, 100%, 97%);
  padding: 20px;
  border-radius: 10px;

}
.title-mon{
  color: hsl(213, 96%, 18%);
  font-weight: 600;
  font-size: 17px;
}




@font-face {
  font-family: 'Ubuntu';
  src: url('@/assets/fonts/Ubuntu-Regular.ttf') format('truetype');
  font-weight: 400;
}

@font-face {
  font-family: 'Ubuntu';
  src: url('@/assets/fonts/Ubuntu-Medium.ttf') format('truetype');
  font-weight: 500;
}

@font-face {
  font-family: 'Ubuntu';
  src: url('@/assets/fonts/Ubuntu-Bold.ttf') format('truetype');
  font-weight: 700;
}
body{
  background-color: hsl(218, 100%, 97%);
  
  height: 100vh;
  margin: 0;
  padding: 0;
  justify-content: center;
  display: flex;
  margin-top: 100px;
  font-family: 'Ubuntu';
}
.section-step{
  background-image: url(./assets/images/bg-sidebar-desktop.svg);
  background-repeat: no-repeat;
  background-size: 200wh;
  margin-top: 10px;
  margin-left:10px;

  width: 200px;
}

.container-main{

  width: 1500px;
  display: flex;
  height: 590px;
  background-color: white;

}
.main{
  margin-left:200px
}

.container-itens{
  display: flex;
  gap:30px;
}

.item{

  width: 200px;
  border-radius: 10px;
  border: 2px solid  hsl(229, 24%, 87%);
}
.img{
  padding: 20px;
  
}
.month{
  display:flex;
  gap:60px;
  margin-top: 60px;
  width: 100%;
  justify-content: center;
  background-color: hsl(218, 100%, 97%);
  padding: 10px;
  border-radius: 10px;
  border:0px
}
.monthly{
  color: hsl(231, 11%, 63%);
}



h2{
  
  color:hsl(213, 96%, 18%);
  font-size: 40px;
  margin-top: 20px;
}
.parag{
  color:hsl(231, 11%, 63%);
  font-family: 'Ubuntu';
}
form{

  width: 500px;
  
  gap:10px;
  display:block;
}
input{
  width: 100%;
  margin-top: 25px;
  height: 30px;
  font-family: 'Ubuntu' ;
  color: hsl(213, 96%, 18%);
  font-weight: 600;
  border: 1px solid hsl(213, 96%, 18%) ;
  padding: 10px;
  border-radius: 5px;
  
}
.submit-step{
  background-color: hsl(243, 100%, 62%);
  padding: 13px;
  border: 0;
  border-radius: 10px;
  width: 130px;
  height: 50px;
  margin-top: 30%;
  font-size: 15px;
  font-weight: 700;
  color: hsl(231, 100%, 99%);
  margin-left: 10%;
  
}
.back{
  margin-top: 35px;
  font-size: 17px;
  border: 0;
  background-color: transparent;
  color:  hsl(243, 100%, 62%);
  font-weight: 700;
}







.step1{
  display: flex;
}
.item:hover {
  background-color:rgba(170, 7, 170, 0.021);
  border: 1px solid  hsl(243, 100%, 62%);
}


.step-out{
    color: hsla(229, 24%, 87%, 0.712);
    font-size: 17px;
    font-weight: 400;
}
.step-down{
    font-size: 20px;
    color: white;
    font-weight: 500;
}


.bi-1-circle-fill, .bi-1-circle, .bi-2-circle-fill, .bi-2-circle, .bi-3-circle-fill, .bi-3-circle{
  color: hsl(218, 100%, 97%);
  font-size: 30px;
}
.container-steps{
  margin-left:10px;
}
.text-step{
  
  margin-left: 10px;
}
.number{
  margin-top:30px
}
.text{
  margin-top: 30px;
  margin-left: 20px;
  
}
.theme{
  color:hsl(243, 100%, 62%) ;
  font-weight: 700;
  font-size:20px
}


.title-service{
  color:hsl(213, 96%, 18%)  ;
  font-size: 20px;
  font-weight: 600;
}
.item-service{
  border: 1px solid  hsl(243, 100%, 62%);
  width: 500px;
  padding: 10px;
  border-radius: 10px;
  display: flex;
  gap: 30px;
  margin-top: 15px;
}
.container-iten{
  flex-direction: column;
}
.check{
  width: 20px;
  
}

</style>
