<template>
  <div class=" pl-5 pr-5 w-full flex flex-wrap">
    <div v-for="index in subArrays" :key="index" class="w-1/5">
      <div v-for="card in index" :key="card" class="w-full">
        <div class="w-full p-2">
          <Card :src="`${card.src}`" class="w-full h-full"/>
        </div>
    </div>
    </div>
  </div>
</template>

<script>
import { reactive, computed } from 'vue'
import Card from '../components/Card.vue'
export default {
  name: 'HomeView',
  components: {
    Card
  },
  setup(){
    let cards = reactive([
      {
        src: '001.jpeg',
        title: 'Title 1',
        user: 'User 1',
      },{
        src: '002.jpeg',
        title: 'Title 2',
        user: 'User 2',
      },{
        src: '003.jpeg',
        title: 'Title 3',
        user: 'User 3',
      },{
        src: '004.jpeg',
        title: 'Title 4',
        user: 'User 4',
      },{
        src: '005.jpeg',
        title: 'Title 5',
        user: 'User 5',
      }, {
        src: '006.jpeg',
        title: 'Title 6',
        user: 'User 6',
      },{
        src: '007.jpeg',
        title: 'Title 7',
        user: 'User 7',
      },{
        src: '008.jpeg',
        title: 'Title 8',
        user: 'User 8',
      },{
        src: '009.jpeg',
        title: 'Title 9',
        user: 'User 9',
      },{
        src: '010.jpeg',
        title: 'Title 10',
        user: 'User 10',
      },{
        src: '011.jpeg',
        title: 'Title 11',
        user: 'User 11',
      }, {
        src: '012.jpeg',
        title: 'Title 12',
        user: 'User 12',
      },{
        src: '013.jpeg',
        title: 'Title 13',
        user: 'User 13',
      },{
        src: '014.jpeg',
        title: 'Title 14',
        user: 'User 14',
      },{
        src: '015.jpeg',
        title: 'Title 15',
        user: 'User 15',
      },{
        src: '016.jpeg',
        title: 'Title 16',
        user: 'User 16',
      },{
        src: '017.jpeg',
        title: 'Title 17',
        user: 'User 17',
      },{
        src: '018.jpeg',
        title: 'Title 18',
        user: 'User 18',
      }, {
        src: '019.jpeg',
        title: 'Title 19',
        user: 'User 19',
      },{
        src: '020.jpeg',
        title: 'Title 20',
        user: 'User 20',
      },{
        src: '021.jpeg',
        title: 'Title 21',
        user: 'User 21',
      },{
        src: '022.jpeg',
        title: 'Title 22',
        user: 'User 22',
      },{
        src: '023.jpeg',
        title: 'Title 23',
        user: 'User 23',
      },{
        src: '024.jpeg',
        title: 'Title 24',
        user: 'User 24',
      }
    ])

    const subArrays = computed (()=> {
      let length = Math.ceil(cards.length / 5)

      const result = new Array(length).fill().map((i) => {
        return cards.splice(0, length)
      })

      return result
    })

    return{
      cards,
      subArrays
    }
  }
}
</script>
