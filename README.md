
<html>

<head>
    <meta content="text/html; charset=utf-8" http-equiv="Content-Type">

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/semantic-ui/2.2.11/semantic.min.css">

    <link href="https://fonts.googleapis.com/css?family=Lato:300,400,700" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css?family=Satisfy" rel="stylesheet">


    <style>
        /* PAPER-CSS */
        @page {
            margin: 0
        }

        body {
            margin: 0
        }

        .sheet {
            margin: 0;
            overflow: hidden;
            position: relative;
            box-sizing: border-box;
            page-break-after: always;
        }

        /** Paper sizes **/
        body.A3 .sheet {
            width: 297mm;
            height: 419mm
        }

        body.A3.landscape .sheet {
            width: 420mm;
            height: 296mm
        }

        body.A4 .sheet {
            width: 210mm;
            height: 296mm
        }

        body.A4.landscape .sheet {
            width: 297mm;
            height: 209mm
        }

        body.A5 .sheet {
            width: 148mm;
            height: 209mm
        }

        body.A5.landscape .sheet {
            width: 210mm;
            height: 147mm
        }

        /** Padding area **/
        .sheet > .padding-10mm {
            padding: 10mm
        }

        .sheet > .padding-15mm {
            padding: 15mm
        }

        .sheet > .padding-20mm {
            padding: 20mm
        }

        .sheet > .padding-25mm {
            padding: 25mm
        }

        /** For screen preview **/
        @media screen {
            body {
                background: #e0e0e0
            }

            .sheet {
                background: white;
                box-shadow: 0 .5mm 2mm rgba(0, 0, 0, .3);
                margin: 5mm;
            }
        }

        /** Fix for Chrome issue #273306 **/
        @media print {
            body.A3.landscape {
                width: 420mm
            }

            body.A3, body.A4.landscape {
                width: 297mm
            }

            body.A4, body.A5.landscape {
                width: 210mm
            }

            body.A5 {
                width: 148mm
            }

            /* HIDE ON PRINT */
            .address, .pli-1, .pli-2 {
                display: none !important;
            }
        }

        /* PAPER-CSS */

        /* Helper Classes */
        .m-no-bottom {
            margin-bottom: 0 !important;
        }

        .m-no-top {
            margin-top: 0 !important;
        }

        .m-no-left {
            margin-left: 0 !important;
        }

        .m-no-right {
            margin-right: 0 !important;
        }

        /* Helper Classes */

        .address {
            border: 2px dashed rgba(0, 0, 0, 0.2);
            position: absolute;
            top: calc(297mm - 214mm - 45mm);
        / / background-color: rgba(0, 0, 0, 0.5);
            left: calc(104mm);
            height: 45mm;
            width: 106mm;
            float: left;
            display: table;
        }

        .address p {
            display: table-cell;
            vertical-align: middle;
            text-align: center;
            font-size: 20px;
        }

        .pli-1 {
            position: absolute;
            top: 33%;
            border: 1px dashed rgba(0, 0, 0, 0.2);
            width: 100%;
        }

        .pli-2 {
            position: absolute;
            top: 66%;
            border: 1px dashed rgba(0, 0, 0, 0.2);
            width: 100%;
        }

    </style>

    <style>

        body {
            color: rgba(0, 0, 0, .87);
        }

        .container {
            position: absolute;
            top:34%;
            font-size: 14px;
            text-align: center;
            margin-left: auto;
            margin-right: auto;
        }

        .content{
            width:80%;
            margin : auto;
        }

        .content p {
            font-size: 16px;
        }

        .fait-a {
            margin-top: 150px;
            margin-left: 30px;
        }

        h1 {
            font-weight: 300;
            font-size: 40px;
        }

        .signature {
            float: right;
            margin-top: 20px;
            margin-right: 20px;
        }

        .signature p {
            font-family: 'Satisfy', cursive;
            font-size: 30px;
        }

        .footer {
            position: absolute;
            bottom: 20px;
            width: 720px;

            margin-left: 30px;
            margin-right: 30px;
        }

        .footer p {
            font-size: 12px;
            text-align: center;
        }

        .header-logo {
            background-color: #21314d;
            height: 80px;
            margin-top: 0;
            width: 101%;
            display: table;
        }

        .header-logo p {
            display: table-cell;
            vertical-align: middle;
            color: white;
            padding-left: 30px;
            font-size: 40px;
            font-weight: 600;
        }

        .destinataire {
            padding-top: 70px;
        }

        .image-bottom {
            position: absolute;
            top: 67%;
        }

        .image-bottom img {
            width: 101%;
        }

        .ui.green.button, .ui.green.buttons .button {
            background-color: #01c3a7;
        }
    </style>
</head>

<body class="A4">

<!-- Each sheet element should have the class "sheet" -->
<!-- "padding-**mm" is optional: you can set 10, 15, 20 or 25 -->
<section class="sheet">
    <div class="address">
        <p>Zone Destinataire <br/>
            <small>
                Présent si il n'y a pas de page porte adresse.
                <br/>(Voir Guide "Zone d'écrasement")
            </small>
        </p>
    </div>

    <div class="pli-1"></div>
    <div class="pli-2"></div>

    <div>
        <div class="header-logo">
            <p>seeuletter</p>
        </div>
        <p class="fait-a">
            A {{ville}}, le {{date}}
        </p>
        <!-- Write HTML just like a web page -->
        <article class="container">
            <div class="content">
                <h1>Bienvenue {{prenom}}.</h1>
                <p>
                    Nous sommes ravis de vous compter parmis nos clients.

                    <br/>
                    <br/>
                    Pour vous souhaiter la bienvenue, nous vous offrons 20% de réduction sur votre prochain achat valable sur tout notre site internet avec le code :
                </p>

                <div class="ui hidden divider"></div>

                <button class="ui button huge green">WELCOME20</button>

                <div class="ui hidden divider"></div>

                <p>
                    Merci pour votre confiance et à très bientôt.
                </p>

                <p>
                    Seeuletter
                </p>
            </div>

        </article>

        <div class="image-bottom">
            <img src="https://res.cloudinary.com/lifebot/image/upload/v1500459685/image_lettre_welcome_2_fcda3u.png" alt=""/>
        </div>

        <div class="footer">
            <p>
                {{ expediteur.nom }} au capital social de {{ expediteur.capital_social }} dont le siège social est situé au {{ expediteur.numero }} {{ expediteur.rue }} {{ expediteur.code_postal }} {{ expediteur.ville }}.
                <br/>
                Immatriulé au RCS de Paris sous le n° {{ expediteur.rcs }}. N° de TVA : {{ expediteur.tva }}.
            </p>
        </div>
    </div>


</section>


</body>

</html>
