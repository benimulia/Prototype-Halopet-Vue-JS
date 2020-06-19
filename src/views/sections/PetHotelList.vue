<template>
  <base-section
    id="info-alt"
    space="56"
  >
    <v-container>
        <v-parallax
            height="300"
            src="https://wallpaperaccess.com/full/1491613.jpg"

        ><v-container fill-height>
      <v-layout align-center>
        <v-flex>
          <h3 class="display-3">Welcome to Halopet Family</h3>

          <span class="subheading">Kami selalu berupaya memberikan pelayanan terbaik untuk kamu para pecinta hewan. Jadi terus ikuti kami di sosial media yang kami miliki dan login untuk mendapatkan banyak promo menarik.</span>

          <v-divider class="my-3"></v-divider>

          <div class="title mb-3">Check out our newest features!</div>

          <v-btn
            class="mx-0"
            color="primary"
            large
            to="contact-us"
          >
            See more
          </v-btn>
        </v-flex>
      </v-layout>
    </v-container></v-parallax>
      <v-row justify="space-between">
        <v-col
          cols="12"
          md="4"
        >
            <v-card light>
                <v-card-title
                >Sort Result
                </v-card-title>
                <v-card-subtitle>Sort your search results by:</v-card-subtitle>
                <v-card-text>
                    <v-radio-group v-model="row" row>
                        <v-radio label="Highest Price" value="radio-1"></v-radio>
                        <v-radio label="Lowest Price" value="radio-2"></v-radio>
                        <v-radio label="Highest Price" value="radio-1"></v-radio>
                        <v-radio label="Lowest Price" value="radio-2"></v-radio>
                    </v-radio-group>
                </v-card-text>
            </v-card> <br>
            <v-card light>
                <v-card-title
                >Filter Result
                <v-btn text class="ml-12 blue--text">Reset Filter</v-btn>
                </v-card-title>
                <v-card-subtitle>Showing results based on categories</v-card-subtitle>
                <hr>

                <v-card-title>Price Range Per Night</v-card-title>
                <v-card-subtitle>
                        <span>{{value1[0].toLocaleString()}}</span> <span > - {{value1[1].toLocaleString()}}</span>
                </v-card-subtitle>
                <v-card-text>
                    <v-range-slider
                        min="0"
                        max="1000000"
                        v-model="value1"
                    ></v-range-slider>
                </v-card-text>
            </v-card> <br>
            <v-card light>
                <v-card-title>Star Rating</v-card-title>
                <v-card-text>
                    <v-row dense>
                        <v-checkbox class="ml-2"></v-checkbox><v-icon color="orange darken-2">star</v-icon>
                    </v-row>
                    <v-row dense>
                        <v-checkbox class="ml-2"></v-checkbox><v-icon color="orange darken-2">star</v-icon><v-icon color="orange darken-2">star</v-icon>
                    </v-row>
                    <v-row dense>
                        <v-checkbox class="ml-2"></v-checkbox><v-icon color="orange darken-2">star</v-icon><v-icon color="orange darken-2">star</v-icon><v-icon color="orange darken-2">star</v-icon>
                    </v-row>
                    <v-row dense>
                        <v-checkbox class="ml-2"></v-checkbox><v-icon color="orange darken-2">star</v-icon><v-icon color="orange darken-2">star</v-icon><v-icon color="orange darken-2">star</v-icon><v-icon color="orange darken-2">star</v-icon>
                    </v-row>
                    <v-row dense>
                        <v-checkbox class="ml-2"></v-checkbox><v-icon color="orange darken-2">star</v-icon><v-icon color="orange darken-2">star</v-icon><v-icon color="orange darken-2">star</v-icon><v-icon color="orange darken-2">star</v-icon><v-icon color="orange darken-2">star</v-icon>
                    </v-row>
                </v-card-text>
            </v-card> <br>
            <v-card light>
                <v-card-title>Facilities</v-card-title>
                <v-card-text>
                    <v-row dense>
                        <v-checkbox class="ml-2" label="Pick Up"></v-checkbox>
                        <v-checkbox class="ml-2" label="Food"></v-checkbox>
                        <v-checkbox class="ml-2" label="Bath"></v-checkbox>
                        <v-checkbox class="ml-2" label="24 check-in"></v-checkbox>
                        <v-checkbox class="ml-2" label="Comfort Bed"></v-checkbox>
                    </v-row>
                </v-card-text>
            </v-card>
        </v-col>

        <v-col
          cols="12"
          md="8"
        >
        <h2>Showing (9) results..</h2>
        <v-container
            style="max-height: 1500px"
            class="overflow-y-auto"
        >
          <v-card
            light
            v-for="(item, i) in items"
            :key="i"
            @click="clickTest"
            class="clickable"
          >
            <div class="d-flex flex-no-wrap justify-space-between mb-3">
              <div>
                <v-card-title
                  class="headline"
                  v-text="item.title"
                ></v-card-title>

                <v-card-subtitle>
                <v-chip
                color="primary"
                outlined
                pill
                small
                >
                {{item.type}}
                </v-chip>
                <v-rating
                :value="item.rating"
                color="amber"
                dense
                half-increments
                readonly
                size="14"
                ></v-rating> ({{item.rating}})
                <v-icon>room</v-icon> {{item.location}}
                </v-card-subtitle>
                <br>
                <v-card-subtitle>
                    <s>30.000</s>
                    <h3 style="color:green">{{item.price}}</h3>
                </v-card-subtitle>
              </div>
              <v-avatar
                class="ma-3 mr-3"
                size="40%"
                tile
              >
                <v-img :src="item.src"></v-img>
              </v-avatar>
            </div>
          </v-card>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'PetHotelList',

    methods: {
        clickTest(){
          this.$router.push('pet-hotel-detail')

        }
    },

    data: () => ({
      value1: [0, 1000000],
      row: null,
      items: [
        {
          src: 'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcR_ET_UH5Jhj_y6U3H9tpIYGfA7apJqHQsSZjO91sKTqt6Ugjl-&usqp=CAU',
          title: 'Perdana Petshop',
          price: 'Rp 70.000',
          rating: '4',
          location: 'Patangpuluhan, Yogyakarta',
          type:'Pet Shop',
        },
        {
          src: 'https://awsimages.detik.net.id/community/media/visual/2018/06/13/c448ad03-5fa2-463e-906a-7cb5110c4484_169.jpeg?w=620',
          title: 'Halim Petshop',
          price: 'Rp 95.000',
          rating: '4.5',
          location: 'Gondokusuman, Yogyakarta',
          type:'Pet Shop',
        },
        {
          src: 'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcT06zjBCQsBBvzQrJFOuIxIVWBXNvRztwTOITpcnAUVdBXzhFK2&usqp=CAU',
          title: 'Hanna Maria',
          price: 'Rp 95.000',
          rating: '5',
          location: 'Pleret, Bantul',
          type:'Individu',
        },
        {
          src: 'https://cdn11.bigcommerce.com/s-yivsuh2/product_images/uploaded_images/dog-shop-no-type.jpg',
          title: 'Penitipan Hewan Argo',
          price: 'Rp 97.000',
          rating: '3',
          location: 'Jatinegara, Yogyakarta',
          type:'Pet Shop',
        },
        {
          src: 'https://sgp1.digitaloceanspaces.com/data-cdn/wp-content/uploads/2019/12/5-Dog-Lover-Cantik-Indonesia-Gemas-Banget.jpg.webp',
          title: 'Putri Rahmadika',
          price: 'Rp 100.000',
          rating: '4.7',
          location: 'Kotabaru, Yogyakarta',
          type:'Individu',
        },
        {
          src: 'https://media-cdn.tripadvisor.com/media/photo-s/11/88/3d/f3/a-good-place-for-dog.jpg',
          title: 'Rara Budianto',
          price: 'Rp 78.000',
          rating: '4.2',
          location: 'Gondomanan, Yogyakarta',
          type:'Individu',
        },
        {
          src: 'https://cdn.medcom.id/dynamic/content/2018/06/12/887708/ZzTBDrcM05.jpg?w=480',
          title: 'Petshop Tara',
          price: 'Rp 120.000',
          rating: '4.9',
          location: 'Tohpati, Yogyakarta',
          type:'Pet Shop',
        },
        {
          src: 'https://img.jakpost.net/c/2018/04/14/2018_04_14_44181_1523696457._medium.jpg',
          title: 'Susilo Ari Santosa',
          price: 'Rp 82.000',
          rating: '3.9',
          location: 'Condongcatur, Yogyakarta',
          type:'Individu',
        },
        {
          src: 'https://elangmedia.co.id/wp-content/uploads/2019/10/Bisnis-Petshop-Online.jpg',
          title: 'Petshop Narara',
          price: 'Rp 125.000',
          rating: '5',
          location: 'Seturan, Yogyakarta',
          type:'Pet Shop',
        },
      ],
    }),
  }
</script>
