<template>
  <q-page class="flex flex-center">
    <div class="container">
    <div class="screen"><span>NOKIA</span>
      <!-- <img class="image" src="https://i.pinimg.com/originals/e5/0c/c6/e50cc6fce3321a71d03526429c7b9c00.jpg" width="100px" alt=""> -->
      <q-input class="image" bg-color="green-7 text-white" v-model="text" />
      <div class="middle-btn" @click="enter()"></div>
      <div class="call-btn" @click="limpaNumeros()">C</div>
      <div class="chevrons">
       </div>
    </div>
    <div class="buttons">
      <div class="button-row1">
        <div class="btns btn-1" @click="digitaNumero('1')">1</div>
        <div class="btns btn-2" @click="digitaNumero('2')">2</div>
        <div class="btns btn-3" @click="digitaNumero('3')">3</div>
      </div>
      <div class="button-row2">
        <div class="btns btn-4" @click="digitaNumero('4')">4</div>
        <div class="btns btn-5" @click="digitaNumero('5')">5</div>
        <div class="btns btn-6" @click="digitaNumero('6')">6</div>
      </div>
      <div class="button-row3">
        <div class="btns btn-7" @click="digitaNumero('7')">7</div>
        <div class="btns btn-8" @click="digitaNumero('8')">8</div>
        <div class="btns btn-9" @click="digitaNumero('9')">9</div>
      </div>
      <div class="button-row4">
        <div class="btns btn-10" @click="digitaNumero('*')">*</div>
        <div class="btns btn-0" @click="digitaNumero(' ')">0</div>
        <div class="btns btn-12" @click="digitaNumero('#')">#</div>
      </div>
    </div>
  </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      text: '2 222 222 33 66 8 88 777 33'
    }
  },
  methods: {
    enter () {
    },
    digitaNumero (num) {
      this.text = this.text += num
    },
    limpaNumeros () {
      this.text = ''
    }
  }
}
</script>

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}
body{
  min-height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
}
.container{
  position:relative;
  width:150px;
  height:300px;
  background:rgba(68, 63, 88);
  border-radius: 50px 50px 50px 50px/300px 300px 300px 300px;
  box-shadow:inset 4px 0px 0 #ccc,
    inset -4px 0 0 #ccc;
}
.container:before{
  position:absolute;
  top:-10px;
  left:17px;
  width:115px;
  height:100px;
  z-index:-1;
  background:rgb(68, 63, 88);
  content:"";
  border-radius:25px/20px;

}
.container:after{
  position:absolute;
  bottom:-10px;
  left:22px;
  width:105px;
  height:100px;
  background:rgb(68, 63, 88);
  content:"";
  border-radius:25px/20px;
}
.screen{
  width:120px;
  height:190px;
  left:15px;
  top:-3px;
  background:#ccc;
  position:absolute;
  border-radius:25% 25% 50% 50%/40% 40% 40% 40%;
  overflow:hidden;

}
.screen:before{
  position:absolute;
  width:110px;
  height:160px;
  content:"";
  top:5px;
  left:5px;
  background:rgb(68, 63, 88);
  border-radius:25% 25% 50% 50%/40% 40% 40% 40%;
}
.screen span{
  position:absolute;
  top:25%;
  left:35%;
  font-size:10px;
  color:#ccc;
}
.image{
  position:absolute;
  top:35%;
  border-radius:5px 5px 10px 10px/20px;
  left:8%;
}
.middle-btn{
  position:absolute;
  width:35px;
  height:10px;
  bottom:26px;
  background:#ccc;
  left:43px;
  border-radius:50%;
}
.middle-btn:before{
  position:absolute;
  width:40px;
  height:15px;
  content:"";
  border-radius:50%;
  box-shadow:inset 5px 5px 0px 0px rgba(204,204,204,0.75),inset -5px -5px 0 0 rgba(204,204,204,0.75);
}
.middle-btn:after{
  position:absolute;
  width:20px;
  left:8px;
  top:-2px;
  height:5px;
  content:"";
  border-radius:2px 2px 2px 2px;
  border-bottom:2px solid #11899a;
}
.call-btn{
  position:absolute;
  width:25px;
  height:20px;
  border:1px solid #000;
  bottom:12px;
  left:10px;
  text-align:center;
  font-size:10px;
  border-radius:5px;
  transform:rotate(30deg) skew(-15deg);
}
.chevrons{
  position:absolute;
  width:40px;
  height:20px;
  border:1px solid #000;
  bottom:15px;
  right:0px;
  border-radius: 5px 10px 10px 10px;
  transform:rotate(-45deg) skew(15deg);
}
.chevrons:after{
  position:absolute;
  width:10px;
  height:10px;
  content:"<";
  font-size:10px;
  left:5px;

}
.chevrons:before{
  position:absolute;
  width:10px;
  height:10px;
  content:">";
  font-size:10px;
  right:5px;
}
.buttons{
  display:flex;
  flex-direction:column;
  position:relative;
  top:55%;
  left:0%;
  width:150px;
  height:120px;
  z-index:1;
}
.button-row1,.button-row2,.button-row3,.button-row4{
  position:absolute;
  display:flex;
}
.button-row1{
  top:5%;
}
.btns{
  margin:0 20px;
  font-size:15px;
  position:absolute;
  background:#ccc;
}
.btn-1,.btn-7,.btn-4,.btn-10{
  width:30px;
  height:20px;
  top:10px;
  border:1px solid #000;
  border-radius:50%;
  text-align:center;
  transform:rotate(30deg)
}
.btn-2,.btn-5,.btn-8,.btn-0{
  width:30px;
  height:20px;
  top:20px;
  left:43px;
  border:1px solid #000;
  border-radius:50%;
  text-align:center;
}
.btn-3,.btn-6,.btn-9,.btn-12{
  width:30px;
  height:20px;
  top:10px;
  left:83px;
  border:1px solid #000;
  border-radius:50%;
  text-align:center;
   transform:rotate(-30deg);
}
.btn-7{
  top:5px;
}
.btn-8{
  top:12px;
}
.btn-9{
  top:5px;
}
.btn-10{
  top:0px;
  left:5px;
}
.btn-0{
  top:3px;
  left:44px;
}
.btn-12{
  top:-2px;
  left:80px;
}
  .button-row2{
  top:30%;
}
.button-row3{
  top:60%;
}
.button-row4{
  top:90%;
}

</style>
