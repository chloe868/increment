<template>
  <div class="cw-banner" id="send-request">
    <div class="text-center mt-5 p-5">
      <h1 class="title" style="font-size:50px;">
        <b>Drop Us A Line!</b>
      </h1>
      <div>
        <p>
          Better yet, come see us in person! We love our customers, so feel free to visit during normal business hours.<br>
          You can contact us in our business hours through email: <a href="mailto:increment2020@gmail.com">increment2020@gmail.com</a> or call/message us <a href="tel:+639171837855">(+63) 9171837855</a>.<br>
          You can also set an appointment to <a href="https://calendly.com/incrementtech2020/services-offered" target="_blank">www.calendly.com/incrementtech2020</a> for a short discussion.
        </p>
      </div>
      <div>
        <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d981.2168207389841!2d123.9130143!3d10.3524954!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0xc2d9b9e99316c59d!2sUniversity%20of%20San%20Carlos%20-%20Talamban%20Campus!5e0!3m2!1sen!2sph!4v1618812110610!5m2!1sen!2sph" width="100%" height="600px" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
      </div>
    </div>
  </div>
</template>
<style scoped lang="scss">
@import "~assets/style/colors.scss";
.cw-banner {
  width: 100%;
  float: left;
  background: white;
  padding-bottom: 60%;
  padding-left: 5%;
  padding-right: 5%;
  height: 100vh;
}
iframe{
  margin-top:5%;
}
a{
  color:#00b89f;
}
.title {
  margin-top: 2%;
}

@media screen and (max-width: 992px) {
iframe{
  margin-top:5%;

}
}
</style>
<script>
import ROUTER from "src/router";
import COMMON from "src/common.js";
export default {
  mounted() {},
  data() {
    return {
      common: COMMON
    };
  },
  methods: {
    redirect(parameter) {
      ROUTER.push(parameter);
    }
  }
};
</script>
