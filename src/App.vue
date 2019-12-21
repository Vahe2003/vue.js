<template>
  <v-app>
    <v-content>
          <v-toolbar app color="#828282" dark>
           <img :src="require('@/assets/logo.png')" height="40"/>
           <v-toolbar-title>ue</v-toolbar-title>
           <v-spacer></v-spacer>
            <v-toolbar-items class="hidden-md-and-down">
            <v-btn class="mx-1" text to="/">1. Basic Variables</v-btn >
            <v-btn class="mx-1" text to="/exercise-two">2. Composing Components</v-btn >
            <v-btn class="mx-1" text to="/exercise-three">3. V-for, Forms</v-btn >
            <v-btn class="mx-1" text to="/exercise-four">4. Form Validation</v-btn >
            <v-btn class="mx-1" text to="/exercise-five">5. App Bar</v-btn >
          </v-toolbar-items>
              <v-app-bar-nav-icon class="hidden-lg-and-up" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
          </v-toolbar>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
      
    >
      <v-list
        dense
      >
        <v-list-item-group
          v-model="group"
        >
          <v-list-item to="/">
            <v-list-item-title>1. Basic Variables</v-list-item-title>
          </v-list-item>

          <v-list-item to="/exercise-two">
            <v-list-item-title>2. Composing Components</v-list-item-title>
          </v-list-item>

          <v-list-item to="/exercise-three">
            <v-list-item-title>3. V-for, Forms</v-list-item-title>
          </v-list-item>

          <v-list-item to="/exercise-four">
            <v-list-item-title>4. Form Validation</v-list-item-title>
          </v-list-item>
           <v-list-item to="/exercise-five">
            <v-list-item-title>5. App Bar</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

      <router-view/>
    </v-content>
  </v-app>
</template>

<script>
export default {
 data: () => ({
    drawer: false,
    group: null
  }),
  watch: {
      group () {
        this.drawer = false
      },
    },
}
</script>
