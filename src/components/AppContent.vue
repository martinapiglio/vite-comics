<script>
</script>

<template>
    <section>
        <div class="container">
            <h1>
                -- Content goes here --
            </h1>
        </div>
    </section>
</template>

<style scoped lang="scss">

    @use 'style/_variables.scss' as *;
    @use 'style/_mixins.scss' as *;

section {
    
    height: 6.5rem;
    color: white;
    background-color: $dark-grey;
        .container {
        @include centerMaxWidth();
        @include centerFlex();

        height:100%;

        }
    }

</style>