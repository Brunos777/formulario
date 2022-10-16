<script>
    export default {
        data:() => ({
            proyecto:"",
            tipo: "",
            urgente:"",
            proyectos:[], 
        }),
        methods: {
            registrarProyecto () {
                const proyecto ={
                    proyecto : this.proyecto,
                    tipo : this.tipo,
                    urgente.urgente= false;
                };
                this.proyectos.push(proyecto);

                console.log(proyecto)
        },
    },
};

</script>







<template>
<form @submit.prevent="registrarProyecto">

<div class="mb-3">
    <label class="form-label"> Proyecto</label>
    <input v-model.trim ="urgente" type="text" class="form-control"/>    //Trim: Limpiar espacios //
</div>
<div class="mb-3">
    <label class="form-label">Actividad</label>
<select class="form select" required>
    <option disabled selected value=""> Seleccione el tipo de actividad ...</option>
    <option value="">  ...</option>
    <option value=""> Backend service con Node.Js...</option>
    <option value=""> App movil con React Native ...</option>

</select>
</div>

<div class="mb-3">
    <label for="exampleInputPassword" class="form-check-label"> Urgente </label>
    <input type="checkbox" class="form-check-input">
</div>

    <button type="submit" class="btn btn-primary"> Guardar</button>

</form>

<hr />
<div class="table.responsive">
    <table class="table">
        <thead>
            <tr>
                <th> # </th>
                <th>Proyecto</th>
                <th>Tipo</th>
                <th>Urgente</th>

            </tr>
        </thead>
                
        <tbody>
            <tr v-for="(proyecto, index) in proyectos" :key="index">
               <td>{{Index + 1}}</td>
               <td>{{proyecto.proyecto}}</td>
               <td>{{proyecto.tipo}}</td>
               <td class="proyecto.urgente ? 'bg-success' : 'bg-danger' ">{{proyecto.urgente ? "Si" : "No" }}</td>

            </tr>
        </tbody>
    </table>
</template>



*//Pintar una variable con corchetes//*
