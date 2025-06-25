<template>
    <div id="home-page">
        <div class="content-wrapper">
            <h1 class="title">משחוק בלמידה</h1>
            <p class="paragraph">
                בעידן של שינוי מתמיד וטכנולוגיה מתקדמת, מערכות החינוך וההכשרה מתמודדות עם אתגרים רבים ובראשם השאלה:
                כיצד להבטיח מעורבות, עניין ומוטיבציה מתמשכת בקרב הלומדים?
            </p>
            <p class="paragraph">
                <span class="highlight">משחוק בלמידה</span> - מכיל את שילוב העקרונות, מנגנונים וחוויות מעולם המשחקים
                בסביבות לימודיות.
                המשחוק, מבוסס על ההבנה כי לאלמנטים כמו: ניקוד, דרגות, תגמולים, תחרויות ואתגרים,
                יש פוטנציאל להגביר את המחויבות וההנעה הפנימית של הלומדת תוך יצירת חוויות חינוכיות ואינטראקטיביות,
                מהנות ובלתי נשכחות.
            </p>

        </div>
    </div>
</template>

<script>
export default {
    name: "home-page",
};
</script>

<style>
@font-face {
  font-family: "dana";
  src: url("@/assets/fonts/DanaYadAlefAlefAlef-Normal.woff");
}

@font-face {
  font-family: "yehuda";
  src: url("@/assets/fonts/yehudaclm-light-webfont.woff");
}

@font-face {
  font-family: "yehuda-bold";
  src: url("@/assets/fonts/yehudaclm-bold-webfont.woff");
}
#home-page {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 3rem 1rem;
    background-color: #f1f9fc;
    min-height: 60vh;
}

.content-wrapper {
    max-width: 800px;
    text-align: right;
}

.title {
    font-size: 5rem;
    color: #003049;
    margin-bottom: 1.5rem;
    text-align: center;
    font-family: "dana";
}

.paragraph {
    font-size: 1.6rem;
    line-height: 1.8;
    margin-bottom: 1rem;
    color: #222;
}

.highlight {
  font-weight: bold;
  font-size: 2rem;
  color: #005377;
}

</style>
