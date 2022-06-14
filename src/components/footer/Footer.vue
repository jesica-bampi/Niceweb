<template>
    <footer>
        <div class="copright">
            <p>&copy;Niceweb - Todos os direitos reservados</p>
        </div>
        <div class="footer-github">
            <a href="https://github.com/jesica-bampi/niceweb" target="_blank">
                <img class="img-fluid" src="@/assets/img/github_icon.png" alt="github icon">
                <p>
                    <span>GitHub</span>
                </p>
            </a>
        </div>

    </footer>
</template>
<style lang="scss" scoped>

$darkgray: #5d5d60;

footer {
    width: 100%;
    height: 5vh;
    color: $darkgray;
    padding: 2rem 3rem;
    display: flex;
    justify-content: space-between;
    position: absolute ;
    bottom: 0;
    @media screen and (max-width: 768px) {
        flex-direction: column;
        height: 8vh;
        align-items: center;
        justify-content: center;
        text-align: center;
        padding: 0.8rem;
    }
}

.copright {
    display: flex;
    justify-content: center;
    align-items: center;
    
    p{
        font-family: 'Font Regular', sans-serif;
        font-size: 1.2rem;
        margin-bottom: 0;
        @media screen and (max-width: 450px) {
            font-size: 0.8rem;
        }
    }
    
}
.footer-github {
    display: flex;
    justify-content: center;
    align-items: center;
    a{
        all: unset;
        cursor: pointer;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 0.5rem;
        @media screen and (max-width: 450px) {
            gap: 0.2rem;
        }

        img{
            width: 2rem;
            height: 2rem;
            @media screen and (max-width: 450px) {
                width: 1.5rem;
                height: 1.5rem;
            }
        }
        p{
            margin-bottom: 0;
            font-family: 'Font Regular', sans-serif;
            font-size: 1rem;
            @media screen and (max-width: 450px) {
                font-size: 0.8rem;
            }
        }
    }
}
</style>