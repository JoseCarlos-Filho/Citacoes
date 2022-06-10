<template>
	<div id="app">
		<!--<Citacoes />
		<Sobre /> -->
		<!-- Utilização de componente dinâmico -->
		<span>
			<button @click="dinamicComponente = 'Citacoes'">Citações</button>
			<button @click="dinamicComponente = 'Sobre'">Sobre</button>
		</span>
		<!-- 
			Tag <keep-alive> não destroi o componente quando vocês
			alterna entre o botão sobre e citações ou seja voce retorna
			na mensagem onde parou de navegar entre os botões de navegação.
			Sem a tag <keep-alive> voccê sempre retona na navegação com
			texto padrão 
		-->
		<keep-alive>
			<!-- Tag component é padrão do Vue.JS -->
			<component :is="dinamicComponente" />
		</keep-alive>

	</div>
</template>

<script>
import Citacoes from './components/Citacoes'
import Sobre from './components/Sobre'

export default {
	components: { Citacoes, Sobre },
	data() {
		return {
			dinamicComponente: 'Citacoes'
		}
	}
}
</script>

<style>
	#app {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 100vh;
		font-size: 1.6rem;
	}

	button {
        outline: none;
        padding: 5px 15px 10px;
        margin: 10px 5px;
        border-radius: 3px;
        font-size: 2rem;
        font-weight: 300;
        color: #FFF;
        background-color: rgba(0, 0, 0, .5);
    }
</style>