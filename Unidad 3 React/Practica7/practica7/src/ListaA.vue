<script>
export default {
    data() {
        return {
            // Alumnos
            alumnos: [
                { nc: 22620001, nombre: 'Arcangel Gonzalez Cruz', carrera: 'Sistemas', gusto: 'Locución y radio' },
                { nc: 22620002, nombre: 'Sofía Martínez Ramírez', carrera: 'Sistemas', gusto: 'Leer novelas' },
                { nc: 22620003, nombre: 'Carlos Eduardo Torres', carrera: 'Sistemas', gusto: 'Programar en Python' },
                { nc: 22620004, nombre: 'Maria Fernández López', carrera: 'Sistemas', gusto: 'Escuchar música' },
                { nc: 22620005, nombre: 'Ricardo Gómez Pérez', carrera: 'Sistemas', gusto: 'Jugar videojuegos' },
                { nc: 22620006, nombre: 'Valeria Sánchez Torres', carrera: 'Sistemas', gusto: 'Hacer ejercicio' }
            ],
            searchQuery: ''
        };
    },
    computed: {
        filteredAlumnos() {
            const query = this.searchQuery.toLowerCase();
            return this.alumnos.filter(alumno =>
                alumno.nombre.toLowerCase().includes(query) ||
                alumno.nc.toString().includes(query) ||
                alumno.carrera.toLowerCase().includes(query) ||
                alumno.gusto.toLowerCase().includes(query)
            );
        }
    }
};
</script>

<template>
    <div class="container">
        <h1 class="titulo">Lista de Alumnos</h1>

        <div class="search-container">
            <input v-model="searchQuery" type="text" placeholder="Buscar alumnos..." class="search-input">
        </div>

        <div class="table-responsive">
            <table class="tabla">
                <thead>
                    <tr>
                        <th @click="sortBy('nc')">No. Control</th>
                        <th @click="sortBy('nombre')">Nombre</th>
                        <th @click="sortBy('carrera')">Carrera</th>
                        <th @click="sortBy('gusto')">Gusto</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="alumno in filteredAlumnos" :key="alumno.nc">
                        <td>{{ alumno.nc }}</td>
                        <td>{{ alumno.nombre }}</td>
                        <td>{{ alumno.carrera }}</td>
                        <td>{{ alumno.gusto }}</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>

<style scoped>
/* Estilos generales */
body {
    background-image: url('file:///C:/Users/arcax/OneDrive/Im%C3%A1genes/fondo.jpg'); /* Cambia por tu ruta */
    background-size: cover; /* Cubre todo el fondo */
    background-position: center; /* Centra la imagen */
    background-attachment: fixed; /* Fija la imagen al desplazarse */
    background-repeat: no-repeat; /* Evita repetición */
    margin: 0;
    padding: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    min-height: 100vh;
}
.container {
    max-width: 1000px;
    margin: 2rem auto;
    padding: 2rem;
    background: rgba(255, 255, 255, 0.9);
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.titulo {
    color: #fff;
    background-color: #0066cc;
    border-radius: 10px;
    padding: 1rem;
    margin-bottom: 1.5rem;
    font-size: 1.8rem;
    text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
}

.search-container {
    margin-bottom: 1.5rem;
}

.search-input {
    width: 100%;
    padding: 0.8rem 1rem;
    border: 2px solid #ddd;
    border-radius: 25px;
    font-size: 1rem;
    transition: all 0.3s ease;
}

.search-input:focus {
    outline: none;
    border-color: #0066cc;
    box-shadow: 0 0 0 3px rgba(0, 123, 255, 0.25);
}

.table-responsive {
    overflow-x: auto;
}

.tabla {
    width: 100%;
    border-collapse: separate;
    border-spacing: 0;
    margin-top: 1rem;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    overflow: hidden;
}

.tabla th,
.tabla td {
    padding: 1rem;
    text-align: center;
    border: 1px solid #e0e0e0;
}

.tabla th {
    background-color: #0066cc;
    color: white;
    font-weight: 600;
    cursor: pointer;
    transition: background-color 0.2s;
}

.tabla th:hover {
    background-color: #0052a3;
}

.tabla tr:nth-child(even) {
    background-color: #f8f9fa;
}

.tabla tr:hover {
    background-color: #e9f5ff;
    transition: background-color 0.2s;
}

/* Responsive */
@media (max-width: 768px) {
    .container {
        padding: 1rem;
        margin: 1rem;
    }

    .tabla th,
    .tabla td {
        padding: 0.5rem;
        font-size: 0.9rem;
    }
}
</style>