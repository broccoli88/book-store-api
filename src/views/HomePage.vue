<template>
    <div class="wrapper">
        <div class="api-content">
            <span class="api-x"> </span>
            <span class="api-x"></span>
            <span class="api-x"></span>
            <span class="api-x"></span>
            <span class="api-x"></span>
        </div>
    </div>
</template>

<script setup>
const searchTerm = "jacek piekara";
const getData = async () => {
    const response = await fetch(
        `https://www.googleapis.com/books/v1/volumes?q=${searchTerm}`
    );
    const data = await response.json();

    console.log(data.items[0].volumeInfo);
};
getData();
</script>

<style scoped>
.wrapper {
    width: 100vw;
    min-height: 100vh;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
</style>