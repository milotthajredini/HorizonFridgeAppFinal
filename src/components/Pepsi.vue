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
                  <p id="priceP">{{ drink.price }}</p>
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
          drinkName: "Pepsi Cola",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/pepsi.png"
        },
        {
          id: 2,
          drinkName: "Pepsi Cola",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/pepsi.png"
        },
        {
          id: 3,
          drinkName: "Pepsi Zero",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/zero.png"
        },
        {
          id: 4,
          drinkName: "Pepsi Zero",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/zero.png"
        },
        {
          id: 5,
          drinkName: "Diet Pepsi",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/diet.png"
        },
        {
          id: 6,
          drinkName: "Diet Pepsi",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/diet.png"
        },
        {
          id: 7,
          drinkName: "Dew",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/dew.png"
        },
        {
          id: 8,
          drinkName: "Dew",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/dew.png"
        },
        {
          id: 9,
          drinkName: "7up",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/7up.png"
        },
        {
          id: 10,
          drinkName: "7up",
          priceTitle: "Price",
          price: "0 .50 €",
          drinkSrc:
            "https://s3.eu-central-1.amazonaws.com/maia.horizon/Drinks/Bottles/7up.png"
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
