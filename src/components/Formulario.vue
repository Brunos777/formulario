<script>
    export default {
        data: () => ({
            proyecto: "",
            tipo: "",
            urgente: false,
            proyectos: [],
        }),
        methods: {
            registrarProyecto() {
                const proyecto = {
                    proyecto: this.proyecto,
                    tipo: this.tipo,
                    urgente: this.urgente,
                };
                this.proyectos.push(proyecto)

                this.proyecto = "";
                this.tipo = "";
                this.urgente = false;
            },
        },
    };
</script>

<template>
    <form @submit.prevent="registrarProyecto">
        <div class="mb-3">
            <label class="form-label">Proyecto</label>
            <input v-model.trim="proyecto" type="text" class="form-control" required/>
        </div>

        <div class="mb-3">
            <label class="forms-label">Actividad</label>
            <select v-model="tipo" class="form-select" required>
                <option disable selected value="">Selecciona un tipo de actividad></option>
                <option>Aplicaciones web con Vue.js</option>
                <option>Backend Service con Node.js</option>
                <option>App móvil con React Native</option>
            </select>        
        </div>

        <div class="mb-3">
            <label for="exampleInputPassword1" class="form-check-label">Urgente</label>
            <input v-model.trim" type="checkbox" class="form-check-control" />
        </div>
        
        <button type="submmit" class="btn btn-primary">Guardar</button>
    </form>
    <hr>
    
    <div class="table-responsive">
        <table class="table table-dark">
            <thead>
                <tr>
                    <th>#</th>
                    <th>Proyecto</th>
                    <th>Tipo</th>
                    <th>Urgente</th>
                </tr>
            </thead>

            <tbody>
                <tr>
                    <td>1</td>
                    <td>Laravel app</td>
                    <td>Larabel</td>
                    <td class="bg-success">Si / No</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>