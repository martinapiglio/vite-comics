<script>
</script>

<template>
    <main>
        <div class="container">
            <h1>
                -- Content goes here --
            </h1>
        </div>
    </main>
</template>

<style scoped lang="scss">

    @use 'style/_variables.scss' as *;
    @use 'style/_mixins.scss' as *;

    main {
    
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