<script>
  // Extensions
  import View from '@/views/View'

  // Mixins
  import LoadSections from '@/mixins/load-sections'

  export default {
    name: 'Payment',

    metaInfo: { title: 'Payment' },

    extends: View,

    mixins: [
      LoadSections([
        'payment',
        'info',
      ]),
    ],

    props: {
      id: {
        type: String,
        default: 'payment',
      },
    },
  }
</script>
