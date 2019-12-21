<template>
  <v-app>
    <v-content>
          <v-toolbar app color="primary" dark>
           <img :src="require('@/assets/logo.png')" height="40"/>
           <v-toolbar-title>ue</v-toolbar-title>
           <v-spacer></v-spacer>
            <v-toolbar-items class="hidden-sm-and-down">
            <v-btn class="mx-1" text to="/">1. Basic Variables</v-btn >
            <v-btn class="mx-1" text to="/exercise-two">2. Composing Components</v-btn >
            <v-btn class="mx-1" text to="/exercise-three">3. V-for, Forms</v-btn >
            <v-btn class="mx-1" text to="/exercise-four">4. Form Validation</v-btn >
            <v-btn class="mx-1" text to="/exercise-five">5. App Bar</v-btn >
          </v-toolbar-items>
          <v-toolbar-side-icon class="hidden-md-and-up"></v-toolbar-side-icon>
          </v-toolbar>
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
