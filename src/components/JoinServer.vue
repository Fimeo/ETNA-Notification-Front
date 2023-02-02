<template>
  <div>
    <h2 class="title">Step 2 : join the server</h2>
    <div class="discord-link">
      <p>Your discord invitation link, valid once and for one day</p>
      <p>Join ETNA Notification server :</p>
      <div class="link">
        <a :href="discordInvitationLink" class="link-ref" target="_blank">{{
          discordInvitationLink
        }}</a>
      </div>
      <p>Next, join the server and go to <code>connect</code> channel. Start notifications with  <code>/connect</code> command to validate your discord account.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "JoinServer",
  props: {
    discordInvitationLink: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      errorField: "",
    };
  },
  methods: {
    catchError(errorMessage) {
      this.errorField = errorMessage;
    },
  },
};
</script>

<style scoped>
.link {
  padding: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2ch;
}
.link-ref {
  color: #6c4079;
  font-weight: 800;
  text-decoration: none;
}
.link-ref:visited {
  color: #6c4079;
}
.link:hover {
  text-decoration: underline;
}
</style>
