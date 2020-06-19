<script>
  // Extensions
  import View from '@/views/View'

  // Mixins
  import LoadSections from '@/mixins/load-sections'

  export default {
    name: 'HotelDetail',

    metaInfo: { title: 'Pet-Hotel-Detail' },

    extends: View,

    mixins: [
      LoadSections([
        'pet-hotel-details',
        'info',
      ]),
    ],

    props: {
      id: {
        type: String,
        default: 'hotel-detail',
      },
    },
  }
</script>
