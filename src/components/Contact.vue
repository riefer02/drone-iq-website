<template>
  <div id="contact-us" ref="contact-us">
    <v-container>
      <RowHeader title="Contact Us" />
      <v-form v-model="valid">
        <v-row class="d-flex justify-center">
          <v-col lg="6">
            <v-row>
              <v-col cols="12">
                <v-text-field
                  v-model="firstname"
                  :rules="nameRules"
                  :counter="10"
                  label="First name"
                  required
                ></v-text-field>
              </v-col>

              <v-col cols="12">
                <v-text-field
                  v-model="lastname"
                  :rules="nameRules"
                  :counter="10"
                  label="Last name"
                  required
                ></v-text-field>
              </v-col>

              <v-col cols="12">
                <v-text-field
                  v-model="email"
                  :rules="emailRules"
                  label="E-mail"
                  required
                ></v-text-field>
              </v-col>
            </v-row>
            <v-row>
              <v-container fluid>
                <v-textarea
                  clearable
                  clear-icon="mdi-cancel"
                  label="Message"
                ></v-textarea>
              </v-container>
            </v-row>
            <v-row>
              <v-col class="d-flex justify-center">
                <v-btn class="mx-2" fab dark large color="red">
                  <v-icon dark>mdi-android</v-icon>
                </v-btn>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-form>
    </v-container>
  </div>
</template>

<script>
import RowHeader from "@/components/RowHeader.vue";
export default {
  name: "ContactForm",
  components: {
    RowHeader,
  },
  data: () => ({
    valid: false,
    firstname: "",
    lastname: "",
    nameRules: [
      (v) => !!v || "Name is required",
      (v) => v.length <= 10 || "Name must be less than 10 characters",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "E-mail is required",
      (v) => /.+@.+/.test(v) || "E-mail must be valid",
    ],
  }),
};
</script>
