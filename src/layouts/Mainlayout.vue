<template>
  <q-layout view="hHh lpR fFf">
    <q-header bordered class="bg-white text-black " height-hint="98">
     <div class="pages-container">
      <q-toolbar>
        <q-toolbar-title>
         <img src="~assets/logo104909.png"  @click="$router.replace('/Home')">
        </q-toolbar-title>
       
        <q-tabs align="center" >
         
          <q-route-tab to="/Home" label="Home" @click="visible=!visible" />
          <q-route-tab to="/Product" label="Product" />
          <q-route-tab to="/Cart" label="Cart" />
       
          <div class="logout">
             <q-btn color="black" text-color="white" label="Logout"  @click="$router.replace('/Login')"/>  
           </div>

        </q-tabs>
      
      </q-toolbar>
    </div>

      
    </q-header>

    <q-page-container>
         <transition name="router-anim" enter-active-class="animated fadeInDown" leave-active-class="fadeOutDown"> <router-view /></transition>
        
    </q-page-container>

  </q-layout>
</template>
<script>
  
</script>
<style scoped>
  @import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";
  img{
   max-width:30%;
   padding: 10px;
  }
.pages-container{

  max-width: 90%;
}
.logout{
 
 margin-left: 20px;
}


</style>