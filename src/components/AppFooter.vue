<template>
    <footer>
        <!-- ? Il footer è diviso in due sezioni -->
        <section id="ftr-list" class="container">
            <!-- Qua ci sono 3 colonne, di cui le 2 più a destra sono degli ul 
                 con le voci di menu CHE ARRIVANO DIRETTAMENTE DALL'APP VUE TRAMITE PROPS-->
            <div class="ftr-block">
                <h4>About</h4>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quisquam cum a praesentium quod itaque reiciendis libero accusamus ratione tempore aliquam? Nulla omnis corrupti placeat fugiat distinctio sunt sequi, blanditiis corporis!</p>
                <p>Logo</p>
            </div>
            <div class="ftr-block">
                <ul>
                    <h4 class="ftr-small-title">Avada Movers</h4>
                    <li v-for="singleItem in menuItems">{{ singleItem.label }}</li>
                </ul>
            </div>
            <div class="ftr-block">
                <ul>
                    <h4 class="ftr-small-title">Recent Posts</h4>
                    <li v-for="singleItem in recentPostItems">{{ singleItem.string }}</li>
                </ul>
            </div>
        </section>
        <section class="call-section">
            <!-- Questa è la sezione che è molto simile alla prima dell'header -->
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
    section#ftr-list {
        ul {
            list-style-type: none;
        }
    }
</style>