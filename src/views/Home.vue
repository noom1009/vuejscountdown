<template>
  <div class="home">
    <div class="content">
      <Navbar />
      <br>
      <h3 class="row gx-3 gy-2 align-items-center"><center>ลอตเตอรี่ออนไลน์</center></h3>
      <p class="row gx-3 gy-2 align-items-center text-danger"><center>ลอตเตอรี่งวดวันที่ {{ deadlinedate }}</center></p>
      <h3 class="row gx-3 gy-2 align-items-center">
        <center>Comming Soon: {{ deadlinedate }}</center>
      </h3>
      <flip-countdown :deadline="deadline1ts"></flip-countdown>
      <Lotto />
    </div>
    <Footer />
  </div>
</template>

<script>
import FlipCountdown from "vue2-flip-countdown";
import Navbar from "../components/Navbar.vue";
import Footer from "../components/Footer.vue";
import Lotto from "../components/Lotto.vue";

import moment from "moment";
//const fmt = "YYYY-MM-DD";
const DASH_DMY = 'DD-MM-YYYY';
export default {
  name: "app",
  components: {
    FlipCountdown,
    Navbar,
    Footer,
    Lotto,
  },
  data() {
    return {
      deadline1ts: "2021-10-01",
      deadlinedate :"01-10-2021"
    };
  },
  computed: {
    deadline1: function () {
      return moment(this.deadlinedate).format(DASH_DMY); 
    },
  },
  methods: {
    timeElapsedHandler: function () {},
  },
};
</script>

