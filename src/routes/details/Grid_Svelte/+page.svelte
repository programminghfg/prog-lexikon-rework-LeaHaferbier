<script>
    import image1 from "$lib/img/image1.svg";
    import image2 from "$lib/img/image2.svg";
    import image3 from "$lib/img/image3.svg";
</script>

<div class="site">
    <div class="content">
        <head>
            <meta charset="UTF-8" />
            <meta http-equiv="X-UA-Compatible" content="IE=edge" />
            <meta
                name="viewport"
                content="width=device-width, initial-scale=1.0"
            />
            <title>Document</title>
            <link rel="stylesheet" href="fonts/stylesheet.css" />
            <link rel="stylesheet" href="css/style.css" />

            <link rel="stylesheet" href="css/desktop.css" />
            <link rel="stylesheet" href="css/mobile.css" />
        </head>

        <body>
            <div id="wrapper">
                <header>
                    <div id="logo">grid</div>
                    <ul class="nav-links">
                        <li class="nav-item"><a href="/">Grundlegendes</a></li>
                        <li class="nav-item"><a href="/">Ausrichtungen</a></li>
                        <li class="nav-item"><a href="/">Responsive</a></li>
                        <li class="nav-item">
                            <a href="/">Home</a>
                        </li>
                    </ul>
                </header>

                <section id="quick-def">
                    <h1>
                        Einführung in Gestaltungsraster <br /> mit dem Grid Layout
                        Module
                    </h1>
                    <br />
                    <h3>
                        Mit CSS Grid erzeugt ihr Gestaltungsraster, indem Zeilen
                        und Spalten für einen Bereich definiert werden. Elemente
                        werden dann den Rasterzellen zugewiesen, wodurch sehr
                        interessante Layouts möglich sind. <br />
                        <br />
                        <b
                            >Komplexe Weblayouts lassen sich weder mit
                            float-basierten Gestaltungsrastern noch mit Flexbox
                            perfekt umsetzen.</b
                        > <br /> <br />
                        CSS Grid ermöglicht »echte« Gestaltungsraster auf Basis von
                        CSS.
                    </h3>
                </section>

                <article id="grundlegendes">
                    <h2>Grundlegende Funktionsweise von CSS Grid</h2>
                    <p>
                        CSS Grids arbeiten mit einem Elternelement, in dem das
                        Raster definiert wird und mit darin enthaltenen
                        Kind-Elementen, die im Raster positioniert werden. Dem
                        Elternelement wird mit Hilfe der
                        <b>Angabedisplay:grid</b>; mitgeteilt, dass CSS Grids
                        genutzt werden sollen. Mit Hilfe der Eigenschaften
                        <b>grid-template-columns</b> und
                        <b>grid-template-rows</b> werden Rasterlinien gezeichnet.
                    </p>
                </article>

                <article id="section-intro1">
                    <p>
                        Das folgende Beispiel erzeugt ein CSS Grid mit drei
                        Zeilen und vier Spalten. Die erste Zeile ist 200 Pixel
                        hoch, die letzte 100 Pixel. Die mittlere Zeile hat die
                        Angabe <b>1fr (1 Fraction)</b>
                        erhalten. Damit erstreckt Sie sich über den noch freien Platz.
                        Wie viel Platz zur Verfügung steht wird durch die Gesamthöhe
                        des .container bestimmt. Beachtet, dass die Angabe 1fr auch
                        0 Pixel bedeuten kann, wenn der Container eine zu niedrige
                        bzw. keine Höhe erhalten hat. Die vier Spalten sind jeweils
                        25% breit.
                    </p>
                </article>

                <code id="code1">
                    <p>hier könnte Code stehen :)</p>
                    <!-- .container {<br>
                        display: grid; <br>
                        grid-template-rows:200px 1fr 100px; <br> <br>
                        grid-template-columns:25% 25% 25% 25%; <br>
                        } -->
                </code>

                <img src={image1} alt="image1" id="bild1" />

                <article id="section-intro2">
                    <p>
                        Wenn innerhalb des Elternelements nun Kind-Elemente
                        liegen, fügen sich die Inhalte automatisch oben links
                        oben nach rechts unten in die Rasterzellen ein.
                    </p>
                </article>

                <code id="code2">
                    <p>hier könnte Code stehen :)</p>
                    <!-- &lt;div class="container"&gt;&lt;div&gt;Element 1&lt;/div&gt;&lt;div&gt;Element 2&lt;/div&gt;
                        <br>…<br>
                        &lt;div&gt;Element 11&lt;/div&gt;&lt;div&gt;Element 12&lt;/div&gt;&lt;/div&gt; -->
                </code>

                <img src={image2} alt="image2" id="bild2" />

                <article id="section-intro3">
                    <p>
                        Standardmäßig ordnen sich die Elemente zeilenbasiert an:
                        Die Zahlen zeigen in welcher Reihenfolge die
                        Kind-Elemente im Grid positioniert werden. Mit der
                        CSS-Eigenschaft <b>grid-auto-flow</b> kann beeinflusst
                        werden, nach welcher Regel die Kind-Elemente im Raster
                        einsortiert werden. Der Wert
                        <b>column</b> führt beispielsweise zu folgender Anordnung:
                    </p>
                </article>

                <code id="code3">
                    <p>hier könnte Code stehen :)</p>
                    <!-- .container { <br> 
                        display: grid; <br>
                        grid-template-rows: 200px 1fr 100px; <br>
                        grid-template-columns: 25% 25% 25% 25%; <br>
                        grid-auto-flow: column; <br>
                        } -->
                </code>

                <img src={image3} alt="image3" id="bild3" />

                <article id="section-intro4">
                    <p>
                        Die Zahlen zeigen an, in welcher Reihenfolge die
                        Kind-Elemente im Grid positioniert werden.
                    </p>
                </article>

                <footer>
                    <div id="logo2">grid</div>
                    <ul class="footer-links">
                        <li class="footer-item">Kontakt</li>
                        <li class="footer-item">Impressum</li>
                        <li class="footer-item">Datenschutz</li>
                    </ul>
                </footer>
            </div>
        </body>
    </div>
</div>

<style>
    * {
        font-family: "Montserrat", Verdana, sans-serif;
        box-sizing: border-box;
    }

    #wrapper {
        width: windowwidth;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
        grid-template-rows: 150px 580px 280px 100px 390px 55px 390px 85px 390px 55px 100px;
        grid-template-areas:
            "kopfzeile kopfzeile kopfzeile kopfzeile kopfzeile kopfzeile"
            "quick-def quick-def quick-def quick-def quick-def quick-def"
            "grundlegendes grundlegendes grundlegendes grundlegendes grundlegendes grundlegendes"
            "text1 text1 text1 text1 text1 text1"
            "leer1 code1 code1 bild1 bild1 leer2"
            "text2 text2 text2 text2 text2 text2"
            "leer3 code2 code2 bild2 bild2 leer4"
            "text3 text3 text3 text3 text3 text3"
            "leer5 code3 code3 bild3 bild3 leer6"
            "text4 text4 text4 text4 text4 text4"
            "footer footer footer footer footer footer";
    }

    header {
        grid-area: kopfzeile;
        padding-left: 30px;
        padding-right: 10px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    #logo {
        display: inline-block;
        font-weight: bold;
        font-size: xx-large;
        color: #006268;
        text-transform: uppercase;
    }

    .nav-links {
        list-style: none;
        display: flex;
    }

    .nav-item a {
        display: inline-block;
        padding: 10px 15px;
        text-decoration: none;
        color: black;
    }

    #quick-def {
        background-color: #006268;
        grid-area: quick-def;
    }

    h1 {
        color: white;
        text-align: center;
        margin-top: 75px;
        letter-spacing: 3px;
    }

    #quick-def h3 {
        color: white;
        padding-left: 200px;
        padding-right: 200px;
        text-align: left;
        font-weight: normal;
        font-size: 20px;
    }

    #grundlegendes {
        grid-area: grundlegendes;
        background-color: white;
    }

    #section-intro1 {
        grid-area: text1;
        background-color: #e0d9d1;
        font-weight: normal;
        font-size: 14px;
    }

    article h2 {
        color: #006268;
        padding-left: 200px;
        padding-right: 350px;
        text-align: left;
        font-weight: normal;
        font-size: 36px;
    }

    p {
        padding-left: 200px;
        padding-right: 200px;
    }

    #code1 {
        grid-area: code1;
        color: #006268;
        font-family: RedHatMono;
        font-weight: normal;
        font-size: 20px;
        max-width: 512px;
        align-self: center;
    }

    #bild1 {
        grid-area: bild1;
    }

    #section-intro2 {
        grid-area: text2;
        background-color: #e0d9d1;
        font-weight: normal;
        font-size: 14px;
    }

    #code2 {
        grid-area: code2;
        color: #006268;
        font-family: RedHatMono;
        font-weight: normal;
        font-size: 20px;
        max-width: 512px;
        align-self: center;
    }

    #bild2 {
        grid-area: bild2;
    }

    #section-intro3 {
        grid-area: text3;
        background-color: #e0d9d1;
        font-weight: normal;
        font-size: 14px;
    }

    #code3 {
        grid-area: code3;
        color: #006268;
        font-family: RedHatMono;
        font-weight: normal;
        font-size: 20px;
        max-width: 512px;
        align-self: center;
    }

    #bild3 {
        grid-area: bild3;
    }

    #section-intro4 {
        grid-area: text4;
        background-color: #e0d9d1;
        font-weight: normal;
        font-size: 14px;
    }

    footer {
        background-color: #006268;
        padding-left: 30px;
        padding-right: 10px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        grid-area: footer;
    }

    #logo2 {
        display: inline-block;
        font-weight: bold;
        font-size: xx-large;
        color: #e0d9d1;
        text-transform: uppercase;
    }

    .footer-links {
        list-style: none;
        display: flex;
    }

    .footer-item {
        display: inline-block;
        padding: 10px 15px;
        text-decoration: none;
        color: white;
    }
</style>
