# fenk.com
"نحو جيل جديد من الويب الذكي
```html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport"
      content="width=device-width,initial-scale=1.0,viewport-fit=cover">

<title>FENK.com — جهاز الويب الذكي</title>

<meta name="description"
      content="FENK.com — نحو جيل جديد من جهاز الويب الذكي. بحث، تصفح، ذكاء اصطناعي، خدمات، سحابة وتواصل.">

<meta name="theme-color" content="#0b0b0b">

<style>
/* =========================================================
   FENK.COM — GLOBAL DESIGN SYSTEM
========================================================= */

:root{
    --black:#090909;
    --black2:#111111;
    --white:#ffffff;
    --silver:#c7c7c7;
    --orange:#ff7a18;
    --orange2:#ffb347;
    --blue:#0a84ff;
    --purple:#8b5cf6;
    --cyan:#22d3ee;
    --glass:rgba(255,255,255,.08);
    --border:rgba(255,255,255,.13);
    --shadow:0 20px 70px rgba(0,0,0,.35);
}

*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:
        "Cairo",
        "Tahoma",
        Arial,
        sans-serif;

    background:
        radial-gradient(circle at 20% 10%,
        rgba(255,122,24,.14),
        transparent 30%),

        radial-gradient(circle at 80% 20%,
        rgba(10,132,255,.16),
        transparent 30%),

        linear-gradient(180deg,
        #070707,
        #0d0d0f 55%,
        #070707);

    color:var(--white);
    min-height:100vh;
    overflow-x:hidden;
}

/* =========================================================
   BACKGROUND
========================================================= */

.aurora{
    position:fixed;
    inset:-30%;
    pointer-events:none;
    z-index:-2;

    background:
        radial-gradient(circle,
        rgba(255,122,24,.10),
        transparent 28%),

        radial-gradient(circle at 70% 30%,
        rgba(139,92,246,.09),
        transparent 28%),

        radial-gradient(circle at 40% 80%,
        rgba(34,211,238,.07),
        transparent 25%);

    filter:blur(80px);
    animation:aurora 14s ease-in-out infinite alternate;
}

@keyframes aurora{
    from{transform:translate(-3%,-2%) scale(1);}
    to{transform:translate(4%,3%) scale(1.08);}
}

/* =========================================================
   HEADER
========================================================= */

header{
    position:sticky;
    top:0;
    z-index:1000;

    height:72px;

    display:flex;
    align-items:center;
    justify-content:space-between;

    padding:0 20px;

    background:rgba(5,5,5,.72);
    backdrop-filter:blur(22px);
    -webkit-backdrop-filter:blur(22px);

    border-bottom:1px solid var(--border);
}

.logo{
    display:flex;
    align-items:center;
    gap:10px;
    cursor:pointer;
}

.logo-icon{
    width:42px;
    height:42px;

    display:grid;
    place-items:center;

    border-radius:14px;

    background:
        linear-gradient(135deg,
        var(--orange),
        #ff4d00);

    box-shadow:
        0 8px 35px rgba(255,122,24,.35);
}

.logo-icon::before{
    content:"🦊";
    font-size:24px;
}

.logo-text{
    font-size:21px;
    font-weight:900;
    letter-spacing:.5px;
}

.logo-text span{
    color:var(--orange);
}

.menu{
    display:flex;
    gap:8px;
}

.menu button{
    border:0;
    background:transparent;
    color:#ddd;

    padding:9px 12px;
    border-radius:12px;

    cursor:pointer;
}

.menu button:hover{
    background:var(--glass);
    color:white;
}

.menu-toggle{
    display:none;
    border:0;
    background:var(--glass);
    color:white;
    border-radius:12px;
    padding:10px;
}

/* =========================================================
   HERO
========================================================= */

.hero{
    min-height:
        calc(100vh - 72px);

    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;

    text-align:center;

    padding:
        70px 20px
        100px;
}

.badge{
    display:inline-flex;
    align-items:center;
    gap:8px;

    padding:8px 14px;

    border:1px solid var(--border);
    border-radius:999px;

    background:rgba(255,255,255,.055);

    color:#ddd;
    font-size:13px;

    box-shadow:var(--shadow);
}

.badge i{
    width:8px;
    height:8px;
    border-radius:50%;
    background:#35e37b;
    box-shadow:0 0 12px #35e37b;
}

.hero h1{
    margin-top:25px;

    font-size:
        clamp(42px,10vw,90px);

    line-height:1;

    font-weight:1000;

    background:
        linear-gradient(
            90deg,
            white,
            #ffcf9b,
            #ff7a18,
            #ffffff
        );

    -webkit-background-clip:text;
    background-clip:text;

    color:transparent;
}

.hero h2{
    margin-top:22px;

    font-size:
        clamp(21px,5vw,38px);

    font-weight:800;
}

.hero p{
    max-width:700px;

    margin:18px auto 0;

    color:#bcbcbc;

    line-height:1.9;

    font-size:16px;
}

/* =========================================================
   SEARCH
========================================================= */

.search-box{
    width:min(760px,100%);

    margin-top:38px;

    padding:7px;

    display:flex;
    align-items:center;
    gap:7px;

    border-radius:24px;

    background:
        linear-gradient(
            135deg,
            rgba(255,255,255,.12),
            rgba(255,255,255,.035)
        );

    border:1px solid var(--border);

    box-shadow:
        0 25px 80px rgba(0,0,0,.45),
        0 0 60px rgba(255,122,24,.06);
}

.search-icon{
    padding:0 10px;
    font-size:22px;
}

#searchInput{
    flex:1;

    min-width:0;

    background:transparent;
    border:0;
    outline:0;

    color:white;

    font-size:16px;

    padding:15px 4px;

    font-family:inherit;
}

#searchInput::placeholder{
    color:#777;
}

.search-button{
    border:0;

    padding:
        13px 21px;

    border-radius:17px;

    color:white;

    background:
        linear-gradient(
            135deg,
            var(--orange),
            #ff4d00
        );

    font-weight:900;

    cursor:pointer;

    box-shadow:
        0 8px 25px
        rgba(255,122,24,.22);
}

.search-button:hover{
    transform:translateY(-1px);
}

/* =========================================================
   QUICK ACTIONS
========================================================= */

.quick{
    display:flex;
    flex-wrap:wrap;
    justify-content:center;

    gap:10px;

    margin-top:20px;
}

.quick button{
    border:1px solid var(--border);

    background:rgba(255,255,255,.045);

    color:#ddd;

    padding:9px 13px;

    border-radius:999px;

    cursor:pointer;
}

.quick button:hover{
    background:rgba(255,122,24,.12);
    border-color:rgba(255,122,24,.4);
}

/* =========================================================
   SERVICES
========================================================= */

.section{
    width:min(1120px,100%);
    margin:auto;

    padding:
        80px 20px;
}

.section-title{
    text-align:center;
    margin-bottom:35px;
}

.section-title h2{
    font-size:
        clamp(28px,6vw,45px);
}

.section-title p{
    color:#999;
    margin-top:8px;
}

.services{
    display:grid;

    grid-template-columns:
        repeat(auto-fit,minmax(180px,1fr));

    gap:15px;
}

.service{
    position:relative;

    padding:22px;

    min-height:155px;

    border:
        1px solid var(--border);

    border-radius:25px;

    background:
        linear-gradient(
            145deg,
            rgba(255,255,255,.075),
            rgba(255,255,255,.025)
        );

    backdrop-filter:blur(15px);

    transition:
        transform .25s,
        border .25s;

    cursor:pointer;
}

.service:hover{
    transform:translateY(-5px);

    border-color:
        rgba(255,122,24,.42);
}

.service-icon{
    font-size:30px;
}

.service h3{
    margin-top:12px;
    font-size:18px;
}

.service p{
    color:#929292;
    margin-top:5px;
    font-size:13px;
    line-height:1.7;
}

/* =========================================================
   DEVICE
========================================================= */

.device-section{
    display:flex;
    justify-content:center;

    padding:
        70px 20px 100px;
}

.device{
    width:min(370px,90vw);

    min-height:650px;

    border:
        8px solid #1b1b1d;

    border-radius:46px;

    background:
        linear-gradient(
            160deg,
            #111,
            #070707
        );

    box-shadow:
        0 40px 100px rgba(0,0,0,.65),
        inset 0 0 0 1px #444;

    padding:20px;

    position:relative;

    overflow:hidden;
}

.device::before{
    content:"";

    position:absolute;

    width:110px;
    height:25px;

    top:8px;
    left:50%;

    transform:translateX(-50%);

    background:#000;

    border-radius:20px;
}

.device-top{
    padding-top:38px;

    text-align:center;
}

.device-top small{
    color:#888;
}

.device-top h3{
    margin-top:5px;
    font-size:26px;
}

.device-search{
    margin-top:22px;

    padding:13px;

    border-radius:18px;

    background:#171717;

    color:#777;
}

.device-grid{
    display:grid;

    grid-template-columns:
        repeat(3,1fr);

    gap:10px;

    margin-top:18px;
}

.app{
    aspect-ratio:1;

    display:flex;
    flex-direction:column;

    align-items:center;
    justify-content:center;

    gap:7px;

    border-radius:18px;

    background:#151515;

    border:1px solid #262626;

    font-size:13px;

    cursor:pointer;
}

.app span{
    font-size:27px;
}

/* =========================================================
   OFFLINE
========================================================= */

.offline-card{
    margin-top:30px;

    padding:20px;

    border-radius:25px;

    border:1px solid rgba(53,227,123,.18);

    background:
        linear-gradient(
            135deg,
            rgba(53,227,123,.07),
            rgba(255,255,255,.025)
        );

    display:flex;
    align-items:center;
    gap:15px;
}

.status{
    width:13px;
    height:13px;

    border-radius:50%;

    background:#35e37b;

    box-shadow:0 0 15px #35e37b;
}

/* =========================================================
   FEATURES
========================================================= */

.feature-list{
    display:grid;

    grid-template-columns:
        repeat(auto-fit,minmax(240px,1fr));

    gap:16px;
}

.feature{
    padding:25px;

    border-radius:25px;

    border:1px solid var(--border);

    background:
        rgba(255,255,255,.04);
}

.feature strong{
    display:block;

    font-size:18px;

    margin-bottom:8px;
}

.feature p{
    color:#999;
    line-height:1.8;
}

/* =========================================================
   FOOTER
========================================================= */

footer{
    border-top:1px solid var(--border);

    padding:35px 20px;

    text-align:center;

    color:#777;
}

footer strong{
    color:white;
}

.footer-links{
    display:flex;
    justify-content:center;
    flex-wrap:wrap;

    gap:18px;

    margin-top:15px;
}

.footer-links a{
    color:#888;
    text-decoration:none;
}

.footer-links a:hover{
    color:var(--orange);
}

/* =========================================================
   TOAST
========================================================= */

.toast{
    position:fixed;

    bottom:25px;
    left:50%;

    transform:
        translate(-50%,120px);

    opacity:0;

    padding:13px 20px;

    border-radius:15px;

    background:#181818;

    border:1px solid var(--border);

    box-shadow:var(--shadow);

    transition:.35s;

    z-index:5000;
}

.toast.show{
    transform:
        translate(-50%,0);

    opacity:1;
}

/* =========================================================
   MOBILE
========================================================= */

@media(max-width:700px){

    header{
        height:64px;
        padding:0 13px;
    }

    .menu{
        display:none;

        position:absolute;

        top:64px;
        left:12px;
        right:12px;

        padding:12px;

        border-radius:18px;

        background:#111;
        border:1px solid var(--border);

        flex-direction:column;
    }

    .menu.open{
        display:flex;
    }

    .menu-toggle{
        display:block;
    }

    .hero{
        min-height:auto;
        padding-top:65px;
    }

    .hero h1{
        font-size:53px;
    }

    .search-box{
        border-radius:20px;
    }

    .search-button{
        padding:
            12px 15px;
    }

    .services{
        grid-template-columns:
            repeat(2,1fr);
    }

    .service{
        min-height:145px;
        padding:17px;
    }

    .device{
        min-height:620px;
    }
}

@media(max-width:380px){

    .services{
        grid-template-columns:1fr;
    }

    .logo-text{
        font-size:17px;
    }

    .hero h1{
        font-size:45px;
    }
}
</style>
</head>

<body>

<div class="aurora"></div>

<!-- =====================================================
     HEADER
===================================================== -->

<header>

    <div class="logo" onclick="goHome()">

        <div class="logo-icon"></div>

        <div class="logo-text">
            FENK<span>.com</span>
        </div>

    </div>

    <button
        class="menu-toggle"
        onclick="toggleMenu()">
        ☰
    </button>

    <nav class="menu" id="menu">

        <button onclick="goHome()">الرئيسية</button>
        <button onclick="scrollToSection('services')">الخدمات</button>
        <button onclick="openAI()">FENK DJ</button>
        <button onclick="scrollToSection('device')">الجهاز</button>
        <button onclick="scrollToSection('about')">حول FENK</button>

    </nav>

</header>


<!-- =====================================================
     HERO
===================================================== -->

<main>

<section class="hero">

    <div class="badge">
        <i></i>
        نظام رقمي ذكي موحّد
    </div>

    <h1>FENK</h1>

    <h2>
        نحو جيل جديد من جهاز الويب الذكي
    </h2>

    <p>
        الإنترنت يأتي إليك.
        ابحث، تصفح، اسأل، أنشئ، خزّن وتواصل
        من تجربة ويب واحدة ذكية.
    </p>


    <!-- SEARCH -->

    <div class="search-box">

        <div class="search-icon">
            🔎
        </div>

        <input
            id="searchInput"
            type="search"
            placeholder="ابحث في FENK أو اسأل FENK DJ..."
            autocomplete="off">

        <button
            class="search-button"
            onclick="performSearch()">
            بحث
        </button>

    </div>


    <div class="quick">

        <button onclick="quickSearch('الذكاء الاصطناعي')">
            🤖 الذكاء الاصطناعي
        </button>

        <button onclick="quickSearch('أخبار اليوم')">
            📰 الأخبار
        </button>

        <button onclick="quickSearch('الجزائر')">
            🇩🇿 الجزائر
        </button>

        <button onclick="openAI()">
            🦊 اسأل FENK DJ
        </button>

    </div>

</section>


<!-- =====================================================
     SERVICES
===================================================== -->

<section
    class="section"
    id="services">

    <div class="section-title">

        <h2>كل الويب في مكان واحد</h2>

        <p>
            منظومة FENK الرقمية
        </p>

    </div>


    <div class="services">

        <div
            class="service"
            onclick="openService('search')">

            <div class="service-icon">🔎</div>

            <h3>FENK Search</h3>

            <p>
                محرك بحث ذكي للويب.
            </p>

        </div>


        <div
            class="service"
            onclick="openAI()">

            <div class="service-icon">🦊</div>

            <h3>FENK DJ</h3>

            <p>
                مساعد الذكاء الاصطناعي.
            </p>

        </div>


        <div class="service">

            <div class="service-icon">🌐</div>

            <h3>FENK Browser</h3>

            <p>
                تصفح الويب من مكان واحد.
            </p>

        </div>


        <div class="service">

            <div class="service-icon">☁️</div>

            <h3>FENK Cloud</h3>

            <p>
                ملفاتك وبياناتك في السحابة.
            </p>

        </div>


        <div class="service">

            <div class="service-icon">✉️</div>

            <h3>FENK Mail</h3>

            <p>
                بريد إلكتروني موحّد.
            </p>

        </div>


        <div class="service">

            <div class="service-icon">💬</div>

            <h3>FENK Chat</h3>

            <p>
                تواصل ومحادثات رقمية.
            </p>

        </div>


        <div class="service">

            <div class="service-icon">🗺️</div>

            <h3>FENK Maps</h3>

            <p>
                استكشاف الأماكن والعالم.
            </p>

        </div>


        <div class="service">

            <div class="service-icon">🛍️</div>

            <h3>FENK Store</h3>

            <p>
                منظومة التطبيقات والخدمات.
            </p>

        </div>


        <div class="service">

            <div class="service-icon">👤</div>

            <h3>FENK ID</h3>

            <p>
                هوية رقمية واحدة.
            </p>

        </div>


        <div class="service">

            <div class="service-icon">🧑‍💻</div>

            <h3>FENK Developers</h3>

            <p>
                أدوات المطورين وواجهات API.
            </p>

        </div>


        <div class="service">

            <div class="service-icon">💼</div>

            <h3>FENK Business</h3>

            <p>
                أدوات الأعمال والمنصات الرقمية.
            </p>

        </div>


        <div class="service">

            <div class="service-icon">🎨</div>

            <h3>FENK Studio</h3>

            <p>
                إنشاء المحتوى والتجارب الرقمية.
            </p>

        </div>

    </div>

</section>


<!-- =====================================================
     SMART DEVICE
===================================================== -->

<section
    class="device-section"
    id="device">

    <div class="device">

        <div class="device-top">

            <small>FENK DEVICE</small>

            <h3>جهاز الويب الذكي</h3>

        </div>


        <div class="device-search">
            🔎 اسأل أو ابحث...
        </div>


        <div class="device-grid">

            <div
                class="app"
                onclick="performSearch()">
                <span>🔎</span>
                بحث
            </div>

            <div
                class="app"
                onclick="openAI()">
                <span>🦊</span>
                DJ
            </div>

            <div class="app">
                <span>🌐</span>
                ويب
            </div>

            <div class="app">
                <span>☁️</span>
                سحابة
            </div>

            <div class="app">
                <span>✉️</span>
                بريد
            </div>

            <div class="app">
                <span>💬</span>
                دردشة
            </div>

            <div class="app">
                <span>🗺️</span>
                خرائط
            </div>

            <div class="app">
                <span>🛍️</span>
                متجر
            </div>

            <div class="app">
                <span>👤</span>
                حساب
            </div>

        </div>


        <div class="offline-card">

            <div class="status"></div>

            <div>

                <strong>
                    وضع FENK Offline
                </strong>

                <p style="color:#888;font-size:12px">
                    الواجهة والموارد المحلية
                    تستمر عند انقطاع الاتصال.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- =====================================================
     FEATURES
===================================================== -->

<section
    class="section"
    id="about">

    <div class="section-title">

        <h2>فلسفة FENK</h2>

        <p>
            أكثر من تطبيق... طبقة ذكية فوق الويب.
        </p>

    </div>


    <div class="feature-list">

        <div class="feature">

            <strong>🧠 ذكاء مدمج</strong>

            <p>
                الوصول إلى أدوات الذكاء الاصطناعي
                من داخل تجربة الويب.
            </p>

        </div>


        <div class="feature">

            <strong>🔎 بحث موحّد</strong>

            <p>
                نقطة دخول واحدة للبحث
                واستكشاف المعلومات.
            </p>

        </div>


        <div class="feature">

            <strong>☁️ سحابة متصلة</strong>

            <p>
                ربط الملفات والخدمات
                والحساب الرقمي في منظومة واحدة.
            </p>

        </div>


        <div class="feature">

            <strong>📱 Mobile First</strong>

            <p>
                تجربة مصممة أولاً للهاتف
                ومتجاوبة مع الشاشات المختلفة.
            </p>

        </div>


        <div class="feature">

            <strong>⚡ Offline Ready</strong>

            <p>
                إمكانية تشغيل الواجهة والموارد
                المحلية عند ضعف أو انقطاع الشبكة.
            </p>

        </div>


        <div class="feature">

            <strong>🔐 Privacy First</strong>

            <p>
                تصميم البنية مع مراعاة
                الخصوصية والتحكم في البيانات.
            </p>

        </div>

    </div>

</section>

</main>


<!-- =====================================================
     FOOTER
===================================================== -->

<footer>

    <div>
        <strong>🦊 FENK.com</strong>
    </div>

    <p style="margin-top:8px">
        نحو جيل جديد من جهاز الويب الذكي
    </p>

    <div class="footer-links">

        <a href="#services">الخدمات</a>
        <a href="#device">الجهاز</a>
        <a href="#about">حول FENK</a>
        <a href="/login">تسجيل الدخول</a>
        <a href="/register">إنشاء حساب</a>

    </div>

    <p style="margin-top:20px;font-size:12px">
        © 2026 FENK — ضيبآ ويب
    </p>

</footer>


<!-- =====================================================
     TOAST
===================================================== -->

<div
    id="toast"
    class="toast">
</div>


<script>

/* =========================================================
   FENK.COM — APPLICATION CORE
========================================================= */

const searchInput =
    document.getElementById("searchInput");

const menu =
    document.getElementById("menu");

const toast =
    document.getElementById("toast");


/* ---------------------------------------------------------
   MENU
--------------------------------------------------------- */

function toggleMenu(){

    menu.classList.toggle("open");

}


/* ---------------------------------------------------------
   HOME
--------------------------------------------------------- */

function goHome(){

    window.scrollTo({
        top:0,
        behavior:"smooth"
    });

    menu.classList.remove("open");

}


/* ---------------------------------------------------------
   SECTION
--------------------------------------------------------- */

function scrollToSection(id){

    const element =
        document.getElementById(id);

    if(element){

        element.scrollIntoView({
            behavior:"smooth"
        });

    }

    menu.classList.remove("open");
}


/* ---------------------------------------------------------
   TOAST
--------------------------------------------------------- */

let toastTimer;

function showToast(message){

    toast.textContent = message;

    toast.classList.add("show");

    clearTimeout(toastTimer);

    toastTimer =
        setTimeout(()=>{
            toast.classList.remove("show");
        },2600);
}


/* ---------------------------------------------------------
   SEARCH
--------------------------------------------------------- */

function performSearch(){

    const query =
        searchInput.value.trim();

    if(!query){

        searchInput.focus();

        showToast(
            "اكتب ما تريد البحث عنه 🔎"
        );

        return;
    }


    /*
      Production:
      يمكن لاحقاً استبدال هذا المسار
      بـ /search?q=
    */

    const url =
        "/search?q=" +
        encodeURIComponent(query);

    showToast(
        "جاري البحث في FENK..."
    );

    setTimeout(()=>{

        window.location.href = url;

    },450);

}


/* ---------------------------------------------------------
   QUICK SEARCH
--------------------------------------------------------- */

function quickSearch(query){

    searchInput.value = query;

    performSearch();

}


/* ---------------------------------------------------------
   ENTER SEARCH
--------------------------------------------------------- */

searchInput.addEventListener(
    "keydown",
    function(event){

        if(event.key === "Enter"){

            performSearch();

        }

    }
);


/* ---------------------------------------------------------
   AI
--------------------------------------------------------- */

function openAI(){

    showToast(
        "فتح FENK DJ 🦊"
    );

    setTimeout(()=>{

        window.location.href =
            "/chat";

    },350);

}


/* ---------------------------------------------------------
   SERVICES
--------------------------------------------------------- */

function openService(service){

    if(service === "search"){

        searchInput.focus();

        window.scrollTo({
            top:0,
            behavior:"smooth"
        });

    }

}


/* =========================================================
   ONLINE / OFFLINE
========================================================= */

function updateNetworkStatus(){

    const online =
        navigator.onLine;

    if(online){

        showToast(
            "FENK متصل بالإنترنت 🌐"
        );

    }else{

        showToast(
            "وضع Offline مفعل — FENK مستمر ⚡"
        );

    }

}

window.addEventListener(
    "online",
    updateNetworkStatus
);

window.addEventListener(
    "offline",
    updateNetworkStatus
);


/* =========================================================
   SERVICE WORKER
========================================================= */

if(
    "serviceWorker"
    in navigator
){

    window.addEventListener(
        "load",
        ()=>{

            /*
              في الإنتاج:
              أنشئ /sw.js
              لتفعيل PWA وOffline Cache.
            */

            navigator.serviceWorker
                .register("/sw.js")
                .catch(()=>{
                    console.log(
                        "Service Worker unavailable"
                    );
                });

        }
    );

}


/* =========================================================
   KEYBOARD SHORTCUT
========================================================= */

document.addEventListener(
    "keydown",
    event => {

        /*
          Ctrl + K
          فتح البحث بسرعة
        */

        if(
            (event.ctrlKey || event.metaKey)
            &&
            event.key.toLowerCase() === "k"
        ){

            event.preventDefault();

            searchInput.focus();

        }

    }
);

</script>

</body>
</html>
```
