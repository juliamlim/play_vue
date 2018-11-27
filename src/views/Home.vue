<template>
  <main>
    <hero />
    <events :events="events" :date="today"/>
    <section id="section">
      <h2>Section</h2>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor, voluptas eius? Inventore suscipit atque laborum voluptas dicta beatae, excepturi, tempora sunt voluptatem error architecto velit, vero id animi exercitationem. Aliquid.</p>
    </section>
  </main>
</template>

<script>
import moment from 'moment'
// @ is an alias to /src
import Hero from '@/components/Hero.vue'
import Events from '@/components/Events.vue'
import env from '@/lib/env-research.js'

export default {
  name: 'home',
  components: {
    Hero,
    Events
  },
  data () {
    return {
      events: [new Event(), new Event(), new Event(), new Event(), new Event()],
      today: moment().add(env.advanceDate[0], env.advanceDate[1]).format('YYYY-MM-DD')
    }
  }
}

class Event {
  constructor () {
    this.venue = 'Venue Name'
    this.price = 234.65
    this.date = moment()
    this.address = '123 Main St.'
  }
}
</script>
<style>
#section {
  margin-top: 50px;
}
</style>
