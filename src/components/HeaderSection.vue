<script setup>
import { headerNav } from "@/constants/index"
</script>

<template>
    <header id="header" role="banner">
        <div class="header__inner">
            <div class="header__logo">
                <a href="#">Zino <em>portfolio</em></a>
            </div>
            <div class="header__nav" role="navigation" aria-label="메인 메뉴" :class="{ show: isNavVisible }">
                <ul>
                    <li v-for="(nav, key) in headerNav" :key="key">
                        <a :href="nav.url" @click="scrollLink($event)">{{ nav.title }}</a>
                    </li>
                </ul>
            </div>
            <div class="header__nav__mobile" id="headerToggle" aria-controls="primary-menu"
                aria-expanded="isNavVisible.toString()" role="button" @click="toggleMobileMenu">
                <span></span>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    data() {
        return {
            isNavVisible: false,
        };
    },
    methods: {
        toggleMobileMenu() {
            this.isNavVisible = !this.isNavVisible;
        },
        scrollLink(event) {
            event.preventDefault();

            const targetId = event.target.getAttribute("href");
            const targetElement = document.querySelector(targetId);

            if (targetElement) {
                targetElement.scrollIntoView({ behavior: "smooth" });
            }
        },
    },
};
</script>



<style lang="scss">
#header {
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    z-index: 10000;

}

.header__inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: var(--subBg100);
    padding: 1rem;
}

.header__logo a {
    font-size: 30px;
    color: var(--red);
    font-weight: 500;
    text-align: center;
    line-height: 1;
}

.header__nav {
    margin-left: auto;
}

.header__nav li {
    display: inline;
    padding: 15px 25px;
}

/* .header__nav li:hover{
    background-color: var(--black);
    border-radius: 10px;
} */
.header__nav li a {
    font-size: 22px;
    font-weight: 500;
    color: var(--mainFont-color);
    position: relative;
}

.header__nav li a:hover {
    text-decoration: underline;
    color: var(--red);
}

.header__nav li a::before {
    content: '';
    width: calc(100% - 30px);
    height: 1px;
    background-color: #fff;
    position: absolute;
    left: 15px;
    bottom: 5px;
    transform: scaleX(0);
    transition: all 0.3s;
}

.header__nav li a:hover::before {
    transition: scalex(1);
    color: var(--white);

}

.header__nav__mobile {
    width: 40px;
    height: 40px;
    cursor: pointer;
    display: none;
}

.header__nav__mobile span {
    display: block;
    width: 40px;
    height: 2px;
    background-color: var(--red);
    margin-top: 19px;
    position: relative;
}

.header__nav__mobile span::before {
    content: '';
    width: 40px;
    height: 2px;
    background-color: var(--red);
    position: absolute;
    right: 0;
    top: 6px;
    transition: width 0.3s;
}

.header__nav__mobile span::after {
    content: '';
    width: 40px;
    height: 2px;
    background-color: var(--red);
    position: absolute;
    left: 0;
    bottom: 6px;
    transition: width 0.3s;
}


@media (max-width: 800px) {
    .header__nav {
        display: none;
    }

    .header__nav.show {
        display: block;
    }

    .header__nav.show ul {
        display: block;
        position: absolute;
        right: 0;
        top: 68px;
        background-color: var(--subBg100);
        z-index: 10000;
        min-width: 159px;
        padding: 20px 0;
    }

    .header__nav.show ul li {
        display: block;
        text-align: right;
    }

    .header__nav.show ul li a {
        display: inline-block;
        padding: 10px;
    }

    .header__nav.show+.header__nav__mobile span::before {
        width: 20px;
    }

    .header__nav.show+.header__nav__mobile span::after {
        width: 20px;
    }

    .header__nav__mobile {
        display: block;
    }
}
</style>