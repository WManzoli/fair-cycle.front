<template>
  <header class="header-area" style="background: #c5c5c5">
    <div id="home" class="header-hero bg_cover">
      <div class="container" style="min-height: 90vh;">
        <v-card class=" mt-100">
          <v-card-title>
            Registro de Atendimento
          </v-card-title>
          <v-card-subtitle>
            Atenção ao preencher os campos.
          </v-card-subtitle>
          <form class="px-3 py-4">
            <v-text-field
              prepend-icon="mdi-account"
              type="text"
              placeholder="Nome do Dono"
              required
            />
            <v-text-field
              prepend-icon="mdi-bike"
              type="text"
              placeholder="Marca da bicicleta"
              required
            />
            <v-text-field
              prepend-icon="mdi-matrix"
              type="text"
              placeholder="Numero de série"
              required
            />
            <v-text-field
              prepend-icon="mdi-text"
              type="text"
              placeholder="Descrição do serviço"
              required
            />
            <v-file-input
              prepend-icon="mdi-file"
              placeholder="Arquivos"
              counter
              multiple
              show-size
              truncate-length="50"
            />
            <span
              class="d-flex align-items-baseline mb-4"
            >
              <v-checkbox
                class="px-2"
                color="red"
                value="red"
                hide-details
              /><span>Declaro que li e concordo com os as informações citadas acima.</span>
            </span>
            <v-btn>
              Enviar
            </v-btn>
            <v-btn @click="$router.push('/home')">
              Cancelar
            </v-btn>
          </form>
        </v-card>
      </div> <!-- container -->
    </div> <!-- header hero -->
  </header>
</template>

<script>

export default {
  data () {
    return {
      // currentWord: '',
      // currentWordArray: ['Segurança', 'Atendimento', 'Manutenção', 'Garagem']
    }
  },
  methods: {
    handleClick () {
      window.setTimeout(function () { window.blipClient.toogleChat() })
    }
  }
}
</script>

<style scoped>

</style>
