<template>
  <div class="container">
    <div class="row">
      <div class="col-md-5 ml-auto">
        <div class="info-area info-horizontal mt-5">
          <div class="icon icon-warning">
            <i class="tim-icons icon-wifi"></i>
          </div>
          <div class="description">
            <h3 class="info-title">Digital Marketing</h3>
            <p class="description">
              We've created the digital marketing automation software designed for social ad analysts, account managers and seo experts.
            </p>
          </div>
        </div>
        <div class="info-area info-horizontal">
          <div class="icon icon-primary">
            <i class="tim-icons icon-triangle-right-17"></i>
          </div>
          <div class="description">
            <h3 class="info-title">Full Support</h3>
            <p class="description">
              We've developed this software with full support in mind and price that doesn't bite and 0$ cost if your business is having a rainy day. We all do
            </p>
          </div>
        </div>
        <div class="info-area info-horizontal">
          <div class="icon icon-info">
            <i class="tim-icons icon-trophy"></i>
          </div>
          <div class="description">
            <h3 class="info-title">Built Audience</h3>
            <p class="description">
              There is also a Fully Customizable Admin Dashboard and Team managment.
            </p>
          </div>
        </div>
      </div>

      <div class="col-md-7 mr-auto">
        <form @submit.prevent="register">
          <card class="card-register card-white">
            <template slot="header">
              <img class="card-img" src="img/card-primary.png" alt="Card image"/>
              <h4 class="card-title">Register</h4>
            </template>

            <base-input
              v-validate="'required'"
              :error="getError('Full Name')"
              v-model="model.fullName"
              name="Full Name"
              placeholder="Full Name"
              addon-left-icon="tim-icons icon-single-02"
            >
            </base-input>

            <base-input
              v-validate="'required|email'"
              :error="getError('email')"
              v-model="model.email"
              name="email"
              placeholder="Email"
              addon-left-icon="tim-icons icon-email-85"
            >
            </base-input>

            <base-input
              v-validate="'required|min:5'"
              :error="getError('password')"
              v-model="model.password"
              name="password"
              type="password"
              placeholder="Password"
              addon-left-icon="tim-icons icon-lock-circle"
            >
            </base-input>

            <base-checkbox class="text-left">
              I agree to the <a href="#something">terms and conditions</a>.
            </base-checkbox>

            <base-button native-type="submit" slot="footer" type="primary" round block size="lg">
              Get Started
            </base-button>
          </card>
        </form>
      </div>
    </div>
  </div>
</template>
<script>
import { BaseCheckbox } from 'src/components';

export default {
  components: {
    BaseCheckbox
  },
  data() {
    return {
      model: {
        email: '',
        fullName: '',
        password: ''
      }
    };
  },
  methods: {
    getError(fieldName) {
      return this.errors.first(fieldName);
    },
    async register() {
      let isValidForm = await this.$validator.validateAll();
      if (isValidForm) {
        // TIP use this.model to send it to api and perform register call
      }
    }
  }
};
</script>
<style></style>
