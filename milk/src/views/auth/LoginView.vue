<script setup>
  import { ref } from 'vue'

  const theme = ref('light')

  function onClick () {
    theme.value = theme.value === 'light' ? 'dark' : 'light'
  }
</script>

<template>
  <v-responsive class="border rounded">
    <v-app :theme="theme">
      <v-app-bar class="px-3">
        <v-spacer></v-spacer>

        <v-btn
          :prepend-icon="theme === 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'"
          text="Theme"
          slim
          @click="onClick"
        ></v-btn>
      </v-app-bar>

      <v-main>
        <v-container>
        
        <v-row> 
        <v-col cols="12" md="6" class="mx-auto">
            <v-card
    class="mx-auto"
    prepend-icon="$vuetify"
    subtitle="High-quality Milk"
    
  >
<v-img src="/img/logo.png" height="200"></v-img>

    <template v-slot:title>
      <span class="font-weight-black">Welcome to Pasteurized Milk</span>
    </template>

    <v-card-text class="bg-surface-light pt-4">
        <v-form fast-fail @submit.prevent>
            <v-text-field label="Email" variant="outlined"></v-text-field>

      <v-text-field label="Password" type="password" variant="outlined"></v-text-field>

      <v-btn class="mt-2" type="submit" block>Log In</v-btn>
    </v-form>    

    <v-divider class="my-5"></v-divider>

    <h5>
    Don't have account? 
    <RouterLink to="/register">Click here to register</RouterLink>
    </h5>
    </v-card-text>
  </v-card>
        </v-col>
        </v-row>
        </v-container>
      </v-main>

      <v-footer border app>2024 - Pasteurized Milk </v-footer>
    </v-app>
  </v-responsive>
</template>