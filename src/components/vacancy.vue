<template>
  <div>
    <header>
      <div class="headline"></div>
      <b-container>
        <b-row class="pt-3 pb-2 justify-content-lg-center">
          <b-col lg="5" md="6" class="d-flex justify-content-start">
            <img src="./../img/logo.svg" height="100" />
          </b-col>
          <b-col lg="5" md="6" class="d-flex justify-content-center pt-4 mt-3 ">
            <div class="d-flex pt-2">
              <img v-for="index in 4" :key="index" src="./../img/star.svg" height="15" />
              <img src="./../img/star_half.svg" height="15" />
            </div>
            <div class="px-2">
              <p class="points mb-0">
                8.4
                <sup>/ 10</sup>
              </p>
            </div>
            <div>
              <img src="./../img/feedbackcompany.svg" height="25" />
            </div>
          </b-col>
        </b-row>
      </b-container>
    </header>
    <div>
      <div class="backgroundImage"></div>
      <b-container>
        <b-row align-h="center" class="py-5">
          <b-col lg="5" md="6" class="d-flex justify-content-center">
            <div class="shadow-sm mb-2 headerCard bg-white">
              <h2 class="px-5 py-4">Bent u onze nieuwe partner?</h2>
              <p class="px-5">
                Lorem ipsum dolor sit amet, consectetur adipiscing
                elit. Nam consequat arcu sed nulla lacinia, quis
                blandit eros facilisis. Mauris mattis nec sem nec
                finibus. Nunc eget leo ut diam imperdiet vehicula
                ac non elit. Pellentesque nisi neque, sodales nec
                sem et, condimentum congue ligula. Integer non
                ullamcorper lacus, sed luctus sapien.
              </p>
              <div class="px-5 py-4">
                <button type="button" class="btn dropdown-toggle button">De mogelijkheden</button>
              </div>
            </div>
          </b-col>
          <b-col lg="5" md="6">
            <div class="p-3">
              <img src="./../img/timo_partner.svg" class="img-fuild imgPartner" alt="timo_partner" />
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>

    <div class="bg-light">
      <b-container class="pt-5">
        <b-row class="justify-content-center">
          <b-col lg="8" sm="12" >
            <b-row class="pt-3 justify-content-center">
              <b-col lg="4" sm="12" md="6" class="mb-5" v-for="(row,index) in rows" :key="index">
                <div class="d-flex justify-content-center">
                  <div align="center" class="shadow-sm p-2 bg-white serviceCard">
                    <div class="py-3">
                      <img :src="getImgUrl(row)" height="50" />
                    </div>
                    <div class="title">
                      <h5 class="px-3">{{row.title}}</h5>
                    </div>
                    <p class="py-2 px-3 text-left">{{row.text}}</p>
                  </div>
                </div>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </b-container>
    </div>
    <footer class="d-flex justify-content-center">
      <div class="d-flex justify-content-between footer">
        <div class="pt-3 pr-3">
          <p>&copy;2013 - 2019 Vliegenenparkeren.nl - Alle rechten voorbehouden</p>
        </div>
        <div class="pt-3 pl-3">
          <p>Bedrijfsgegevens / Privacy policy / Algemene voorwaarden / Sitemap</p>
        </div>
      </div>
    </footer>
  </div>
</template>
<script>
export default {
  name: "vacancy",
  data() {
    return {
      rows: [
        {
          image: "range",
          title: "Groot bereik",
          text:
            "Lorem ipsum dolor sit amet,consectetur adipiscing elit. Nam consequat arcu sed nulla lacinia,quis blandit eros facil."
        },
        {
          image: "freeSignup",
          title: "Gratis aanmelden",
          text:
            "Lorem ipsum dolor sit amet,consectetur adipiscing elit. Nam consequat arcu sed nulla lacinia,quis blandit eros facil."
        },
        {
          image: "service",
          title: "Klantenservice",
          text:
            "Lorem ipsum dolor sit amet,consectetur adipiscing elit. Nam consequat arcu sed nulla lacinia,quis blandit eros facil."
        },
        {
          image: "support",
          title: "Support en inzage",
          text:
            "Lorem ipsum dolor sit amet,consectetur adipiscing elit. Nam consequat arcu sed nulla lacinia,quis blandit eros facil."
        },
        {
          image: "money",
          title: "Verdien geld",
          text:
            "Lorem ipsum dolor sit amet,consectetur adipiscing elit. Nam consequat arcu sed nulla lacinia,quis blandit eros facil."
        },
        {
          image: "quality",
          title: "Kwalitatief aanbod",
          text:
            "Lorem ipsum dolor sit amet,consectetur adipiscing elit. Nam consequat arcu sed nulla lacinia,quis blandit eros facil."
        },
        {
          image: "wrench",
          title: "Maatwerk oplossingen",
          text:
            "Lorem ipsum dolor sit amet,consectetur adipiscing elit. Nam consequat arcu sed nulla lacinia,quis blandit eros facil."
        },
        {
          image: "thumbs",
          title: "Gemak",
          text:
            "Lorem ipsum dolor sit amet,consectetur adipiscing elit. Nam consequat arcu sed nulla lacinia,quis blandit eros facil."
        }
      ]
    };
  },
  methods: {
    getImgUrl(row) {
      var images = require.context("./../img/", true, /\.png$/);
      return images("./" + row.image + ".png");
    }
  }
};
</script>

<style scoped>
header{
  background-image: url("./../img/clouds.png");
   background-repeat: no-repeat;
  background-size: 100% 100%;
}
.headerCard {
  max-width: 23rem;
}
.headerCard p {
  font-size: 13px;
}
.headerCard h2 {
  font-weight: bolder;
}

.imgPartner {
  max-height: 300px;
}

.serviceCard {
  max-width: 14rem;
  border-bottom: 10px solid #00bfff;
}
.serviceCard p {
  font-size: 13px;
  color: black;
}
.title {
  height: 50px;
}
footer {
  background-color: #005070;
}
.footer {
  width: 80%;
}
.footer p {
  color: #6192a7;
  font-size: 12px;
}
.points {
  font-weight: bold;
  font-size: 18px;
  color: #005070;
}
sup {
  color: #00bfff;
  font-weight: lighter;
}
.headline {
  position: absolute;
  top: 98px;
  height: 25px;
  width: 100%;
  background-color: #00bfff;
}
.backgroundImage {
  clip-path: polygon(0 0, 100% 0, 100% 40%, 0 70%);
  background-color: whitesmoke;
  position: absolute;
  width: 100%;
  height: 500px;
}
.button {
  background-color: #00bfff;
  color: white;
}
</style>