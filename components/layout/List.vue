<template>
  <v-card>
    <v-card-title>
      리스트
      <v-spacer></v-spacer>
      <v-text-field
        v-model="search"
        append-icon="mdi-magnify"
        label="검색"
        single-line
        hide-details
      ></v-text-field>
    </v-card-title>
    <v-data-table
      :headers="headers"
      :items="stores"
      :search="search"
    >
    </v-data-table>
  </v-card>
</template>
<script>
  export default {
    data () {
      return {
        search: '',
        headers: [
          {
            text: '순번',
            align: 'start',
            sortable: false,
            value: 'no',
          },
          { text: '약국', value: 'name' },
          { text: '주소', value: 'address' },
          { text: '번호', value: 'phone' },
          { text: '운영 시간', value: 'serviceTime' }
        ],
        stores: [
          {
            no: 1,
            name: '배곧다온약국',
            address: '경기도 시흥시 배곧3로 86, 1층 107호',
            phone: '031-431-1661',
            serviceTime: '09:00 ~ 19:00'
          },
          {
            no: 2,
            name: '지성약국',
            address: '경기도 시흥시 배곧4로 32-27 109호',
            phone: '031-319-1065',
            serviceTime: '10:00 ~ 19:00'
          },
          {
            no: 3,
            name: 'M메디칼약국',
            address: '경기도 시흥시 배곧3로 96 M플러스 1층 130호',
            phone: '031-499-7599',
            serviceTime: '08:30 ~ 13:30'
          },
          {
            no: 4,
            name: '푸른약국',
            address: '경기도 시흥시 역전로301번길 34',
            phone: '031-432-0250',
            serviceTime: '09:00 ~ 12:00'
          },
          {
            no: 5,
            name: '세종약국',
            address: '경기 시흥시 정왕1동 2014-2',
            phone: '031-432-7200',
            serviceTime: '14:00 ~ 18:00'
          },
          {
            no: 6,
            name: '정왕라성약국',
            address: '경기도 시흥시 옥구상가3길 7-1',
            phone: '031-496-9693',
            serviceTime: '10:00 ~ 16:00'
          },
          {
            no: 7,
            name: '해수약국',
            address: '경기도 시흥시 정왕동 1726-1 광개토왕빌딩 305호',
            phone: '031-432-5721',
            serviceTime: '10:00 ~ 17:00'
          },
          {
            no: 8,
            name: '종로세명약국',
            address: '경기도 시흥시 정왕대로 220 중심상가1길 1 (1층)',
            phone: '031-431-4044',
            serviceTime: '10:00 ~ 23:00'
          },
          {
            no: 9,
            name: '굿모닝약국',
            address: '경기도 시흥시 정왕대로 220 중심상가1길 1 (3층)',
            phone: '031-319-8286',
            serviceTime: '09:00 ~ 13:00'
          },
          {
            no: 10,
            name: '정문약국',
            address: '경기도 시흥시 정왕대로 230 제일프라자(중심상가3길 15)',
            phone: '031-496-0903',
            serviceTime: '09:00 ~ 14:00'
          },
          {
            no: 11,
            name: '시화연합약국',
            address: '경기도 시흥시 정왕대로 56 세종월드',
            phone: '031-499-5221',
            serviceTime: '09:00 ~ 21:00'
          },
          {
            no: 12,
            name: '한중약국',
            address: '경기도 시흥시 정왕시장길 62',
            phone: '031-319-0569',
            serviceTime: '10:00 ~ 22:00'
          },
          {
            no: 13,
            name: '삼성약국',
            address: '경기도 시흥시 정왕신길로139번길 5',
            phone: '031-432-6300',
            serviceTime: '08:00 ~ 22:00'
          },
          {
            no: 14,
            name: '정왕한사랑약국',
            address: '경기도 시흥시 정왕신길로49번길 19',
            phone: '031-497-7873',
            serviceTime: '09:00 ~ 13:00'
          },
          {
            no: 15,
            name: '건강약국',
            address: '경기도 시흥시 중심상가4길 18 중심상가2길 16',
            phone: '031-433-3923',
            serviceTime: '09:00 ~ 21:30'
          },
          {
            no: 16,
            name: '시화라성약국',
            address: '경기도 시흥시 중심상가로 143',
            phone: '031-498-8704',
            serviceTime: '09:00 ~ 23:00'
          },
          {
            no: 17,
            name: '영남녹십자약국',
            address: '경기도 시흥시 중심상가로 224 영남아파트(중심상가로 41)',
            phone: '031-497-4544',
            serviceTime: '10:00 ~ 22:00'
          },
          {
            no: 18,
            name: '영남녹십자약국',
            address: '경기도 시흥시 중심상가로 224 영남아파트(중심상가로 41)',
            phone: '031-497-4544',
            serviceTime: '10:00 ~ 22:00'
          },
          {
            no: 19,
            name: '하나로약국',
            address: '경기도 시흥시 평안상가1길 17 정왕천동로 47',
            phone: '031-433-9350',
            serviceTime: '09:00 ~ 23:00'
          }
        ],
      }
    },
  }
  </script>