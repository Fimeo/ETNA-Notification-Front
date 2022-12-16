<template>
  <div class="page-wrapper">
    <div class="wrapper">
      <div class="card">
        <div class="card-body" v-if="!invitationLink">
          <RegisterForm @register="userRegistered" />
        </div>
        <div class="card-body" v-else>
          <JoinServer :discord-invitation-link="invitationLink" />
        </div>
        <AdditionalInformation />
      </div>
    </div>
  </div>
</template>

<script>
import RegisterForm from "@/components/RegisterForm.vue";
import JoinServer from "@/components/JoinServer.vue";
import AdditionalInformation from "@/components/AdditionalInformation.vue";

export default {
  name: "RegisterPage",
  components: {
    AdditionalInformation,
    JoinServer,
    RegisterForm,
  },
  data() {
    return {
      invitationLink: "",
    };
  },
  methods: {
    catchError(errorMessage) {
      this.errorField = errorMessage;
    },
    userRegistered(link) {
      this.invitationLink = link;
    },
  },
};
</script>

<style scoped>
.page-wrapper {
  padding-bottom: 100px;
  padding-top: 100px;
  background: linear-gradient(to top right, #fc2c77 0%, #6c4079 100%);
  min-height: 100vh;
}
.wrapper {
  max-width: 680px;
  margin: 0 auto;
}
.card {
  background: #fff;
  border-radius: 10px;
  box-shadow: 0 8px 20px 0 rgb(0 0 0 / 15%);
}
.card-body {
  padding: 57px 65px 65px;
}
</style>
