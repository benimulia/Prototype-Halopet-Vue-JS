<template>
  <base-section
    id="features"
    class="secondary"
  >
    <v-responsive
      class="mx-auto"
      max-width="1350"
    >
      <v-container fluid>
        <v-row>
          <v-col
            v-for="card in cards"
            :key="card.title"
            cols="12"
            sm="4"
            md="3"
          >
            <base-info-card
              align="center"
              dark
              v-bind="card"
            />
          </v-col>
        </v-row>
      </v-container>
    </v-responsive>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionFeatures',

    data: () => ({
      cards: [
        {
          icon: 'mdi-open-in-app',
          title: 'Access Halopet',
          text: 'Akses aplikasi Halopet melalui platform website maupun mobile app.',
        },
        {
          icon: 'mdi-book-open-outline',
          title: 'Book for Your Pet Hotel',
          text: 'Pesan hotel untuk hewan kesayanganmu sesuai dengan keinginanmu di Halopet.',
        },
        {
          icon: 'mdi-cash-usd-outline',
          title: 'Payment',
          text: 'Bayar tagihan melalui jalur pembayaran yang tersedia. Tentu saja pembayaran di Halopet sudah terjamin dan pastinya aman.',
        },
        {
          icon: 'mdi-check-circle-outline',
          title: 'Done',
          text: 'Jika sudah melakukan pembayaran, kamu dapat meminta penyedia jasa penitipan hewan untuk menjemput hewan peliharaanmu. Kemudian kamu dapat memantau kondisi hewan peliharaanmu melalui aplikasi Halopet. ',
        },
      ],
    }),
  }
</script>
