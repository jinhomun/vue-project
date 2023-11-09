<script setup>
import { portText } from "@/constants/index"
</script>


<template>
    <section id="port">
        <nav class="port__inner">
            <div class="port__title">
                portfolio<em>나의 작업물</em>
            </div>
            <div class="port__wrap">
                <div v-for="(text, key) in portText" :key="key" :class="['port__item p' + (key + 1)]">
                    <span class="num">{{ text.num }}</span>
                    <a href={{text.code}}>
                        <img :src="text.img" :alt="text.name">
                    </a>
                    <h3 class="title">{{ text.title }}</h3>
                    <p class="desc">
                        {{ text.desc }}
                    </p>
                    <a href={{text.view}}>사이트 보기</a>
                </div>
            </div>
        </nav>
    </section>
</template>

<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

export default {
    mounted: function () {
        this.scrollAnimation();
    },
    methods: {
        scrollAnimation() {
            gsap.registerPlugin(ScrollTrigger);
            const horSection = gsap.utils.toArray(".port__item");

            gsap.to(horSection, {
                xPercent: -120 * (horSection.length - 1),
                ease: "none",
                scrollTrigger: {
                    trigger: "#port",
                    start: "top top",
                    end: "+=3000",
                    pin: true,
                    scrub: 1,
                    markers: false,
                    invalidateOnRefresh: true,
                    anticipatePin: 1,
                }
            });
        }
    }
}
</script>

<style lang="scss">
#port {
    width: 100%;
    overflow: hidden;
}

.port__inner {
    padding: 16px;
}

.port__title {
    border-bottom: 0.4vw solid #2b2b2b;
    border-bottom: 0.4vw solid var(--white);
    color: #2b2b2b;
    color: var(--red);
    font-family: nanumSquareNeo;
    font-family: var(--mainKor-font);
    font-size: 4vw;
    font-weight: 900;
    height: 5vw;
    line-height: 1.6;
    margin-bottom: 16px;
    text-indent: -0.26vw;
    text-transform: uppercase;
    width: 100%;
}

.port__title em {
    font-size: 1.25rem;
    font-weight: 400;
    line-height: 2;
}

.port__wrap {
    display: flex;
    flex-wrap: wrap;
    width: 7000px;
}

.port__item {
    width: 500px;
    height: 70vh;
    padding: 2.5rem;
    margin-right: 20px;
}

.port__item.p1 {
    background-color: var(--subBg200);
}

.port__item.p2 {
    background-color: var(--subBg400);
}

.port__item.p3 {
    background-color: var(--subBg200);
}

.port__item.p4 {
    background-color: var(--subBg400);
}

.port__item.p5 {
    background-color: var(--subBg200);
}

.port__item.p6 {
    background-color: var(--subBg400);
}

.port__item.p7 {
    background-color: var(--subBg200);
}

.port__item.p8 {
    background-color: var(--subBg400);
}

.port__item.p9 {
    background-color: var(--subBg200);
}

.port__item.p10 {
    background-color: var(--subBg400);
}

.port__item .num {
    font-family: var(--mainNum-font);
    font-size: 2rem;
}

.port__item img {
    display: block;
    margin-top: -20px;
    transition: margin-top 0.3s;
    border-radius: 5px;
    filter: saturate(0%);
    transition: all 0.3s;
}

.port__item img:hover {
    margin-top: 0;
    filter: saturate(100%);
}

.port__item .title {
    border-bottom: 2px solid #2b2b2b;
    border-bottom: 2px solid var(--black100);
    color: #2b2b2b;
    color: var(--black100);
    font-size: 1.5rem;
    font-weight: 700;
    margin-bottom: 1rem;
    padding: 0.8rem 0;
    text-align: center;
}

.port__item .desc {
    font-size: 1rem;
}
</style>