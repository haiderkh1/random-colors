<template>
  <footer class="footer">
    <p>
      Developed with ❤️ by
      <a href="https://github.com/haiderkh1">Haider Khan</a>
    </p>
  </footer>
</template>
<script>
export default {
  name: "Footer",
};
</script>
<style>
.footer {
  text-align: center;
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  color: #fff;
  text-shadow: 2px 2px 5px #111;
  font-weight: bold;
}
.footer a {
  color: tomato;
}
</style>
