<template>
  <section id="hero">
    <v-img
      :min-height="minHeight"
      :src="require('@/assets/home-dog.jpg')"
      class="white--text"
      gradient="to right, rgba(5, 11, 31, .8), rgba(5, 11, 31, .8)"
    >
      <v-container class="fill-height px-4 py-12">
        <v-responsive
          class="d-flex align-center"
          height="100%"
          max-width="700"
          width="100%"
        >
          <base-heading title="FIND YOUR PET HOTEL HERE!" />

          <base-body>
            Temukan tempat terbaik untuk menitipkan hewan peliharaanmu di sini. Pilih lokasi dan kriteria hotel yang kamu mau.
            Halopet menyediakan berbagai macam pilihan hotel hewan untuk menitipkan hewan kesayanganmu.
          </base-body>

          <div
            :class="$vuetify.breakpoint.smAndDown ? 'flex-column align-start' : 'align-center'"
            class="d-flex flex-wrap"
          >
            <!-- <base-text-field
            hide-details
            label="Input Location"
          >
            <template v-slot:append-outer>
              <v-btn
                class="ml-n1"
                height="40"
                outlined
                style="margin-top: -7px;"
              >
                SEARCH
              </v-btn>
            </template>
            </base-text-field> -->
             <v-card
              class=""
              color="#ffffff"
              width="80%"
             >
              <v-card-text>
                <v-container>
                  <v-row>
                     <v-col cols="12" sm="12" md="12">
                      <v-text-field
                        id="location"
                        label="Location"
                        name="location"
                        prepend-icon="my_location"
                        type="text"
                        required
                        light
                      />
                     </v-col>
                     <v-col cols="12" sm="6" md="6">
                       <v-menu
                          v-model="menu1"
                          :close-on-content-click="false"
                          :nudge-right="40"
                          transition="scale-transition"
                          offset-y
                          min-width="290px"
                          light
                        >
                          <template v-slot:activator="{ on }">
                            <v-text-field
                              v-model="date1"
                              label="Check-In"
                              prepend-icon="event"
                              readonly
                              v-on="on"
                              light
                            ></v-text-field>
                          </template>
                          <v-date-picker
                            v-model="date1"
                            @input="menu1 = false"
                            min="2020-06-04">
                          </v-date-picker>
                        </v-menu>
                     </v-col>
                     <v-col cols="12" sm="6" md="6">
                       <v-menu
                          v-model="menu2"
                          :close-on-content-click="false"
                          :nudge-right="40"
                          transition="scale-transition"
                          offset-y
                          min-width="290px"
                          light
                        >
                          <template v-slot:activator="{ on }">
                            <v-text-field
                              v-model="date2"
                              label="Check-Out"
                              prepend-icon="event"
                              readonly
                              v-on="on"
                              light
                            ></v-text-field>
                          </template>
                          <v-date-picker
                            v-model="date"
                            @input="menu2 = false"
                            min="2020-06-04">
                          </v-date-picker>
                        </v-menu>
                     </v-col>
                     <v-col cols="12" sm="6" md="6">
                        <v-select
                        :items="items"
                        label="Pet"
                        light
                        prepend-icon="pets"
                        >
                        </v-select>
                     </v-col>
                     <v-col cols="12" sm="6" md="6">
                     </v-col>
                     <v-col cols="12" sm="6" md="6">
                        <v-select
                        :items="items2"
                        label="Filter"
                        light
                        prepend-icon="tune"
                        >
                        </v-select>
                     </v-col>
                     <v-col cols="12" sm="12" md="12">
                         <v-btn to="/pet-hotel" class="blue--text" color="#ffcc00" dark large block>Search</v-btn>
                     </v-col>
                  </v-row>
                </v-container>
              </v-card-text>
              <v-card-actions>
                <v-spacer />

              </v-card-actions>
            </v-card>
          </div>
        </v-responsive>
      </v-container>
    </v-img>
  </section>
</template>

<script>
  export default {
    name: 'SectionHero',

    data: () => ({
      date1: new Date().toISOString().substr(0, 10),
      date2: new Date().toISOString().substr(0, 10),
      menu1: false,
      menu2: false,
      items: ['Dog', 'Cat', 'Bird', 'Fish', 'Reptile'],
      items2: ['Near', 'Far', 'Cheap', 'Expensive', 'Rating'],
    }),

    provide: {
      theme: { isDark: true },
    },

    computed: {
      minHeight () {
        const height = this.$vuetify.breakpoint.mdAndUp ? '100vh' : '50vh'

        return `calc(${height} - ${this.$vuetify.application.top}px)`
      },
    },
  }
</script>
