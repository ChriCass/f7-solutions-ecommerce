<script setup>
import { ref } from "vue";
import Dropdown from "@/Components/Dropdown.vue";
import DropdownLink from "@/Components/DropdownLink.vue";
import NavLink from "@/Components/NavLink.vue";
import { onMounted } from "vue";

 
onMounted(() => {
    const showMenu = (toggleId, navId) => {
        const toggle = document.getElementById(toggleId),
            nav = document.getElementById(navId);

        toggle.addEventListener("click", () => {
            nav.classList.toggle("show-menu");
            toggle.classList.toggle("show-icon");
        });
    };

    showMenu("nav-toggle", "nav-menu");

    const dropdownItems = document.querySelectorAll(".dropdown__item");

    dropdownItems.forEach((item) => {
        const dropdownButton = item.querySelector(".dropdown__button");

        dropdownButton.addEventListener("click", () => {
            const showDropdown = document.querySelector(".show-dropdown");

            toggleItem(item);

            if (showDropdown && showDropdown !== item) {
                toggleItem(showDropdown);
            }
        });
    });

    const toggleItem = (item) => {
        const dropdownContainer = item.querySelector(".dropdown__container");

        if (item.classList.contains("show-dropdown")) {
            dropdownContainer.removeAttribute("style");
            item.classList.remove("show-dropdown");
        } else {
            dropdownContainer.style.height =
                dropdownContainer.scrollHeight + "px";
            item.classList.add("show-dropdown");
        }
    };

    const mediaQuery = window.matchMedia("(min-width: 1118px)"),
        dropdownContainer = document.querySelectorAll(".dropdown__container");

    const removeStyle = () => {
        if (mediaQuery.matches) {
            dropdownContainer.forEach((e) => {
                e.removeAttribute("style");
            });

            dropdownItems.forEach((e) => {
                e.classList.remove("show-dropdown");
            });
        }
    };

    window.addEventListener("resize", removeStyle);

    function scrollHeader() {
        const nav = document.getElementById("header");

        if (window.scrollY >= 80) {
            nav.classList.add("scroll-header");
        } else {
            nav.classList.remove("scroll-header");
        }
    }

    window.addEventListener("scroll", scrollHeader);
});
</script>

<template>
    <div>
        <div class="h-100 text-dark">
            <!--=============== HEADER ===============-->
            <header class="header" id="header">
                <nav class="nav pading">
                    <div class="nav__data">
                        <a href="#" class="nav__logo"> Logo </a>
                    </div>

                    <!--=============== NAV MENU ===============-->
                    <div class="nav__menu" id="nav-menu">
                        <ul class="nav__list">
                            <!--=============== DROPDOWN 1 ===============-->
                            <li class="dropdown__item">
                                <div class="nav__link dropdown__button">
                                    Contenidos
                                    <i
                                        class="ri-arrow-down-s-line dropdown__arrow"
                                    ></i>
                                </div>

                                <div class="dropdown__container">
                                    <div class="dropdown__content">
                                        <div class="dropdown__group">
                                            <span class="dropdown__title"
                                                >Cursos introductorios</span
                                            >

                                            <ul class="dropdown__list">
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Bootcamp FullStack</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Introducción a CSS</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Introducción a
                                                        Javascript</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Introducción a Git</a
                                                    >
                                                </li>
                                            </ul>
                                        </div>

                                        <div class="dropdown__group">
                                            <span class="dropdown__title"
                                                >Cursos bootcampes</span
                                            >

                                            <ul class="dropdown__list">
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Desarrollador
                                                        Flutter</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Desarrollador Java</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Desarrollador Web con
                                                        React</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Desarrollador Django</a
                                                    >
                                                </li>
                                            </ul>
                                        </div>

                                        <div class="dropdown__group">
                                            <span class="dropdown__title"
                                                >Bootcamps</span
                                            >

                                            <ul class="dropdown__list">
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Desarrollador
                                                        FullStack</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Desarrollador de
                                                        APPS</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Diseñador UI/UX</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Hacking Ético</a
                                                    >
                                                </li>
                                            </ul>
                                        </div>

                                        <div class="dropdown__group">
                                            <span class="dropdown__title"
                                                >Certificaciones</span
                                            >

                                            <ul class="dropdown__list">
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Certificaciones de
                                                        cursos</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Certifiacaiones de
                                                        bootcamp</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Certificaciones
                                                        gratuitas</a
                                                    >
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </div>
                            </li>

                            <!--=============== DROPDOWN 2 ===============-->
                            <li class="dropdown__item">
                                <div class="nav__link dropdown__button">
                                    Recursos
                                    <i
                                        class="ri-arrow-down-s-line dropdown__arrow"
                                    ></i>
                                </div>

                                <div class="dropdown__container">
                                    <div class="dropdown__content">
                                        <div class="dropdown__group">
                                            <span class="dropdown__title"
                                                >Plantillas Web</span
                                            >

                                            <ul class="dropdown__list">
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Plantillas gratis</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Plantillas premium</a
                                                    >
                                                </li>
                                            </ul>
                                        </div>

                                        <div class="dropdown__group">
                                            <span class="dropdown__title"
                                                >Diseños</span
                                            >

                                            <ul class="dropdown__list">
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Diseños webs</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Diseños de apps</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Diseños de
                                                        componentes</a
                                                    >
                                                </li>
                                            </ul>
                                        </div>

                                        <div class="dropdown__group">
                                            <span class="dropdown__title"
                                                >Otros</span
                                            >

                                            <ul class="dropdown__list">
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Recent blogs</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Video tutoriales</a
                                                    >
                                                </li>
                                                <li>
                                                    <a
                                                        href="#"
                                                        class="dropdown__link"
                                                        >Webinar</a
                                                    >
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </div>
                            </li>

                            <li>
                                <a href="#" class="nav__link">Precios</a>
                            </li>
                            <li class="nav__link">
                                <form action="" class="search">
                                    <input
                                        type="search"
                                        placeholder="Buscar curso"
                                        class="search_input"
                                    />
                                    <div class="search_boton">
                                        <i
                                            class="ri-search-2-line search_icon"
                                        ></i>
                                    </div>
                                </form>
                            </li>
                        </ul>
                    </div>

                    <div class="nav__btns">
                

                        <Dropdown :align="end" width="48">
                            <template #trigger>
                                <button
                                    type="button"
                                    class="dropbtn"
                                    data-bs-toggle="dropdown"
                                    aria-expanded="false"
                                >
                                    {{ $page.props.auth.user.first_name }}
                                </button>
                            </template>

                            <template #content>
                                <DropdownLink
                                    :href="route('profile.edit')"
                                    class="dropdown-item"
                                    >Profile</DropdownLink
                                >
                                <DropdownLink
                                    :href="route('logout')"
                                    method="post"
                                    as="button"
                                    class="dropdown-item"
                                >
                                    Log Out
                                </DropdownLink>
                            </template>
                        </Dropdown>
                    </div>

                    <div class="nav__toggle" id="nav-toggle">
                        <i class="ri-menu-line nav__toggle-menu"></i>
                        <i class="ri-close-line nav__toggle-close"></i>
                    </div>
                </nav>
            </header>

            <!-- Page Heading -->
            <header v-if="$slots.header">
                <div class="container mt-10 mb-5">
                    <slot name="header"></slot>
                </div>
            </header>

            <!-- Page Content -->
            <main>
                <slot></slot>
            </main>
        </div>
    </div>
</template>
