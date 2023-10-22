<template>
    <div class="cadastro-main">
        <div class="cadastro-container">
            <!-- Titulo principal -->
            <h1>Descubra os <span> Investimentos do Momento </span> e esteja 
            sempre à <span>frente das novidades</span> em nossa carteira.
            </h1>

            <!-- Subtitulo-->
            <p>Junte-se a nós e <span>potencialize</span> seus ganhos financeiros!</p>
        
            <p class="msgError">Componente de Mensagem</p>
            <form class="cadastro-form" id="cadastro-form">
                <!-- Nome do Usuario-->
               <div class="input-container">
                    <input type="text" id="nome" v-model="nome" required>
                    <label for="nome">Nome completo</label>
                </div>

                <!-- Nome do Email-->
                <div class="input-container">
                     <input type="text" id="email" v-model="email" required @input="validateEmail">
                    <label for="email">Email</label>
                    <i data-v-e8645e48="" class="las la-info-circle" data-tooltip="Informações 
                    importantes serão enviadas para este endereço"></i>
                </div>

                <!-- Nome do CPF-->
                <div class="input-container">
                    <input type="text" id="cpf" v-model="cpf" required>
                    <label for="cpf">CPF</label>
                </div>

                <!-- Nome do Telefone-->
                <div class="input-container">
                     <input type="tel" id="telefone" v-model="telefone" required>
                    <label for="telefone">Telefone de Contato</label>
                </div>

                 <!-- Btn Enviar-->
                <div class="input-container">
                     <button type="submit"  class="btnEnviar" id="submit-btn" >Enviar</button>
                </div>

                <!-- autoriza os dados -->
                <div class="input-containercheckbox">
                    <input type="checkbox" id="autorizacao" v-model="autorizacao" required>
                     <label for="autorizacao"> Ao continuar, você autoriza a coleta de seus dados pessoais.<br> Nossa <a href="https://www.ativainvestimentos.com.br/Institucional/Compliance/LGPD/">Política de Privacidade</a> com o objetivo de comunicar informações sobre investimentos.</label>
                </div>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    nome: "Formulario",
};
</script>


<style scoped>

</style>
