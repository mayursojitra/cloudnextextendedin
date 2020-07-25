<template>
  <v-content class="ma-0">
    <v-container fluid class="mt-0 pt-0">
      <v-row justify="center" align="center">
        <v-col md="10" sm="11" xl="10" cols="12" class="mt-0 pt-0">
          <StartScreen />
        </v-col>
      </v-row>
    </v-container>

    <v-container fluid :class="this.$vuetify.theme.dark == true?'grey darken-4':'grey lighten-4'">
      <v-row justify="center" align="center">
        <v-col md="10" sm="11" xl="10" cols="12">
          <stats />
        </v-col>
      </v-row>
    </v-container>

    <v-container fluid class>
      <v-row justify="center" align="center">
        <v-col md="10" sm="11" xl="10" cols="12">
          <eventContext />
        </v-col>
      </v-row>
    </v-container>

    <v-container
      fluid
      :class="this.$vuetify.theme.dark == true?'grey darken-4 elevation-5':'grey lighten-4'"
      style="min-height:330px"
    >
      <v-row align="center" justify="center">
        <v-col md="10" sm="11" xl="10" cols="12">
          <eventOverview />
        </v-col>
      </v-row>
    </v-container>

    <v-container fluid class>
      <v-row justify="center" align="center">
        <v-col md="10" sm="11" xl="10" cols="12">
          <CodeOfConductSection />
        </v-col>
      </v-row>
    </v-container>

    <v-container 
    fluid
    :class="this.$vuetify.theme.dark == true?'grey darken-4 elevation-5':'grey lighten-4'">
      <v-row justify="center" align="center">
        <v-col md="10" sm="11" xl="10" cols="12">
          <communityPartner />
        </v-col>
      </v-row>
    </v-container>

    <v-container fluid>
      <v-row justify="center" align="center">
        <v-col md="8" xl="7">
          <SocialShare/>
        </v-col>
      </v-row>
    </v-container>
  </v-content>
</template>

<script>
// @ is an alias to /src
import StartScreen from "@/components/home/StartScreen";
export default {
  name: "Home",
  components: {
    StartScreen,
    stats: () => import(/* webpackChunkName: "homeStats" */ "@/components/home/stats"),
    eventContext: () => import(/* webpackChunkName: "homeContext" */ "@/components/home/eventContext"),
    eventOverview: () => import(/* webpackChunkName: "homeOverview" */ "@/components/home/overview"),
    CodeOfConductSection: () => import(/* webpackChunkName: "homeGuidelines" */ "@/components/codeOfConduct/guidelines"),
    communityPartner: () => import(/* webpackChunkName: "communityPartners" */ "@/components/home/communityPartners"),
    SocialShare: () => import(/* webpackChunkName: "homeSocialShare" */ "@/components/common/SocialShare"),
  }
};
</script>
