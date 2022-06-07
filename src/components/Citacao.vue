<template>
    <div class="citacao">
        <!--{{ texto }} -->
        <!-- A tag slot renderiza elementos html no componente -->
        <slot></slot>
    </div>
</template>

<script>
export default {
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
        text-shadow: 1px 1px 5px white;
    }

    p {
        text-shadow: 1px 1px 5px white;
    }

    h6 {
        text-shadow: 1px 1px 5px white;
    }
</style>
