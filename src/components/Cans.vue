<template
  ><div>
    <v-container
      style="margin:0;padding:0;height:200px !important;"
      id="container"
    >
      <v-row
        no-gutters
        class="rowBottles"
        align-content="center"
        justify="center"
      >
        <v-col
          v-for="kanaqe in kanaqet"
          id="colona"
          :key="kanaqe.id"
          cols="10"
          sm="1"
        >
          <div class="pijetContainer">
            <v-img
              :contain="true"
              :eager="true"
              style="z-index:3;"
              height="175px"
              :src="kanaqe.drinkSrc"
            ></v-img>
            <div class="prices">
              <div class="prices-innerDiv">
                <h3>{{ kanaqe.drinkName }}</h3>
                <div class="pSmall">
                  <p id="priceP">{{ kanaqe.price }}</p>
                </div>
              </div>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
/*eslint-disable*/
// import axios from 'axios';
import "../assets/css/Bottles/Bottles.css";
export default {
  data: function() {
    return {
      kanaqet: [
        {
          id: 1,
          drinkName: "Coca Cola",
          priceTitle: "Price",
          price: "0.50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Cans/cc.png"
        },
        {
          id: 2,
          drinkName: "Coca Cola",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Cans/cc.png"
        },
        {
          id: 3,
          drinkName: "Coca Zero",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Cans/zero.png"
        },
        {
          id: 4,
          drinkName: "Coca Zero",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Cans/zero.png"
        },
        {
          id: 5,
          drinkName: "Fanta",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Cans/fanta.png"
        },
        {
          id: 6,
          drinkName: "Fanta",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Cans/fanta.png"
        },
        {
          id: 7,
          drinkName: "Schweppes",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Cans/bitter.png"
        },
        {
          id: 8,
          drinkName: "Tonic",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Cans/tonic.png"
        },
        {
          id: 9,
          drinkName: "Sprite",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Cans/sprite.png"
        },
        {
          id: 10,
          drinkName: "Sprite",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Cans/sprite.png"
        }
      ],
      methods: {
        priceMethod() {
          document.getElementById("priceP").style.color = "red";
          console.log("testt");
        }
      },
      mounted() {
        this.priceMethod();
      }
    };
  }

  // async beforeMount() {
  //   await this.fetchPijet();
  //},

  // methods: {
  //   async fetchPijet() {
  //     await axios.get('http://localhost:4000/drink').then((res) => {
  //       this.drinks = res.data;
  //       console.log('this drinks ', this.drinks);
  //     });
  //   },
  // },
};
</script>

<style></style>
