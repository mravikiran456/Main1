<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated class="bg-white text-black " height-hint="98">
     <div class="pages-container">
      <q-toolbar>
        <q-toolbar-title>
         <img src="~assets/logo104909.png"  @click="$router.replace('/Home')">
        </q-toolbar-title>
       
        <q-tabs align="center" >
         
          <q-route-tab to="/Home" label="Home" />
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
         
          <router-view />
   
 
    </q-page-container>

  </q-layout>
</template>
<script>
  
</script>
<style scoped>
  img{
   max-width: 50%;
   padding: 10px;
  }
.pages-container{

  max-width: 90%;
}
.logout{
 
 margin-left: 20px;
}
.page{
  width: 100%;
  max-width: 768px;
  padding: 15px;
  box-sizing: border-box;
}
.view-enter-active,.view-leave-active{
  transition: opacity 0.5s ease-in-out,transform 0.5s ease;
}
.view-enter,.view-leave-to{
  opacity: 0;
}
.view-enter-to,.view-leave{
 opacity: 1;
 transform: translate(0px); 
}
</style>