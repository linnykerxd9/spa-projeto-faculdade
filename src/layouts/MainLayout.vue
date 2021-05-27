
<template>
  <q-layout view="hHh lpR fff">

    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
         <q-btn dense flat round icon="menu" @click="left = !left" />

        <q-toolbar-title class="text=h4">
          <q-avatar>
            <img src="../assets/study.svg">
          </q-avatar>
          Cursos
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="left" side="left" bordered>
       <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          Essential Links
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer class="text-white bg-footer">
      <q-toolbar>
        <p class="text-blue-2">
          Cursos - todos os direitos reservados &copy;
        </p>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>


<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
  {
    title: 'Home',
    caption: 'início do app',
    icon: 'home',
    link: '/'
  },
  {
    title: 'Formações',
    caption: 'lista dos cursos',
    icon: 'list',
    link: '/#/formacoes'
  },
  {
    title: 'Atividades',
    caption: 'lista de atividades',
    icon: 'list',
    link: '/#/atividades'
  },
  {
    title: 'Usuário',
    caption: 'lista de usuários',
    icon: 'account_circle',
    link: '/#/usuarios'
  },
];

export default {
  name: 'MainLayout',
  components: { EssentialLink },
  data () {
    return {
      left: false,
      essentialLinks: linksData
    }
  }
}
</script>

<style>
.bg-footer{
  background-color:#0d3b69;
}
</style>
