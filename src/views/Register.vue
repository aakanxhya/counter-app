<template>
  <v-layout class="align center">
    <v-card width="1000">
      <v-card-title class="Create">
        <h1 class="headline">Create your own Account</h1>
        <h1 class="headline">Let's Get Started</h1>
      </v-card-title>
      <v-chip variant="elevated">
        Log-in with Google
      </v-chip>
      <v-divider class="border-opacity-100" color="black">OR</v-divider>
    </v-card>
  </v-layout>
  <v-form v-model="valid">
    <v-container>
      <v-row>
        <v-col cols="12">
          <v-text-field
            v-model="name"
            :rules="nameRules"
            :counter="10"
            label="Name"
            required
          ></v-text-field>
        </v-col>

        <v-col cols="12">
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
          ></v-text-field>
        </v-col>

        <v-col cols="12">
          <v-text-field
            v-model="password"
            :rules="nameRules"
            :counter="10"
            label="Password"
            required
          ></v-text-field>
        </v-col>
      </v-row>
    </v-container>
  </v-form>
</template>

<script>
export default {
  name: "RegisterVue",
  data: () => ({
    valid: false,
    name: '',
    nameRules: [
      value => {
        if (value) return true

        return 'Name is required.'
      },
      value => {
        if (value?.length <= 10) return true

        return 'Name must be less than 10 characters.'
      },
    ],
    email: '',
    emailRules: [
      value => {
        if (value) return true

        return 'E-mail is required.'
      },
      value => {
        if (/.+@.+\..+/.test(value)) return true

        return 'E-mail must be valid.'
      },
    ],
  }),
}
</script>

<style>

</style>
