<template>
    <li>
        <div class="profile-card">
            <header v-on:click="toggleClass" class="profile-header">
                <img :src="dino.image" />
                <h2>{{dino.name}}</h2>
            </header>
            <section class="skills-container" :class="{ hidden: hidden }">
                <SkillList v-bind:skills="dino.skills" />
            </section>
        </div>
    </li>
</template>

<script>
import SkillList from "./SkillList"

export default {
    name: "Card",
    components: {
        SkillList
    },
    data() { 
        return {
            hidden: true,
        }
    },
    methods: {
        toggleClass() {
            if (this.hidden === true) {
                this.hidden = false;
            } else if (this.hidden === false) {
                this.hidden = true;
            }
        }
    },
    props: ['dino']
}

</script>

<style>

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
.hidden {
    display: none;
}

</style>