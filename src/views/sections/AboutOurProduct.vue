<template>
  <base-section id="about-our-product">
    <base-section-heading
      color="grey lighten-2"
      icon="mdi-vuetify"
      title="About our Product"
    />

    <v-container>
      <v-row>
        <v-col
          v-for="card in cards"
          :key="card.title"
          cols="12"
          md="4"
        >
          <base-info-card v-bind="card" />
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionAboutOurProduct',

    data: () => ({
      cards: [
        {
          title: 'Easy to Find Your Pet Hotel',
          subtitle: 'Simple App',
          text: 'Melalui Halopet, kamu akan menemukan hotel untuk hewan kesayanganmu dengan sangat mudah dan cepat. Halopet menyediakan berbagai pilihan hotel hewan sesuai dengan keinginanmu melalui fitur filter yang ada.',
          callout: '01',
        },
        {
          title: 'Easy to Control Your Pet',
          subtitle: 'Control',
          text: 'Halopet menyediakan fitur Control untuk memantau keadaan hewan peliharaan kamu yang sedang dititipkan. Melalui fitur Chatting, kamu juga bisa bertanya tentang keadaan hewan kamu kepada pemiliki jasa penitipan hewan.',
          callout: '02',
        },
        {
          title: 'Get More promos here',
          subtitle: 'Special Offers',
          text: 'Halopet menyediakan berbagai macam promo yang dapat kamu gunakan. Terus ikuti sosial media ata pun website Halopet untuk keterangan lebih lanjut.',
          callout: '03',
        },
      ],
    }),
  }
</script>
