<template>
  <v-app>
    <v-content>
      <v-container>
        <v-app-bar app>
           <img :src="require('@/assets/logo.png')" height="40"/>
           <v-toolbar-title class = "mx-4">Vue</v-toolbar-title>
           <v-spacer></v-spacer>
          <div class="hidden-sm-and-down">
          <router-link class="mx-2" to="/">1. Basic Variables</router-link>
          <router-link class="mx-2" to="/exercise-two">2. Composing Components</router-link>
          <router-link class="mx-2" to="/exercise-three">3. V-for, Forms</router-link>
          <router-link class="mx-2" to="/exercise-four">4. Form Validation</router-link>
          <router-link class="mx-2" to="/exercise-five">5. App Bar</router-link>
          </div>
          <div class="hidden-md-and-up">
          <v-app-bar-nav-icon></v-app-bar-nav-icon>
           </div>
        </v-app-bar>
      </v-container>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>
export default {
 data: () => ({
    
  })
}
</script>
