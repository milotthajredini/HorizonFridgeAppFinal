<template
  ><div>
    <v-container
      style="margin:0;padding:0;height:208px !important;"
      id="container"
    >
      <v-row
        no-gutters
        class="rowBottles"
        align-content="center"
        justify="center"
        style="height:208px !important"
      >
        <v-col
          v-for="drink in drinks"
          id="colona"
          :key="drink"
          cols="10"
          sm="1"
        >
          <div class="pijetContainer">
            <v-img
              :contain="true"
              :eager="true"
              style="z-index:3;"
              height="175px"
              :src="drink.drinkSrc"
            ></v-img>
            <div class="prices">
              <div class="prices-innerDiv">
                <h3>{{ drink.drinkName }}</h3>
                <div class="pSmall">
                  <p>{{ drink.price }}</p>
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
      drinks: [
        {
          id: 1,
          drinkName: "Coca-Cola",
          priceTitle: "Price",
          price: "1 .00 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/final.png"
        },
        {
          id: 2,
          drinkName: "Coca-Cola",
          priceTitle: "Price",
          price: "0 .20 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/final.png"
        },
        {
          id: 3,
          drinkName: "Coca Zero",
          priceTitle: "Price",
          price: "1 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/cczero1.png"
        },
        {
          id: 4,
          drinkName: "Coca  Zero",
          priceTitle: "Price",
          price: "0 .65 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/cczero1.png"
        },
        {
          id: 5,
          drinkName: "Fanta",
          priceTitle: "Price",
          price: "0 .85 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/fanta1.png"
        },
        {
          id: 6,
          drinkName: "Fanta",
          priceTitle: "Price",
          price: "2 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/fanta1.png"
        },
        {
          id: 7,
          drinkName: "Schweppes",
          priceTitle: "Price",
          price: "4 .60 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/bitter.png"
        },
        {
          id: 8,
          drinkName: "Tonic",
          priceTitle: "Price",
          price: "8 .90 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/tonic3.png"
        },
        {
          id: 9,
          drinkName: "Sprite",
          priceTitle: "Price",
          price: "9 .99 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/sprite1.png"
        },
        {
          id: 10,
          drinkName: "Sprite",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/sprite1.png"
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
