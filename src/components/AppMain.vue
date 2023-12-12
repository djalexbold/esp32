<template>
  <div id="main-form">
    <div id="form">
      <h2>Sensor 1</h2>
    </div>
    <div id="form">
      <h2>Sensor 2</h2>
    </div>
    <div id="form">
      <h2>Sensor 3</h2>
    </div>
    <div id="form">
      <h2>Sensor 4</h2>
    </div>
    <div id="form">
      <h2>Sensor 5</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppMain",
  methods: {
    currentYear() {
      let now = new Date();
      return now.getFullYear();
    },
  },
};
</script>


<style>
#main-form{
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  flex-flow: nowrap;
  justify-content: center;
  align-content: space-evenly;
  flex-wrap: wrap;

}
#form {
  display: inline-block;
  width: 100px;
  height: 75px;
  margin: 5px;
  border-radius: 10px;
  background-color: #8efffa;
  border: 3px solid #009f9f;
  box-shadow:
      inset 0 -3em 3em rgba(0, 0, 0, 0.1),
      0.3em 0.3em 1em rgba(0, 0, 0, 0.3);

}
</style>
