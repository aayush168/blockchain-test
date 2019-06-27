<template>
  <v-form ref="form"
    v-model="valid"
    lazy-validation>
    <v-container>
      <h2 class="headline font-weight-light">Add User Info</h2><br>
      <v-layout row wrap>
        <v-flex xs12 sm6>
          <v-text-field
            v-model="firstname"
            label="First Name"
            :rules="[rules.required]"
          ></v-text-field>
        </v-flex>
        <v-flex xs12 sm6>
          <v-text-field
            v-model="lastname"
            label="Last Name"
            :rules="[rules.required]"
          ></v-text-field>
          
        </v-flex>
        <v-flex xs12 sm6>
          <v-text-field
            v-model="email"
            label="Email"
            :rules="[rules.required]"
          ></v-text-field>
        </v-flex>

        <v-flex xs12 sm6>
          <v-text-field
            v-model="phone"
            label="Phone"
            :rules="[rules.required]"
          ></v-text-field>
          
        </v-flex>
        <v-flex xs12 sm6>
          <v-text-field
            v-model="address"
            label="Address"
            :rules="[rules.required]"            
          ></v-text-field>
        </v-flex>

        <v-flex xs12 sm6>
          <v-text-field
            v-model="dob"
            label="Date of Birth"
            :rules="[rules.required]"
          ></v-text-field>
          
        </v-flex>
        <v-btn color="success" @click="register">Register</v-btn>
      </v-layout>
    </v-container>
  </v-form>
</template>

<script>
export default {
  data() {
    return {
      firstname: '',
      lastname: '',
      email: '',
      phone: '',
      address: '',
      dob: '',
      rules: {
        required: value => !!value || 'Required.',
        min: v => v.length >= 8 || 'Min 8 characters',
        emailMatch: () => ('The email and password you entered don\'t match')
      }
    }
  },
  methods: {
    register() {
      this.$refs.form.validate()
    }
  }
}
</script>

<style>

</style>
