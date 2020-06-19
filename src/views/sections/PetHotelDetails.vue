<template>
<div>
  <v-card
    class="mx-auto mt-6 mb-8"
    max-width="80%"
  >
    <v-responsive :aspect-ratio="16/9">
      <v-card-title>
        <!-- <v-icon
          large
          left
        >
          mdi-twitter
        </v-icon> -->
        <span class="mb-1"><h2>Perdana Petshop</h2></span>
        <v-spacer></v-spacer><span><v-icon>bookmark_border</v-icon></span>
      </v-card-title>
      <v-card-subtitle>
        <v-chip
          color="primary"
          pill
          small
          class="mb-1"
          >
          Petshop
        </v-chip>
        <v-rating
          :value="4"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
          class="mb-1"
        ></v-rating> (4)
        <v-icon>room</v-icon> Patangpuluhan, Yogyakarta
      </v-card-subtitle>
      <v-card-text>
        <v-carousel
          cycle
          height="400"
          hide-delimiter-background
          show-arrows-on-hover
          class="mb-4"
        >
          <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
          >
          </v-carousel-item>
        </v-carousel>
        <v-row>
          <v-col
            align="right"
            cols="12"
          >
            <h3 class="mb-2">Price / day</h3>
            <h2 class="mb-3" style="color:#ff6f00">Rp 100.000</h2>
            <v-dialog v-model="dialog" persistent max-width="600px">
              <template v-slot:activator="{ on, attrs }">
                <v-btn
                  style="width:25%;"
                  color="#ff6f00"
                  class="white--text"
                  v-bind="attrs"
                  v-on="on"
                >BOOK NOW !
                </v-btn>
              </template>
              <v-card>
                <v-card-title>
                  <span class="headline">Your Information</span>
                </v-card-title>
                <v-card-text>
                  <v-container>
                    <v-row>
                      <!-- <v-col cols="12" sm="6" md="4">
                        <v-text-field label="Legal first name*" required></v-text-field>
                      </v-col>
                      <v-col cols="12" sm="6" md="4">
                        <v-text-field label="Legal middle name" hint="example of helper text only on focus"></v-text-field>
                      </v-col>
                      <v-col cols="12" sm="6" md="4">
                        <v-text-field
                          label="Legal last name*"
                          hint="example of persistent helper text"
                          persistent-hint
                          required
                        ></v-text-field>
                      </v-col> -->
                      <v-col cols="12">
                        <v-text-field label="Full Name*" required></v-text-field>
                      </v-col>
                      <v-col cols="12" sm="6" md="6">
                        <v-text-field label="Mobile Number*" type="number" min="0" step="1" oninput="validity.valid||(value='');" required persistent-hint hint="e.g. 081234567890"></v-text-field>
                      </v-col>
                      <v-col cols="12" sm="6" md="6">
                        <v-text-field label="Email Address*" type="email"></v-text-field>
                      </v-col>
                      <v-col cols="12">
                        <v-text-field label="Your Pet Name" type="text" required></v-text-field>
                      </v-col>
                      <v-col cols="12" sm="6">
                        <v-select
                          :items="['Cat', 'Dog', 'Bird', 'Reptile', 'Rabbit']"
                          label="Pet Type*"
                          required
                        ></v-select>
                      </v-col>
                      <v-col cols="12" sm="6">
                        <v-autocomplete
                          :items="['Pick Up','Best Food','Best Cage','Own Food']"
                          label="Special Request"
                          multiple
                        ></v-autocomplete>
                      </v-col>
                      <v-col cols="12">
                        <v-text-field label="Notes" type="text" required persistent-hint hint="Place your additional notes like your pet allergy, special request, etc."></v-text-field>
                      </v-col>
                    </v-row>
                  </v-container>
                  <small>*indicates required field</small>
                </v-card-text>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn color="blue darken-1" text @click="dialog = false">Close</v-btn>
                  <v-btn color="blue darken-1" text @click="dialog = false">Save</v-btn>
                </v-card-actions>
              </v-card>
            </v-dialog>
          </v-col>
          <v-col><v-divider></v-divider></v-col>
          <v-col
            align="left"
            cols="12"
          >
            <base-title
              space="0"
              title="FACILITIES"
              class="mb-3"
              weight="500"
            />
            <v-card
              class="d-flex flex-row mb-6"
              flat
              tile
            >
              <span
                class="pa-8 mr-4"
                outlined
                tile
                align="center"
              > <v-icon x-large color="blue darken-2">ac_unit</v-icon> <br>
                <h3>AC</h3>
              </span>
              <span
                class="pa-8 mr-4"
                outlined
                tile
                align="center"
              > <v-icon x-large color="blue darken-2">nights_stay</v-icon> <br>
                <h3>Open Until Night</h3>
              </span>
              <span
                class="pa-8 mr-4"
                outlined
                tile
                align="center"
              > <v-icon x-large color="blue darken-2">fastfood</v-icon> <br>
                <h3>Food</h3>
              </span>
              <span
                class="pa-8 mr-4"
                outlined
                tile
                align="center"
              > <v-icon x-large color="blue darken-2"> mdi-shower-head</v-icon> <br>
                <h3>Shower</h3>
              </span>
              <span
                class="pa-8 mr-4"
                outlined
                tile
                align="center"
              > <v-icon x-large color="blue darken-2">mdi-dog-service</v-icon> <br>
                <h3>Pet Training</h3>
              </span>
              <span
                class="pa-8 mr-4"
                outlined
                tile
                align="center"
              > <v-icon x-large color="blue darken-2">mdi-bed</v-icon> <br>
                <h3>Comfort Bed</h3>
              </span>
            </v-card>
          </v-col>
        </v-row>
      </v-card-text>
    </v-responsive>
  </v-card>
  <v-card
    class="mx-auto mt-6 mb-8"
    max-width="80%"
  >
      <v-card-title>
        <!-- <v-icon
          large
          left
        >
          mdi-twitter
        </v-icon> -->
        <span class="mb-1"><h3>Location Info</h3></span>
      </v-card-title>
      <v-card-subtitle>
        <v-icon>room</v-icon> Jl. Patangpuluhan No.11, Yogyakarta 55243
      </v-card-subtitle>
      <v-card-text>
        <iframe
          allowfullscreen
          aria-hidden="false"
          frameborder="0"
          height="200"
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15812.486303688762!2d110.38427866372041!3d-7.776931499658068!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e7a5828f6fb7ef7%3A0xb710cc588f40770e!2sUniversitas%20Kristen%20Duta%20Wacana!5e0!3m2!1sen!2sid!4v1590846799947!5m2!1sen!2sid"
          style="border:0; display: block;"
          tabindex="0"
          width="100%"
          class="mb-2"
        />
        <div
          align="center"
        >
          This Petshop can pick up your pet
        </div>
      </v-card-text>
  </v-card>
  <v-card
    class="mx-auto mt-6 mb-8"
    max-width="80%"
  >
      <v-card-title>
        <!-- <v-icon
          large
          left
        >
          mdi-twitter
        </v-icon> -->
        <span class="mb-1"><h3>Customer Review</h3></span>
      </v-card-title>
      <v-card-text>
        <v-row>
          <v-col sm="12">
            <v-card
              class="pa-2"
              outlined
              tile
            >
              <div class="col-4">
                19 Juni 2020
              </div>
              <div class="col-12">
                Petshopnya keren, pegawai nya ramah dan peliharaan saya dirawat dengan baik.
              </div>
              <div align="right">
                <v-icon>mdi-account-circle</v-icon> Sulaiman
              </div>
            </v-card><v-card
              class="pa-2"
              outlined
              tile
            >
              <div class="col-4">
                17 Juni 2020
              </div>
              <div class="col-12">
                Saya sangat suka dengan pelayanannya
              </div>
              <div align="right">
                <v-icon>mdi-account-circle</v-icon> Burhan
              </div>
            </v-card><v-card
              class="pa-2"
              outlined
              tile
            >
              <div class="col-4">
                16 Juni 2020
              </div>
              <div class="col-12">
                Wah bagus banget nih pelayanan petshopnya!
              </div>
              <div align="right">
                <v-icon>mdi-account-circle</v-icon> Siska
              </div>
            </v-card>
          </v-col>
          <v-col align="right">
            <v-btn color="blue darken-1" text>SEE MORE</v-btn>
          </v-col>
        </v-row>
      </v-card-text>
  </v-card>
</div>
</template>

<script>
  export default {
    data () {
      return {
        dialog: false,
        items: [
          {
            src: 'https://awsimages.detik.net.id/community/media/visual/2018/06/13/c448ad03-5fa2-463e-906a-7cb5110c4484_169.jpeg?w=620',
          },
          {
            src: 'https://cdn.medcom.id/dynamic/content/2018/06/12/887708/ZzTBDrcM05.jpg?w=480',
          },
          {
            src: 'https://cdn11.bigcommerce.com/s-yivsuh2/product_images/uploaded_images/dog-shop-no-type.jpg',
          },
        ],
      }
    },
  }
</script>