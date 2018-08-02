<template>
    <main>
        <section id="profiles-container">
            <h2>Profiles</h2>
            <ul id="profiles"></ul>
        </section>
    </main>
</template>

<script>
import Card from './Card'
export default {
    name: "Profiles"
}
</script>

<style>
main {
    grid-row: 2/3;
}

main section {
    padding: 0 20px 0 20px;
    display: grid;
    grid-template-columns: repeat(auto-fit, x100%);
    grid-gap: 10px;
    margin: 0 auto;
    width: 50%;
}

small {
    color: black;
    font-size: .5rem;
    margin-left: 10px;
}

p {
    font-size: .8rem;
}

/* Profile Cards */

.profile-card {
    border-radius: 6px;
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.3);
    padding: 10px;
  /* margin: 0 auto 10px auto; */
}

.profile-header {
    display: flex;
    flex-flow: row nowrap;
}

.profile-header img {
    width: 100px;
    height: 100px;
    border: 1px solid darkgrey;
    margin: 0 10px 0 10px;
}

.skills-list {
    list-style: none;
}

</style>