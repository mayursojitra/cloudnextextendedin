<template>
  <v-container fluid>
    <v-row justify="start" align="start">
      <v-col cols="12" md="12" lg="12" xl="12">
        <p class="google-font" offset-cols="1" :class="this.$vuetify.theme.dark?'white--text':'grey--text text--darken-2'" style="font-weight: 350;font-size:200%">Themes</p>
        <v-tabs
          v-model="model"
          :color="this.$vuetify.theme.dark?'white':'primary'"
          :grow="getMobileTab()"
          left
          show-arrows
          :centered="getMobileTab()"
          :slider-color="this.$vuetify.theme.dark?'white':'primary'"
          class="grey lighten-2 mx-0"
          :background-color="$vuetify.theme.dark ? 'grey darken-4' : 'grey lighten-4'"
          :class="$vuetify.theme.dark ? 'row-border-dark' : 'row-border-white'"
        >
          <v-tab
            href="#day1"
            class="google-font"
            style="text-transform: capitalize;font-weight: bold;"
          >
            Industry Insights
          </v-tab>
          <v-tab
            href="#day2"
            class="google-font"
            style="text-transform: capitalize;font-weight: bold;"
          >
            Productivity & Collaboration
          </v-tab>
          <v-tab
            href="#day3"
            class="google-font"
            style="text-transform: capitalize;font-weight: bold;"
          >
            Infrastructure
          </v-tab>
          <v-tab
            href="#day4" 
            class="google-font"
            style="text-transform: capitalize;font-weight: bold;"
          >
            Security
          </v-tab>
          <v-tab
            href="#day5" 
            class="google-font"
            style="text-transform: capitalize;font-weight: bold;"
          >
            Data Analytics
          </v-tab>
          <v-tab
            href="#day6" 
            class="google-font"
            style="text-transform: capitalize;font-weight: bold;"
          >
            Data Management & Databases
          </v-tab>
          <v-tab
            href="#day7" 
            class="google-font"
            style="text-transform: capitalize;font-weight: bold;"
          >
            Application Modernization
          </v-tab>
          <v-tab
            href="#day8" 
            class="google-font"
            style="text-transform: capitalize;font-weight: bold;"
          >
            Cloud AI
          </v-tab>
          <v-tab
            href="#day9" 
            class="google-font"
            style="text-transform: capitalize;font-weight: bold;"
          >
            Business Application Platform
          </v-tab>
        </v-tabs>
      </v-col>
    </v-row>
    <v-row class="my-0 py-0" >
      <v-col cols="12" class="my-0 py-0 " >
        <v-tabs-items v-model="model" :class="$vuetify.theme.dark ? 'grey darken-4' : 'grey lighten-4'">
          <v-tab-item
            value="day1"
            class="my-0 py-0"
            :class="$vuetify.theme.dark ? 'grey darken-4' : 'grey lighten-4'"
          >
            <v-container fluid class="py-0 my-0 px-0">
              <v-row>
                <v-col>
                  <p class="google-font" style="text-align:justify">
                    Insights from Google Cloud executives, focusing on transformational efforts across industries working with customers and ecosystem partners.
                  </p>
                </v-col>
              </v-row>
            </v-container>
          </v-tab-item>
          <v-tab-item
            value="day2"
            class="my-0 py-0"
            :class="$vuetify.theme.dark ? 'grey darken-4' : 'grey lighten-4'"
          >
            <v-container fluid class="py-0 my-0 px-0">
              <v-row>
                <v-col>
                  <p class="google-font" style="text-align:justify">
                    Change the way teams work with solutions designed for humans and built for impact.
                  </p>
                </v-col>
              </v-row>
            </v-container>
          </v-tab-item>
          <v-tab-item
            value="day3"
            class="my-0 py-0"
           :class="$vuetify.theme.dark ? 'grey darken-4' : 'grey lighten-4'"
          >
            <v-container fluid class="py-0 my-0 px-0">
              <v-row>
                <v-col>
                  <p class="google-font" style="text-align:justify">
                    Migrate and modernize workloads on Google's global, secure, and reliable infrastructure.
                  </p>
                </v-col>
              </v-row>
            </v-container>
          </v-tab-item>
          <v-tab-item
            value="day4"
            class="my-0 py-0"
            :class="$vuetify.theme.dark ? 'grey darken-4' : 'grey lighten-4'"
          >
            <v-container fluid class="py-0 my-0 px-0">
              <v-row>
                <v-col>
                  <p class="google-font" style="text-align:justify">
                  Detect, investigate, and respond to online threats to help protect your business.
                  </p>
                </v-col>
              </v-row>
            </v-container>
          </v-tab-item>
          <v-tab-item
            value="day5"
            class="my-0 py-0"
           :class="$vuetify.theme.dark ? 'grey darken-4' : 'grey lighten-4'"
          >
            <v-container fluid class="py-0 my-0 px-0">
              <v-row>
                <v-col>
                  <p class="google-font" style="text-align:justify">
                    Generate instant insights from data at any scale with a serverless, fully managed analytics platform that significantly simplifies analytics.
                  </p>
                </v-col>
              </v-row>
            </v-container>
          </v-tab-item>
          <v-tab-item
            value="day6"
            class="my-0 py-0"
           :class="$vuetify.theme.dark ? 'grey darken-4' : 'grey lighten-4'"
          >
            <v-container fluid class="py-0 my-0 px-0">
              <v-row>
                <v-col>
                  <p class="google-font" style="text-align:justify">
                    Migrate and manage enterprise data with security, reliability, high availability, and fully managed data services.
                  </p>
                </v-col>
              </v-row>
            </v-container>
          </v-tab-item>
          <v-tab-item
            value="day7"
            class="my-0 py-0"
           :class="$vuetify.theme.dark ? 'grey darken-4' : 'grey lighten-4'"
          >
            <v-container fluid class="py-0 my-0 px-0">
              <v-row>
                <v-col>
                  <p class="google-font" style="text-align:justify">
                    Develop and run applications using open source and other software without operations staff.
                  </p>
                </v-col>
              </v-row>
            </v-container>
          </v-tab-item>
          <v-tab-item
            value="day8"
            class="my-0 py-0"
           :class="$vuetify.theme.dark ? 'grey darken-4' : 'grey lighten-4'"
          >
            <v-container fluid class="py-0 my-0 px-0">
              <v-row>
                <v-col>
                  <p class="google-font" style="text-align:justify">
                    Add intelligence and efficiency to your business with AI and machine learning.
                  </p>
                </v-col>
              </v-row>
            </v-container>
          </v-tab-item>
          <v-tab-item
            value="day9"
            class="my-0 py-0"
           :class="$vuetify.theme.dark ? 'grey darken-4' : 'grey lighten-4'"
          >
            <v-container fluid class="py-0 my-0 px-0">
              <v-row>
                <v-col>
                  <p class="google-font" style="text-align:justify">
                    Design, secure, analyze, and scale APIs anywhere with visibility and control.
                  </p>
                </v-col>
              </v-row>
            </v-container>
          </v-tab-item>
        </v-tabs-items>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "overview",
  data: () => ({
    model: "day1",
  }),
  methods: {
    getMobileTab() {
      if (window.innerWidth < 500) return true;
      else return false;
    },
  },
};
</script>
