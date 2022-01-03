<template>
    <img src="https://res.cloudinary.com/ravikiran143/image/upload/v1641192548/sellers-commerce-office_wrbjpf.jpg" class="wave" alt="login-wave">
    <div class="row" style="height: 90vh">
      
      <!-- <div class="col-6 col-md-6 flex justify-center content-center">
        <img src="https://res.cloudinary.com/ravikiran143/image/upload/v1640927365/logo104909_hid3fj_xhf2jl.png" class="responsive" alt="login-image">
        
      </div> -->
      <div v-bind:class="{'justify-center': $q.screen.md || $q.screen.sm ||$q.screen.xs} " 
           class="col-6 col-md-6 flex justify-center content-center">
        <q-card v-bind:style="$q.screen.lt.sm ? {'width': '80%'} : {'width': '50%'}" style="background-color:#00000060;" class="m-3">
          <q-card-section>
            <q-avatar size="103px" class="absolute-center">
              <img src="https://res.cloudinary.com/ravikiran143/image/upload/v1641191561/processed-8672c00f-7915-41ad-9e8c-663ad4f93097_2JzepVO3_ena7ix.png" alt="avatar" class="logo">
            </q-avatar>
          </q-card-section>
          <q-card-section>
            <div class="q-pt-lg">
              <div class="col text-h6 ellipsis flex justify-center">
                <h2 class="text-h2 text-uppercase q-my-none text-weight-regular login1" style="font-weight: bolder;">Login</h2>
              </div>
            </div>
          </q-card-section>
          <q-card-section>
            <q-form class="q-gutter-md" @submit.prevent="submitForm">
              <q-input label="Username" v-model="login.username" class="input" >
              </q-input>
              <q-input label="Password" type="password" v-model="login.password" class="input">
              </q-input>
              <div>
                <q-btn class="full-width"  style="background-color: #ffbf5f;" label="Login" type="submit"  to="/home"  rounded></q-btn>
                <div class="text-center q-mt-sm q-gutter-lg">
                  <router-link class="text-black" to="/login" style="font-weight: bolder;">Create a Account</router-link>
                </div>
              </div>
            </q-form>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </template>
  
  <script>
  import { useQuasar } from 'quasar'
  import { mapActions } from 'vuex'
  
  let $q
  
  export default {
    name: 'Login',
    data () {
      return {
        login: {
          username: 'Ravi',
          password: 'ravi1998'
        }
      }
    },
    methods: {
      ...mapActions('auth', ['doLogin']),
      async submitForm () {
        if (!this.login.username || !this.login.password) {
          $q.notify({
            type: 'negative',
            message: 'Os dados informados são inválidos.'
          })
        } else if (this.login.password.length < 6) {
          $q.notify({
            type: 'negative',
            message: 'A senha deve ter 6 ou mais caracteres.'
          })
        } else {
          try {
            await this.doLogin(this.login)
            const toPath = this.$route.query.to || '/admin'
            this.$router.push(toPath)
          } catch (err) {
            if (err.response.data.detail) {
              $q.notify({
                type: 'negative',
                message: err.response.data.detail
              })
            }
          }
        }
      }
    },
    mounted () {
      $q = useQuasar()
    }
  }
  </script>
  
  <style scoped>
  .wave {
    position: fixed;
    height: 100%;
    width: 100%;
    left: 0;
    bottom: 0;
    z-index: -1;
  }
  .logo{
  background: position 0;
  }
  .login1{
    font-size: large;
  }
  .input{
   
    font-size: x-large;
    background-color: #00000021;
 
    
    
  }
  </style>