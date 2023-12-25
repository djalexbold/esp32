<template>
  <transition name="modal-fade">
    <div class="modal-backdrop">
      <div class="modal"
           role="dialog"
           aria-labelledby="modalTitle"
           aria-describedby="modalDescription"
      >
        <button
            type="button"
            @click="close"
            aria-label="Close modal"
            class="btn-close"
        >
          x
        </button>
        <div>
          <h4> {{ message.name }} </h4>
          <ul>
            <li>Temperature: {{ message.temperature }} C°</li>
            <li>Humidity: {{ message.humidity }} %</li>
            <li>Pressure: {{ message.pressure }} mmhg</li>
            <li>Pressure: {{ message.waterlevel }} m</li>
            <li>Pressure: {{ message.acidity }} %</li>
          </ul>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: 'ModalWindow',
  data() {
    return {}
  },
  methods: {
    close() {
      this.$emit('close');
    },
  },
  props: ["message"],
};
</script>

<style>
.modal-backdrop {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.3);
  display: flex;
  justify-content: center;
  align-items: flex-start;
  padding-top: 15em;
}

.modal {
  background-color: #8efffa;
  border-radius: 10px;
  box-shadow: inset 0 -3em 3em rgba(0, 0, 0, 0.1),
  0 0 0 2px rgb(255, 255, 255),
  0.3em 0.3em 1em rgba(0, 0, 0, 0.3);
  overflow-x: auto;
  display: flex;
  width: 30em;
  height: 20em;
  flex-direction: column;
}

.btn-close {
  border: none;
  font-size: 20px;
  text-align: right;
  padding: 5px 10px 5px 5px;
  cursor: pointer;
  font-weight: bold;
  color: white;
  background: #009f9f;
}
.modal h4 {
  padding-left: 10px;
}
</style>
