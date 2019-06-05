<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <li
                class="list-group-item"
                v-for="value in servers" v-bind:key="value.name">
                {{ value.name }} | Status: {{value.status}}
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
                servers: [
                    {
                        name: 'Server #1',
                        status: 'Normal'
                    },
                    {
                        name: 'Server #2',
                        status: 'Critical'
                    },
                    {
                        name: 'Server #3',
                        status: 'Critical'
                    },
                    {
                        name: 'Server #4',
                        status: 'Normal'
                    },
                    {
                        name: 'Server #5',
                        status: 'Normal'
                    }
                ]
            }
        }
    }
</script>


<style scoped>
/* not only one global DOM but many separate DOMs 
we see data-v-1d3b3738 as style property on our page when we click inspect
this is created by vue. All styles are included in the head section of the document
automatically. 
*/
    div{
        border: 1px solid blue;
    }
</style>
