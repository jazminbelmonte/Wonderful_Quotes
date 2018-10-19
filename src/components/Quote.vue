<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div class="panel-body quote">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
</script>

<style>
    .panel {
        color: goldenrod;
        font-family: Helvetica;
        font-size: 16px;
    }
    .quote {
        cursor: pointer;
    }
    .quote:hover {
        background-color: lightgoldenrodyellow;
    }
</style>