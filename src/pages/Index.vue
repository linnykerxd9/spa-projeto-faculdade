<template>
  <q-page class="container">
    <div id="info">
      <div class="row justify-center q-pa-lg">
        <div class="col col-xs-12 col-sm-12 col-md-5 col-lg-3">
          <header><h2>Cursos de Tecnologia e Negócios Digitais</h2></header>
          <p>Você vai estudar, práticar, discutir e aprender em uma comunidade de inquietos e inovadores</p>
        </div>
        <div class="col col-xs-12 col-sm-12 col-md-3 col-lg-3">
          <img src="../assets/estudante.svg" alt="uma estudante com seus livros"/>
        </div>
      </div>
    </div>
    <section id="descCursos">
      <div class="row justify-center q-pa-lg">
        <header><h3>Formações</h3></header>
      </div>
    	<div class="q-pa-md row justify-start wrap q-gutter-md justify-center">
		    <q-card class="my-card" v-for="curso in cursos" :key="curso.id">
		      <q-card-section>
		      	<q-img :src="curso.imagem" spinner-color="white" />
		        <div class="text-h5 text-indigo-9">{{ curso.titulo }}</div>
		      </q-card-section>

		      <q-card-section class="q-pt-none">
		        <p>{{ curso.descricao }}</p>
		        <q-btn color="primary" label="Começar" />
		      </q-card-section>
		    </q-card>
    	</div>
    </section>
    <section id="depoimentos" class="bg-indigo-1 q-pb-xl">
    	<div class="row q-pa-md q-gutter-md">
    		<div class="col col-lg-4 offset-lg-2">
    			<header><h4 class="text-blue-9 q-mt-xs">A maior plataforma brasileira de cursos de tecnologia.</h4></header>
    			<p class="text-body1">São 1272 cursos, 100% em português. E novos lançamentos todas as semanas.</p>
    		</div>
    		<div class="col col-lg-2">
    			<q-card class="p-pa-md">
		      <q-card-section>
		        <div class="text-h5 text-indigo-9">José Pedro</div>
		      </q-card-section>

		      <q-card-section class="q-pt-none">
		        <p>Se você não sabe a ordem do que deve aprender e praticar para dominar uma tecnologia, a forma como os cursos estão organizados e estruturados nos ajuda muito.</p>
		      </q-card-section>
		    </q-card>
    		</div>
    		<div class="col col-lg-2">
    			<q-card class="p-pa-md">
		      <q-card-section>
		        <div class="text-h5 text-indigo-9">Mariana Souza</div>
		      </q-card-section>

		      <q-card-section class="q-pt-none">
		        <p>Consegui fazer uma mudança de carreira em uma área muito disputada e estou muito feliz:</p>
		      </q-card-section>
		    </q-card>
    		</div>
    	</div>
    </section>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data() {
    return{
        cursos:[{
  			id:1,
  			titulo: "Curso HTML5 e CSS3",
  			descricao: "O Curso de HTML5 e CSS3 vai ensinar a criar sites usando a linguagem de marcação hipertexto (HTML) e folhas de estilo em cascata (CSS).",
  			imagem:"../../formacoes/css-file.svg"
  		},
  		{
  			id:2,
  			titulo: "Git e GitHub",
  			descricao: "Curso de Git e GitHub: grátis, prático e sem usar comandos no terminal.",
  			imagem:"../../formacoes/git.svg"
  		},
  		{
  			id:3,
  			titulo: "Javascript",
  			descricao: "Curso de JavaScript, voltado para iniciantes sobre ECMAScript, a versão padronizada do JS.",
  			imagem:"../../formacoes/coding.svg"
  		},
  		{
  			id:4,
  			titulo: "Vue.js",
  			descricao: "Construa do zero uma Single Page Application e crie seus próprio componentes.",
  			imagem:"../../formacoes/device.svg"
  		}]
    }
  }
}
</script>

<style>
div#info{
	background-color: #2a7ae4;
	color: #fff;
}
div#info h2{
	font-weight: 800;
}
div#info p{
	font-size: 23px;
}
#descCursos{
  margin-bottom:2%;
}
section#descCursos h3{
	margin-bottom: 0.2em;
	font-weight: 300;
}
.my-card{
  width: 100%;
  max-width: 250px;
}
</style>
