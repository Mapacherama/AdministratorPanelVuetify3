<template>
  <v-app>
    <v-main>
      <v-container>
        <v-row justify="center">
          <v-col cols="12" sm="8" md="4">
            <v-card class="elevation-12">
              <v-toolbar dark color="primary">
                <v-toolbar-title>Login</v-toolbar-title>
              </v-toolbar>
              <v-card-text>
                <v-form @submit.prevent="login">
                  <v-text-field
                    label="Email"
                    type="email"
                    v-model="email"
                    required
                  ></v-text-field>
                  <v-text-field
                    label="Password"
                    type="password"
                    v-model="password"
                    required
                  ></v-text-field>
                  <v-btn color="primary" type="submit">Login</v-btn>
                </v-form>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      password: "",
    };
  },
  methods: {
    login() {
      // Add login logic here
      console.log(`Email: ${this.email}, Password: ${this.password}`);
    },
  },
};
</script>
