<script setup>
import { skillText } from '../constants';
</script>

<template>
    <section id="skill">
        <div class="skill__inner">
            <h2 class="skill__title">
                challenge <em>나의 도전</em>
            </h2>
            <div class="skill__desc">
                <div v-for="(skill, key) in skillText" :key="key">
                    <span>{{ key + 1 }}.</span>
                    <h3>{{ skill.title }}</h3>
                    <p>{{ skill.desc }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.skill__inner {
    padding: 16px;
    display: flex;
    justify-content: space-between;
}

.skill__title {
    position: sticky;
    top: 65px;
    left: 0;
    width: 48%;
    height: 4.9vw;
    font-size: 4vw;
    font-weight: 900;
    line-height: 1.6;
    text-transform: uppercase;
    font-family: var(----mainEng-font);
    border-bottom: 0.4vw solid var(--red);
    color: var(--red);
}

.skill__title em {
    font-family: var(--mainKor-font);
    font-size: 1.25rem;
    font-weight: 400;
    display: inline-block;
    vertical-align: 4px;
}

.skill__desc {
    width: 50%;
}

.skill__desc span {
    font-size: 5vw;
    line-height: 1.5;
    font-weight: 900;
    font-family: var(--mainNum-font);
    color: var(--mainFont-color);
}

.skill__desc h3 {
    font-size: 1.5rem;
    text-decoration: underline;
    text-underline-position: under;
    margin-bottom: 1vw;
    color: var(--mainFont-color);

}

.skill__desc p {
    margin-bottom: 30vh;
    color: var(--mainFont-color);
    font-family: var(--mainKor-font);
    font-size: 1.1rem;
}


@media (max-width: 800px) {
    .skill__inner {
        flex-direction: column;
    }

    .skill__title {
        width: 100%;
        margin-bottom: 10vw;
        height: auto;
        background-color: var(--mainBg-color);
    }

    .skill__desc {
        width: 100%;
    }

    .skill__desc span {
        font-size: 20vw;
    }
}
</style>