<template>
  <div>
    <NavBar />
    <div class="max-w-1200 mx-auto" style="padding-top: 85px;">
      <h1 class="text-center">Find the Japanese Translation of the word you type below.</h1>
      <input v-model="text" placeholder="Enter your name" />
      <button v-on:click="call_api(text)">- Go! -</button>
      <div class="mt-2">You Searched: {{ text }}</div>
      <template v-if="output">
        <div v-for="(item, index) in output" :key="index">
          <div
            class="bg-gray-500 mb-5 flex flex-row"
            style="height: 15rem; box-shadow: 10px 10px 5px grey;"
          >
            <div class="bg-gray-100" style="height: 100%; flex-basis: 25%;">
              <div class="flex flex-col">
                <ruby style="font-size: 3rem;" class="pl-5 pt-10">
                  {{ item.term }}
                  <rt>{{ item.reading }}</rt>
                </ruby>
              </div>
            </div>
            <div class style="flex-basis: 75%;">{{ formatMeanings(item.meanings) }}</div>
          </div>
        </div>
      </template>
    </div>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue'
export default {
  components: {
    NavBar
  },
  data() {
    return {
      text: '',
      output: [],
      hasSearched: false
    }
  },
  methods: {
    async call_api(userIn) {
      this.hasSearched = true
      this.$axios
        .get(
          `https://cors-anywhere.herokuapp.com/http://beta.jisho.org/api/v1/search/words?keyword=\"${userIn}\"`
        )
        .then(response => {
          console.log(response)
          let output = []
          let results = response.data.data
          results.forEach(function(item) {
            //Other readings are alternate forms. Take just the main reading
            let terms = item.japanese[0].word
            let readings = item.japanese[0].reading
            /*
            let readings = []
            let terms = []
            item.japanese.forEach(vocab => {
              readings.push(vocab.reading)
              terms.push(vocab.word)
            })
            */
            let meanings = []
            item.senses.forEach(vocab => {
              meanings.push(vocab.english_definitions)
            })

            var result = {
              term: terms,
              reading: readings,
              meanings: meanings
            }
            output.push(result)
          })
          this.output = output
          console.log(this.output)
        })
    },
    formatMeanings(meaning) {
      let list = ''
      meaning.forEach(def => {
        let strList = ''
        def.forEach(defMeaning => {
          strList = strList.concat(defMeaning, ', ')
        })
        list = list.concat(strList, '\n')
      })
      console.log(list)
      return list
    }
  }
}
</script>

<style>
</style>