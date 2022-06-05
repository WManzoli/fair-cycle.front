<template>
  <header class="header-area">
    <div class="navbar-area px-4" :class="{ sticky: scrolled }">
      <div class="container ">
        <div class="row  ">
          <div class="w-100 py-2 ">
            <nav class="d-flex justify-content-between">
              <h1 class="navbar-brand" href="index.html">
                <img style="width: 3rem" src="~/assets/basic/assets/images/logo.png" alt="Logo">&nbsp;- Fair Cycle
              </h1>

              <div class="">
                <p v-if="$route.fullPath !== '/painel' " class="main-btn wow fadeInUp" data-wow-duration="1.3s" data-wow-delay="1.1s" @click="isModalVisible = !isModalVisible">
                  Entrar
                </p>
                <p v-else-if="$route.fullPath !== '/home' && !isModalVisible" class="main-btn wow fadeInUp" data-wow-duration="1.3s" data-wow-delay="1.1s" @click="$router.push('/home')">
                  Sair
                </p>
              </div>

              <v-card v-if="isModalVisible" class="mr-3 mt-1 login-modal" @mouseleave="isModalVisible = !isModalVisible">
                <v-list>
                  <v-list-item>
                    <v-list-item-avatar>
                      <img
                        src="https://blipmediastore.blob.core.windows.net/public-medias/Media_facbbeb5-1e48-479e-b117-9c59138c6071"
                        alt="Fairzinho"
                      >
                    </v-list-item-avatar>

                    <v-list-item-content class="pl-2">
                      <v-list-item-title>Seja Bem-Vindo</v-list-item-title>
                      <v-list-item-subtitle>Att Fairzinho.</v-list-item-subtitle>
                    </v-list-item-content>

                    <!--                    <v-list-item-action>-->
                    <!--                      <v-btn-->
                    <!--                        :class="fav ? 'red&#45;&#45;text' : ''"-->
                    <!--                        icon-->
                    <!--                        @click="fav = !fav"-->
                    <!--                      >-->
                    <!--                        <v-icon>mdi-heart</v-icon>-->
                    <!--                      </v-btn>-->
                    <!--                    </v-list-item-action>-->
                  </v-list-item>
                </v-list>

                <v-divider />

                <v-list>
                  <v-list-item>
                    <v-text-field
                      v-model="user"
                      :rules="rules"
                      counter
                      maxlength="25"
                      type="text"
                      label="Login"
                    />
                  </v-list-item>

                  <v-list-item>
                    <v-text-field
                      v-model="password"
                      :append-icon="show ? 'mdi-eye' : 'mdi-eye-off'"
                      :rules="[rules.required, rules.min]"
                      :type="show ? 'text' : 'password'"
                      label="Senha"
                      hint="Pelo menos 5 caracteres"
                      counter
                      @click:append="show = !show"
                    />
                  </v-list-item>
                </v-list>

                <v-card-actions>
                  <v-spacer />

                  <v-btn
                    text
                    @click="isModalVisible = false"
                  >
                    Voltar
                  </v-btn>
                  <v-btn
                    color="primary"
                    text
                    @click="pushToRoute('/painel')"
                  >
                    Enviar
                  </v-btn>
                </v-card-actions>
              </v-card>
            </nav> <!-- navbar -->
          </div>
        </div> <!-- row -->
      </div> <!-- container -->
    </div> <!-- navbar area -->
  </header>
</template>

<script>
import $ from 'jquery'

export default {
  data () {
    return {
      isModalVisible: false,
      scrolled: false,
      fav: true,
      menu: false,
      message: false,
      hints: true,
      show: false,
      user: 'Admin',
      password: '12345',
      rules: {
        required: value => !!value || 'Required.',
        min: v => v.length >= 8 || 'Minimo de 5 caracteres'
      }
    }
  },
  mounted () {
    // Sticky headesr
    $(window).on('scroll', () => {
      this.scrolled = $(window).scrollTop() > 20
    })
  },
  methods: {
    pushToRoute (value) {
      this.$router.push(value)
      this.isModalVisible = false
    }
  }
}
</script>
