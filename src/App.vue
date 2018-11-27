<template>
  <body class="wrap">
    <header>
      <nav>
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
      </nav>
    </header>
    <router-view/>
  </body>
</template>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto:100,300');

* {
  font-family: 'Roboto', Verdana, Tahoma, 'Trebuchet MS', Arial, sans-serif;
  font-weight: 500;
  box-sizing: border-box;
}
body {
  background: #e0e0e0;
}
.wrap {
  width: 90%;
  max-width: 980px;
  margin: 0 auto;
}
</style>
