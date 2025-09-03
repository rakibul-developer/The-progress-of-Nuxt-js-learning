<template>
    <div>
        <header style="background-color: #f1f1ff; width: 100%;">
            <div style="display: flex; flex-direction: column; justify-content: space-between; align-items: center;">
                <h3>Header</h3>
                <ul style="list-style: none; padding: 0; display: flex; gap: 1rem;">
                    <li>
                        <NuxtLink to="/">Home</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/admin">Admin</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/about">About</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/contact">Contact</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/blog">Blog</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/users">Users</NuxtLink>
                    </li>
                </ul>
            </div>
        </header>

        <main style="width: 1200px; margin: 0 auto;">
            <slot />
        </main>

        <footer style="background-color: #f1f1ff; width: 100%; padding: 1rem; text-align: center;">
            <p>Footer Content</p>
        </footer>
    </div>
</template>
