<template>
    <section id="hero">
      <h1>Venue Price</h1>
      <p>Bid to reseve your show or event at local venues.</p>
    </section>
</template>

<style scoped>
#hero {
  height: 50vh;
  padding: 20vh 0 0;
}

h1,
p {
  opacity: 0;
  transform: translateX(50px);
  animation: flyIn 2s ease 0.5s forwards;
}

h1 {
  font-size: 3em;
  transform: translateY(-50px);
  animation-delay: 0.2s;
}

@keyframes flyIn {
  0% { opacity: 0; }
  100% { transform: translateX(0) translateY(0); opacity: 1; }
}
</style>
