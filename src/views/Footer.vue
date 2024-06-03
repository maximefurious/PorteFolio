<script setup>
  const year = new Date().getFullYear()
</script>

<template>
    <footer class="footer">
        <div class="footer__content">
            <p>&copy; {{ year }} - Tous droits réservés</p>
            <p>Créé par <a href="mailto:maxime.boujeant@gmail.com">Maxime Boujeant</a></p>
        </div>
    </footer>
</template>

<style scoped>
.footer {
    width: 100%;
    background-color: var(--secondary);
    color: var(--text);
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
}

.footer__content {
    width: 80%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.footer__content a {
    color: var(--primary);
}

.footer__content a:hover {
    color: var(--primary);
    text-decoration: underline;
}

</style>