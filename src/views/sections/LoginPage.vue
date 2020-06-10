<template>
  <base-section
    id="pro-features"
  >
    <v-img
      :src="require('@/assets/logo-halopet-2.png')"
      class="mx-auto mb-8"
      max-width="200"
    />

    <base-section-heading title="Login Page">
      Login now to <strong>Halopet</strong> and you will<br>get more promos.
    </base-section-heading>

    <v-container>
      <v-row
        align="center"
        justify="center"
      >
        <v-col
          cols="12"
          md="5"
        >

          <div class="text-center">
          <v-card
              color="#ffffff"
              width="100%"
              flat

             >
              <v-card-text>
                <v-container>
                  <v-row>
                     <v-col cols="12" sm="12" md="12">
                        <v-text-field
                            label="Email"
                            name="login"
                            prepend-icon="mdi-account"
                            type="text"
                        ></v-text-field>
                     </v-col>
                     <v-col cols="12" sm="12" md="12">
                        <v-text-field
                            id="password"
                            label="Password"
                            name="password"
                            prepend-icon="mdi-lock"
                            type="password"
                        ></v-text-field>
                     </v-col>
                     <v-col cols="12" sm="12" md="12">
                         <v-btn class="black--text" color="#ffcc00" dark large block>Login</v-btn>
                     </v-col>
                  </v-row>
                </v-container>
              </v-card-text>
              <v-card-actions>
                <v-spacer />

              </v-card-actions>
            </v-card>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionProChart',

    data: () => ({
      features: [
        ['Components', 23, '40+'],
        ['Example Pages', 3, 10],
        ['Bugfixes and Issues', true, true],
        ['Vue CLI Support', true, true],
        ['News, Project, and Pricing Pages', false, true],
        ['6 Months Free Updates', false, true],
        ['Price', 'Free', '$60'],
      ],
    }),
  }
</script>
