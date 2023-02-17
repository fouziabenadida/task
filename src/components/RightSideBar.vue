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
    <!-- <h1>ici doit etre dynamique</h1> -->
    <strong class="ml-3 white--text">Overall Progress</strong> <br />
    <strong class="ml-3 grey--text caption">Suziki Frontend</strong>
    <div class="text-center mb-5 mt-n5">
      <v-progress-circular
        :size="100"
        :width="12"
        :value="70"
        color="orange"
        class="mt-5"
      >
        70%</v-progress-circular
      >
    </div>
    <strong class="ml-3 white--text">Recent Activities</strong>
    <strong class="ml-3 grey--text caption">{{ currentDate() }}</strong>
    <v-list three-line>
      <v-list-item-group>
        <template v-for="item in files">
          <v-list-item :key="item.title">
            <v-list-item-avatar>
              <img :src="item.avatar" />
            </v-list-item-avatar>
            <template>
              <v-list-item-content>
                <v-list-item-title
                  v-html="item.title"
                  class="white--text"
                ></v-list-item-title>
                <v-list-item-subtitle
                  v-text="item.subtitle"
                  class="grey--text"
                ></v-list-item-subtitle>
                <v-list-item-subtitle
                  v-text="item.time"
                  class="grey--text"
                ></v-list-item-subtitle>
              </v-list-item-content>
            </template>
          </v-list-item>
        </template>
      </v-list-item-group>
    </v-list>

    <v-row>
      <v-col cols="12" sm="6">
        <v-card
          class="d-flex align-center ml-4"
          height="60px"
          width="120px"
          color="#21212B"
        >
          <v-row>
            <v-col cols="12" sm="12">
              <v-list-item two-line class="text-center">
                <v-list-item-content>
                  <v-list-item-title class="white--text">550</v-list-item-title>
                  <v-list-item-subtitle class="grey--text caption mt-2"
                    >Total Project</v-list-item-subtitle
                  >
                </v-list-item-content>
              </v-list-item>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
      <v-col cols="12" sm="6">
        <v-card
          class="d-flex align-center mx-2"
          height="60px"
          width="120px"
          color="#21212B"
        >
          <v-row>
            <v-col cols="12" sm="12">
              <v-list-item two-line class="text-center">
                <v-list-item-content>
                  <v-list-item-title class="white--text">200</v-list-item-title>
                  <v-list-item-subtitle class="grey--text caption mt-2"
                    >Upcoming</v-list-item-subtitle
                  >
                </v-list-item-content>
              </v-list-item>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
      <v-col cols="12" sm="6">
        <v-card
          class="d-flex align-center ml-4"
          height="60px"
          width="120px"
          color="#21212B"
        >
          <v-row>
            <v-col cols="12" sm="12">
              <v-list-item two-line class="text-center">
                <v-list-item-content>
                  <v-list-item-title class="white--text">320</v-list-item-title>
                  <v-list-item-subtitle class="grey--text caption mt-2"
                    >In Progress</v-list-item-subtitle
                  >
                </v-list-item-content>
              </v-list-item>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
      <v-col cols="12" sm="6">
        <v-card
          class="d-flex align-center ml-4"
          height="60px"
          width="120px"
          color="#21212B"
        >
          <v-row>
            <v-col cols="12" sm="12">
              <v-list-item two-line class="text-center">
                <v-list-item-content>
                  <v-list-item-title class="white--text">129</v-list-item-title>
                  <v-list-item-subtitle class="grey--text caption mt-2"
                    >Completed</v-list-item-subtitle
                  >
                </v-list-item-content>
              </v-list-item>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "RightSideBar",
  data() {
    return {
      files: [
        {
          avatar: "https://cdn.vuetifyjs.com/images/lists/1.jpg",
          time: "5 Mins Ago",
          subtitle: `Backend Developer`,
          title: `<strong>Mike Loke</strong>`,
        },
        {
          avatar: "https://cdn.vuetifyjs.com/images/lists/2.jpg",
          time: "15 Mins Ago",
          subtitle: `Senior Quality Assurance`,
          title: `<strong>Sarah Hosten</strong>`,
        },
        {
          avatar: "https://cdn.vuetifyjs.com/images/lists/3.jpg",
          time: "30 Mins Ago",
          subtitle: `Business Development`,
          title: `<strong>Dena Thompson</strong>`,
        },
      ],
    };
  },
  methods: {
    currentDate() {
      const current = new Date();
      const date = `${current.getDate()}/${
        current.getMonth() + 1
      }/${current.getFullYear()}`;
      return date;
    },
  },
};
</script>

<style>
.v-card.borderme {
    border: 2px solid #704232 !important;
}
 .col-12 {
    padding: 5px !important;
}
.v-btn.withoutupercase{
    text-transform: none !important;
}</style>
