<script lang="ts">
import type { PropType } from "vue";
import Tag from "./Tag.vue";

export default {
    components: { Tag },
    props: {
        ingredientes: {
            type: Array as PropType<string[]>,
            required: true,
        },
    },
};
</script>

<template>
    <section>
        <span class="subtitulo-lg sua-lista-texto"> Sua Lista: </span>
        <!-- diretiva if pra exibir ou não informações -->
        <ul v-if="ingredientes.length" class="ingredientes-sua-lista">
            <li v-for="ingrediente in ingredientes" v-bind:key="ingrediente">
                <Tag :texto="ingrediente" :ativa="true" />
            </li>
        </ul>

        <!-- diretiva else pra exibir ou não informações -->
        <p v-else class="paragrafo lista-vazia">
            <img src="../assets/images/icones/lista-vazia.svg" alt="" />Sua
            lista está vazia, selecione ingredientes para iniciar.
        </p>
    </section>
</template>

<style scoped>
.sua-lista-texto {
    color: var(--coral, #f0633c);
    display: block;
    text-align: center;
    margin-bottom: 1.5rem;
}

.ingredientes-sua-lista {
    display: flex;
    justify-content: center;
    gap: 1rem 1.5rem;
    flex-wrap: wrap;
}

.lista-vazia {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 0.25rem;

    color: var(--coral, #f0633c);
    text-align: center;
}
</style>
