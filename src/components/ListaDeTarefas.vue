<template>
    <ul class="list-group mt-4">
        <li class="list-group-item" v-for="tarafa in getTarefasFiltradas()" :key="tarafa.titulo">
            <input @change="evento => tarafa.finalizada = evento.target.checked" :checked="tarafa.finalizada" :id="tarafa.titulo" type="checkbox">
            <label :class="{ done: tarafa.finalizada === true }" class="ms-3" :for="tarafa.titulo">
            {{ tarafa.titulo }}
            </label>
        </li>
    </ul>
</template>