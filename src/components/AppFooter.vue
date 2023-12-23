<template>
  <footer>
    <div>
      Made With 🖤 by
      <span><a href="https://t.me/djalexbold" target="_blank" rel="noopener noreferrer">Alex Bold</a></span>
      ©️ 2022 - {{ currentYear() }} License ©️ BFS
    </div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
  methods: {
    currentYear() {
      let now = new Date();
      return now.getFullYear();
    },
  },
};
</script>

<style>
footer {
  position: fixed;
  bottom: 0;
  padding: 5px 5px;
  margin-top: 50px;
  width: 100%;
  text-align: center;
  background-color: azure;
  opacity: 70%;
  font-size: 0.7rem;
}
</style>
