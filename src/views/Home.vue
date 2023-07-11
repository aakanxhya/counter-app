<template>
    <v-layout class=" align-center justify-center d-flex">
        <v-card width="500">
          <v-card-title class="primary">
            <h2 class="headline">Log-in</h2>
          </v-card-title>
          <v-card-text>
              <v-text-field
                v-model="email"
                label="Email"
                required
              ></v-text-field>
              <v-text-field
                v-model="password"
                label="Password"
                type="password"
                required
              ></v-text-field>
              <v-btn color="primary" type="submit">Login</v-btn>
          </v-card-text>
        </v-card>
    </v-layout>
</template>


<script>
export default {
  data() {
    return {
      email: '',
      password: ''
    };
  },
  methods: {
    login() {
      console.log('login');
      console.log('Email:', this.email);
      console.log('Password:', this.password);
    }
  }
};
</script>

<style scoped>
.primary {
  background-color: #6284a7;
}
.headline {
 color: aliceblue !important;
}
</style>