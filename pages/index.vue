<template>
  <div class="container">
    <canvas id="canvas" width="2000" height="1000"></canvas>
    <div class="info">
      <h1 class="title">Marshmallow</h1>
      <p class="subtitle">Chase • your • dreams</p>
      
    </div>
    <p class="call-to-action"><span>JUN</span> <br><span>30</span> <br><span>2021</span></p>
    
    
  </div>
</template>

<script>
export default {
  mounted(){
    console.log("rive",rive);
    const anim = new rive.Rive({
    src: '/onboarding.riv',
    canvas: document.getElementById('canvas'),
    autoplay: true,
    stateMachines: 'Scene 1',
    layout: new rive.Layout({
      fit: 'cover',
      alignment: 'centerLeft',

      })
  })
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  width:100vw;
  display: flex;
  justify-content: center;
    align-items: center;

  flex-direction: column;
  overflow: hidden;
}
#canvas{
  overflow: hidden;
  
  object-fit: cover;
  filter:saturate(1.2) contrast(1.2);
}

.title {
  font-family: 'Heebo', 'Helvetica Neue', Arial, sans-serif;
    display: block;
    font-weight: 900;
    font-size: 35px;
    color: white;
    -webkit-text-decoration: italic;
    text-decoration: auto;
    letter-spacing: 1px;
    z-index: 100;
    text-transform: lowercase;
    letter-spacing: 2px;
    
}

.subtitle {
  z-index: 100;
    font-weight: 500;
    font-size: 10px;
    color: #6227e8;
    word-spacing: 2px;
    /* padding-bottom: 15px; */
    text-transform: uppercase;
    letter-spacing: 1px;
}
.call-to-action{
  z-index: 100;
  font-weight: 900;
  font-size: 10vw;
  color: #a0b1e0;
  line-height: 90%;
  word-spacing: 5px;
  padding-top: 100px;
  padding-bottom: 15px; 
  position: absolute;
  bottom: 80px;
  right:100px;
  text-align: right;
}
.call-to-action span:nth-child(1){
  color:#ffffeb;
}
.call-to-action span:nth-child(5){
  color:#6127e8;
}
.call-to-action span:nth-child(3){
  color:#35ffbf;
}
.info{
  position: absolute;
  top: 80px;
  left: 100px;
}
.links {
  padding-top: 15px;
}
</style>
