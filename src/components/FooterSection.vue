<script setup>
import { footerText } from "@/constants/index"
</script>
<template>
    <footer id="footer" role="contentinfo">
        <div class="footer__inner">
            <h2 class="footer__text">
                <div>ZINO</div>
                <div>@ZINO</div>
            </h2>
            <div class="footer__info">
                <div class="left">
                    <div class="title">
                        <a href="#">sign up</a>
                    </div>
                    <p class="desc">회원가입을 하시면 댓글과 게시판 기능을 이용할 수 있습니다.</p>
                </div>
                <div class="right">
                    <h3>social</h3>
                    <ul v-for="(footer, key) in footerText" :key="key">
                        <li>
                            <a href={{footer.link}}>{{ footer.title }}</a>
                            <em>{{ footer.desc }}</em>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footer__right">
                &copy; 2023 webstoryboy<br />
                이 사이트는 비트를 이용하여 제작하였습니다.
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
#footer {
    font-family: var(--mainKor-font);
}

.footer__inner {
    padding: 16px;
}

.footer__text {
    font-size: 12px;
    text-transform: uppercase;
    border-top: 1px solid var(--mainFont-color);
    border-bottom: 1px solid var(--mainFont-color);
    display: flex;
    justify-content: space-between;
    color: var(--mainFont-color);
}

.footer__info {
    display: flex;
    justify-content: space-between;
    margin: 100px 0;
}

.left {
    width: 40%;

}

.title {
    border-top: 2px solid var(--mainFont-color);
    border-bottom: 1px solid var(--mainFont-color);
    padding: 20px 0;
    text-transform: uppercase;
    font-weight: 700;
    transition: all 0.3s;
    color: var(--mainFont-color);
}

.title:hover {
    background-color: var(--white);
    color: var(--black);
    padding-left: 10px;
    border-color: transparent;
}

.desc {
    font-size: 12px;
    padding-top: 20px;
    color: var(--mainFont-color);
}


.right {
    width: 50%;
}

.right h3 {
    border-top: 2px solid var(--mainFont-color);
    font-size: 10px;
    margin-bottom: 40px;
    padding-top: 10px;
    color: var(--mainFont-color);
}

.right ul {
    border-top: 1px solid var(--mainFont-color);
}

.right li {
    border-bottom: 1px solid var(--mainFont-color);
}

.right a {
    padding: 14px 0;
    font-size: 14px;
    display: inline-block;
    text-transform: uppercase;
    color: var(--mainFont-color);
}

.right em {
    font-size: 12px;
    padding-left: 10px;
    opacity: 0;
    transition: all 0.3s;
    color: var(--mainFont-color);
}

.right em:hover {
    opacity: 1;
}


.footer__right {
    text-align: center;
    text-transform: uppercase;
    font-size: 12px;
    margin-bottom: 20px;
    color: var(--mainFont-color);
}
</style>
