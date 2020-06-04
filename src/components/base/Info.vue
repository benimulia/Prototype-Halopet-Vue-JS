<template>
  <v-theme-provider :dark="dark">
    <div>
      <base-img
        :src="require('@/assets/logo-halopet-1.png')"
        contain
        max-width="128"
        max-height="120"
        width="100%"
        space="10"
      />
      <br><br>
      <base-title
        size="body-1"
        space="4"
        title="HALOPET"
        weight="regular"
      />

      <base-body>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo pariatur quidem, quis modi iure nihil commodi suscipit, corporis dicta adipisci, voluptatum quia cupiditate. Nulla minus voluptatum nostrum deleniti, asperiores facere.
      </base-body>

      <base-btn
        class="mb-12"
        color="white"
        outlined
      >
        More Info
      </base-btn>
    </div>
  </v-theme-provider>
</template>

<script>
  export default {
    name: 'BaseInfo',

    props: {
      title: String,
      dark: Boolean,
    },

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
