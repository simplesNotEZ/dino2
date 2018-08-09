<template>
    <section id="profiles-container">
        <h2>Profiles</h2>
        <ul id="profiles">
            <Card v-for="dino in dinosArray" :key='dino.id' :dino='dino' />
        </ul>
    </section>
    
</template>

<script>
import Card from './Card'

export default {
    name: "Profiles",
    components: {
        Card
    },
    props: ['dinosArray']
}
</script>

<style>

small {
    color: black;
    font-size: .5rem;
    margin-left: 10px;
}
p {
    font-size: .8rem;
}

</style>