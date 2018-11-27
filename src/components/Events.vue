<template>
  <section id="events">
    <h2>Hot Venues Near You</h2>
    <img src="@/assets/map.png" alt="What's happening around your area.">
    <ul>
      <form action="">
        <input type="date" name="date" id="date" :value="date">
      </form>
      <li v-for="(e, i) in events" :key="i">
        <h5>${{ e.price }}</h5>
        <h4>
          <span class="day">{{ e.date.format('D') }}</span>
          <span class="month">{{ e.date.format('MMM') }}</span>
        </h4>
        <h3>
          {{ e.venue }}
          <p>{{ e.address }}</p>
        </h3>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  props: ['events', 'date']
}
</script>

<style scoped>
#events::after {
  content: '';
  display: table;
  clear: both;
}
img {
  width: 55%;
  height: 300px;
  float: left;
  border-radius: 3px;
  box-shadow: 0 8px 40px -10px rgba(0,0,0,0.2);
}
ul {
  width: 45%;
  height: 300px;
  float: left;
  padding: 0 20px;
  margin: 0;
  list-style: none;
  overflow: scroll;
}
li {
  padding: 15px;
  margin-bottom: 20px;
  background-color: whitesmoke;
  border-radius: 3px;
  box-shadow: 0 8px 30px -10px rgba(0,0,0,0.2);
}
h4 {
  width: 70px;
  float: left;
  border-right: 1px solid dimgray;
  text-align: center;
  margin: 0;
  padding-right: 10px;
}
h4 .day { font-size: 25px; display: block; }
h4 .month { font-size: 15px; }
h3 {
  margin: 5px;
  margin-left: 95px;
}
h3 p {
  margin: 4px 0 0;
  font-size: 12px;
}
h5 {
  float: right;
}
</style>
