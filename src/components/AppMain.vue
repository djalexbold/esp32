<template>

  <div id="main-form">
    <template v-for="item in sensors">
      <div id="form" @click="showModal(item)">
        <h4>{{ item.id }}-{{item.name}}</h4>
        <ul>
          <li>Temperature: {{ item.temperature }} C°</li>
          <li>Humidity: {{ item.humidity }} %</li>
          <li>Pressure: {{ item.pressure }} mmhg</li>
        </ul>
      </div>
    </template>
    <ModalWindow
        v-show="isModalVisible"
        @close="closeModal"
        v-bind:message="modalId"
    />
  </div>
</template>

<script>
import ModalWindow from "@/components/ModalWindow.vue";
import Mixins from "@/mixins/mixins";

export default {
  name: "AppMain",
  components: {
    ModalWindow
  },

  data() {
    return {
      modalId: [],
      isModalVisible: false,
      sensors: [
        {
          id: 1,
          name: 'Home',
          temperature: -14,
          humidity: 75,
          pressure: 745,
          waterlevel: 11,
          acidity: 45
        },
        {
          id: 2,
          name: 'Terrace',
          temperature: -5,
          humidity: 70,
          pressure: 740
        },
        {
          id: 3,
          name: 'Garden',
          temperature: -12,
          humidity: 65,
          pressure: 735
        },
        {
          id: 4,
          name: 'Construction',
          temperature: -11,
          humidity: 70,
          pressure: 742,
          acidity: 89
        },
        {
          id: 5,
          name: 'sdgfdfgfd sdffgfg',
          temperature: -14,
          humidity: 76,
          pressure: 748
        },
      ]
    }
  },
  methods: {
    showModal(item) {
      this.isModalVisible = true;
      this.modalId = item

    },
    closeModal() {
      this.isModalVisible = false;
    },
    currentYear() {
      let now = new Date();
      return now.getFullYear();
    },
  },
  mixins: [Mixins],
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
  list-style-type: none;
  width: 100%;
  padding-left: 0;
}

#form {
  user-select: none;
  cursor: pointer;
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

/*  модальное окно  */


</style>
