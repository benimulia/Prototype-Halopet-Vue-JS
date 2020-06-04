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
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis illum veniam cum dolores ratione commodi beatae quas maxime, laboriosam excepturi solut!
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
        },
        {
          color: 'yellow',
          title: 'Filter Your Pet Hotel',
          icon: 'mdi-tune',
        },
        {
          color: 'yellow',
          title: 'Trusted Pet Hotel',
          icon: 'mdi-shield-check',
        },
        {
          color: 'yellow',
          title: 'Control Your Pet ',
          icon: 'mdi-hand',
        },
        {
          color: 'yellow',
          title: 'Pick My Pet Up',
          icon: 'mdi-motorbike',
        },
        {
          color: 'yellow',
          title: '24/7 Support',
          icon: 'mdi-help-circle-outline',
        },
      ],
    }),
  }
</script>
