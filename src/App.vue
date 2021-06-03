<template>
  <div id="app">
    <link rel="preconnect" href="https://fonts.gstatic.com">
<link rel="preconnect" href="https://fonts.gstatic.com">
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@200;300&family=Nunito+Sans:ital,wght@0,600;1,200;1,300&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.10.1/css/all.css">
  <link rel="stylesheet" href="https://michalsnik.github.io/aos/">  
  <link rel="stylesheet" href="https://unpkg.com/aos@2.3.1/dist/aos.css">
 
   <div class="top background">
       <div class="menu sticky" >
      <nav :class="{'show':showSidebar}">
        <input type="checkbox" id="check" >
        <label for="check" class="checkbtn" >
          <i class="fas fa-bars" @click="showNav"></i>
        </label>
<lable class="box">This Interior</lable> 
          <ul class="menu-ul">
            <li> <a href="">Home</a> </li>
             <li> <a href="">Collection</a> </li>
             <li> <a href="">About</a> </li>
             <li> <a href="">Contact</a> </li>
         </ul>
      </nav>
      </div>
         <div class="navigation-links" :class="{'show':showSidebar}">
           <transition-group name="fade">
             <div v-show= "showLink" key="1" style="color:white; font-size:20px;">Home</div>  
             <div v-show= "showLink"  key="2" style="color:white; font-size:20px;">collection</div>
             <div v-show= "showLink"  key="3" style="color:white; font-size:20px;">About</div>
             <div v-show= "showLink"  key="4" style="color:white;font-size:20px;">Contact</div>
           </transition-group>
         </div>
           <div class="img-container">
              <img class="img" src="./assets/photo1.png">
          </div>
   
         <div class="page-title">
             <h1 class="title">Modern interior</h1>
             <p class="title-info" >A full-service resdential & <br> commercial interior design and <br> staging company offering  <br> professional organizing & <br> eco-services </p>
              <h3 class="read more">Read more <i id="icon"  class="fas fa-long-arrow-alt-right" style="color:white;"></i></h3>
         </div>
       <div class="designer-info">
          <img class="designer" src="./assets/photo2.png">
        <span><h2>Aliza Webber</h2> <br> <p>Interior designer</p> </span>
        <h1>Designed in 2020 by <br>  Aliza Webber</h1>
        </div>
  </div>
    <section>
      <div class="design-title">
      <h4>  Our Designs </h4>
      </div>
    </section>
<div class="box-img">
  <span style="--i:1;"><img src="./assets/design 1.jpg" /></span>
  <span style="--i:2;"><img src="./assets/design 2.jpg" /></span>
  <span style="--i:3;"><img src="./assets/design 3.jpg" /></span>
  <span style="--i:4;"><img src="./assets/design 4.jpg" /></span>
  <span style="--i:5;"><img src="./assets/design 5.jpg" /></span>
  <span style="--i:6;"><img src="./assets/design 6.jpg" /></span>
  <span style="--i:7;"><img src="./assets/design 7.jpg" /></span>
  <span style="--i:8;"><img src="./assets/design 8.jpg" /></span>
</div>
</div>

</template>

 <script>
 export default {
   data: ()=> {
        return {
         showSidebar:false,
         showLink:false
        }
   },
   methods:{
     showNav(){
       if(this.showSidebar){
             this.showLink = false;
             setTimeout(()=>{
               this.showSidebar = false;
             }, 500);

       } 
       else{
              this.showSidebar = true;
                 setTimeout(()=>{
               this.showLink = true;
             }, 500);

       }
     }
   }

 }
 
</script>

<style>
*{
 margin:0%;
 border-radius:5px;
 
}
#app{
  width:100%;
  background:black;
  height:450vh;
  
 }
 .sticky{
   position:fixed;
   width:100%;
   z-index:100;
  
 }
 .box{
  margin:1rem;
  font-size:15px;
  color:rgb(192, 192, 192);
  width:100px;
  height:25px;
  border:1px solid gray;
  text-transform: uppercase;
  text-align:center;
  padding-top:0px 100px;
  line-height:80px;
}
.show{
  height:500px;
  background:red;
 
} 
 
nav{
  background: #0082e6;
  height:80px;
  width:100%;
}
nav ul{
      float:right;
      margin-right:20px;
 }
nav ul li{
      display:inline-block;
      line-height:80px;
      margin:0 5px;
     
    }
nav ul li a{
  color:white;
  text-decoration:none;
  display:inline-block;
  font-size:18px;
  font-family: 'Montserrat', sans-serif;
  font-weight: bold;
  padding:10px 38px;
  border-bottom:1px solid transparent;   
}
a:hover{
   border-radius:0px;
}
.checkbtn{
  font-size:30px;
  color:white;
  float:right;
  line-height:80px;
  margin-right:40px;
  cursor:pointer;
   display:none;
}
#check{
display: none;
}
.page-title{
  margin-top:-32.5rem;
  width:40%;
  height:50%;
  margin-left:4rem;
}
.page-title .title{
  color: #fff;
  font-size:4em;
  }
  .page-title .title-info{
    color:rgb(221, 216, 216);
    font-size:20px;
    font-family: 'Montserrat', sans-serif;
    font-weight: 400;
    margin:2rem 0 2rem ;
  }
   .page-title h3 {
     color:rgb(248, 239, 239);
     font-size:18px;
    font-family: 'Montserrat', sans-serif;
     
   }
.page-title #icon{
   margin-left:1rem;
   font-size:18px;
}
.img-container{
  position:relative;
  margin-left:45rem;
}
.img-container .img{
  width:750px;
  height:500px;
  margin-top:12rem;
  border-radius:0px;
}
 .designer-info{
   position: absolute;
   width:400px;
   height:150px;
   background:black;
   margin-left:65rem;
   margin-top:10rem;
   border-radius:0px;
   }
 .designer-info .designer {
  width:50px;
  height:50px;
  display:flex;
  border-radius:50%;
  margin:15px;
}
.designer-info h2{
  font-family: 'Nunito Sans', sans-serif;
  font-size:21px;
  color:white;
  margin-top:-4rem;
  margin-left:5rem;
}
.designer-info p{
  font-size:14px;
  color:rgb(112, 111, 111);
  margin-top:-1rem;
  margin-left:5rem;
  font-family:'Poppins', sans-serif;
}
.designer-info h1{
  font-size:20px;
  color:white;
  margin:1rem;
  font-family: 'Libre Baskerville', serif;
  font-weight: inherit;
  letter-spacing: 1px;
}
h4{
  font-variant: small-caps;
  font-size:30px;
  letter-spacing: 10px;
  color:#fff;
  margin-top:25rem;
  text-align:center;
  filter:blur(1px);
  font-weight:100;
  text-shadow: 0 0 10px rgba(255,255,255, 1),
               0 0 20px rgba(255,255,255, 1),
               0 0 40px rgba(255,255,255, 1),
               0 0 80px rgba(255,255,255, 1),
               0 0 160px rgba(255,255,255, 1);
-webkit-animation: glow 1s ease-in-out infinite alternate;
  -moz-animation: glow 1s ease-in-out infinite alternate;
  animation: glow 1s ease-in-out infinite alternate;
}

@keyframes glow {
  from {
    text-shadow: 0 0 10px rgb(16, 218, 245), 0 0 20px rgb(16, 128, 148), 0 0 30px #00d7e6, 0 0 40px #a7fdfd, 0 0 50px #8dd6f3, 0 0 60px #0ba7ce, 0 0 70px #1dbfdb;
  }
  
  to {
    text-shadow: 0 0 20px rgb(12, 201, 226), 0 0 30px #0b97b9, 0 0 40px #107ba5, 0 0 50px #074597, 0 0 60px #1c0ed4, 0 0 70px #1554dd, 0 0 80px #072d75;
  }
}

   .box-img{
    
    margin-left:40rem;
    justify-content: center;
    margin-top:10rem;
    width:200px;
    height:200px;
    transform-style:preserve-3d;
    animation:animate 20s linear infinite;
  }
  @keyframes animate{
    0%{
      transform: perspective(1000px) rotateY(0deg);
    }
    100%{
      transform: perspective(1000px) rotateY(360deg);
    }

  }
  .box-img span{
    position:absolute;
    width:100%;
    height:100%;
    transform-origin: center;
    transform-style:preserve-3d;
    transform: rotateY(calc(var(--i) * 45deg)) translateZ(400px);
    -webkit-box-reflect:below 0px linear-gradient(transparent,transparent,#0004 )
  }
  .box-img span img{
    position:absolute;
    width:100%;
    height:100%;
  }
  @media (max-width:952px) {
    label.logo{
      font-size:30px;
      padding-left:50px;
    }
    nav ul li a{
      font-size:16px;
    }

 }
 @media (max-width:858px) {
   .checkbtn{
     display:block;
   }
.page-title{
  margin-top:-32.5rem;
  width:40%;
  height:50%;
  margin-left:54rem;
}   
nav ul{
  display:none;
      
      margin-left:40rem;
 }
nav ul li{
      display:inline-block;
      line-height:80px;
      margin:0 5px;
     
    }

    
 }
</style>