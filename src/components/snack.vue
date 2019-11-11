<template>
  <div class="text-center ma-2">
    <v-snackbar
      v-model="this.$parent.snackOpen"
      :color="success"
    >
      {{ this.$parent.snackText }}
    </v-snackbar>
  </div>
</template>
<script>
    export default {
        data() {
            return {
            }
        },
    }
</script>