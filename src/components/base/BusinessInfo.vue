<template>
  <v-theme-provider :dark="dark">
    <div>
      <base-info-card
        title="KEEP IN TOUCH WITH US"
        pace="6"
      >
        Hubungi kami di media sosial yang tersedia. Kami akan merespon pesanmu dengan cepat.
      </base-info-card>

      <base-business-contact dense />
    </div>
  </v-theme-provider>
</template>

<script>
  export default {
    name: 'BaseBusinessInfo',

    props: { dark: Boolean },

    data: () => ({
      business: [
        {
          icon: 'mdi-map-marker-outline',
          title: 'Address',
          text: 'Jl. Dr. Wahidin Sudirohusodo No.5-25<br>Gondokusuman, Yogyakarta 55125',
        },
        {
          icon: 'mdi-cellphone',
          title: 'Phone',
          text: '088216152324',
        },
        {
          icon: 'mdi-email',
          title: 'Email',
          text: 'beni.mulia@si.ukdw.ac.id <br> nikolaus.wijaya@si.ukdw.ac.id',
        },
      ],
    }),
  }
</script>
