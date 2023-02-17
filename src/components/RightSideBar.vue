<template>
  <v-navigation-drawer app color="#14141C" right width="290">
    <v-toolbar color="rgba(0,0,0,0)" flat>
      <v-icon color="#7C7C7F" class="mr-4"> fas fa-search</v-icon>
      <v-badge bordered overlap color="red" dot class="mr-8">
        <v-icon color="#7C7C7F">far fa-bell</v-icon>
      </v-badge>
      <v-divider vertical inset color="#7C7C7F" class=""></v-divider>
      <v-spacer></v-spacer>
      <v-badge bordered bottom color="#49D9A0" dot offset-x="10" offset-y="10">
        <v-avatar size="30" class="ml-n3">
          <v-img src="https://cdn.vuetifyjs.com/images/lists/4.jpg"></v-img>
        </v-avatar>
      </v-badge>
      <v-btn text color="#7C7C7F">Joie</v-btn>
      <v-btn icon dark class="ml-n3">
        <v-icon x-small color="#7C7C7F">fas fa-chevron-down</v-icon>
      </v-btn>
    </v-toolbar>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "RightSideBar",
  data() {
    return {};
  },
};
</script>

<style></style>
