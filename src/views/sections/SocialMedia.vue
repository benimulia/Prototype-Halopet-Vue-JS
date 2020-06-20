<template>
  <v-theme-provider dark>
    <base-section
      id="social"
      class="accent text-center"
      space="56"
    >
      <base-icon class="mb-8">
        mdi-instagram
      </base-icon>

      <base-section-heading
        color="transparent"
        title="Social Media"
      >
      Anda dapat melakukan kontak dengan kami melalui media sosial/website kami
      </base-section-heading>

      <a
        class="d-inline-block mb-8"
        href="https://halopet.fti.ukdw.ac.id/"
        style="text-decoration: none;"
        target="_blank"
      >
        https://halopet.fti.ukdw.ac.id/
      </a>

      <div class="py-4" />

      <v-btn
        class="font-weight-bold"
        color="white"
        href="https://www.instagram.com/siukdw/"
        light
        min-width="168"
        target="_blank"
        x-large
      >
        Follow Us

        <v-icon right>
          mdi-open-in-new
        </v-icon>
      </v-btn>
    </base-section>
  </v-theme-provider>
</template>

<script>
  export default {
    name: 'SectionNews',

    provide: {
      heading: { align: 'center' },
    },
  }
</script>
