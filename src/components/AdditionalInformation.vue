<template>
  <div class="information">
    <div class="label">
      <h2 class="title">Information</h2>
    </div>
    <div class="content">
      <p>
        This service allows to receive notifications from the
        <a href="https://intra.etna-alternance.net/" target="_blank"
          >intranet</a
        >
        of ETNA - Ivry sur Seine school on a dedicated Discord server.
      </p>
      <br />
      <p>
        This project is <b>not an official</b> project but is realized by a
        master student.
      </p>
      <br />
      <p>
        This service tries to solve the problem of notifications that are not
        published on a real time communication channel.
      </p>
      <br />
      <p>
        The first step is to register to this service, for that the credentials
        of your ETNA account are needed to allow the script to retrieve your
        pending notifications every 30 minutes.
      </p>
      <p>
        This information is stored in a database and encrypted with a reversible
        method (RSA) because the clear identifiers are needed for API calls on
        the intranet. However, the server is secure and this data will not be
        used outside bot or resold.
      </p>
      <br />
      <p>
        You are asked for your discord account ID to recognize your linked
        account in the second step.
      </p>
      <br />
      <p>
        Once the account is validated, an invitation link on the server is
        provided. It allows you to join a shared discord server. Then type the
        command <code>/connect</code> in the channel <code>connect</code>. A
        personal channel will be created which only your account and the
        administrator can access.
      </p>
      <br />
      <p>Notifications will be sent to you on this channel.</p>
      <br />
      <p>
        This service allows you to run the bot automatically. If you want to set
        up your own server, the source code is available on
        <a href="https://github.com/Fimeo/ETNA-Notification" target="_blank"
          >Github</a
        >
      </p>
      <br />
      <p>
        This service does not guarantee a continuity of service, the intranet is
        trusted and it does not prevent you from going there without recent
        notification.
      </p>
      <br />
      <p>
        If you want to unsubscribe from this service, just quit the server
        and/or change your password.
      </p>
      <br />
      <p>
        Sources :
        <br />
        <a href="https://github.com/Fimeo/ETNA-Notification-Front"
          >https://github.com/Fimeo/ETNA-Notification-Front</a
        >
        <br />
        <a href="https://github.com/Fimeo/ETNA-Notification"
          >https://github.com/Fimeo/ETNA-Notification</a
        >
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "AdditionalInformation",
};
</script>

<style scoped></style>
