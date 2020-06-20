<template>
  <base-section id="theme-features">
    <base-section-heading title="KEUNGGULAN HALOPET">
      Halopet menyediakan berbagai fitur unggulan yang dapat kamu manfaatkan untuk keperluanmu, khususnya dalam hal menitipkan hewan. Fitur unggulan itulah yang akan membantumu menemukan hotel yang tepat untuk hewan kesayanganmu.
    </base-section-heading>

    <v-container>
      <v-row>
        <v-col
          v-for="(feature, i) in features"
          :key="i"
          cols="12"
          md="6"

        >
          <base-avatar-card
            v-bind="feature"
            align="left"
            horizontal
          >
          <v-row
          v-bind="feature"
          horizontal
          >
          <v-col

          v-text="feature.isi">

          </v-col>
          </v-row>

          </base-avatar-card>
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionThemeFeatures',

    data: () => ({
      features: [
        {
          color: 'yellow',
          title: 'Search for Pet Hotel',
          icon: 'mdi-home-search-outline',
          isi: 'Memudahkan anda mencari hotel untuk hewan kesayangan anda',
        },
        {
          color: 'yellow',
          title: 'Filter Your Pet Hotel',
          icon: 'mdi-tune',
          isi: 'Memudahkan anda melakukan filter sesuai dengan kebutuhan anda',
        },
        {
          color: 'yellow',
          title: 'Trusted Pet Hotel',
          icon: 'mdi-shield-check',
          isi: 'Menyediakan Hotel Hewan yang terpercaya ',
        },
        {
          color: 'yellow',
          title: 'Control Your Pet ',
          icon: 'mdi-hand',
          isi: 'Memudahkan anda mengontrol hewan yang anda dititipkan dengan fitur report/chat yang disediakan Halopet',
        },
        {
          color: 'yellow',
          title: 'Pick My Pet Up',
          icon: 'mdi-motorbike',
          isi:'Menyediakan fitur penjemputan hewan peliharaan anda',
        },
        {
          color: 'yellow',
          title: '24/7 Support',
          icon: 'mdi-help-circle-outline',
          isi:'Costumer service kami siap membantu anda 24 jam',
        },
      ],
    }),
  }
</script>
