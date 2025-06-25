<template>
    <div id="buttons">
        <div class="intro">
            <p>
                לפניכם שמונה כלים דיגיטליים אשר יסייעו לכם בתכנון והעברת הדרכות או הכשרות.
            </p>
            <p>
                כל כלי מלווה בהסבר קצר, קישור לשימוש ישיר, והצעות לשילובו בתהליך הלמידה ודוגמאות.
            </p>
        </div>

        <div class="button-grid">
            <button v-for="(pdf, index) in pdfs" :key="index" @click="openPdf(pdf.link)" class="pdf-button">
                {{ pdf.name }}
            </button>
        </div>
    </div>
</template>

<script>
export default {
    name: "buttons",
    data() {
        return {
            pdfs: [
                { name: "מחולל פעילויות", link: "/pdfs/מחולל פעילויות אינטראקטיביות.pdf" },
                { name: "ניהול כיתה", link: "/pdfs/ניהול כיתה באופן משחוקי.pdf" },
                { name: "חשיפת תמונה", link: "/pdfs/כלי לפעילויות אינטראקטיביות עם חשיפה הדרגתית של תמונה - Vimboar.pdf" },
                { name: "פריצת מנעולים", link: "/pdfs/משחק פריצת מנעולים.pdf" },
                { name: "כתב סתרים", link: "/pdfs/מחולל כתב סתרים.pdf" },
                { name: "לוח ניקוד", link: "/pdfs/לוח ניקוד.pdf" },
                { name: "גלגל הגרלה", link: "/pdfs/גלגל הגרלה.pdf" },
                { name: "באזר מקוון", link: "/pdfs/באזר מקוון.pdf" },
            ]
        };
    },
    methods: {
        openPdf(link) {
            window.open(link, "_blank");
        },
    },
};
</script>

<style>
#buttons {
    padding: 3rem 1.5rem;
    background-color: #f4fbff;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.intro {
    max-width: 800px;
    text-align: center;
    margin-bottom: 2rem;
}

.section-title {
    font-size: 2rem;
    color: #003049;
    margin-bottom: 1rem;
}

.intro p {
  font-size: 1.5rem;
    line-height: 1.8;
    margin-bottom: 1rem;
    color: #222;
}

.button-grid {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  width: 100%;
  max-width: 600px;
}

.pdf-button {
    background-color: #003049;
    color: white;
    border: none;
    border-radius: 12px;
    padding: 1rem 1.8rem;
    font-size: 2rem;
    cursor: pointer;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    transition: background-color 0.3s ease, transform 0.2s;
}

.pdf-button:hover {
    background-color: #005377;
    transform: translateY(-2px);
}

</style>
