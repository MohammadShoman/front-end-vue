<template>
  <div class="facebook">
<img class="logo" src="https://static.xx.fbcdn.net/rsrc.php/y8/r/dF5SId3UHWd.svg" />
<p class="description">Connect with friends and the world<br>around you on Facebook.</p>

  </div>
</template>

<script>
export default {
name:'Facebook',
}
</script>

<style>
.facebook{
    display:flex;
    flex-direction: column;
    width:50%;
    margin-left:15% ;
    
}
.logo{
    margin-top:-50px;
    width:300px;
    height: 100px;
}
.description{
    font-size:25px;
    font-family:arial;
    width:100%;
    color:#606770;
    margin-left:8%;
}
</style>