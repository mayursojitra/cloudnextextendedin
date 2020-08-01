<template>
  <v-content class="ma-0">
    <v-container
      fluid
      class="pb-0"
      :class="$vuetify.theme.dark ? 'row-border-dark' : 'row-border-white'"
    >
      <v-row justify="center" align="center">
        <v-col md="10" class="py-0 my-0">
          <v-toolbar flat 
          class="py-0 mt-0 my-0" 
          tabs 
          height="120%" 
          :class="$vuetify.theme.dark==true?'grey darken-4':'white'">
            <v-toolbar-title
              :class="$vuetify.theme.dark == true ? 'white--text' : 'grey--text text--darken-2'"
              class="google-font my-5"
              style="font-weight: 350;font-size:200%"
              >Schedules
            </v-toolbar-title>
            <template v-slot:extension>
              <p>
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Voluptatibus atque dolorum sequi ex cumque praesentium, quaerat
                molestias? Earum quod libero sit veniam. Dolorem provident
                quibusdam, necessitatibus laborum perspiciatis ipsam laudantium.
              </p>
            </template>

            <template v-slot:extension>
              <v-tabs
                v-model="model"
                :grow="getMobileTab()"
                :centered="getMobileTab()"
                color="primary"
                slider-color="primary"
              >
                <v-tab href="#day1">
                  19 July
                </v-tab>
                <v-tab href="#day2">
                  25 July
                </v-tab>
                <v-tab href="#day3">
                  26 July
                </v-tab>
                <v-tab href="#day4">
                  1 August
                </v-tab>
                <v-tab href="#day5">
                  2 August
                </v-tab>
                <v-tab href="#day6">
                  8 August
                </v-tab>
                <v-tab href="#day7">
                  9 August
                </v-tab>
                <v-tab href="#day8">
                  15 August
                </v-tab>
                <v-tab href="#day9">
                  16 August
                </v-tab>
              </v-tabs>
            </template>
          </v-toolbar>
        </v-col>
      </v-row>
    </v-container>

    <v-container fluid>
      <v-row justify="center" align="center">
        <v-col md="10">
          <v-tabs-items v-model="model">
            <v-tab-item
              value="day1"
              :class="$vuetify.theme.dark ? 'black' : 'white'">
              <v-container>
                <v-row>
                  <v-col>
                    <h3 class="google-font">Industry Insights</h3>
                    <p class="google-font" style="text-align:justify;">
                      Insights from Google Cloud executives, focusing on transformational efforts across industries working with customers and ecosystem partners.
                    </p>
                    <ScheduleDetails :data="ScheduleData[0]" />
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
            <v-tab-item value="day2" :class="$vuetify.theme.dark ? 'black' : 'white'">
              <v-container>
                <v-row>
                  <v-col>
                    <h3 class="google-font">Productivity & Collaboration</h3>
                    <p class="google-font" style="text-align:justify;">
                      Change the way teams work with solutions designed for humans and built for impact.
                    </p>
                    <ScheduleDetails :data="ScheduleData[1]" />
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
            <v-tab-item value="day3" :class="$vuetify.theme.dark ? 'black' : 'white'">
              <v-container>
                <v-row>
                  <v-col>
                    <h3 class="google-font">Productivity & Collaboration</h3>
                    <p class="google-font" style="text-align:justify;">
                      Change the way teams work with solutions designed for humans and built for impact.
                    </p>
                    <ScheduleDetails :data="ScheduleData[2]" />
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
            <v-tab-item value="day4" :class="$vuetify.theme.dark ? 'black' : 'white'">
              <v-container>
                <v-row>
                  <v-col>
                    <h3 class="google-font">Infrastructure</h3>
                    <p class="google-font" style="text-align:justify;">
                      Migrate and modernize workloads on Google's global, secure, and reliable infrastructure.
                    </p>
                    <v-btn
                      href="https://www.meetup.com/GDG-Nagpur/events/272140921/"
                      target="_blank"
                      aria-label="Home BTN"
                      color="primary"
                      style="text-transform: capitalize;"
                      class="google-font mr-4 mt-2"
                      depressed
                      large
                      dark
                    >Register for 1st August</v-btn>
                    <ScheduleDetails :data="ScheduleData[3]" />
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
            <v-tab-item value="day5" :class="$vuetify.theme.dark ? 'black' : 'white'">
              <v-container>
                <v-row>
                  <v-col>
                    <h3 class="google-font">Infrastructure</h3>
                    <p class="google-font" style="text-align:justify;">
                      Migrate and modernize workloads on Google's global, secure, and reliable infrastructure.
                    </p>
                    <v-btn
                      href="https://www.meetup.com/GDG-Nagpur/events/272140971/"
                      target="_blank"
                      aria-label="Home BTN"
                      color="primary"
                      style="text-transform: capitalize;"
                      class="google-font mr-4 mt-2"
                      depressed
                      large
                      dark
                    >Register for 2nd August</v-btn>
                    <ScheduleDetails :data="ScheduleData[4]" />
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
            <v-tab-item value="day6" :class="$vuetify.theme.dark ? 'black' : 'white'">
              <v-container>
                <v-row>
                  <v-col>
                    <h3 class="google-font">Security</h3>
                    <p class="google-font" style="text-align:justify;">
                      Detect, investigate, and respond to online threats to help protect your business.
                    </p>
                    <ComingSoon :data="'30th July, 2020'"/>
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
            <v-tab-item value="day7" :class="$vuetify.theme.dark ? 'black' : 'white'">
              <v-container>
                <v-row>
                  <v-col>
                    <h3 class="google-font">Security</h3>
                    <p class="google-font" style="text-align:justify;">
                      Detect, investigate, and respond to online threats to help protect your business.
                    </p>
                    <ComingSoon :data="'30th July, 2020'"/>
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
            <v-tab-item value="day8" :class="$vuetify.theme.dark ? 'black' : 'white'">
              <v-container>
                <v-row>
                  <v-col>
                    <h3 class="google-font">Security</h3>
                    <p class="google-font" style="text-align:justify;">
                      Detect, investigate, and respond to online threats to help protect your business.
                    </p>
                    <ComingSoon :data="'2nd August, 2020'"/>
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
            <v-tab-item value="day9" :class="$vuetify.theme.dark ? 'black' : 'white'">
              <v-container>
                <v-row>
                  <v-col>
                    <h3 class="google-font">Security</h3>
                    <p class="google-font" style="text-align:justify;">
                      Detect, investigate, and respond to online threats to help protect your business.
                    </p>
                    <ScheduleDetails :data="ScheduleData[8]" />
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
          </v-tabs-items>
        </v-col>
      </v-row>

    <v-row justify="center" align="center">
      <v-col md="8" xl="7">
        <SocialShare/>
      </v-col>
    </v-row>
    </v-container>
  </v-content>
</template>

<script>
import ScheduleDetails from "../components/Schedule/ScheduleDetails";
import ScheduleData from "../assets/data/schedule.json";
export default {
  name: "",
  components: {
    ScheduleDetails,
    ComingSoon:()=>import('@/components/common/ComingSoon'),
    SocialShare: () => import("@/components/common/SocialShare")
  },
  data: () => ({
    model: "day5",
    ScheduleData: [],
  }),
  mounted() {
    this.ScheduleData = ScheduleData
  },
  methods: {
    getMobileTab() {
      if (window.innerWidth < 500) return true;
      else return false;
    },
  },
};
</script>

<style >
.row-border-white {
  border-bottom: 1px solid #e0e0e0;
}
.row-border-dark {
  border-bottom: 1px solid #292929;
  background: #212121;
}
</style>
