<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
      clipped
    >
      <v-list dense>
        <v-subheader class="mt-4 grey--text text--darken-1">SUBSCRIPTIONS</v-subheader>
        <v-list>
          <v-list-item
            v-for="item in profile"
            :key="item.text"
            link
          >
            <v-list-item-avatar>
              <img
                :src="`${item.picture}`"
                :alt="`${item.text}`"
              >
            </v-list-item-avatar>
            <v-list-item-title v-text="item.text" />
          </v-list-item>
        </v-list>
        <v-list-item
          class="mt-4"
          link
        >
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      clipped-left
      color="red"
      dense
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-icon class="mx-4">fab fa-youtube</v-icon>
      <v-toolbar-title class="mr-12 align-center">
        <span class="title">Sihueng Mask Information</span>
      </v-toolbar-title>
      <v-spacer />
    </v-app-bar>

    <v-content>
      <v-container class="fill-height">
        <v-row
          justify="center"
          align="center"
        >
          <v-alert
            icon="mdi-shield-lock-outline"
            prominent
            text
            type="info"
          >
            본 사이트는 시흥 시내의 마스크 판매 약국을 안내해 주는 사이트입니다.<br>
            경기도 시흥시청의 약국 운영 현황 데이터를 통해 제작 되었습니다.
          </v-alert>
        </v-row>
        <v-row
          justify="center"
          align="center"
        >
          <List />
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import Vue from "vue"
import List from '~/components/layout/List'
import Vuetify from "vuetify"
Vue.use(Vuetify)

export default {
    components: {
      List
    },
    props: {
      source: String,
    },
    data: () => ({
      drawer: null,
      profile: [
        {
          picture: "https://scontent-ssn1-1.xx.fbcdn.net/v/t1.0-9/79198884_1340919062745797_6705783545060655104_n.jpg?_nc_cat=105&_nc_sid=85a577&_nc_oc=AQk-KbR_ZU0kFveJcyxg2Qg_tfE8laosxj0XL6OvryZ7L8zyPmuFuxguRZIKVNXSYiY&_nc_ht=scontent-ssn1-1.xx&oh=aa0368b6df321c4ab45a67321d492ebe&oe=5E94215E",
          text: '백계훈',
          link: 'https://github.com/BackGyeHoon'
        }
      ],
    }),
    created () {
      this.$vuetify.theme.dark = true
    },
  }
</script>

<style scoped lang="scss">
.container {
  width: 100%;
  height: auto;
}
</style>
