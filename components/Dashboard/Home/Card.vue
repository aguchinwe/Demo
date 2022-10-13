<template>
  <v-card
    width="100%"
    class="pa-4 d-flex fill-width align-center white--text"
    
    height="130"
    elevation="0"
    :to="to"
  >
  <!-- :style="`background-image: url('/svg/card-background-${bgSVG}.svg');
   background-repeat: no-repeat;
  background-size: cover;`" -->
    <v-row class="fill-height" no-gutters>
      <v-col cols="12" class="d-flex align-end">
        <span class="text-subtitle-2">{{ title }}</span>
      </v-col>
      <v-col cols="12">
        <div
          class="d-flex flex-row sf-pro-display align-center font-weight-bold"
        >
          <!-- <div class="col-12">
            <span
              :class="`${
                $vuetify.breakpoint.smAndDown ? 'm-number-size ' : 'number-size'
              }`"
              >{{ number }}</span
            >
          </div> -->

          <!-- <div class="col-md-3 col-4">
            <span class="percentage-size">{{ percentage }}</span>
          </div> -->
        </div>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  data: () => ({}),
  computed: {
    bgSVG() {
      if ((this.cardIndex + 4) % 5 == 0) {
        return "blue";
      } else if ((this.cardIndex + 3) % 5 == 0) {
        return "green";
      } else if ((this.cardIndex + 2) % 5 == 0) {
        return "cyan";
      } else if ((this.cardIndex + 1) % 5 == 0) {
        return "red";
      } else if (this.cardIndex % 5 == 0) {
        return "light-green";
      }
    },
  },
  props: {
    cardIndex: {
      type: Number,
      default: 0,
    },
    title: {
      type: String,
      default: "title",
    },
    number: {
      type: Number,
      default: 0,
    },
    percentage: {
      type: String,
      default: "5%",
    },
    to: {
      type: String,
      default: "",
    },
  },
};
</script>

<style>
.m-number-size {
  font-size: 35px;
}

.number-size {
  font-size: 50px;
}

.percentage-size {
  font-size: 20px;
}
</style>

