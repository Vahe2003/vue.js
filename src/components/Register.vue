<template>
<v-card>
  <v-form v-model = "valid">
    <v-container>
      <v-row>
      <v-col cols="12">
      <v-text-field v-model = "firstname" label="First Name" aria-required :rules="[v => !!v || 'Name is required']">   
       </v-text-field>
       <v-text-field v-model = "lastname" label="Last Name" aria-required :rules="[v => !!v || 'Last is required']">   
       </v-text-field>
      <v-text-field :type="show1 ? 'text' : 'password'" @click:append="show1 = !show1" :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'" v-model = "password" label="Password" aria-required :rules="passwordRules">   
       </v-text-field>
        <v-text-field type = 'email' v-model = 'email' label="Email" aria-required :rules="emailRules">   
       </v-text-field>
       <v-btn :disabled = "!valid" color="success">Login</v-btn>
       </v-col>
      </v-row>
    </v-container>
  </v-form>
</v-card>
</template>

<script>
export default {
    data: () => ({
      show1: false,
      firstname: null,
      lastname: null,
      password: null,
      email: null,
      valid:true,
      emailRules: [
    v => !!v || 'Email is required',
    v => /.+@.+/.test(v) || 'E-mail must be valid'
],
passwordRules: [
      v => !!v || 'Password is required',
    v => (v && v.length >= 8) || 'Password must have 8+ characters',
    v => /(?=.*[A-Z])/.test(v) || 'Must have one uppercase character',
    v => /(?=.*\d)/.test(v) || 'Must have one number',
    v => /([!@$%])/.test(v) || 'Must have one special character [!@#$%]'
]
  }),
}
</script>

