<template>

    <div class="urna-teclado">
        <div class="urna-teclado-numerico">
            <div class="urna-teclado-numerico-linha">
                <button @click="adicionaNumero(1)">1</button>
                <button @click="adicionaNumero(2)">2</button>
                <button @click="adicionaNumero(3)">3</button>
            </div>
            <div class="urna-teclado-numerico-linha">
                <button @click="adicionaNumero(4)">4</button>
                <button @click="adicionaNumero(5)">5</button>
                <button @click="adicionaNumero(6)">6</button>
            </div>
            <div class="urna-teclado-numerico-linha">
                <button @click="adicionaNumero(7)">7</button>
                <button @click="adicionaNumero(8)">8</button>
                <button @click="adicionaNumero(9)">9</button>
            </div>
            <div class="urna-teclado-numerico-linha">
                <button @click="adicionaNumero(0)">0</button>
            </div>

        </div>
        <div class="urna-teclado-acoes">
                <button class="btn-branco" @click="votarEmBranco()">BRANCO</button>
                <button class="btn-corrige" @click="corrige()">CORRIGE</button>
                <button class="btn-confirma" @click="confirmar()">CONFIRMA</button>

        </div>

    </div>

</template>


<script>
export default{
    name:"tecladoUrna",
    props: {
        adicionaNumero: Function,
        corrige: Function,
        confirmar: Function,
        votarEmBranco: Function,
    }
}

</script>


<style>

.urna-teclado{
    width: 38%;
    height: 100%;
    background-color: var(--ballot-box-keyboard-color);
    padding: 20px;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
}

.urna-teclado-numerico{
    width: 100%;
}

.urna-teclado-numerico-linha {
    display: flex;
    justify-content: space-around;
    margin-bottom: 20px;
}

.urna-teclado-numerico button{
    background-color: var(--ballot-box-keyboard-button-color);
    color: var(--light-text-color);
    font-size: 30px;
    border-radius: 10px;
    width: 80px;
    height: 50px;

}

.urna-teclado-acoes {
    display: flex;
    justify-content: space-between;
}

.urna-teclado-acoes button{
    color: var(--dark-text-color);
    font-size: 15px;
    border-radius: 5px;
    width: 30%;
    height: 50px;
}

.btn-branco{
    background-color: var(--ballot-box-white-button-color);
}

.btn-corrige{
    background-color: var(--ballot-box-correct-button-color);
}

.btn-confirma{
    background-color: var(--ballot-box-confirm-button-color);
}

</style>