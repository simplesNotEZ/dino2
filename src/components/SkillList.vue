<template>
    <div>
        <h4>Skills</h4>
        <ul class="skills-list">
            <Skills v-for='skill in skills' :key='skill.id' :skill="skill"/>
        </ul>
    </div>
</template>

<script>
import Skills from "./Skills"
export default {
    name: "SkillList",
    components: {
        Skills
    },
    props: ['skills']
}
</script>

<style>

.skills-list {
    list-style: none;
}

</style>