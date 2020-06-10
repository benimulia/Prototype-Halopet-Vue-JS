<script>
  // Extensions
  import View from '@/views/View'

  // Mixins
  import LoadSections from '@/mixins/load-sections'

  export default {
    name: 'Hotel',

    metaInfo: { title: 'Pet-Hotel' },

    extends: View,

    mixins: [
      LoadSections([
        'pet-hotel-list',
        'info',
      ]),
    ],

    props: {
      id: {
        type: String,
        default: 'hotel',
      },
    },
  }
</script>
