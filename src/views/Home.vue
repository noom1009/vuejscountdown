<template>
  <div class="home">
    <Navbar />
    <h3 class="row gx-3 gy-2 align-items-center"><center>Comming Soon: {{ deadline1ts }}</center></h3>
    <flip-countdown :deadline="deadline1ts"></flip-countdown>

  </div>
</template>

<script>
import FlipCountdown from "vue2-flip-countdown";
import Navbar from "../components/Navbar.vue";


import moment from "moment";
const fmt = "YYYY-MM-DD HH:mm:ss";
export default {
  name: "app",
  components: {
    FlipCountdown,
    Navbar,

  },
  data() {
    return {
      deadline1ts: "2021-10-01 00:00:00",
      deadline2: moment().add(30, "s").format(fmt),
      deadline3: moment().add(1000, "d").add(10, "s").format(fmt),
      deadline4: moment().add(2, "h").format(fmt),
      deadline5: moment().add(24, "h").format(fmt),
    };
  },
  computed: {
    deadline1: function () {
      return moment(this.deadline1ts).format(fmt);
    },
  },
  methods: {
    timeElapsedHandler: function () {},
  },
};
</script>
