<template>
  <div class="container">
    <div>
      <Navbar />
      <Login />
      <Footer />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.container {
    background-color: black;
  background-image: url('@/assets/img/login-background.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  margin: 0 auto;
  min-height: 100vh;
  min-width: 100vw;
  display: flex;
  justify-content: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
