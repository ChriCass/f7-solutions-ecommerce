<script setup>
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import "../../css/grid.min.css";
import { Head } from "@inertiajs/vue3";
</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <template #header>
            <div>
                <h2>
                    Bienvenido de nuevo,
                    {{ $page.props.auth.user.first_name }} !:)
                </h2>
            </div>
        </template>
        <div class="container">
            <!-- Aquí comienza la sección de la plantilla Vue -->
            <nav class="navbar navbar-expand-lg bg-white">
                <div class="container">
                    <div class="collapse navbar-collapse" id="navbarNav">
                        <ul class="navbar-nav">
                            <li class="nav-item">
                                <a
                                    class="nav-link mx-3 active"
                                    aria-current="page"
                                    href="#"
                                    >Mis cursos</a
                                >
                            </li>
                            <li class="nav-item">
                                <a class="nav-link mx-3" href="#"
                                    >Mis favoritos</a
                                >
                            </li>
                            <li class="nav-item">
                                <a class="nav-link mx-3" href="#"
                                    >Proximos eventos</a
                                >
                            </li>
                        </ul>
                    </div>
                </div>
            </nav>
            <section class="row">
                <div class="col d-flex justify-content-center mt-5">
                    <div class="card">
                        <img
                            class="card-img-top"
                            src="img/1.jpg"
                            alt="Card image"
                        />
                        <div class="card-body">
                            <div class="card-title-container">
                                <h5 class="card-title">Título de la Tarjeta</h5>
                            </div>
                            <div class="cardparagraph-container">
                                <p class="card-text">
                                    Este es un ejemplo de texto de la tarjeta.
                                    Puede contener una pequeña descripción.
                                </p>
                            </div>
                           
                        </div>
                        <div>
                            <button class="card-button">Botón</button>
                        </div>
                       
                    </div>
                </div>
                <div class="col d-flex justify-content-center mt-5">
                    <div class="card">
                        <img
                            class="card-img-top"
                            src="img/1.jpg"
                            alt="Card image"
                        />
                        <div class="card-body">
                            <div class="card-title-container">
                                <h5 class="card-title">Título de la Tarjeta</h5>
                            </div>
                            <div class="cardparagraph-container">
                                <p class="card-text">
                                    Este es un ejemplo de texto de la tarjeta.
                                    Puede contener una pequeña descripción.
                                </p>
                            </div>
                            <a href="#" class="card-link">Enlace</a>
                        </div>
                        <button class="card-button">Botón</button>
                    </div>
                </div>
                <div class="col d-flex justify-content-center mt-5">
                    <div class="card">
                        <img
                            class="card-img-top"
                            src="img/1.jpg"
                            alt="Card image"
                        />
                        <div class="card-body">
                            <div class="card-title-container">
                                <h5 class="card-title">Título de la Tarjeta</h5>
                            </div>
                            <div class="cardparagraph-container">
                                <p class="card-text">
                                    Este es un ejemplo de texto de la tarjeta.
                                    Puede contener una pequeña descripción.
                                </p>
                            </div>
                            <a href="#" class="card-link">Enlace</a>
                        </div>
                        <button class="card-button">Botón</button>
                    </div>
                </div>
                <div class="col d-flex justify-content-center mt-5">
                    <div class="card">
                        <img
                            class="card-img-top"
                            src="img/1.jpg"
                            alt="Card image"
                        />
                        <div class="card-body">
                            <div class="card-title-container">
                                <h5 class="card-title">Título de la Tarjeta</h5>
                            </div>
                            <div class="cardparagraph-container">
                                <p class="card-text">
                                    Este es un ejemplo de texto de la tarjeta.
                                    Puede contener una pequeña descripción.
                                </p>
                            </div>
                            <a href="#" class="card-link">Enlace</a>
                        </div>
                        <button class="card-button">Botón</button>
                    </div>
                </div>
                <div class="col d-flex justify-content-center mt-5">
                    <div class="card">
                        <img
                            class="card-img-top"
                            src="img/1.jpg"
                            alt="Card image"
                        />
                        <div class="card-body">
                            <div class="card-title-container">
                                <h5 class="card-title">Título de la Tarjeta</h5>
                            </div>
                            <div class="cardparagraph-container">
                                <p class="card-text">
                                    Este es un ejemplo de texto de la tarjeta.
                                    Puede contener una pequeña descripción.
                                </p>
                            </div>
                            <a href="#" class="card-link">Enlace</a>
                        </div>
                        <button class="card-button">Botón</button>
                    </div>
                </div>
            </section>

            <section class="bg-dark p-5 mt-5">
                <div class="container">
                    <div class="row justify-content-center text-center">
                        <div class="col-12 m-5">
                            <h5 class="fs-1 fw-bold mb-3">
                                Algun tipo de promocion aqui
                            </h5>
                            <p class="fs-4">
                                Cuanto tiempo falta o que se io
                                <span>24/7 </span>Support.
                            </p>
                            <a
                                name=""
                                id=""
                                class="btn btn-primary"
                                href="#"
                                role="button"
                                >ir a esa promo</a
                            >
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </AuthenticatedLayout>
    <footer class="footer section mt-5">
        <div class="footer__container container grid">
            <div class="footer__content">
                <a href="#" class="footer__logo">LOGO</a>
                <p class="footer__description">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Omnis, nesciunt!
                </p>
            </div>

            <div class="footer__content">
                <h3 class="footer__title">Planes de servicio</h3>
                <ul class="footer__links">
                    <li>
                        <a href="#" class="footer__link">Desarrollador Web</a>
                    </li>
                    <li>
                        <a href="#" class="footer__link"
                            >Desarrollador Javascript</a
                        >
                    </li>
                    <li>
                        <a href="#" class="footer__link"
                            >Desarrollaoor python</a
                        >
                    </li>
                    <li>
                        <a href="#" class="footer__link"
                            >Desarrollador PYthon</a
                        >
                    </li>
                </ul>
            </div>

            <div class="footer__content">
                <h3 class="footer__title">Lenguajes</h3>
                <ul class="footer__links">
                    <li><a href="#" class="footer__link">Python</a></li>
                    <li><a href="#" class="footer__link">Ruby</a></li>
                    <li><a href="#" class="footer__link">Laravel</a></li>
                    <li><a href="#" class="footer__link">Java</a></li>
                    <li><a href="#" class="footer__link">Javascript</a></li>
                </ul>
            </div>

            <div class="footer__content">
                <h3 class="footer__title">Comunidad</h3>
                <ul class="footer__links">
                    <li><a href="#" class="footer__link">Soporte</a></li>
                    <li><a href="#" class="footer__link">Preguntas</a></li>
                    <li>
                        <a href="#" class="footer__link">Solicitar ayuda</a>
                    </li>
                </ul>
            </div>

            <div class="footer__social">
                <h3 class="footer__title">Redes sociales</h3>
                <ul class="footer__redes">
                    <a href="#" class="footer__social-link"
                        ><i class="ri-facebook-circle-line"></i
                    ></a>
                    <a href="#" class="footer__social-link"
                        ><i class="ri-twitter-line"></i
                    ></a>
                    <a href="#" class="footer__social-link"
                        ><i class="ri-instagram-line"></i
                    ></a>
                </ul>
            </div>
        </div>

        <p class="footer__copy">&#169; F5 SOLUTIONS - 2023</p>
    </footer>
</template>
