<script>
import ErrorLabel from "@/components/ErrorLabel.vue";
import axios from "axios";

export default {
  components: { ErrorLabel },
  data() {
    return {
      form: {
        login: "",
        password: "",
        discordAccountName: "",
      },
      errorString: "",
    };
  },
  methods: {
    submitForm() {
      axios
        .post(import.meta.env.VITE_BASE_URL + "/register", this.form)
        .then((resp) => {
          this.$emit("register", resp.data.invitation);
        })
        .catch((error) => {
          this.errorString = error.response.data.message;
        });
    },
  },
};
</script>

<template>
  <h2 class="title">Step 1 : Registration</h2>
  <form @submit.prevent="submitForm">
    <div class="row row-space">
      <div class="col">
        <div class="input-group">
          <label class="label" for="email">Etna login</label>
          <input
            v-model="form.login"
            type="text"
            name="login"
            class="input-4"
            required
            placeholder="name_l"
            pattern="^[a-zA-Z0-9._]+$"
          />
        </div>
        <div class="input-group">
          <label class="label" for="password">Etna password</label>
          <input
            v-model="form.password"
            type="password"
            name="password"
            class="input-4"
            required
          />
        </div>
        <div class="input-group">
          <label class="label" for="discordAccountName"
            >Discord account with discriminator (#)</label
          >
          <input
            type="text"
            v-model="form.discordAccountName"
            name="discordAccountName"
            class="input-4"
            required
            placeholder="Name#1234"
            pattern="^.{2,32}#[0-9]{4}$"
          />
        </div>
      </div>
    </div>
    <div v-if="errorString">
      <ErrorLabel :message="errorString" />
    </div>
    <div class="p15">
      <button class="btn" type="submit">Register</button>
    </div>
  </form>
</template>

<style scoped>
.row {
  display: flex;
  flex-wrap: wrap;
}
.row-space {
  justify-content: space-between;
}
.col {
  width: 100%;
}
.input-group {
  position: relative;
  margin-bottom: 22px;
}
.label {
  font-size: 16px;
  color: #555;
  text-transform: capitalize;
  display: block;
  margin-bottom: 5px;
}
input {
  outline: none;
  margin: 0;
  border: none;
  box-shadow: none;
  width: 100%;
  font-size: 14px;
  font-family: inherit;
}
.input-4 {
  line-height: 50px;
  background: #fafafa;
  box-shadow: inset 0 1px 3px 0 rgb(0 0 0 / 8%);
  border-radius: 5px;
  padding: 0 20px;
  font-size: 16px;
  color: #666;
  transition: all 0.4s ease;
  box-sizing: border-box;
}
.p15 {
  padding-top: 15px;
}
.btn {
  display: inline-block;
  line-height: 50px;
  padding: 0 50px;
  background: #4272d7;
  transition: all 0.4s ease;
  cursor: pointer;
  border-radius: 5px;
  font-size: 18px;
  color: #fff;
  font-family: poppins, arial, helvetica neue, sans-serif;
}
.btn:hover {
  background: #3868cd;
}
button {
  outline: none;
  background: 0 0;
  border: none;
}
</style>
