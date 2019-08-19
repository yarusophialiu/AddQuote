<template>
    <div id="col-sm-6">
        <div id="panel panel-default">
             <div class="panel-body quote ">
                 <slot></slot>
            </div>
        </div>
    </div>
    
</template>

<script>
    export default {
        props: ['quotes']
    }
</script>

<style>
    .panel-body {
        font-family: 'Arizonia', cursive;
        font-size: 24px;
        color: #6e6e6e;
    }

    .quote {
        cursor: pointer;
    }

    .quote:hover {
        background-color: #ffe2e2
    }
</style>