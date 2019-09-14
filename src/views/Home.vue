<template>

<v-app>
  <v-banner single-line>
    Setup del proyecto, todo listo para empezar el desarrollo!
    <template v-slot:actions>
      <v-btn
        @click="sayhi()"
        text
        color="deep-purple accent-4"
      >
        Hi!
      </v-btn>
    </template>
  </v-banner>
</v-app>
  
</template>

<script>
import HelloWorld from '../components/HelloWorld';

export default {
  components: {
    HelloWorld,
  },
  methods: {

    sayhi(){
      alert('Muestra');
    }

  },
};
</script>
