<template>
  <v-container fluid>
    <v-row justify="start" align="start">
      <v-col cols="12" md="12" lg="12" xl="12">
        <p class="google-font" offset-cols="1" :class="this.$vuetify.theme.dark?'white--text':'grey--text text--darken-2'" style="font-weight: 350;font-size:200%">Community Partners</p>
      </v-col>
      <v-col cols="3" md="6" lg="3" xl="3" sm="6" v-for="(itemp,i) in communities" :key="i">
            <div class="client-logo ma-0">
                <a :href="itemp.meetup" target="_blank">
                    <v-tooltip bottom>
                    <template v-slot:activator="{ on }">
                        <v-img
                        :src="getPartnerImgUrl(itemp.image)"
                        :lazy-src="getPartnerImgUrl(itemp.image)"
                        class="white"
                        contain
                        style="height:4em"
                        v-on="on"
                        >
                            <v-layout
                                slot="placeholder"
                                fill-height
                                align-center
                                justify-center
                                ma-0
                            >
                                <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                            </v-layout>
                        </v-img>
                    </template>
                    <span class="google-font">{{itemp.name}}</span>
                    </v-tooltip>
                </a>
            </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Partners from "@/assets/data/partners.json";
export default {
  data() {
    return {
      communities: Partners.communities
    };
  }
};
</script>


