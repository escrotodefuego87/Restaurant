<template>
  <v-app>
    <Login :dialogShared="initialDialog" @log="setInitial"/>
    <Signin :signShared="initialSign" @sign="setSign"/>
    <v-toolbar dark fixed>
      <router-link to="/" exact tag="h1">
        <v-toolbar-title>FOOD FOLKS</v-toolbar-title>
      </router-link>
      <div class="flex-grow-1"></div>
      <v-toolbar-items>
        <v-btn text @click="handleLogin()">Log in</v-btn>
        <v-btn text @click="handleSignin()">Sign in</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    
    <router-view></router-view>
  </v-app>
</template>

<script>
import Home from './views/Home';
import Login from "./components/Login";
import Signin from "./components/Signin";

export default {
  name: 'App',
  components: {
    Home,
    Login,
    Signin
  },
  data: () => ({  
    initialDialog: false,
    initialSign: false

  }),
  methods: {
    handleLogin(){
      this.initialDialog = true;
    },
    handleSignin(){
      this.initialSign = true;
    },
    setInitial(log){
      this.initialDialog = log;
    },
    setSign(sign){
      this.initialSign = sign;
    }
  },
  mounted(){

},

};
</script>
