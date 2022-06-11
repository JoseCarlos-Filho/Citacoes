<template>
    <div class="citacao">
        <!--{{ texto }} -->
        <!-- A tag slot renderiza elementos html no componente -->
        <!-- utilizando slots nomeados -->
        <slot name="fonte"></slot>
        <slot name="texto"></slot>
        <slot name="autor"></slot>
    </div>
</template>

<script>
export default {
    // created() {
    //     // eslint-disable-next-line no-console
    //     console.log("Created");
    // },
    // destoryed() {
    //     // eslint-disable-next-line no-console
    //     console.log("Destoryed");
    // },
    // activated() {
    //     // eslint-disable-next-line no-console
    //     console.log("Activated");
    // },
    // deactivated() {
    //     // eslint-disable-next-line no-console
    //     console.log("Deactivated");
    // }

    // props: ['texto']
}
</script>

<style scoped>
    .citacao {
        border: 1px solid #DDD;
        background-color: rgba(0, 0, 0, .1);
        padding: 25px;
        max-width: 450px;
        border-radius: 30px;
        box-shadow: 1px 1px 20px black;
    }

    h1 {
        text-shadow: 1px 1px 3px white;
    }

    p {
        text-shadow: 1px 1px 3px white;
    }

    h6 {
        text-shadow: 1px 1px 3px white;
    }
</style>
