<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Biodata - Dea Nur Ramadani</title>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&display=swap" rel="stylesheet" />
    <style>
        /* ---------- RESET ---------- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(145deg, #fce4ec 0%, #f3e5f5 50%, #e8eaf6 100%);
            padding: 20px;
        }

        /* ---------- CARD UTAMA ---------- */
        .card {
            max-width: 480px;
            width: 100%;
            background: rgba(255, 255, 255, 0.75);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border-radius: 48px;
            padding: 36px 28px 40px;
            box-shadow:
                0 30px 60px rgba(0, 0, 0, 0.12),
                0 10px 30px rgba(0, 0, 0, 0.06),
                inset 0 1px 0 rgba(255, 255, 255, 0.6);
            border: 1px solid rgba(255, 255, 255, 0.4);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .card:hover {
            transform: translateY(-4px);
            box-shadow:
                0 40px 80px rgba(0, 0, 0, 0.15),
                0 15px 40px rgba(0, 0, 0, 0.08);
        }

        /* Decorative blur orbs */
        .card::before {
            content: '';
            position: absolute;
            top: -100px;
            right: -100px;
            width: 280px;
            height: 280px;
            background: radial-gradient(circle, rgba(236, 64, 122, 0.15), transparent 70%);
            border-radius: 50%;
            pointer-events: none;
            z-index: 0;
        }
        .card::after {
            content: '';
            position: absolute;
            bottom: -80px;
            left: -80px;
            width: 240px;
            height: 240px;
            background: radial-gradient(circle, rgba(103, 58, 183, 0.12), transparent 70%);
            border-radius: 50%;
            pointer-events: none;
            z-index: 0;
        }

        /* ---------- KONTEN ---------- */
        .content {
            position: relative;
            z-index: 1;
        }

        /* ---------- AVATAR ---------- */
        .avatar-wrapper {
            display: flex;
            justify-content: center;
            margin-bottom: 18px;
        }

        .avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: linear-gradient(135deg, #ec407a, #ab47bc);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 52px;
            font-weight: 700;
            color: #fff;
            box-shadow:
                0 12px 30px rgba(171, 71, 188, 0.35),
                0 0 0 4px rgba(255, 255, 255, 0.6);
            user-select: none;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            flex-shrink: 0;
        }

        .avatar:hover {
            transform: scale(1.04);
            box-shadow:
                0 16px 40px rgba(171, 71, 188, 0.45),
                0 0 0 6px rgba(255, 255, 255, 0.7);
        }

        /* ---------- NAMA ---------- */
        .name {
            text-align: center;
            font-size: 28px;
            font-weight: 800;
            color: #1a1a2e;
            letter-spacing: -0.5px;
            line-height: 1.2;
            margin-bottom: 2px;
        }

        .name span {
            background: linear-gradient(135deg, #ec407a, #ab47bc);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .subtitle {
            text-align: center;
            font-size: 14px;
            font-weight: 400;
            color: #7a7a9a;
            letter-spacing: 0.3px;
            margin-bottom: 22px;
        }

        /* ---------- DIVIDER ---------- */
        .divider {
            width: 60px;
            height: 3px;
            margin: 0 auto 22px;
            background: linear-gradient(90deg, #ec407a, #ab47bc);
            border-radius: 6px;
            opacity: 0.5;
        }

        /* ---------- INFO LIST ---------- */
        .info-list {
            display: flex;
            flex-direction: column;
            gap: 14px;
            margin-bottom: 24px;
        }

        .info-item {
            display: flex;
            align-items: flex-start;
            gap: 14px;
            padding: 12px 16px;
            background: rgba(255, 255, 255, 0.55);
            backdrop-filter: blur(6px);
            -webkit-backdrop-filter: blur(6px);
            border-radius: 18px;
            border: 1px solid rgba(255, 255, 255, 0.5);
            transition: background 0.25s ease, transform 0.2s ease;
        }

        .info-item:hover {
            background: rgba(255, 255, 255, 0.8);
            transform: translateX(4px);
        }

        .info-icon {
            width: 38px;
            height: 38px;
            min-width: 38px;
            border-radius: 12px;
            background: linear-gradient(135deg, #f8e8ff, #f3e5f5);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #ab47bc;
            font-size: 17px;
            box-shadow: 0 2px 8px rgba(171, 71, 188, 0.10);
        }

        .info-text {
            flex: 1;
        }

        .info-label {
            font-size: 11px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            color: #7a7a9a;
            margin-bottom: 1px;
        }

        .info-value {
            font-size: 15px;
            font-weight: 500;
            color: #1a1a2e;
            line-height: 1.4;
        }

        .info-value .highlight {
            background: linear-gradient(135deg, #ec407a, #ab47bc);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-weight: 600;
        }

        /* ---------- MOTTO ---------- */
        .motto-box {
            background: linear-gradient(135deg, rgba(236, 64, 122, 0.08), rgba(171, 71, 188, 0.08));
            border-radius: 20px;
            padding: 18px 20px;
            margin: 6px 0 24px;
            border-left: 4px solid #ab47bc;
            text-align: center;
        }

        .motto-box .quote-icon {
            color: #ab47bc;
            font-size: 20px;
            opacity: 0.5;
            margin-right: 6px;
        }

        .motto-box .motto-text {
            font-size: 16px;
            font-weight: 600;
            color: #1a1a2e;
            line-height: 1.5;
            font-style: italic;
        }

        .motto-box .motto-text .highlight {
            background: linear-gradient(135deg, #ec407a, #ab47bc);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-style: normal;
        }

        /* ---------- TOMBOL ---------- */
        .btn-project {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            width: 100%;
            padding: 16px 20px;
            background: linear-gradient(135deg, #ec407a, #ab47bc);
            color: #fff;
            font-size: 16px;
            font-weight: 600;
            font-family: 'Poppins', sans-serif;
            border: none;
            border-radius: 60px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 8px 24px rgba(171, 71, 188, 0.30);
            text-decoration: none;
            letter-spacing: 0.3px;
            position: relative;
            overflow: hidden;
        }

        .btn-project::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.15), transparent 60%);
            pointer-events: none;
        }

        .btn-project:hover {
            transform: translateY(-3px) scale(1.01);
            box-shadow: 0 14px 36px rgba(171, 71, 188, 0.40);
        }

        .btn-project:active {
            transform: translateY(1px) scale(0.98);
            box-shadow: 0 4px 12px rgba(171, 71, 188, 0.30);
        }

        .btn-project i {
            font-size: 18px;
            transition: transform 0.3s ease;
        }

        .btn-project:hover i {
            transform: translateX(4px) scale(1.1);
        }

        .btn-project .btn-label {
            position: relative;
            z-index: 1;
        }

        /* ---------- RESPONSIVE ---------- */
        @media (max-width: 500px) {
            .card {
                padding: 28px 18px 32px;
                border-radius: 36px;
            }

            .avatar {
                width: 100px;
                height: 100px;
                font-size: 42px;
            }

            .name {
                font-size: 24px;
            }

            .info-item {
                padding: 10px 14px;
            }

            .info-value {
                font-size: 14px;
            }

            .btn-project {
                font-size: 14px;
                padding: 14px 18px;
            }

            .motto-box .motto-text {
                font-size: 14px;
            }
        }

        @media (max-width: 380px) {
            .card {
                padding: 22px 14px 26px;
            }

            .avatar {
                width: 84px;
                height: 84px;
                font-size: 34px;
            }

            .name {
                font-size: 20px;
            }

            .info-value {
                font-size: 13px;
            }
        }
    </style>
</head>
<body>

    <div class="card">
        <div class="content">

            <!-- AVATAR -->
            <div class="avatar-wrapper">
                <div class="avatar">D</div>
            </div>

            <!-- NAMA -->
            <h1 class="name"><span>Dea Nur Ramadani</span></h1>
            <p class="subtitle">✦ Calon Business Women ✦</p>

            <div class="divider"></div>

            <!-- INFO LIST -->
            <div class="info-list">

                <!-- Tanggal Lahir -->
                <div class="info-item">
                    <div class="info-icon"><i class="fas fa-cake-candles"></i></div>
                    <div class="info-text">
                        <div class="info-label">Tanggal Lahir</div>
                        <div class="info-value">13 Agustus 2012</div>
                    </div>
                </div>

                <!-- Hobi -->
                <div class="info-item">
                    <div class="info-icon"><i class="fas fa-book-open"></i></div>
                    <div class="info-text">
                        <div class="info-label">Hobi</div>
                        <div class="info-value">
                            <span class="highlight">Mengerjakan MTK</span> &amp;
                            <span class="highlight">Membaca Novel</span>
                        </div>
                    </div>
                </div>

                <!-- Cita-cita -->
                <div class="info-item">
                    <div class="info-icon"><i class="fas fa-briefcase"></i></div>
                    <div class="info-text">
                        <div class="info-label">Cita-cita</div>
                        <div class="info-value">
                            Menjadi <span class="highlight">Business Women</span>
                        </div>
                    </div>
                </div>

            </div>

            <!-- MOTTO -->
            <div class="motto-box">
                <div class="motto-text">
                    <i class="fas fa-quote-left quote-icon"></i>
                    Sukses itu hasil dari <span class="highlight">ketekunan</span>,
                    bukan hanya <span class="highlight">kebetulan</span>
                    <i class="fas fa-quote-right quote-icon" style="margin-left:6px;"></i>
                </div>
            </div>

            <!-- TOMBOL PROJECT -->
            <a href="https://ceandy1245.github.io/aplikasi-ilustrasi-pembangunan-rumah-melalui-3D/"
            target="_blank"
            rel="noopener noreferrer"
            class="btn-project">
            <span class="btn-label">
                <i class="fas fa-cube"></i> Lihat Project 3D
            </span>
            <i class="fas fa-arrow-right"></i>
        </a>

    </div>
</div>

</body>
</html>
