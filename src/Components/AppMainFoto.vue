<script>
import { store } from '../store';
export default {
    name: 'AppMainFoto',
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="container mt-3">
        <ul class="row">
            <li class="col-3" v-for="card in store.results">
                <img :src="card.image" alt="">
                <h2> {{ card.name }}</h2>
                <p>{{ card.status }}</p>
                <p> {{ card.species }}</p>
            </li>
        </ul>
    </div>
</template>

<style>
img {
    width: 100%;
}
</style>