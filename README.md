<!DOCTYPE html>
<html lang="pt-BR">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Aviação TFF — Aviões de Papel</title>

    <style>

        * {
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            margin: 0;
            background: #050505;
            color: #f5f5f5;
            font-family: Arial, Helvetica, sans-serif;
        }

        button,
        input,
        textarea,
        select {
            font-family: inherit;
        }

        button {
            cursor: pointer;
        }

        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: #050505;
        }

        ::-webkit-scrollbar-thumb {
            background: #333;
            border-radius: 20px;
        }

        /* ================= HEADER ================= */

        header {
            position: sticky;
            top: 0;
            z-index: 100;

            height: 72px;

            padding: 0 5%;

            display: flex;
            align-items: center;
            justify-content: space-between;

            gap: 30px;

            background: rgba(5, 5, 5, .94);

            border-bottom: 1px solid #1d1d1d;

            backdrop-filter: blur(15px);
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;

            font-size: 20px;
            font-weight: 800;

            letter-spacing: -.5px;
        }

        .logo-icon {
            width: 38px;
            height: 38px;

            display: flex;
            align-items: center;
            justify-content: center;

            background: white;
            color: black;

            border-radius: 10px;
        }

        nav {
            display: flex;
            align-items: center;
            gap: 28px;
        }

        nav a {
            color: #888;
            text-decoration: none;

            font-size: 14px;

            transition: .2s;
        }

        nav a:hover {
            color: white;
        }

        .cart-button {
            background: white;
            color: black;

            border: 0;

            padding: 10px 15px;

            border-radius: 9px;

            font-weight: 700;
        }

        /* ================= HERO ================= */

        .hero {
            min-height: 620px;

            padding: 100px 7%;

            display: flex;
            align-items: center;
            justify-content: space-between;

            gap: 60px;

            background:
                radial-gradient(
                    circle at 80% 40%,
                    #202020 0,
                    transparent 28%
                ),
                #050505;
        }

        .hero-content {
            max-width: 700px;
        }

        .tag {
            display: inline-block;

            padding: 7px 11px;

            border: 1px solid #333;

            border-radius: 50px;

            color: #aaa;

            font-size: 11px;

            letter-spacing: 1px;

            font-weight: bold;
        }

        .hero h1 {
            margin: 22px 0;

            font-size: clamp(45px, 7vw, 88px);

            line-height: .95;

            letter-spacing: -5px;
        }

        .hero h1 span {
            color: #777;
        }

        .hero p {
            max-width: 570px;

            color: #888;

            line-height: 1.7;

            font-size: 16px;
        }

        .hero-buttons {
            display: flex;

            gap: 12px;

            margin-top: 30px;

            flex-wrap: wrap;
        }

        .primary {
            background: white;
            color: black;

            border: 0;

            padding: 14px 20px;

            border-radius: 9px;

            font-weight: bold;
        }

        .secondary {
            background: transparent;

            color: white;

            border: 1px solid #333;

            padding: 14px 20px;

            border-radius: 9px;
        }

        .hero-plane {
            width: 330px;
            height: 330px;

            display: flex;

            align-items: center;
            justify-content: center;

            border: 1px solid #222;

            border-radius: 50%;

            background:
                radial-gradient(
                    circle,
                    #151515,
                    #050505
                );
        }

        .hero-plane span {
            font-size: 150px;

            transform: rotate(-15deg);

            filter: grayscale(1);
        }

        /* ================= SECTIONS ================= */

        section {
            padding: 90px 7%;
        }

        .section-header {
            display: flex;

            align-items: end;

            justify-content: space-between;

            gap: 30px;

            margin-bottom: 35px;
        }

        .section-label {
            color: #666;

            font-size: 11px;

            letter-spacing: 2px;

            font-weight: bold;
        }

        .section-title {
            margin: 8px 0 0;

            font-size: 38px;

            letter-spacing: -1.5px;
        }

        .section-description {
            color: #666;

            max-width: 500px;

            line-height: 1.6;
        }

        /* ================= ESTATÍSTICAS ================= */

        .stats {
            padding-top: 0;

            padding-bottom: 30px;
        }

        .stats-grid {
            display: grid;

            grid-template-columns:
                repeat(4, 1fr);

            gap: 1px;

            background: #222;

            border: 1px solid #222;

            border-radius: 14px;

            overflow: hidden;
        }

        .stat {
            background: #0b0b0b;

            padding: 28px;
        }

        .stat-icon {
            color: #666;

            font-size: 20px;
        }

        .stat-number {
            margin: 15px 0 5px;

            font-size: 28px;

            font-weight: bold;
        }

        .stat-name {
            color: #666;

            font-size: 13px;
        }

        /* ================= CATÁLOGO ================= */

        .catalog {
            background: #080808;

            border-top: 1px solid #151515;

            border-bottom: 1px solid #151515;
        }

        .catalog-grid {
            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 18px;
        }

        .product {
            background: #0d0d0d;

            border: 1px solid #202020;

            border-radius: 14px;

            overflow: hidden;

            transition: .25s;
        }

        .product:hover {
            transform: translateY(-4px);

            border-color: #444;
        }

        .product-image {
            height: 220px;

            display: flex;

            align-items: center;
            justify-content: center;

            background:
                linear-gradient(
                    135deg,
                    #111,
                    #080808
                );

            border-bottom: 1px solid #1c1c1c;
        }

        .product-image span {
            font-size: 90px;

            filter: grayscale(1);

            transform: rotate(-10deg);
        }

        .product-info {
            padding: 23px;
        }

        .product-category {
            color: #666;

            font-size: 10px;

            letter-spacing: 1.5px;

            font-weight: bold;
        }

        .product h3 {
            margin: 10px 0;

            font-size: 20px;
        }

        .product-description {
            color: #666;

            line-height: 1.6;

            min-height: 50px;

            font-size: 13px;
        }

        .product-bottom {
            display: flex;

            justify-content: space-between;

            align-items: center;

            margin-top: 20px;

            gap: 10px;
        }

        .price {
            font-weight: bold;

            font-size: 18px;
        }

        .product-button {
            background: white;

            color: black;

            border: 0;

            padding: 10px 13px;

            border-radius: 7px;

            font-size: 12px;

            font-weight: bold;
        }

        /* ================= ESTADO VAZIO ================= */

        .empty {
            grid-column: 1 / -1;

            padding: 80px 20px;

            text-align: center;

            border: 1px dashed #292929;

            border-radius: 14px;

            color: #555;
        }

        .empty-icon {
            font-size: 45px;

            margin-bottom: 15px;

            filter: grayscale(1);
        }

        /* ================= TABELA ================= */

        .table-wrapper {
            border: 1px solid #202020;

            border-radius: 14px;

            overflow-x: auto;

            background: #0b0b0b;
        }

        table {
            width: 100%;

            min-width: 800px;

            border-collapse: collapse;
        }

        th {
            color: #666;

            font-size: 11px;

            letter-spacing: 1px;

            text-align: left;

            padding: 18px;

            background: #0f0f0f;
        }

        td {
            padding: 18px;

            border-top: 1px solid #1c1c1c;

            color: #aaa;

            font-size: 13px;
        }

        .status {
            display: inline-block;

            padding: 6px 9px;

            border-radius: 5px;

            background: #171717;

            color: #777;

            font-size: 11px;
        }

        /* ================= CLIENTES ================= */

        .clients {
            background: #080808;

            border-top: 1px solid #151515;
        }

        .client-grid {
            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 18px;
        }

        .client {
            padding: 25px;

            background: #0d0d0d;

            border: 1px solid #202020;

            border-radius: 14px;
        }

        .client-avatar {
            width: 45px;
            height: 45px;

            border-radius: 50%;

            background: #191919;

            display: flex;

            align-items: center;
            justify-content: center;

            color: #777;

            margin-bottom: 18px;
        }

        .client h3 {
            margin: 0 0 8px;
        }

        .client p {
            color: #666;

            font-size: 13px;

            line-height: 1.6;
        }

        /* ================= BOTÕES ================= */

        .add-button {
            background: white;

            color: black;

            border: 0;

            padding: 12px 16px;

            border-radius: 8px;

            font-weight: bold;
        }

        /* ================= MODAIS ================= */

        .modal {
            display: none;

            position: fixed;

            inset: 0;

            z-index: 200;

            align-items: center;

            justify-content: center;

            padding: 20px;

            background:
                rgba(0, 0, 0, .8);

            backdrop-filter: blur(8px);
        }

        .modal-box {
            width: 100%;

            max-width: 520px;

            background: #101010;

            border: 1px solid #292929;

            border-radius: 15px;

            padding: 30px;

            box-shadow:
                0 20px 70px
                rgba(0, 0, 0, .5);
        }

        .modal-header {
            display: flex;

            align-items: center;

            justify-content: space-between;

            margin-bottom: 25px;
        }

        .modal-header h2 {
            margin: 0;
        }

        .close {
            background: #1b1b1b;

            border: 0;

            color: #888;

            width: 35px;

            height: 35px;

            border-radius: 8px;
        }

        label {
            display: block;

            color: #888;

            font-size: 12px;

            margin-bottom: 7px;
        }

        input,
        textarea,
        select {
            width: 100%;

            padding: 13px;

            margin-bottom: 18px;

            background: #080808;

            border: 1px solid #292929;

            color: white;

            border-radius: 8px;

            outline: none;
        }

        input:focus,
        textarea:focus,
        select:focus {
            border-color: #555;
        }

        textarea {
            resize: vertical;

            min-height: 90px;
        }

        .modal-actions {
            display: flex;

            justify-content: flex-end;

            gap: 10px;
        }

        .cancel {
            background: #191919;

            color: #aaa;

            border: 1px solid #292929;

            padding: 12px 17px;

            border-radius: 8px;
        }

        /* ================= FOOTER ================= */

        footer {
            padding: 50px 7%;

            border-top: 1px solid #1b1b1b;

            background: #030303;

            color: #555;
        }

        footer strong {
            color: white;

            font-size: 19px;
        }

        /* ================= RESPONSIVO ================= */

        @media(max-width: 900px) {

            nav {
                display: none;
            }

            .hero {
                padding-top: 70px;

                flex-direction: column;

                align-items: flex-start;
            }

            .hero-plane {
                align-self: center;
            }

            .stats-grid {
                grid-template-columns:
                    repeat(2, 1fr);
            }

            .catalog-grid {
                grid-template-columns:
                    repeat(2, 1fr);
            }

            .client-grid {
                grid-template-columns: 1fr;
            }

        }

        @media(max-width: 600px) {

            header {
                padding: 0 20px;
            }

            .hero {
                padding: 70px 25px;
            }

            .hero h1 {
                letter-spacing: -3px;
            }

            .hero-plane {
                width: 250px;

                height: 250px;

                align-self: center;
            }

            .hero-plane span {
                font-size: 110px;
            }

            section {
                padding: 65px 25px;
            }

            .stats-grid {
                grid-template-columns: 1fr;
            }

            .catalog-grid {
                grid-template-columns: 1fr;
            }

            .section-header {
                align-items: flex-start;

                flex-direction: column;
            }

        }

    </style>

</head>


<body>


<!-- ================= HEADER ================= -->

<header>

    <div class="logo">

        <div class="logo-icon">
            ✈
        </div>

        Aviação TFF

    </div>


    <nav>

        <a href="#inicio">
            Início
        </a>

        <a href="#modelos">
            Modelos
        </a>

        <a href="#pedidos">
            Pedidos
        </a>

        <a href="#clientes">
            Clientes
        </a>

    </nav>


    <button
        class="cart-button"
        onclick="abrirCarrinho()"
    >

        🛒

        <span id="contador">
            0
        </span>

    </button>

</header>



<!-- ================= HERO ================= -->

<section
    id="inicio"
    class="hero"
>

    <div class="hero-content">

        <span class="tag">
            AVIAÇÃO TFF / STORE
        </span>


        <h1>

            Aviação TFF

            <br>

            <span>
                Aviões feitos para voar.
            </span>

        </h1>


        <p>

            Plataforma da Aviação TFF para
            cadastro, gerenciamento e venda
            de aviões de papel.

        </p>


        <div class="hero-buttons">

            <a
                href="#modelos"
                class="primary"
                style="text-decoration:none;"
            >

                Explorar modelos

            </a>


            <a
                href="#pedidos"
                class="secondary"
                style="text-decoration:none;"
            >

                Ver pedidos

            </a>

        </div>

    </div>


    <div class="hero-plane">

        <span>
            ✈️
        </span>

    </div>

</section>



<!-- ================= ESTATÍSTICAS ================= -->

<section class="stats">

    <div class="stats-grid">


        <div class="stat">

            <div class="stat-icon">
                ✈
            </div>

            <div
                id="totalModelos"
                class="stat-number"
            >
                0
            </div>

            <div class="stat-name">
                Modelos cadastrados
            </div>

        </div>


        <div class="stat">

            <div class="stat-icon">
                ◉
            </div>

            <div
                id="totalClientes"
                class="stat-number"
            >
                0
            </div>

            <div class="stat-name">
                Clientes
            </div>

        </div>


        <div class="stat">

            <div class="stat-icon">
                □
            </div>

            <div
                id="totalPedidos"
                class="stat-number"
            >
                0
            </div>

            <div class="stat-name">
                Pedidos
            </div>

        </div>


        <div class="stat">

            <div class="stat-icon">
                $
            </div>

            <div class="stat-number">
                —
            </div>

            <div class="stat-name">
                Faturamento
            </div>

        </div>


    </div>

</section>



<!-- ================= MODELOS ================= -->

<section
    id="modelos"
    class="catalog"
>

    <div class="section-header">

        <div>

            <div class="section-label">
                01 / CATÁLOGO
            </div>

            <h2 class="section-title">
                Modelos da Aviação TFF
            </h2>

        </div>


        <button
            class="add-button"
            onclick="abrirModelo()"
        >

            + Novo modelo

        </button>

    </div>


    <p class="section-description">

        Cadastre os aviões de papel
        disponíveis para venda.

    </p>


    <div
        id="catalogo"
        class="catalog-grid"
    >

        <div class="empty">

            <div class="empty-icon">
                ✈
            </div>

            <strong>
                Nenhum modelo cadastrado
            </strong>

            <p>
                Os produtos aparecerão aqui
                quando você cadastrar um modelo.
            </p>

        </div>

    </div>

</section>



<!-- ================= PEDIDOS ================= -->

<section id="pedidos">

    <div class="section-header">

        <div>

            <div class="section-label">
                02 / PEDIDOS
            </div>

            <h2 class="section-title">
                Pedidos
            </h2>

        </div>

    </div>


    <p class="section-description">

        Acompanhe os pedidos realizados
        pelos clientes da Aviação TFF.

    </p>


    <div class="table-wrapper">

        <table>

            <thead>

                <tr>

                    <th>
                        ID
                    </th>

                    <th>
                        CLIENTE
                    </th>

                    <th>
                        MODELO
                    </th>

                    <th>
                        VALOR
                    </th>

                    <th>
                        DATA
                    </th>

                    <th>
                        STATUS
                    </th>

                </tr>

            </thead>


            <tbody id="tabelaPedidos">

                <tr>

                    <td
                        colspan="6"
                        style="
                            text-align:center;
                            padding:55px;
                            color:#555;
                        "
                    >

                        Nenhum pedido registrado.

                    </td>

                </tr>

            </tbody>

        </table>

    </div>

</section>



<!-- ================= CLIENTES ================= -->

<section
    id="clientes"
    class="clients"
>

    <div class="section-header">

        <div>

            <div class="section-label">
                03 / CLIENTES
            </div>

            <h2 class="section-title">
                Clientes
            </h2>

        </div>


        <button
            class="add-button"
            onclick="abrirCliente()"
        >

            + Novo cliente

        </button>

    </div>


    <p class="section-description">

        Cadastre e consulte os clientes
        da Aviação TFF.

    </p>


    <div
        id="listaClientes"
        class="client-grid"
    >

        <div class="empty">

            <div class="empty-icon">
                ◉
            </div>

            <strong>
                Nenhum cliente cadastrado
            </strong>

            <p>
                Os clientes aparecerão aqui
                depois do cadastro.
            </p>

        </div>

    </div>

</section>



<!-- ================= MODAL MODELO ================= -->

<div
    id="modalModelo"
    class="modal"
>

    <div class="modal-box">

        <div class="modal-header">

            <h2>
                Novo modelo
            </h2>

            <button
                class="close"
                onclick="fecharModelo()"
            >
                ×
            </button>

        </div>


        <label>
            Nome do avião
        </label>

        <input
            id="nomeModelo"
            type="text"
            placeholder="Nome do modelo"
        >


        <label>
            Descrição
        </label>

        <textarea
            id="descricaoModelo"
            placeholder="Descreva o modelo..."
        ></textarea>


        <label>
            Categoria
        </label>

        <select id="categoriaModelo">

            <option value="">
                Selecione uma categoria
            </option>

            <option>
                Distância
            </option>

            <option>
                Velocidade
            </option>

            <option>
                Acrobacia
            </option>

            <option>
                Tradicional
            </option>

            <option>
                Outro
            </option>

        </select>


        <label>
            Valor
        </label>

        <input
            id="valorModelo"
            type="number"
            step="0.01"
            placeholder="Digite o valor"
        >


        <div class="modal-actions">

            <button
                class="cancel"
                onclick="fecharModelo()"
            >
                Cancelar
            </button>


            <button
                class="primary"
                onclick="salvarModelo()"
            >
                Salvar modelo
            </button>

        </div>

    </div>

</div>



<!-- ================= MODAL CLIENTE ================= -->

<div
    id="modalCliente"
    class="modal"
>

    <div class="modal-box">

        <div class="modal-header">

            <h2>
                Novo cliente
            </h2>

            <button
                class="close"
                onclick="fecharCliente()"
            >
                ×
            </button>

        </div>


        <label>
            Nome
        </label>

        <input
            id="nomeCliente"
            type="text"
            placeholder="Nome completo"
        >


        <label>
            E-mail
        </label>

        <input
            id="emailCliente"
            type="email"
            placeholder="E-mail"
        >


        <label>
            Telefone
        </label>

        <input
            id="telefoneCliente"
            type="text"
            placeholder="Telefone"
        >


        <div class="modal-actions">

            <button
                class="cancel"
                onclick="fecharCliente()"
            >
                Cancelar
            </button>


            <button
                class="primary"
                onclick="salvarCliente()"
            >
                Salvar cliente
            </button>

        </div>

    </div>

</div>



<!-- ================= FOOTER ================= -->

<footer>

    <strong>
        ✈ Aviação TFF
    </strong>

    <p>
        Plataforma de gerenciamento e venda
        de aviões de papel.
    </p>

    <p>
        Nenhum produto, cliente ou pedido
        é pré-cadastrado.
    </p>

</footer>



<!-- ================= JAVASCRIPT ================= -->

<script>

    let modelos = [];

    let clientes = [];

    let pedidos = [];

    let carrinho = [];


    /* ================= MODELOS ================= */

    function abrirModelo() {

        document.getElementById(
            "modalModelo"
        ).style.display = "flex";

    }


    function fecharModelo() {

        document.getElementById(
            "modalModelo"
        ).style.display = "none";

    }


    function salvarModelo() {

        const nome =
            document
                .getElementById("nomeModelo")
                .value
                .trim();


        const descricao =
            document
                .getElementById("descricaoModelo")
                .value
                .trim();


        const categoria =
            document
                .getElementById("categoriaModelo")
                .value;


        const valor =
            document
                .getElementById("valorModelo")
                .value;


        if (!nome) {

            alert(
                "Digite o nome do modelo."
            );

            return;

        }


        if (!valor) {

            alert(
                "Digite o valor do modelo."
            );

            return;

        }


        modelos.push({

            id: Date.now(),

            nome: nome,

            descricao: descricao,

            categoria: categoria,

            valor: valor

        });


        document.getElementById(
            "nomeModelo"
        ).value = "";


        document.getElementById(
            "descricaoModelo"
        ).value = "";


        document.getElementById(
            "categoriaModelo"
        ).value = "";


        document.getElementById(
            "valorModelo"
        ).value = "";


        fecharModelo();

        renderizarModelos();

    }



    function renderizarModelos() {

        const catalogo =
            document.getElementById(
                "catalogo"
            );


        catalogo.innerHTML = "";


        if (modelos.length === 0) {

            catalogo.innerHTML = `

                <div class="empty">

                    <div class="empty-icon">
                        ✈
                    </div>

                    <strong>
                        Nenhum modelo cadastrado
                    </strong>

                    <p>
                        Os produtos aparecerão aqui
                        quando você cadastrar um modelo.
                    </p>

                </div>

            `;

        }


        modelos.forEach(
            function(modelo, index) {

                catalogo.innerHTML += `

                    <div class="product">

                        <div class="product-image">

                            <span>
                                ✈️
                            </span>

                        </div>


                        <div class="product-info">

                            <div class="product-category">

                                ${
                                    modelo.categoria ||
                                    "SEM CATEGORIA"
                                }

                            </div>


                            <h3>

                                ${modelo.nome}

                            </h3>


                            <div class="product-description">

                                ${
                                    modelo.descricao ||
                                    "Sem descrição."
                                }

                            </div>


                            <div class="product-bottom">

                                <div class="price">

                                    R$
                                    ${Number(
                                        modelo.valor
                                    ).toFixed(2)}

                                </div>


                                <button
                                    class="product-button"
                                    onclick="adicionarCarrinho(${index})"
                                >

                                    Adicionar

                                </button>

                            </div>

                        </div>

                    </div>

                `;

            }
        );


        document.getElementById(
            "totalModelos"
        ).innerText = modelos.length;

    }



    /* ================= CLIENTES ================= */

    function abrirCliente() {

        document.getElementById(
            "modalCliente"
        ).style.display = "flex";

    }


    function fecharCliente() {

        document.getElementById(
            "modalCliente"
        ).style.display = "none";

    }


    function salvarCliente() {

        const nome =
            document
                .getElementById("nomeCliente")
                .value
                .trim();


        const email =
            document
                .getElementById("emailCliente")
                .value
                .trim();


        const telefone =
            document
                .getElementById("telefoneCliente")
                .value
                .trim();


        if (!nome) {

            alert(
                "Digite o nome do cliente."
            );

            return;

        }


        clientes.push({

            id: Date.now(),

            nome: nome,

            email: email,

            telefone: telefone

        });


        document.getElementById(
            "nomeCliente"
        ).value = "";


        document.getElementById(
            "emailCliente"
        ).value = "";


        document.getElementById(
            "telefoneCliente"
        ).value = "";


        fecharCliente();

        renderizarClientes();

    }



    function renderizarClientes() {

        const lista =
            document.getElementById(
                "listaClientes"
            );


        lista.innerHTML = "";


        if (clientes.length === 0) {

            lista.innerHTML = `

                <div class="empty">

                    <div class="empty-icon">
                        ◉
                    </div>

                    <strong>
                        Nenhum cliente cadastrado
                    </strong>

                    <p>
                        Os clientes aparecerão aqui
                        depois do cadastro.
                    </p>

                </div>

            `;

        }


        clientes.forEach(
            function(cliente) {

                lista.innerHTML += `

                    <div class="client">

                        <div class="client-avatar">
                            ◉
                        </div>


                        <h3>
                            ${cliente.nome}
                        </h3>


                        <p>
                            ${
                                cliente.email ||
                                "E-mail não informado"
                            }
                        </p>


                        <p>
                            ${
                                cliente.telefone ||
                                "Telefone não informado"
                            }
                        </p>

                    </div>

                `;

            }
        );


        document.getElementById(
            "totalClientes"
        ).innerText = clientes.length;

    }



    /* ================= CARRINHO ================= */

    function adicionarCarrinho(index) {

        carrinho.push(
            modelos[index]
        );


        document.getElementById(
            "contador"
        ).innerText = carrinho.length;


        alert(
            "Modelo adicionado ao carrinho."
        );

    }


    function abrirCarrinho() {

        if (carrinho.length === 0) {

            alert(
                "O carrinho está vazio."
            );

            return;

        }


        let texto =
            "CARRINHO — AVIAÇÃO TFF\n\n";


        carrinho.forEach(
            function(item, index) {

                texto +=

                    (index + 1) +
                    " — " +
                    item.nome +
                    " | R$ " +
                    Number(
                        item.valor
                    ).toFixed(2) +
                    "\n";

            }
        );


        alert(texto);

    }



    /* ================= INICIALIZAÇÃO ================= */

    renderizarModelos();

    renderizarClientes();

</script>


</body>

</html>

