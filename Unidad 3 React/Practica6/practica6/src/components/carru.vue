<template>
    <div class="container mt-5">
        <h2 class="text-center mb-4">Nuestros Gatos</h2>

        <div id="gatoCarousel" class="carousel slide" data-bs-ride="carousel">
            <div class="carousel-inner text-center">
                <!-- Card 1 - Gato Negro -->
                <div class="carousel-item active">
                    <div class="d-flex justify-content-center">
                        <div class="card" style="width: 18rem; background-color: #1e1e1e; color: white;">
                            <img src="https://placekitten.com/300/200" class="card-img-top" alt="Gato Negro">
                            <div class="card-body text-center">
                                <h5 class="card-title">Gato Negro</h5>
                                <p class="card-text">Los gatos negros son misteriosos y cariñosos. ¡Adóptalo!</p>
                                <button class="btn btn-warning">Adoptar</button>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Card 2 - Gato Naranja -->
                <div class="carousel-item">
                    <div class="d-flex justify-content-center">
                        <div class="card" style="width: 18rem; background-color: #FFA500; color: white;">
                            <img src="https://placekitten.com/301/200" class="card-img-top" alt="Gato Naranja">
                            <div class="card-body text-center">
                                <h5 class="card-title">Gato Naranja</h5>
                                <p class="card-text">Juguetón y sociable, este gato naranja busca un hogar.</p>
                                <button class="btn btn-dark">Adoptar</button>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Card 3 - Gato Blanco -->
                <div class="carousel-item">
                    <div class="d-flex justify-content-center">
                        <div class="card" style="width: 18rem; background-color: #f8f9fa; color: black;">
                            <img src="https://placekitten.com/302/200" class="card-img-top" alt="Gato Blanco">
                            <div class="card-body text-center">
                                <h5 class="card-title">Gato Blanco</h5>
                                <p class="card-text">Tranquilo y elegante, el gato blanco es un compañero ideal.</p>
                                <button class="btn btn-primary">Adoptar</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Controles del carrusel -->
            <button class="carousel-control-prev" type="button" data-bs-target="#gatoCarousel" data-bs-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#gatoCarousel" data-bs-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
            </button>
        </div>
    </div>
</template>

<style>
.carousel-inner {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 350px;
}

.carousel-control-prev-icon,
.carousel-control-next-icon {
    background-color: black;
    border-radius: 50%;
}
</style>
