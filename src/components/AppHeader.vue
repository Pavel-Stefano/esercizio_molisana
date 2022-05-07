<template>
   <header>
        <a href="/" class="brand">
            <img src="../assets/images/logo.png" alt="La Molisana" />
        </a>

        <nav>
            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <a :class="{ active: link.active }" :href="link.url">
                        {{ link.text }}
                    </a>
                </li>
            </ul>
        </nav>
     </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data(){
    return {
        links: [
                {
                    text: "Home",
                    url: "#",
                    active: false,
                },
                {
                    text: "Prodotti",
                    url: "#",
                    active: false,
                },
                {
                    text: "Chi Siamo",
                    url: "#",
                    active: false,
                },
                {
                    text: "Contatti",
                    url: "#",
                    active: false,
                },
            ],
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/vars";
@import "../style/mixins";

header {
    text-align: center;

    ul {
        list-style: none;
        margin: 2.5rem 1rem 4rem;
        @include center();

        li a {
            display: inline-block;
            padding: 1rem;
            text-decoration: none;
            font-weight: 600;
            transition: background 0.3s;

            &.active,
            &:hover {
                background: lighten($primary, 70%);
            }
        }
    }
}
</style>
