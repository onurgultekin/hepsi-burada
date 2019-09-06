<template>
  <div>
    <div class="max-w-lg rounded overflow-hidden shadow-md mx-auto">
      <div class="px-6 py-4 text-center">
        <button v-if="!submitClicked" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded inline-flex items-center outline-none" @click="submitClick()">
          <svg class="fill-current w-4 h-4 mr-2" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
            viewBox="0 0 52 52" style="enable-background:new 0 0 52 52;" xml:space="preserve">
          <path d="M26,0C11.664,0,0,11.663,0,26s11.664,26,26,26s26-11.663,26-26S40.336,0,26,0z M38.5,28H28v11c0,1.104-0.896,2-2,2
            s-2-0.896-2-2V28H13.5c-1.104,0-2-0.896-2-2s0.896-2,2-2H24V14c0-1.104,0.896-2,2-2s2,0.896,2,2v10h10.5c1.104,0,2,0.896,2,2
            S39.604,28,38.5,28z"/>
          <g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g>
          </svg>
          <span>Submit a link</span>
        </button>
        <button v-else class="bg-gray-500 hover:bg-gray-600 text-white font-bold py-2 px-4 rounded inline-flex items-center outline-none" @click="returnToLinksClick()">
          <svg class="fill-current w-4 h-4 mr-2" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
              viewBox="0 0 492 492" style="enable-background:new 0 0 492 492;" xml:space="preserve">
            <g>
              <g>
                <path d="M464.344,207.418l0.768,0.168H135.888l103.496-103.724c5.068-5.064,7.848-11.924,7.848-19.124
                  c0-7.2-2.78-14.012-7.848-19.088L223.28,49.538c-5.064-5.064-11.812-7.864-19.008-7.864c-7.2,0-13.952,2.78-19.016,7.844
                  L7.844,226.914C2.76,231.998-0.02,238.77,0,245.974c-0.02,7.244,2.76,14.02,7.844,19.096l177.412,177.412
                  c5.064,5.06,11.812,7.844,19.016,7.844c7.196,0,13.944-2.788,19.008-7.844l16.104-16.112c5.068-5.056,7.848-11.808,7.848-19.008
                  c0-7.196-2.78-13.592-7.848-18.652L134.72,284.406h329.992c14.828,0,27.288-12.78,27.288-27.6v-22.788
                  C492,219.198,479.172,207.418,464.344,207.418z"/>
              </g>
            </g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g>
          </svg>
          <span>Return to links</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'SubmitLink',
  methods: {
    submitClick () {
      this.$store.commit('submitClicked', true)
    },
    returnToLinksClick () {
      this.$store.commit('submitClicked', false)
    }
  },
  computed:
    mapState({
      submitClicked: state => state.submitClicked
    })
}
</script>
