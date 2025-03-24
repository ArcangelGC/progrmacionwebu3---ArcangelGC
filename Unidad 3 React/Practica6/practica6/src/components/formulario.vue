<template>
    <div class="container mt-5">
        <h2 class="text-center">Formulario de Adopción</h2>
        <p class="text-center">Adopta un gato negro o naranja y dale un hogar lleno de amor 🐱</p>

        <div class="row">
            <div class="col-md-6">
                <div class="card" style="background-color: #1e1e1e; color: white; padding: 20px; border-radius: 10px;">
                    <h4 class="text-center">Adoptar un Gato Negro</h4>
                    <form>
                        <div class="mb-3">
                            <label class="form-label">Nombre</label>
                            <input type="text" class="form-control" placeholder="Tu nombre">
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Correo Electrónico</label>
                            <input type="email" class="form-control" placeholder="correo@ejemplo.com">
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Ciudad</label>
                            <input type="text" class="form-control" placeholder="Tu ciudad">
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Celular</label>
                            <input type="tel" class="form-control" placeholder="Tu número">
                        </div>
                        <button type="submit" class="btn btn-warning w-100">Adoptar 🖤</button>
                    </form>
                </div>
            </div>

            <div class="col-md-6">
                <div class="card" style="background-color: #FFA500; color: white; padding: 20px; border-radius: 10px;">
                    <h4 class="text-center">Adoptar un Gato Naranja</h4>
                    <form>
                        <div class="mb-3">
                            <label class="form-label">Nombre</label>
                            <input type="text" class="form-control" placeholder="Tu nombre">
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Correo Electrónico</label>
                            <input type="email" class="form-control" placeholder="correo@ejemplo.com">
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Ciudad</label>
                            <input type="text" class="form-control" placeholder="Tu ciudad">
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Celular</label>
                            <input type="tel" class="form-control" placeholder="Tu número">
                        </div>
                        <button type="submit" class="btn btn-dark w-100">Adoptar 🧡</button>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>

<style>
.container h2 {
    color: #333;
    font-weight: bold;
}
</style>
