<template>
	<div class="body">
    <LandingHeader></LandingHeader>
		<TechnologiesBanner></TechnologiesBanner>
		<TechnologiesContent></TechnologiesContent>
    <LandingFooter></LandingFooter>
    <span class="return-to-top" @click="scrollTo()">
      <i class="fas fa-angle-up" style="font-size: 35px"></i>
    </span>
  </div>
</template>

<style lang="scss" scoped>
@import "~assets/style/colors.scss";
div.item-holder{
  position: 'absolute';
  top: -20%;
  z-index: 10;
}
.item-holder{
  width: 100%;
  height: 500px;
}
.item-content{
  padding: 20px;
  width: 40%;
  float: left;
  margin-left: 5%;
  margin-right: 5%;
  height: 750px;
  display: flex;
  flex-direction: column;
  border-bottom: solid 20px gray;
  // -webkit-box-shadow: 5px -5px 15px -5px rgba(0, 0, 0, 0.3);
  // -moz-box-shadow: 5px -5px 15px -5px rgba(0, 0, 0, 0.3);
  // border-radius: 10px;
}
.item-content:hover{
  cursor: pointer;
  border-bottom: solid 20px blue;
  border-radius: 10px;
}
//
.title{
  text-decoration: underline;
  height: 100px;
  line-height: 100px;
}
//
.details-text{
  width: 100%;
  float: left;
  margin-top: 25px;
  text-align: center;
  font-size: 17px;
}
.action{
  width: 100%;
  height: 150px;
  line-height: 150px;
  border-top: solid 5px gray;
  margin-top: auto;
}
@media (max-width: 992px){
  .text-holder{
    width: 96%;
    margin-left: 2%;
    margin-right: 2%;
  }
  .item-holder{
    height: auto;
    min-height: 70vh;
    overflow-y: hidden;
  }
  .item-content{
    width: 100%;
    margin-right: 0%;
    margin-left: 0%;
  }
  ul{
    padding: 10px;
  }
  ul li .inclusion-text{
    width: 90%;
    margin-left: 0%;
  }
  ul li i{
    width: 10%;
  }
}
//
.body{
  margin: 0px;
}
.return-to-top {
  position: fixed;
  bottom: 10px;
  right: 10px;
  background: $white;
  color: primary;
  height: 50px;
  width: 50px;
  border-radius: 5px;
  line-height: 62px;
  text-align: center;
}

.fa-angle-up {
  color: $primary !important;
}
.return-to-top:hover {
  cursor: pointer;
  color: $primary;
}
</style>

<script>
import ROUTER from 'src/router'
import Jquery from 'jquery'
import LandingHeader from 'src/home/Landing/Header.vue'
import TechnologiesBanner from 'src/home/Technologies/Banner.vue'
import TechnologiesContent from 'src/home/Technologies/Content.vue'
import LandingFooter from 'src/home/Landing/Footer.vue'
export default {
  components: {
    LandingHeader,
    TechnologiesBanner,
    TechnologiesContent,
    LandingFooter
  },
  mounted() {},
  data() {
    return {};
  },
  methods: {
    redirect(parameter) {
      ROUTER.push(parameter);
    },
    scrollTo() {
      Jquery("html, body").animate(
        {
          scrollTop: Jquery("#header").offset().top,
        },
        500
      );
    },
  },
};
</script>

