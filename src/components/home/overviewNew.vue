<template>
    <v-row>
        <v-col cols="12">
            <p class="google-font" offset-cols="1" :class="this.$vuetify.theme.dark?'white--text':'grey--text text--darken-2'" style="font-weight: 350;font-size:200%">Themes</p>
        </v-col>
        <v-col md="4" cols="12" sm="4">
            <v-card class="pa-5 elevation-0" outlined :class="$vuetify.theme.dark == true ? 'darkModeCard' : 'whiteThemeCard'">
                <h2 class="google-font mt-2 mb-2">Industry Insights</h2>
                <p class="google-font">Insights from Google Cloud executives, focusing on transformational efforts across industries working with customers and ecosystem partners.</p>
                <p class="google-font mt-5 mb-0" style="font-size:120%">Follow <a href="https://twitter.com/GDG_Surat/status/1282948449269280773" target="_blank"><b>@gdg_surat</b></a></p>
            </v-card>
        </v-col>
        <v-col md="4" cols="12" sm="4">
            <v-card class="pa-5 elevation-0" outlined :class="$vuetify.theme.dark == true ? 'darkModeCard' : 'whiteThemeCard'">
                <h2 class="google-font mt-2 mb-2">Productivity & Collaboration</h2>
                <p class="google-font">Change the way teams work with solutions designed for humans and built for impact.</p>
                <p class="google-font mt-5 mb-0" style="font-size:120%">Follow <a href="https://twitter.com/gdgnashik/status/1284811131136045056" target="_blank"><b>@gdgnashik</b></a></p>
            </v-card>
        </v-col>
        <v-col md="4" cols="12" sm="4">
            <v-card class="pa-5 elevation-0" outlined :class="$vuetify.theme.dark == true ? 'darkModeCard' : 'whiteThemeCard'">
                <h2 class="google-font mt-2 mb-2">Infrastructure</h2>
                <p class="google-font">Migrate and modernize workloads on Google's global, secure, and reliable infrastructure.</p>
                <p class="google-font mt-5 mb-0" style="font-size:120%">Follow <a href="https://twitter.com/GDGCloudAhm" target="_blank"><b>@GDGCloudAhm</b></a></p>
            </v-card>
        </v-col>
    </v-row>
</template>