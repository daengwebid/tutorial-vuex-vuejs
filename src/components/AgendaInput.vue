<template>
    <div class="col-md-6">
        <div class="card">
            <div class="card-header">
                <h3 class="card-title">List Agenda</h3>
            </div>
            <div class="card-body">
                <ul>
                    <li v-for="row in listAgenda" :key="row"><strong>{{ row.hari }}</strong>: {{ row.kegiatan }}</li>
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        name: 'AgendaInput',
        computed: {
            listAgenda() {
                return this.$store.state.listAgenda
            }
        }
    }
</script>