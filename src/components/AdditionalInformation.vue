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
        of the school ETNA - Ivry sur Seine on a dedicated Discord server.
      </p>

      <p>
        This project is not an official project but is realized by a master
        student.
      </p>

      <p>
        This service tries to solve the problem of notifications that are not
        published on a real time communication channel.
      </p>

      <p>
        The first step to take advantage of this service is to provide your ETNA
        account credentials. This information is required to allow the bot to
        retrieve your pending notifications every 30 minutes.
      </p>

      <p>
        Your login information is stored in a database and encrypted with a
        reversible method (RSA). Indeed, the API provided by ETNA requires the
        identification data in clear text to retrieve the access token in order
        to make requests on the intranet. The server is secured and these data
        will not be used outside this bot. Your data will never be disclosed and
        shared.
      </p>

      <p>
        You are also asked for your discord account ID to recognize your linked
        account and generate a unique invitation on the server.
      </p>

      <p>
        Your login is not your ETNA email but only the identifier. The discord
        account must specify the discriminator (#).
      </p>

      <p>
        If your information is valid, an invitation link to join the server is
        provided. It allows you to join a shared discord server where you will
        receive notifications.
      </p>

      <p>
        Finally, you have to validate the link between your discord account and
        the ETNA account by using the /connect command in the connect channel. A
        personal channel will be created, which only your account and the
        administrator can access.
      </p>

      <p>
        All new notifications will be sent to your personal channel. They are
        retrieved every 30 minutes. Only new notifications will be sent. You
        will also receive reminders for events scheduled in your calendar in the
        previous hour.
      </p>

      <p>
        This service exclusively stores the external identifiers of
        notifications and events to determine if the notifications are already
        sent. It does not store the content of the notifications or the events.
        It does not store access tokens.
      </p>

      <p>
        This service runs on a server and does not require maintenance. However,
        if you want to set it up by yourself, the source code is available on
        <a href="https://github.com/Fimeo/ETNA-Notification" target="_blank"
          >Github</a
        >.
      </p>

      <p>
        The continuity of service is not guaranteed, the intranet remains the
        trusted source and this bot does not prevent you from going there
        without recent notification.
      </p>

      <p>
        If you want to stop receiving notifications, use the stop command or
        quit the server or change your password.
      </p>

      <p>
        If you have changed your password or discord account, simply start over
        at step 1 of registration.
      </p>
      <p>
        <b>Sources :</b>
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

<style scoped>
p {
  margin-bottom: 10px;
}
</style>
