<template>
  <v-app-bar app color="primary" dark>
    <v-app-bar-nav-icon @click="toggleSidebar"></v-app-bar-nav-icon>
    <v-toolbar-title>Cloud Hosting Provider</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-menu offset-y>
      <template #activator="{ on }">
        <v-avatar size="32">
          <v-icon>mdi-account-circle</v-icon>
        </v-avatar>
      </template>
      <v-list>
        <v-list-item @click="logout">
          <v-list-item-title>Logout</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </v-app-bar>
</template>

<script>
  export default {
  methods: {
    toggleSidebar() {
      // Add logic to toggle sidebar here
      console.log("Toggle sidebar");
    },
    logout() {
      // Add logout logic here
      console.log("Logout");
    },
  },
};
</script>
