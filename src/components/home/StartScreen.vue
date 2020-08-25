<template>
  <v-container fluid>
    <v-row align="center" justify="center">
      <v-col cols="12" md="5" lg="4" class="text-center">
        <v-img :src="require('@/assets/img/common/cloud_banner.jpeg')">
          <template v-slot:placeholder>
            <v-row class="fill-height ma-0" align="center" justify="center">
              <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
            </v-row>
          </template>
        </v-img>
      </v-col>
      <v-col cols="12" md="7" lg="7">
        <h1
          class="google-font mt-5 mb-0"
          :class="this.$vuetify.theme.dark?'white--text':'grey--text text--darken-2'"
        >Google Cloud Next Extended'20</h1>
        <p class="google-font mt-0" style="font-size:80%">
          Follow up event of
          <a rel="noreferrer" href="https://cloud.withgoogle.com/next/sf/live/" target="_blank">Google Cloud Next</a>
        </p>
        <p
          class="google-font"
          style="font-size:130%"
        >Cloud Next On AirExtended 2020, and Yes, We Can't Believe How Many Words that is Either</p>
        <p
          class="google-font"
        >These are unprecedented times. Yes we said it. We know you've heard that word so often in the past few months, it's become background noise, so if you're still reading, good job. We usually do Next Extended in our own cities every year, surrounded with friendly, welcoming faces and slices of Domino's Mexican Green Wave, but you know. Unprecedented times.</p>
        <p
          class="google-font"
        >So instead we're going online this time, freeing ourselves from the confines of our cities and collaborating with GDGs from all over West India, to bring Next Extended right to your bedroom. Yes, your bedroom, don't pretend you get out of bed on Sundays. 9 weeks, 11 GDGs, a host of speakers from all over the world, cutting edge topics for all skill levels, and most importantly, that community experience you've been missing.</p>

        <p
          class="google-font"
          :class="this.$vuetify.theme.dark?'white--text':'grey--text text--darken-2'"
          style="font-size:120%"
        >July 19 - Sept 12, 2020 IST</p>

        <p class="google-font" style="font-size:100%;color:#9e9e9e">
          <span v-for="(item,i) in mainData.hashtags" :key="i">
            <v-chip
              :href="'https://twitter.com/hashtag/'+item"
              rel="noopener"
              target="_blank"
              small
              label
              class="mr-1"
            >#{{item}}</v-chip>
            <!-- &nbsp; -->
          </span>
        </p>
          <v-btn
            href="http://bit.ly/gdganthos"
            target="_blank"
            aria-label="Home BTN"
            color="primary"
            style="text-transform: capitalize;"
            class="google-font mr-4 mt-2"
            depressed
            large
            dark
          >Register for 29th August</v-btn>
        <v-btn
          href="https://www.youtube.com/channel/UC9wSs8WwgTzFMjI8zRjHV9w"
          target="_blank"
          aria-label="Home BTN"
          color="#c4302b"
          style="text-transform: capitalize;"
          class="google-font mt-2"
          depressed
          large
          dark
        >YouTube Channel</v-btn>

        <!-- <v-btn
            aria-label="Home BTN"
            color="primary"
            style="text-transform: capitalize;"
            class="google-font"
            depressed
            large
            target="_blank"
            href="https://cloudnextextendedin.web.app/"
            dark
        >Register Here 2</v-btn>-->
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import aboutEvent from "@/assets/data/about.json";
export default {
  data: () => ({
    mainData: {}
  }),
  mounted() {
    this.mainData = aboutEvent;
  }
};
</script>