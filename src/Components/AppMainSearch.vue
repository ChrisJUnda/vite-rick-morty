<script>
import { store } from '../store';


export default {
    name: 'AppMainSearch',
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <div class="text-center mb-4 fw-bold">
        Found {{ store.results.length }} Characters
    </div>
</template>