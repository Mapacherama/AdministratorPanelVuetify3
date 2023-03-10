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
                  <v-btn class="secondary" color="primary" type="submit">Login</v-btn>
                  <!-- <v-alert
                  class="mt-8"
      text
      color="error"
    >
      <h3 class="headline">
        <v-icon>mdi-cancel</v-icon>
        Delete User</h3>
      <div>Are you sure that you want to remove the user?</div>

      <v-divider
        class="my-4 info"
        style="opacity: 0.22"
      ></v-divider>

      <v-row
        align="left"
        no-gutters
      >

        <v-row class="grow ml-1">This action can not be undone!</v-row>
        <v-spacer></v-spacer>
          <v-btn
            color="critical"
            outlined
          >
            Confirm & Delete
          </v-btn>
        </div>
      </v-row>
    </v-alert> -->
    <!-- <v-alert class="mt-5"
    type="success"
    title="Form successfully submitted!"
    text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus! Eaque cupiditate minima, at placeat totam, magni doloremque veniam neque porro libero rerum unde voluptatem!"
  ></v-alert> -->
  <v-sheet
    elevation="12"
    max-width="600"
    rounded="lg"
    width="100%"
    class="pa-4 text-center mt-5 mx-auto"
  >
    <v-icon
      class="mb-5"
      color="primary"
      icon="mdi-check-circle"
      size="112"
    ></v-icon>

    <h2 class="text-h5 mb-6">The form has been submitted!</h2>

    <p class="mb-4 text-medium-emphasis text-body-2">
      To see a report on this form, click <a href="#" class="text-decoration-none text-info">View form submission report.</a>

      <br>

      Otherwise, you're done!
    </p>

    <v-divider class="mb-4"></v-divider>

    <div class="text-end">
      <v-btn
        class="text-none"
        color="primary"
        rounded
        variant="flat"
        width="90"
      >
        Done
      </v-btn>
    </div>
  </v-sheet>
    <template>

</template>
                  <template>
</template>
                </v-form>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>

      </v-container>
      <div class="text-center">

    <v-menu :location="location">
      <template v-slot:activator="{ props }">
        <v-btn
          color="primary"
          dark
          v-bind="props"
        >
          Dropdown
        </v-btn>
      </template>

      <v-list>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
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
