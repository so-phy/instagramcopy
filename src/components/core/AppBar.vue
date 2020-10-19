<template>
  <v-app-bar color="white" elevation="1">
    <router-link to="/camera"
      ><v-btn icon><v-icon>mdi-camera</v-icon></v-btn></router-link
    >
    <v-spacer></v-spacer>
    <v-img
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Instagram_logo.svg/1200px-Instagram_logo.svg.png"
      alt="logo"
      max-width="120"
    />
    <v-spacer></v-spacer>
    <router-link to=""
      ><v-btn icon><v-icon>mdi-send</v-icon></v-btn></router-link
    >
  </v-app-bar>
</template>

<script>
  export default {};
</script>

<style lang="scss" scoped></style>
