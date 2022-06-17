<template>
    <div class="wrapper">
        <NavBar />
    </div>
</template>

<script setup>
// const searchTerm = "jacek piekara";
// let title = ref("");
// let author = ref("");

// const getData = async () => {
//     const response = await fetch(
//         `https://www.googleapis.com/books/v1/volumes?q=${searchTerm}`
//     );

//     const data = await response.json();

//     title.value = data.items[0].volumeInfo.title;
//     author.value = data.items[0].volumeInfo.authors[0];
// };
// getData();
import NavBar from "../components/NavBar.vue";
import { ref } from "@vue/reactivity";
</script>

<style scoped>
.wrapper {
    width: 100vw;
    min-height: 100vh;

    /* display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center; */
}

/* .api-content {
    width: 40vw;
    height: 30vh;

    display: flex;
    flex-direction: column;
    gap: 2rem;
    justify-content: center;
    align-items: center;

    background-color: var(--color-primary-light);
} */
</style>