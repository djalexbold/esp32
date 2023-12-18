<template>
  <div id="main-form">
    <div id="form">
      <h4>Sensor 1</h4>
    </div>
    <div id="form">
      <h4>Sensor 2</h4>
      <ul>
        <li>temperature: 34</li>
        <li>Humidity:33</li>
        <li>Pressure:4</li>
      </ul>
    </div>
    <div id="form">
      <h4>Sensor 3</h4>
    </div>
    <div id="form">
      <h4>Sensor 4</h4>
    </div>
    <div id="form">
      <h4>Sensor 5</h4>
      <ul>
        <li>temperature: 34</li>
      </ul>
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
#main-form {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  flex-flow: nowrap;
  justify-content: left;
  align-content: space-evenly;
  flex-wrap: wrap;
}

#form > h4 {
  text-align: center;
}

#form > ul {
  background-color: blueviolet;
  list-style-type: none;
  width: 100%;
  padding-left: 0;
}

#form {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  justify-content: space-evenly;
  width: 100px;
  height: 75px;
  margin: 5px;
  padding: 3px;
  border-radius: 10px;
  background-color: #8efffa;
  border: 3px solid #009f9f;
  box-shadow: inset 0 -3em 3em rgba(0, 0, 0, 0.1),
  0.3em 0.3em 1em rgba(0, 0, 0, 0.3);
}
</style>
