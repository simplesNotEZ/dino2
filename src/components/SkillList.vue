<template>
    <div class="profile-card">
        <header class="profile-header">
            <img src="{{image}}" />
            <h2>{{name}}</h2>
        </header>
        <section class="skills-container hidden">
            <h4>Skills</h4>
            <ul class="skills-list">
                {{#each skills}}
                <li>{{this}}</li>
                {{/each}}
            </ul>
        </section>
    </div>
</template>

<script>
export default {
    name: "SkillList"
}
</script>

<style>
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