<template>
     <div>
     <q-card>
          <q-tabs
            v-model="tab"
            dense
            class="text-grey"
            active-color="primary"
            indicator-color="primary"
            align="center"
            narrow-indicator
          >
            <q-tab name="mails" label="Men" />
            <q-tab name="alarms" label="Women" />
            
          </q-tabs>
  
          <q-separator />
  
          <q-tab-panels v-model="tab" animated>
            <q-tab-panel name="mails">
              <div class="text-h6">Men</div>
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
            </q-tab-panel>
  
            <q-tab-panel name="alarms">
              <div class="text-h6">Women</div>
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
            </q-tab-panel>
  
           
          </q-tab-panels>
        </q-card>
  
       
     
     </div>
</template>

    
<script>
     import { ref } from 'vue'
     
     export default {
       setup () {
         return {
           tab: ref('mails')
         }
       }
     }
     </script>


<style>

</style>