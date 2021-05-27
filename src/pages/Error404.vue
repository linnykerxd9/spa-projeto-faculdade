<template>
  <div class="fullscreen bg-404 text-white text-center q-pa-md container">
    <div>
      <q-toolbar-title class="text-h5">
        <q-avatar><img src="/imagens/study.svg" alt="logo cursos"></q-avatar>
        Cursos
      </q-toolbar-title>
     <div class="flex flex-center">
       <div>
          <div style="font-size: 20vh">
        404
      </div>
      <img src="/imagens/404.svg" alt="" style="width:45%; height:45%;">
      <div class="text-h4" style="opacity:.4">
        Oops. Algo não funcionou corretamente...
      </div>

      <q-btn
        class="q-mt-xl"
        color="white"
        text-color="blue"
        unelevated
        to="/"
        label="retornar ao início"
        no-caps
      />
    </div>
       </div>
     </div>
  </div>
</template>

<script>
export default {
  name: 'Error404'
}
</script>
<style>
.bg-404{
  background-color:#2a7ae4;
}
</style>
