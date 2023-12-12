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
  background-color: #8efffa;
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
}

#logo-text{
  flex-grow: 1;
  background-color: #01bdbd;
  padding-left: 1rem;
  border-radius: 25px 0 0 25px;
  color: #f8fdff;
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
