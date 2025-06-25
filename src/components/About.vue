<template>
    <footer class="about-footer">
        <div class="about-content">
            <div class="text-section">
                <div v-for="(title, index) in titleArray" :key="'title-' + index" class="about-item">
                    <h3 class="title-content">{{ title }}</h3>
                    <p v-for="(name, idx) in namesArray[index]" :key="'name-' + idx" class="name-content">
                        {{ name }}
                    </p>
                </div>
            </div>

            <div class="contact-section">
                <p class="contact-label">ליצירת קשר:</p>
                <a href="mailto:mador.till@gmail.com" class="contact-link">mador.till@gmail.com</a>
                <img src="/src/assets/media/TillLogo.svg" alt="till-logo" class="till-logo" />
            </div>
        </div>
    </footer>
</template>



<script>
export default {
    name: "AboutPage",
    data() {
        return {
            showFooter: false,
            titleArray: ["מפתחת ראשית", "רמ\"ד טי\"ל", "שנת פיתוח"],
            namesArray: [["סמל אדוה אבא"], ["רס\"ם עדן בן חמו"], ["יוני 2025"]],
        };
    },
    mounted() {
        window.addEventListener("scroll", this.checkScroll);
    },
    beforeUnmount() {
        window.removeEventListener("scroll", this.checkScroll);
    },
    methods: {
        // checkScroll() {
        //     const scrollPosition = window.scrollY + window.innerHeight;
        //     const bottom = document.documentElement.offsetHeight;

        //     this.showFooter = scrollPosition >= bottom - 10;
        // },
    },
};
</script>

<style>
.about-footer {
    width: 100%;
    background-color: #ffffff;
    box-shadow: 0 -2px 8px rgba(0, 0, 0, 0.1);
    padding: 1rem 2rem;
    text-align: center;
    height: 20vh;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: auto;
}

.about-content {
    display: flex;
    gap: 2rem;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    width: 100%;
    max-width: 1000px;
}

.about-item {
    text-align: right;
    min-width: 120px;
}

.title-content {
    margin: 0.2rem;
    font-size: 1rem;
    font-weight: bold;
}

.name-content {
    margin: 0;
    font-size: 0.9rem;
}

.till-logo {
    width: 4rem;
    height: auto;
}

.contact-section {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 0.8rem;
}

.contact-label {
    font-weight: bold;
    font-size: 0.95rem;
    margin: 0;
}

.contact-link {
    font-size: 0.9rem;
    color: #003049;
    text-decoration: none;
}

.contact-link:hover {
    text-decoration: underline;
}
</style>
