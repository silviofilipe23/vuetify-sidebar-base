<template>
  <div>
    <v-container fluid class="grey lighten-1 pa-0">
      <v-layout
        align-center
        style="min-height: 100vh; background-color: #fa705f"
      >
        <router-view></router-view>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "LoginLayout",
};
</script>

<style lang="scss">
html {
  overflow: hidden !important;
}
</style>