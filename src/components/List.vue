<script setup lang="ts">

</script>



<template>
	
    <div class="list">

        <table>
            <tr>
                <th>Word</th>
                <th>Word in Spanish</th>
                <th>Pronunciation</th>
            </tr>
            <tr>
                <td>Hello</td>
                <td>Hola</td>
                <td>jelou</td>
            </tr>
            <tr>
                <td>Love</td>
                <td>Amor</td>
                <td>lav</td>
            </tr>
            <tr>
                <td>Tree</td>
                <td>Árbol</td>
                <td>tri</td>
            </tr>
            <tr>
                <td>Sun</td>
                <td>Sol</td>
                <td>sán</td>
            </tr>
            <tr>
                <td>Book</td>
                <td>Libro</td>
                <td>buk</td>
            </tr>
            <tr>
                <td>Water</td>
                <td>Agua</td>
                <td>uóter</td>
            </tr>
            <tr>
                <td>Friend</td>
                <td>Amigo/amiga</td>
                <td>frend</td>
            </tr>
            <tr>
                <td>House</td>
                <td>Casa</td>
                <td>jáus</td>
            </tr>
            <tr>
                <td>Cat</td>
                <td>Gato/gata</td>
                <td>kat</td>
            </tr>
            <tr>
                <td>Time</td>
                <td>Tiempo</td>
                <td>taim</td>
            </tr>
        </table>

    </div>
    
</template>



<style scoped>

    .list {}
    .list table {}

    .list table tr {}

    .list table tr th {}
    .list table tr td {
        padding: 10px;
        font-size: 20px;
        font-weight: 600;
    }
    .list table tr td:nth-child(1) {
        color: #fff;
        background-color: rgb(11, 114, 24);
    }
    .list table tr td:nth-child(2) {
        color: #000;
        background-color: greenyellow;
    }
    .list table tr td:nth-child(3) {
        color: #000;
        background-color: yellow;
    }

</style>