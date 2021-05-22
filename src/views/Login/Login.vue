<template>
  <v-flex sm12 md8 offset-md2 class="pa-sm-15 pa-lg-0 pa-md-0 pa-5">
    <v-row class="row-login ma-0">
      <v-col
        cols="12"
        lg="6"
        md="6"
        sm="12"
        class="deep-orange lighten-4 banner hidden-sm-and-down"
      >
        <v-row align="center" justify="center">
          <v-img src="@/assets/img-login2.svg" width="calc(50%)"></v-img>
        </v-row>
      </v-col>
      <v-col cols="12" lg="6" md="6" sm="12" class="form">
        <v-row align="center" style="height: 100%" class="pa-lg-15 pa-md-1">
          <v-col cols="12" sm="12">
            <h1 class="text-h3 font-weight-black">Vamos lá!</h1>
            <h5 class="text-subtitle1 py-5 grey--text font-weight-light">
              Entre com os dados que você inseriu no cadastro.
            </h5>

            <v-row class="pb-10">
              <v-col cols="12" lg="6" sm="12">
                <v-btn color="red" class=" white--text" large block>
                  <v-icon left>mdi-google</v-icon> google</v-btn
                ></v-col
              >
              <v-col cols="12" lg="6" sm="12">
                <v-btn large block color="light-blue darken-4 white--text">
                  <v-icon color="white" left>mdi-facebook</v-icon>
                  facebook
                </v-btn></v-col
              >
            </v-row>

            <v-divider></v-divider>

            <v-form class="pt-10">
              <v-text-field
                label="Email"
                placeholder="Email"
                outlined
                type="email"
              ></v-text-field>

              <v-text-field
                label="Senha"
                placeholder="Senha"
                outlined
                type="password"
                @click:append="showPassword = !showPassword"
                :append-icon="
                  showPassword ? 'mdi-eye-outline' : 'mdi-eye-off-outline'
                "
              ></v-text-field>
              
              <v-btn class="mt-5" color="primary" large block>Login</v-btn>
              <h5 class="text-subtitle1">
                Ainda não se inscreveu? <a href="">Inscreva-se</a>
              </h5>
            </v-form>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-flex>
</template>

<script>
export default {
  name: "Login",
  data: () => ({
    showPassword: false,
  }),
};
</script>

<style lang="scss" scoped>
.row-login {
  height: 80vh;
}
.banner {
  border-top-left-radius: 15px;
  border-bottom-left-radius: 15px;
}
.form {
  background-color: #fff;
  border-top-right-radius: 15px;
  border-bottom-right-radius: 15px;
}

@media screen and (max-width: 961px) {
  .form {
    border-radius: 15px !important;
  }
}
</style>