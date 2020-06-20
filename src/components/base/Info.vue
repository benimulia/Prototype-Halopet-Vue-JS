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
        Halopet merupakan suatu usaha bisnis berbasis teknologi yang menyediakan wadah atau media untuk mempertemukan orang yang bersedia merawat hewan peliharaan (profesional maupun pecinta) dengan pemilik hewan yang akan menitipkan hewan peliharaannya.
      </base-body>


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
