<template>
<div>
    <base-section id="about-our-product">
    <base-section-heading
      color="grey lighten-2"
      title="Booking Confirmation"
    />

    <v-container>
      <v-row>
        <v-col
          align="left"
          cols="12"
          md="4"
        >
            <base-info-card
                title="Price Details"
                pace="6"
            >
            </base-info-card>
        </v-col>
        <v-col
            cols="12"
            md="8"
        ></v-col>
        <v-col>
            <v-card
                width="60%"
                class="mb-8 "
            >
                <v-responsive :aspect-ratio="16/9">
                    <v-card-text>
                        <h4>(1x) Day Pet Hotel</h4> <v-spacer></v-spacer> <h4>Rp 100.000</h4>
                    </v-card-text>
                </v-responsive>
            </v-card>
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</div>
</template>

<script>
  export default {
    data () {
      return {

      }
    },
  }
</script>