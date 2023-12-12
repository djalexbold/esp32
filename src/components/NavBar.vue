<template>
  <nav>
    <div id="logo">
      <img src="../assets/esp32-logo.png" alt="Logo"/>
    </div>
    <div id="logo-text">
      <h1>Water station App</h1>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style>
nav {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
}

#logo-text{
  flex-grow: 1;
  background-color: #01bdbd;
  margin: 1rem 0 1rem 0.5rem;
  padding-left: 3rem;
  border-radius: 25px 0 0 25px;
  color: #f8fdff;
  box-shadow:
      inset 0 -3em 3em rgba(0, 0, 0, 0.1),
      0 0 0 2px rgb(255, 255, 255),
      0.3em 0.3em 1em rgba(0, 0, 0, 0.3);
}

#logo > img {
  object-fit: cover;
  width: 5rem;
  padding: 0.5rem;
}

h1 > a:visited,
a:link {
  text-decoration: none;
  color: black;
}
</style>
