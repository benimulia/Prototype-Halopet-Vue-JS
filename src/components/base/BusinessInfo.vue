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
          text: '(0274) 123 456<br>(0274) 789 012',
        },
        {
          icon: 'mdi-email',
          title: 'Email',
          text: 'cs@halopet.com<br>beni@halopet.com',
        },
      ],
    }),
  }
</script>
