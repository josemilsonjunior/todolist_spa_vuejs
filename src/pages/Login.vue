<template>
  <q-page padding class="flex flex-center">
    <div class="row col-12">
      <q-card class="col-12">
        <q-card-section>
          <div class="text-h6">toDoList - Login</div>
        </q-card-section>
        <q-card-section class="row q-col-gutter-md q-pr-none">
          <div class="row q-col-gutter-md col-12">
            <q-input class="col-12" filled v-model="user.login" label="Login" />
            <q-input class="col-12" type="password" filled v-model="user.senha" label="Senha" />
          </div>
        </q-card-section>
        <q-card-section class="col-12 text-right  ">
          <q-btn label="cadastrar" class="q-mr-sm" color="secondary"/>
          <q-btn label="login" @click="logar" color="primary"/>
        </q-card-section>
      </q-card>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'Login',
  data () {
    return {
      user: {
        login: '',
        senha: ''
      }
    }
  },
  methods: {
    logar () {
      this.$q.notify({
        message: 'Usuário logado com sucesso!',
        color: 'positive'
      })
      this.$router.push('/')
    }
  }
}
</script>
