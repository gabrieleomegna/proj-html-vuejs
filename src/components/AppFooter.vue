<template>
    <footer>
        <!-- ? Il footer è diviso in due sezioni -->
        <div id="ftr-list-container">
            <section id="ftr-list" class="container">
                <!-- Qua ci sono 3 colonne, di cui le 2 più a destra sono degli ul 
                     con le voci di menu CHE ARRIVANO DIRETTAMENTE DALL'APP VUE TRAMITE PROPS-->
                <div class="ftr-block">
                    <h4>About</h4>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quisquam cum a praesentium quod itaque reiciendis libero accusamus ratione tempore aliquam? Nulla omnis corrupti placeat fugiat distinctio sunt sequi, blanditiis corporis!</p>
                    <p></p>
                </div>
                <div class="ftr-block">
                    <ul>
                        <h4 class="ftr-small-title">Avada Movers</h4>
                        <li v-for="singleItem in menuItems">&#8250;  {{ singleItem.label }}</li>
                    </ul>
                </div>
                <div class="ftr-block">
                    <ul>
                        <h4 class="ftr-small-title">Recent Posts</h4>
                        <li v-for="singleItem in recentPostItems">&#8250;  {{ singleItem.string }}</li>
                    </ul>
                </div>
            </section>
        </div>
        <section id="copyright">
            <!-- Questa è la sezione che è molto simile alla prima dell'header -->
            <p>© Copyright 2012-2020 | Avada Theme By ThemeFusion | All Rights Reserved | Powered by GabriPress</p>
            <div id="brands-symbols">
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-instagram"></i>
                <i class="fa-brands fa-youtube"></i>
            </div>
        </section>
    </footer>
</template>
<script>
export default {
    props: {
        menuItems: {
            type: Object,
            required: true
        },
        recentPostItems: {
            type: Object,
            required: true
        }
    }
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

footer {
    background-color: $hdr-ftr-bg-color;
    padding-top: .75rem;
    div#ftr-list-container {
        background-color: white;
        // margin-top: 1rem;
        section#ftr-list {
            @include flex(row, space-between, stretch);
            padding: 3rem 0;
            background-color: white;
            .ftr-block{
                width: calc((100%/3) - 1rem);
                margin-right: .5rem;
                ul {
                    list-style-type: none;
                    *:not(h4) {
                        margin-bottom: 1.4rem;
                        font-size: .7rem;
                        font-weight: 500;
                    }
                    *:not(h4):hover {
                        color: #6abf16;
                    }
                }
            }
            .ftr-block:first-child p{
                text-align: start;
                line-height: 1.3rem;  
                font-size: .7rem;
                font-weight: 500;
            };
        
            .ftr-block h4 {
                text-transform: uppercase;
                font-weight: 900;
                margin-bottom: 1.5rem;
            }
        }
    }
    section#copyright {
        color: white;
        padding: 1.8rem;
        * {
            text-align: center;
        };
        p {
            margin-bottom: 1.6rem;
            font-size: .6rem;
        };
        div#brands-symbols > * {
            margin-right: 1rem;
            font-size: .9rem;
        }
    }
}
    
</style>