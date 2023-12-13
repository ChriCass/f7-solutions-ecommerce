       <nav
                class="navbar py-4 navbar-light bg-white navbar-expand-md border-bottom"
            >
                <!-- Primary Navigation Menu -->
                <div class="container-fluid">
                    <div class="d-flex justify-content-between">
                        <div class="d-flex">
                            <!-- Navigation Links -->
                            <div class="navbar-nav d-md-flex">
                                <NavLink
                                    :href="route('dashboard')"
                                    :active="route().current('dashboard')"
                                    class="nav-item nav-link"
                                >
                                    Dashboard
                                </NavLink>
                            </div>
                        </div>
                    </div>

                    <!-- Logo en el centro siempre visible -->
                    <div class="d-none d-lg-flex align-items-center">
                        <ul class="navbar-nav">
                            <li class="nav-item dropdown mx-3">
                                <a
                                    class="nav-link dropdown-toggle"
                                    href="#"
                                    role="button"
                                    data-bs-toggle="dropdown"
                                    aria-expanded="false"
                                >
                                    Dropdown
                                </a>
                                <ul class="dropdown-menu">
                                    <li>
                                        <a class="dropdown-item" href="#"
                                            >Action</a
                                        >
                                    </li>
                                    <li>
                                        <a class="dropdown-item" href="#"
                                            >Another action</a
                                        >
                                    </li>
                                    <li><hr class="dropdown-divider" /></li>
                                    <li>
                                        <a class="dropdown-item" href="#"
                                            >Something else here</a
                                        >
                                    </li>
                                </ul>
                            </li>
                            <li class="nav-item dropdown mx-3">
                                <a
                                    class="nav-link dropdown-toggle"
                                    href="#"
                                    role="button"
                                    data-bs-toggle="dropdown"
                                    aria-expanded="false"
                                >
                                    Dropdown
                                </a>
                                <ul class="dropdown-menu">
                                    <li>
                                        <a class="dropdown-item" href="#"
                                            >Action</a
                                        >
                                    </li>
                                    <li>
                                        <a class="dropdown-item" href="#"
                                            >Another action</a
                                        >
                                    </li>
                                    <li><hr class="dropdown-divider" /></li>
                                    <li>
                                        <a class="dropdown-item" href="#"
                                            >Something else here</a
                                        >
                                    </li>
                                </ul>
                            </li>
                            <li class="d-flex align-items-center">
                                <a class="dropdown-item" href="#"
                                    >Another action</a
                                >
                            </li>
                            <li class="mx-3">
                                <input
                                    type="email"
                                    class="form-control px-5"
                                    id="exampleFormControlInput1"
                                    placeholder="name@example.com"
                                />
                            </li>
                        </ul>
                    </div>

                    <div class="d-none d-md-flex align-items-end">
                        <!-- Settings Dropdown -->
                        <div class="ms-3 position-relative">
                            <Dropdown :align="end" width="48">
                                <template #trigger>
                                    <button
                                        type="button"
                                        class="btn btn-secondary dropdown-toggle"
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
                    </div>

                    <!-- Botón para menú desplegable solo en móviles y tabletas -->
                    <button
                        class="navbar-toggler no-border d-lg-none"
                        type="button"
                        data-bs-toggle="offcanvas"
                        data-bs-target="#offcanvasRight"
                        aria-controls="offcanvasRight"
                    >
                        <span class="navbar-toggler-icon"></span>
                    </button>

                    <!-- Offcanvas solo para móviles y tabletas -->
                    <div
                        class="offcanvas text-white offcanvas-end d-md-none d-lg-none"
                        tabindex="-1"
                        id="offcanvasRight"
                        aria-labelledby="offcanvasRightLabel"
                    >
                        <div class="offcanvas-header">
                            <button
                                type="button"
                                class="btn-close text-white text-reset"
                                data-bs-dismiss="offcanvas"
                                aria-label="Close"
                            ></button>
                        </div>
                        <div class="offcanvas-body">
                            <ul class="navbar-nav">
                                <div class="d-flex d-md-none align-items-end">
                                    <!-- Settings Dropdown -->
                                    <div class="ms-3 position-relative">
                                        <Dropdown :align="end" width="48">
                                            <template #trigger>
                                                <button
                                                    type="button"
                                                    class="btn btn-secondary dropdown-toggle"
                                                    data-bs-toggle="dropdown"
                                                    aria-expanded="false"
                                                >
                                                    {{
                                                        $page.props.auth.user
                                                            .first_name
                                                    }}
                                                </button>
                                            </template>

                                            <template #content>
                                                <DropdownLink
                                                    :href="
                                                        route('profile.edit')
                                                    "
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
                                </div>
                            </ul>
                        </div>
                    </div>
                </div>
            </nav>