<script>
export default {
    name: 'AppHeaderTitle'
}
</script>

<template>
    <h1 class="text-center mb-4"> Rick & Morty App</h1>
    <form class="d-flex justify-content-center ">
        <input type="text" placeholder="Search Character" class="border rounded">

        <select class="border rounded" name="" id="">
            <option value="Opzione-1">
                Select status
            </option>
        </select>

        <button class="border rounded p-1 btn btn-primary">
            Search
        </button>

        <button class="border rounded p-1 btn btn-warning">
            Reset
        </button>

    </form>

</template>

<style scoped>
form {
    gap: 10px;
}
</style>