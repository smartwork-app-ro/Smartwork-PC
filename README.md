<!DOCTYPE html>
<html lang="ro" dir="ltr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Programul de muncă (2026 &amp; 2027)</title>

    <!-- Setări PWA & Pictogramă personalizată (înlocuiește litera gri "G" pe Android/Chrome) -->
    <meta name="application-name" content="SmartWork">
    <meta name="apple-mobile-web-app-title" content="SmartWork">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="theme-color" content="#1d4ed8">

    <link id="app-favicon" rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 512 512'%3E%3Cdefs%3E%3ClinearGradient id='bg' x1='0' y1='0' x2='1' y2='1'%3E%3Cstop offset='0%25' stop-color='%232563eb'/%3E%3Cstop offset='100%25' stop-color='%231e3a8a'/%3E%3C/linearGradient%3E%3C/defs%3E%3Crect width='512' height='512' rx='112' fill='url(%23bg)'/%3E%3Cg transform='rotate(-7 240 245)'%3E%3Crect x='92' y='112' width='284' height='256' rx='36' fill='%23f8fafc'/%3E%3Cpath d='M92 148c0-20 16-36 36-36h212c20 0 36 16 36 36v42H92v-42z' fill='%231d4ed8'/%3E%3Crect x='152' y='84' width='24' height='54' rx='12' fill='%230f172a'/%3E%3Crect x='292' y='84' width='24' height='54' rx='12' fill='%230f172a'/%3E%3Crect x='132' y='214' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='188' y='214' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='244' y='214' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='300' y='214' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='132' y='266' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='188' y='266' width='40' height='36' rx='8' fill='%232563eb'/%3E%3Cpath d='M198 284l7 7 15-15' stroke='%23ffffff' stroke-width='6' fill='none' stroke-linecap='round' stroke-linejoin='round'/%3E%3Crect x='244' y='266' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3C/g%3E%3Cpath d='M402 92l26-26M420 124l36-10M426 158l32 8' stroke='%23ffffff' stroke-width='12' stroke-linecap='round'/%3E%3Crect x='66' y='324' width='156' height='118' rx='24' fill='%23f8fafc' stroke='%231e3a8a' stroke-width='8'/%3E%3Cpath d='M116 324v-20c0-10 8-18 18-18h20c10 0 18 8 18 18v20' fill='none' stroke='%230f172a' stroke-width='12'/%3E%3Cpath d='M66 366c48 22 108 22 156 0' fill='none' stroke='%231e3a8a' stroke-width='8'/%3E%3Crect x='128' y='362' width='32' height='34' rx='8' fill='%231e3a8a'/%3E%3Ccircle cx='352' cy='346' r='104' fill='%23f8fafc' stroke='%231e3a8a' stroke-width='18'/%3E%3Cpath d='M352 266v14M352 412v14M272 346h14M418 346h14' stroke='%231e3a8a' stroke-width='10' stroke-linecap='round'/%3E%3Cpath d='M324 322l28 26 42-38' fill='none' stroke='%230f172a' stroke-width='14' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E">
    <link id="apple-touch-icon" rel="apple-touch-icon" href="">
    <link id="pwa-manifest" rel="manifest" href="">

    <script>
        /* Generează automat pictograma PNG (512x512) și Manifestul Web App pentru Android/Chrome */
        (function setupCustomSmartWorkIcon() {
            try {
                const canvas = document.createElement('canvas');
                canvas.width = 512;
                canvas.height = 512;
                const ctx = canvas.getContext('2d');
                if (!ctx) return;

                function roundRect(c, x, y, w, h, r) {
                    c.beginPath();
                    c.moveTo(x + r, y);
                    c.arcTo(x + w, y, x + w, y + h, r);
                    c.arcTo(x + w, y + h, x, y + h, r);
                    c.arcTo(x, y + h, x, y, r);
                    c.arcTo(x, y, x + w, y, r);
                    c.closePath();
                }

                // 1. Fundal albastru rotunjit
                const grad = ctx.createLinearGradient(0, 0, 512, 512);
                grad.addColorStop(0, '#2563eb');
                grad.addColorStop(1, '#1e3a8a');
                ctx.fillStyle = grad;
                roundRect(ctx, 0, 0, 512, 512, 112);
                ctx.fill();

                // 2. Raze albe dreapta-sus
                ctx.strokeStyle = '#ffffff';
                ctx.lineWidth = 13;
                ctx.lineCap = 'round';
                ctx.beginPath();
                ctx.moveTo(398, 94); ctx.lineTo(426, 66);
                ctx.moveTo(418, 128); ctx.lineTo(456, 116);
                ctx.moveTo(424, 164); ctx.lineTo(458, 172);
                ctx.stroke();

                // 3. Calendar înclinat
                ctx.save();
                ctx.translate(236, 244);
                ctx.rotate(-7 * Math.PI / 180);
                ctx.translate(-236, -244);

                ctx.fillStyle = '#f8fafc';
                roundRect(ctx, 90, 112, 286, 256, 34);
                ctx.fill();

                ctx.fillStyle = '#1d4ed8';
                ctx.beginPath();
                ctx.moveTo(90, 146);
                ctx.arcTo(90, 112, 124, 112, 34);
                ctx.lineTo(342, 112);
                ctx.arcTo(376, 112, 376, 146, 34);
                ctx.lineTo(376, 188);
                ctx.lineTo(90, 188);
                ctx.closePath();
                ctx.fill();

                // Inele calendar
                ctx.fillStyle = '#0f172a';
                roundRect(ctx, 152, 82, 24, 54, 12);
                ctx.fill();
                roundRect(ctx, 290, 82, 24, 54, 12);
                ctx.fill();

                // Pătrățele zile
                const cols = [132, 188, 244, 300];
                const rows = [212, 266, 316];
                rows.forEach((ry, rIdx) => {
                    cols.forEach((cx, cIdx) => {
                        if (rIdx === 2 && cIdx === 0) return;
                        if (rIdx === 1 && cIdx === 1) {
                            ctx.fillStyle = '#2563eb';
                            roundRect(ctx, cx, ry, 40, 36, 8);
                            ctx.fill();
                            ctx.strokeStyle = '#ffffff';
                            ctx.lineWidth = 6;
                            ctx.beginPath();
                            ctx.moveTo(cx + 10, ry + 18);
                            ctx.lineTo(cx + 17, ry + 25);
                            ctx.lineTo(cx + 31, ry + 11);
                            ctx.stroke();
                        } else {
                            ctx.fillStyle = '#cbd5e1';
                            roundRect(ctx, cx, ry, 40, 36, 8);
                            ctx.fill();
                        }
                    });
                });
                ctx.restore();

                // 4. Servietă alb-albastru stânga-jos
                ctx.strokeStyle = '#0f172a';
                ctx.lineWidth = 13;
                roundRect(ctx, 116, 286, 56, 46, 14);
                ctx.stroke();

                ctx.fillStyle = '#f8fafc';
                roundRect(ctx, 64, 322, 160, 120, 24);
                ctx.fill();
                ctx.strokeStyle = '#1e3a8a';
                ctx.lineWidth = 7;
                ctx.stroke();

                ctx.beginPath();
                ctx.moveTo(64, 366);
                ctx.quadraticCurveTo(144, 392, 224, 366);
                ctx.stroke();

                ctx.fillStyle = '#1e3a8a';
                roundRect(ctx, 128, 360, 32, 34, 8);
                ctx.fill();

                // 5. Ceas dreapta-jos
                ctx.fillStyle = '#f8fafc';
                ctx.beginPath();
                ctx.arc(352, 346, 102, 0, Math.PI * 2);
                ctx.fill();
                ctx.strokeStyle = '#1e3a8a';
                ctx.lineWidth = 18;
                ctx.stroke();

                // Repere ceas
                ctx.strokeStyle = '#1e3a8a';
                ctx.lineWidth = 10;
                ctx.beginPath();
                ctx.moveTo(352, 268); ctx.lineTo(352, 282);
                ctx.moveTo(352, 410); ctx.lineTo(352, 424);
                ctx.moveTo(274, 346); ctx.lineTo(288, 346);
                ctx.moveTo(416, 346); ctx.lineTo(430, 346);
                ctx.stroke();

                // Acele ceasului
                ctx.strokeStyle = '#0f172a';
                ctx.lineWidth = 14;
                ctx.beginPath();
                ctx.moveTo(324, 322);
                ctx.lineTo(352, 348);
                ctx.lineTo(394, 310);
                ctx.stroke();

                const pngDataUrl = canvas.toDataURL('image/png');
                const favLink = document.getElementById('app-favicon');
                const appleLink = document.getElementById('apple-touch-icon');
                if (favLink) {
                    favLink.type = 'image/png';
                    favLink.href = pngDataUrl;
                }
                if (appleLink) {
                    appleLink.href = pngDataUrl;
                }

                // Manifest Web App pentru ecranul principal Android
                const manifestObj = {
                    name: 'SmartWork - Programul de muncă',
                    short_name: 'SmartWork',
                    start_url: window.location.href,
                    display: 'standalone',
                    background_color: '#f8fafc',
                    theme_color: '#1d4ed8',
                    icons: [
                        { src: pngDataUrl, sizes: '192x192', type: 'image/png', purpose: 'any maskable' },
                        { src: pngDataUrl, sizes: '512x512', type: 'image/png', purpose: 'any maskable' }
                    ]
                };
                const manifestBlob = new Blob([JSON.stringify(manifestObj)], { type: 'application/manifest+json' });
                const manifestLink = document.getElementById('pwa-manifest');
                if (manifestLink) {
                    manifestLink.href = URL.createObjectURL(manifestBlob);
                }
            } catch (e) {}
        })();
    </script>

    <style>
        /* =====================================================================
           1. DESIGN TOKENS & BASE STYLES (100% SELF-CONTAINED)
           ===================================================================== */
        :root {
            --bg-body: #f8fafc;
            --bg-card: #ffffff;
            --bg-subtle: #f1f5f9;
            --border-color: #e2e8f0;
            --border-strong: #cbd5e1;
            --text-main: #0f172a;
            --text-secondary: #475569;
            --text-muted: #64748b;

            --indigo-50: #eef2ff;
            --indigo-100: #e0e7ff;
            --indigo-200: #c7d2fe;
            --indigo-600: #4f46e5;
            --indigo-700: #4338ca;

            --amber-50: #fffbeb;
            --amber-100: #fef3c7;
            --amber-200: #fde68a;
            --amber-700: #b45309;
            --amber-800: #92400e;

            --emerald-50: #ecfdf5;
            --emerald-200: #a7f3d0;
            --emerald-700: #047857;
            --emerald-800: #065f46;

            --rose-50: #fff1f2;
            --rose-100: #ffe4e6;
            --rose-200: #fecdd3;
            --rose-600: #e11d48;
            --rose-700: #be123c;

            --shadow-sm: 0 1px 2px rgba(15, 23, 42, 0.05);
            --shadow-md: 0 4px 12px rgba(15, 23, 42, 0.08);
            --shadow-xl: 0 20px 35px -10px rgba(15, 23, 42, 0.25);
        }

        *, *::before, *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html, body {
            height: 100%;
            direction: ltr;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, Helvetica, Arial, sans-serif;
            background-color: var(--bg-body);
            color: var(--text-main);
            -webkit-font-smoothing: antialiased;
            line-height: 1.4;
        }

        body {
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        body.fullscreen-schedule-active {
            overflow: hidden !important;
        }

        button, select, input {
            font-family: inherit;
        }

        ::-webkit-scrollbar {
            width: 6px;
            height: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f5f9;
        }
        ::-webkit-scrollbar-thumb {
            background: #cbd5e1;
            border-radius: 999px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #94a3b8;
        }

        /* =====================================================================
           2. HEADER & NAVIGATION CONTROLS
           ===================================================================== */
        .app-header {
            background: var(--bg-card);
            border-bottom: 1px solid var(--border-color);
            box-shadow: var(--shadow-sm);
            position: sticky;
            top: 0;
            z-index: 30;
            padding: 12px 16px;
        }

        .header-inner {
            max-width: 1600px;
            margin: 0 auto;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 12px;
        }

        .brand-trigger {
            display: flex;
            align-items: center;
            gap: 12px;
            cursor: pointer;
            padding: 6px 10px;
            margin-left: -10px;
            border-radius: 14px;
            transition: background-color 0.2s ease, transform 0.15s ease;
            user-select: none;
            background: transparent;
            border: none;
            text-align: left;
        }

        .brand-trigger:hover {
            background-color: var(--indigo-50);
        }

        .brand-trigger:active {
            transform: scale(0.99);
        }

        .brand-icon {
            width: 42px;
            height: 42px;
            border-radius: 12px;
            background: linear-gradient(135deg, #2563eb, #1e3a8a);
            color: #ffffff;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
            box-shadow: 0 4px 10px rgba(37, 99, 235, 0.28);
            overflow: hidden;
        }

        .brand-title-row {
            display: flex;
            align-items: center;
            gap: 8px;
            flex-wrap: wrap;
        }

        .brand-title {
            font-size: 1.15rem;
            font-weight: 800;
            color: var(--text-main);
            text-decoration: underline;
            text-decoration-color: var(--indigo-200);
            text-decoration-thickness: 2px;
            text-underline-offset: 4px;
        }

        .brand-trigger:hover .brand-title {
            color: var(--indigo-700);
        }

        .year-badge {
            display: inline-flex;
            align-items: center;
            padding: 2px 8px;
            border-radius: 999px;
            font-size: 0.72rem;
            font-weight: 700;
            background: var(--indigo-50);
            color: var(--indigo-700);
            border: 1px solid var(--indigo-200);
        }

        .brand-subtitle {
            font-size: 0.75rem;
            color: var(--text-muted);
            margin-top: 2px;
        }

        .week-navigator {
            display: flex;
            align-items: center;
            gap: 6px;
            background: var(--bg-subtle);
            padding: 5px;
            border-radius: 14px;
            border: 1px solid var(--border-color);
            flex-wrap: wrap;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
            padding: 8px 12px;
            border-radius: 10px;
            font-size: 0.8rem;
            font-weight: 600;
            border: 1px solid var(--border-color);
            background: #ffffff;
            color: var(--text-main);
            cursor: pointer;
            transition: all 0.15s ease;
            white-space: nowrap;
        }

        .btn:hover {
            background: #f8fafc;
            border-color: var(--border-strong);
        }

        .btn:active {
            transform: translateY(1px);
        }

        .btn-icon {
            padding: 8px;
        }

        .btn-primary {
            background: var(--indigo-600);
            color: #ffffff;
            border-color: var(--indigo-600);
            box-shadow: 0 2px 6px rgba(79, 70, 229, 0.25);
        }

        .btn-primary:hover {
            background: var(--indigo-700);
            border-color: var(--indigo-700);
        }

        .btn-save {
            background: #059669;
            color: #ffffff;
            border-color: #047857;
            box-shadow: 0 2px 6px rgba(5, 150, 105, 0.25);
        }

        .btn-save:hover {
            background: #047857;
            border-color: #065f46;
        }

        .btn-save.has-unsaved {
            background: #d97706;
            border-color: #b45309;
            box-shadow: 0 0 0 3px rgba(217, 119, 6, 0.22);
        }

        .btn-save.has-unsaved:hover {
            background: #b45309;
            border-color: #92400e;
        }

        .btn-soft-indigo {
            background: var(--indigo-50);
            color: var(--indigo-700);
            border-color: var(--indigo-200);
        }

        .btn-soft-indigo:hover {
            background: var(--indigo-100);
        }

        .btn-soft-amber {
            background: var(--amber-50);
            color: var(--amber-800);
            border-color: var(--amber-200);
        }

        .btn-soft-amber:hover {
            background: var(--amber-100);
        }

        .btn-whatsapp {
            background: #16a34a;
            color: #ffffff;
            border-color: #15803d;
            box-shadow: 0 2px 6px rgba(22, 163, 74, 0.22);
        }

        .btn-whatsapp:hover {
            background: #15803d;
            border-color: #166534;
        }

        .btn-email {
            background: #0284c7;
            color: #ffffff;
            border-color: #0369a1;
            box-shadow: 0 2px 6px rgba(2, 132, 199, 0.22);
        }

        .btn-email:hover {
            background: #0369a1;
            border-color: #075985;
        }

        .btn-danger-soft {
            background: var(--rose-50);
            color: var(--rose-700);
            border-color: var(--rose-200);
        }

        .btn-danger-soft:hover {
            background: var(--rose-100);
        }

        .select-control {
            padding: 7px 10px;
            border-radius: 10px;
            border: 1px solid var(--border-strong);
            background: #ffffff;
            color: var(--text-main);
            font-size: 0.82rem;
            font-weight: 700;
            cursor: pointer;
            outline: none;
        }

        .select-control:focus {
            border-color: var(--indigo-600);
            box-shadow: 0 0 0 3px rgba(79, 70, 229, 0.15);
        }

        .header-actions {
            display: flex;
            align-items: center;
            gap: 8px;
            flex-wrap: wrap;
        }

        /* =====================================================================
           3. LEGEND, SHARE ACTIONS & STATS BAR
           ===================================================================== */
        .sub-toolbar {
            max-width: 1600px;
            width: 100%;
            margin: 12px auto 0;
            padding: 0 16px;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 10px;
        }

        .legend-list {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 6px;
            font-size: 0.73rem;
        }

        .legend-pill {
            display: inline-flex;
            align-items: center;
            gap: 5px;
            padding: 4px 9px;
            border-radius: 8px;
            font-weight: 600;
            border: 1px solid transparent;
        }

        .legend-dot {
            width: 8px;
            height: 8px;
            border-radius: 50%;
        }

        .right-toolbar-group {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 8px;
        }

        .share-group {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            flex-wrap: wrap;
        }

        .stats-bar {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.78rem;
            color: var(--text-secondary);
            background: #ffffff;
            padding: 6px 12px;
            border-radius: 12px;
            border: 1px solid var(--border-color);
        }

        .stats-bar strong {
            color: var(--text-main);
            font-weight: 800;
        }

        /* =====================================================================
           4. SCHEDULE TABLE CONTAINER (MONDAY - SUNDAY)
           ===================================================================== */
        .main-workspace {
            flex: 1;
            max-width: 1600px;
            width: 100%;
            margin: 12px auto 20px;
            padding: 0 16px;
            display: flex;
            flex-direction: column;
        }

        #fullscreen-overlay-shell {
            flex: 1;
            display: flex;
            flex-direction: column;
        }

        #fullscreen-rotated-stage {
            flex: 1;
            display: flex;
            flex-direction: column;
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            box-shadow: var(--shadow-md);
            overflow: hidden;
            position: relative;
        }

        #fullscreen-top-bar {
            display: none;
            align-items: center;
            justify-content: space-between;
            gap: 10px;
            padding: 8px 14px;
            background: #0f172a;
            color: #ffffff;
            border-bottom: 1px solid #334155;
            flex-shrink: 0;
        }

        #fullscreen-overlay-shell.active #fullscreen-top-bar {
            display: flex;
        }

        .fs-title-group {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.85rem;
            font-weight: 700;
        }

        .fs-actions-group {
            display: flex;
            align-items: center;
            gap: 6px;
            flex-wrap: wrap;
        }

        .fs-btn {
            padding: 5px 10px;
            border-radius: 8px;
            font-size: 0.75rem;
            font-weight: 700;
            border: 1px solid #475569;
            background: #1e293b;
            color: #f8fafc;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 5px;
        }

        .fs-btn:hover {
            background: #334155;
        }

        .fs-btn-save {
            background: #059669;
            border-color: #047857;
            color: #ffffff;
        }

        .fs-btn-save:hover {
            background: #047857;
        }

        .fs-btn-wa {
            background: #16a34a;
            border-color: #15803d;
            color: #ffffff;
        }

        .fs-btn-wa:hover {
            background: #15803d;
        }

        .fs-btn-mail {
            background: #0284c7;
            border-color: #0369a1;
            color: #ffffff;
        }

        .fs-btn-mail:hover {
            background: #0369a1;
        }

        .fs-btn-exit {
            background: #e11d48;
            border-color: #e11d48;
            color: #ffffff;
        }

        .fs-btn-exit:hover {
            background: #be123c;
        }

        #table-scroll-wrapper {
            width: 100%;
            overflow-x: auto;
            overflow-y: auto;
            flex: 1;
        }

        table.schedule-table {
            width: 100%;
            border-collapse: collapse;
            table-layout: fixed;
            min-width: 760px;
            direction: ltr;
        }

        col.col-employee { width: 19%; }
        col.col-day      { width: 10.4%; }
        col.col-days-cnt { width: 8.2%; }

        .schedule-table thead th {
            position: sticky;
            top: 0;
            z-index: 15;
            background: #f1f5f9;
            border-bottom: 2px solid var(--border-strong);
            border-right: 1px solid var(--border-color);
            padding: 10px 4px;
            text-align: center;
            font-size: 0.78rem;
            font-weight: 800;
            color: var(--text-main);
        }

        .schedule-table thead th.sticky-col {
            position: sticky;
            left: 0;
            z-index: 25;
            direction: ltr;
            unicode-bidi: isolate;
            text-align: left;
            padding-left: 12px;
            background: var(--indigo-600);
            color: #ffffff;
            border-right: 2px solid var(--indigo-700);
        }

        .schedule-table thead th.weekend-col {
            background: var(--amber-100);
            color: var(--amber-800);
            border-bottom-color: #f59e0b;
        }

        .schedule-table thead th.today-col {
            background: var(--indigo-100);
            color: var(--indigo-700);
            border-bottom-color: var(--indigo-600);
        }

        .today-red-dot {
            display: inline-block;
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background-color: #e11d48;
            box-shadow: 0 0 0 2px rgba(225, 29, 72, 0.22);
            margin-left: 4px;
            vertical-align: middle;
            flex-shrink: 0;
        }

        .day-name-row {
            display: inline-flex;
            align-items: center;
            justify-content: center;
        }

        .day-name {
            display: inline-block;
            font-size: 0.8rem;
            font-weight: 800;
            letter-spacing: -0.01em;
        }

        .day-date {
            display: block;
            font-size: 0.7rem;
            font-weight: 600;
            opacity: 0.85;
            margin-top: 2px;
        }

        .schedule-table tbody td {
            border-bottom: 1px solid var(--border-color);
            border-right: 1px solid var(--border-color);
            padding: 5px 4px;
            vertical-align: middle;
            text-align: center;
            height: 64px;
        }

        .schedule-table tbody tr:hover td {
            background-color: #f8fafc;
        }

        .schedule-table tbody td.sticky-col {
            position: sticky;
            left: 0;
            z-index: 20;
            direction: ltr;
            unicode-bidi: isolate;
            text-align: left;
            padding: 6px 8px 6px 12px;
            border-left: 4px solid var(--indigo-600);
            border-right: 2px solid var(--indigo-200);
            box-shadow: 2px 0 6px rgba(79, 70, 229, 0.08);
        }

        .schedule-table tbody tr:hover td.sticky-col {
            background: linear-gradient(90deg, var(--indigo-100) 0%, var(--indigo-50) 100%);
        }

        .emp-cell-wrap {
            display: flex;
            flex-direction: row;
            direction: ltr;
            align-items: center;
            justify-content: space-between;
            gap: 4px;
        }

        .emp-info {
            min-width: 0;
            flex: 1;
            direction: ltr;
            unicode-bidi: isolate;
            text-align: left;
        }

        .emp-name {
            direction: ltr;
            unicode-bidi: isolate;
            text-align: left;
            font-size: 0.96rem;
            font-weight: 900;
            letter-spacing: -0.01em;
            color: #1e1b4b;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            line-height: 1.2;
        }

        .emp-role {
            display: inline-block;
            direction: ltr;
            unicode-bidi: isolate;
            text-align: left;
            font-size: 0.68rem;
            font-weight: 800;
            color: #ffffff;
            background: var(--indigo-600);
            border: 1px solid var(--indigo-700);
            border-radius: 6px;
            padding: 1px 7px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-top: 3px;
            max-width: 100%;
        }

        .emp-del-btn {
            opacity: 0;
            background: var(--rose-50);
            color: var(--rose-600);
            border: 1px solid var(--rose-200);
            border-radius: 6px;
            width: 22px;
            height: 22px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            flex-shrink: 0;
            transition: opacity 0.15s ease;
        }

        .schedule-table tbody tr:hover .emp-del-btn {
            opacity: 1;
        }

        .schedule-table tbody td.weekend-cell {
            background-color: rgba(254, 243, 199, 0.28);
        }

        .shift-slot {
            width: 100%;
            height: 100%;
            min-height: 46px;
            border-radius: 10px;
            padding: 4px 3px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            border: 1px solid transparent;
            transition: transform 0.1s ease, box-shadow 0.15s ease, border-color 0.15s ease;
            user-select: none;
        }

        .shift-slot:hover {
            transform: translateY(-1px);
            box-shadow: 0 3px 8px rgba(15, 23, 42, 0.08);
        }

        .shift-empty {
            border: 1px dashed #cbd5e1;
            color: #94a3b8;
            background: rgba(255, 255, 255, 0.6);
            font-size: 0.72rem;
            font-weight: 600;
        }

        .shift-empty:hover {
            border-color: var(--indigo-600);
            color: var(--indigo-600);
            background: var(--indigo-50);
        }

        .shift-work {
            background: var(--emerald-50);
            border-color: var(--emerald-200);
            color: var(--emerald-800);
        }

        .shift-extra {
            background: var(--amber-50);
            border-color: var(--amber-200);
            color: var(--amber-800);
        }

        .shift-vrij {
            background: #f1f5f9;
            border-color: #cbd5e1;
            color: #475569;
        }

        .shift-vakantie {
            background: var(--rose-50);
            border-color: var(--rose-200);
            color: var(--rose-700);
        }

        .shift-title {
            font-size: 0.8rem;
            font-weight: 800;
            line-height: 1.15;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            max-width: 100%;
        }

        .shift-sub {
            font-size: 0.64rem;
            font-weight: 700;
            opacity: 0.9;
            margin-top: 2px;
            white-space: nowrap;
        }

        .days-count-badge {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 4px 8px;
            border-radius: 8px;
            font-size: 0.76rem;
            font-weight: 800;
            background: var(--indigo-50);
            color: var(--indigo-700);
            border: 1px solid var(--indigo-200);
        }

        .schedule-table tfoot td {
            background: #f8fafc;
            border-top: 2px solid var(--border-strong);
            border-right: 1px solid var(--border-color);
            padding: 8px 4px;
            text-align: center;
            font-size: 0.72rem;
            font-weight: 700;
            color: var(--text-secondary);
        }

        .schedule-table tfoot td.sticky-col {
            position: sticky;
            left: 0;
            z-index: 20;
            direction: ltr;
            unicode-bidi: isolate;
            background: #f1f5f9;
            text-align: left;
            padding-left: 12px;
            color: var(--text-main);
            border-right: 2px solid var(--border-strong);
        }

        /* =====================================================================
           5. 90-DEGREE ROTATED FULLSCREEN SCHEDULE MODE
           ===================================================================== */
        #fullscreen-overlay-shell.active {
            position: fixed;
            inset: 0;
            z-index: 50;
            width: 100vw;
            height: 100vh;
            height: 100dvh;
            background: #0f172a;
            overflow: hidden;
        }

        #fullscreen-overlay-shell.active #fullscreen-rotated-stage {
            border-radius: 0;
            border: none;
            width: 100%;
            height: 100%;
            max-width: none;
            max-height: none;
            transition: transform 0.25s ease;
        }

        #fullscreen-overlay-shell.active.rotated-ccw #fullscreen-rotated-stage,
        #fullscreen-overlay-shell.active.rotated-cw #fullscreen-rotated-stage {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 100dvh;
            height: 100vw;
            max-width: none;
            max-height: none;
        }

        #fullscreen-overlay-shell.active.rotated-ccw #fullscreen-rotated-stage {
            transform: translate(-50%, -50%) rotate(-90deg);
        }

        #fullscreen-overlay-shell.active.rotated-cw #fullscreen-rotated-stage {
            transform: translate(-50%, -50%) rotate(90deg);
        }

        #fullscreen-overlay-shell.active #table-scroll-wrapper {
            overflow-x: hidden !important;
            overflow-y: auto !important;
            -webkit-overflow-scrolling: touch;
            flex: 1 1 auto;
            width: 100%;
            height: 100%;
            min-height: 0;
        }

        #fullscreen-overlay-shell.active table.schedule-table {
            min-width: 0 !important;
            width: 100% !important;
            height: auto;
            table-layout: fixed !important;
            direction: ltr !important;
            border-collapse: collapse !important;
        }

        #fullscreen-overlay-shell.active col.col-employee { width: 26%; }
        #fullscreen-overlay-shell.active col.col-day      { width: 9.2%; }
        #fullscreen-overlay-shell.active col.col-days-cnt { width: 9.6%; }

        #fullscreen-overlay-shell.active .schedule-table thead th,
        #fullscreen-overlay-shell.active .schedule-table thead th.sticky-col,
        #fullscreen-overlay-shell.active .schedule-table tbody td,
        #fullscreen-overlay-shell.active .schedule-table tbody td.sticky-col,
        #fullscreen-overlay-shell.active .schedule-table tfoot td,
        #fullscreen-overlay-shell.active .schedule-table tfoot td.sticky-col {
            position: static !important;
            top: auto !important;
            left: auto !important;
            right: auto !important;
            bottom: auto !important;
        }

        #fullscreen-overlay-shell.active .schedule-table thead th {
            padding: 5px 2px;
            font-size: 0.68rem;
        }

        #fullscreen-overlay-shell.active .schedule-table thead th.sticky-col {
            direction: ltr !important;
            unicode-bidi: isolate;
            text-align: left !important;
            padding-left: 8px;
            background: var(--indigo-600);
            color: #ffffff;
            border-right: 2px solid var(--indigo-700);
        }

        #fullscreen-overlay-shell.active .schedule-table tbody td {
            padding: 3px 2px;
            height: auto;
            min-height: 44px;
            overflow: visible;
        }

        #fullscreen-overlay-shell.active td.sticky-col {
            direction: ltr !important;
            unicode-bidi: isolate;
            text-align: left !important;
            background: linear-gradient(90deg, var(--indigo-100) 0%, #ffffff 100%) !important;
            border-left: 4px solid var(--indigo-600) !important;
            border-right: 2px solid var(--indigo-600) !important;
            padding: 4px 5px 4px 7px !important;
            box-shadow: 2px 0 8px rgba(79, 70, 229, 0.16);
        }

        #fullscreen-overlay-shell.active .emp-cell-wrap {
            display: flex !important;
            flex-direction: row !important;
            direction: ltr !important;
            justify-content: flex-start !important;
            align-items: center !important;
            width: 100%;
        }

        #fullscreen-overlay-shell.active .emp-info,
        #fullscreen-overlay-shell.active .emp-name,
        #fullscreen-overlay-shell.active .emp-role {
            display: block !important;
            visibility: visible !important;
            opacity: 1 !important;
            direction: ltr !important;
            unicode-bidi: isolate;
            text-align: left !important;
            white-space: normal !important;
            overflow: visible !important;
            text-overflow: clip !important;
            word-break: normal;
            overflow-wrap: break-word;
            max-width: 100%;
        }

        #fullscreen-overlay-shell.active .emp-name {
            font-size: 0.86rem;
            font-weight: 900;
            line-height: 1.15;
            color: #1e1b4b !important;
            background: rgba(255, 255, 255, 0.92);
            padding: 2px 4px;
            border-radius: 4px;
        }

        #fullscreen-overlay-shell.active .emp-role {
            display: inline-block !important;
            font-size: 0.62rem;
            font-weight: 800;
            line-height: 1.1;
            color: #ffffff !important;
            background: var(--indigo-600) !important;
            border: none !important;
            border-radius: 5px;
            padding: 1px 5px;
            margin-top: 2px;
        }

        #fullscreen-overlay-shell.active .emp-del-btn {
            display: none !important;
        }

        #fullscreen-overlay-shell.active .shift-slot {
            min-height: 36px;
            padding: 2px;
            border-radius: 7px;
        }

        #fullscreen-overlay-shell.active .shift-title {
            font-size: 0.68rem;
        }

        #fullscreen-overlay-shell.active .shift-sub {
            font-size: 0.56rem;
        }

        #fullscreen-overlay-shell.active .days-count-badge {
            padding: 3px 5px;
            font-size: 0.66rem;
        }

        @media (max-width: 767px) {
            #fullscreen-overlay-shell.active #fullscreen-top-bar {
                display: none !important;
            }
        }

        /* =====================================================================
           6. MODALS & TOAST NOTIFICATIONS
           ===================================================================== */
        .modal-backdrop {
            position: fixed;
            inset: 0;
            z-index: 60;
            background: rgba(15, 23, 42, 0.55);
            backdrop-filter: blur(2px);
            display: none;
            align-items: center;
            justify-content: center;
            padding: 16px;
        }

        .modal-backdrop.open {
            display: flex;
        }

        #fullscreen-rotated-stage .modal-backdrop {
            position: absolute;
            inset: 0;
            z-index: 75;
            padding: 10px;
        }

        #fullscreen-rotated-stage .modal-card {
            max-height: 92%;
            display: flex;
            flex-direction: column;
        }

        #fullscreen-rotated-stage .modal-body {
            padding: 12px 14px;
            gap: 10px;
            max-height: none;
            flex: 1;
            overflow-y: auto;
        }

        #fullscreen-rotated-stage .preset-grid {
            grid-template-columns: repeat(4, 1fr);
            gap: 6px;
        }

        #fullscreen-rotated-stage .preset-btn {
            padding: 6px 8px;
        }

        #fullscreen-rotated-stage .modal-header,
        #fullscreen-rotated-stage .modal-footer {
            padding: 10px 14px;
        }

        .modal-card {
            background: #ffffff;
            border-radius: 18px;
            width: 100%;
            max-width: 520px;
            box-shadow: var(--shadow-xl);
            border: 1px solid var(--border-color);
            overflow: hidden;
            animation: modalPop 0.16s ease-out;
        }

        @keyframes modalPop {
            from { opacity: 0; transform: scale(0.96); }
            to   { opacity: 1; transform: scale(1); }
        }

        .modal-header {
            padding: 14px 18px;
            border-bottom: 1px solid var(--border-color);
            display: flex;
            align-items: center;
            justify-content: space-between;
            background: #f8fafc;
        }

        .modal-title {
            font-size: 0.98rem;
            font-weight: 800;
            color: var(--text-main);
        }

        .modal-subtitle {
            font-size: 0.75rem;
            color: var(--text-muted);
            margin-top: 2px;
        }

        .modal-close {
            width: 30px;
            height: 30px;
            border-radius: 8px;
            border: 1px solid var(--border-color);
            background: #ffffff;
            color: var(--text-secondary);
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
        }

        .modal-body {
            padding: 16px 18px;
            display: flex;
            flex-direction: column;
            gap: 14px;
            max-height: 75vh;
            overflow-y: auto;
        }

        .preset-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 8px;
        }

        .preset-btn {
            padding: 9px 10px;
            border-radius: 10px;
            border: 1px solid var(--border-color);
            background: #ffffff;
            text-align: left;
            cursor: pointer;
            transition: all 0.12s ease;
        }

        .preset-btn:hover {
            border-color: var(--indigo-600);
            background: var(--indigo-50);
        }

        .preset-btn strong {
            display: block;
            font-size: 0.78rem;
            color: var(--text-main);
        }

        .preset-btn span {
            font-size: 0.68rem;
            color: var(--text-muted);
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 4px;
        }

        .form-group label {
            font-size: 0.74rem;
            font-weight: 700;
            color: var(--text-secondary);
        }

        .form-input {
            padding: 8px 10px;
            border-radius: 10px;
            border: 1px solid var(--border-strong);
            font-size: 0.84rem;
            color: var(--text-main);
            outline: none;
        }

        .form-input:focus {
            border-color: var(--indigo-600);
            box-shadow: 0 0 0 3px rgba(79, 70, 229, 0.14);
        }

        .modal-footer {
            padding: 12px 18px;
            border-top: 1px solid var(--border-color);
            background: #f8fafc;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 8px;
        }

        .png-preview-box {
            background: #f1f5f9;
            border: 1px solid var(--border-strong);
            border-radius: 12px;
            padding: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 180px;
            max-height: 46vh;
            overflow: auto;
        }

        .png-preview-img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            box-shadow: var(--shadow-md);
            background: #ffffff;
        }

        .share-helper-note {
            background: var(--indigo-50);
            border: 1px solid var(--indigo-200);
            color: var(--indigo-700);
            border-radius: 10px;
            padding: 8px 12px;
            font-size: 0.75rem;
            font-weight: 600;
            line-height: 1.35;
        }

        #toast-container {
            position: fixed;
            bottom: 16px;
            right: 16px;
            z-index: 80;
            display: flex;
            flex-direction: column;
            gap: 8px;
            pointer-events: none;
            max-width: 360px;
        }

        #fullscreen-rotated-stage #toast-container {
            position: absolute;
            bottom: 12px;
            right: 12px;
            z-index: 90;
        }

        .toast-item {
            background: #0f172a;
            color: #ffffff;
            padding: 10px 14px;
            border-radius: 12px;
            font-size: 0.8rem;
            font-weight: 600;
            box-shadow: var(--shadow-md);
            animation: slideUp 0.2s ease-out;
        }

        @keyframes slideUp {
            from { opacity: 0; transform: translateY(10px); }
            to   { opacity: 1; transform: translateY(0); }
        }

        /* =====================================================================
           7. PRINT STYLES
           ===================================================================== */
        @media print {
            .app-header, .sub-toolbar, .emp-del-btn, #fullscreen-top-bar {
                display: none !important;
            }
            .main-workspace {
                margin: 0;
                padding: 0;
                max-width: none;
            }
            #fullscreen-rotated-stage {
                box-shadow: none;
                border: none;
            }
            .schedule-table tbody td.sticky-col,
            .schedule-table thead th.sticky-col,
            .schedule-table tfoot td.sticky-col {
                position: static;
                box-shadow: none;
            }
        }
    </style>
</head>
<body>
    <!-- TOP HEADER BAR -->
    <header class="app-header">
        <div class="header-inner">
            <button type="button" id="brand-trigger-btn" class="brand-trigger" title="Click pentru a deschide Programul de muncă rotit la 90° pe tot ecranul">
                <div class="brand-icon">
                    <svg width="28" height="28" viewBox="0 0 512 512" fill="none">
                        <g transform="rotate(-7 240 245)">
                            <rect x="75" y="95" width="290" height="265" rx="34" fill="#ffffff"/>
                            <path d="M75 129c0-19 15-34 34-34h222c19 0 34 15 34 34v42H75v-42z" fill="#93c5fd"/>
                            <rect x="135" y="68" width="24" height="52" rx="12" fill="#0f172a"/>
                            <rect x="280" y="68" width="24" height="52" rx="12" fill="#0f172a"/>
                            <rect x="175" y="245" width="44" height="40" rx="8" fill="#2563eb"/>
                            <path d="M186 265l8 8 16-16" stroke="#ffffff" stroke-width="7" stroke-linecap="round" stroke-linejoin="round"/>
                        </g>
                        <rect x="55" y="315" width="160" height="122" rx="22" fill="#ffffff" stroke="#1e3a8a" stroke-width="10"/>
                        <circle cx="355" cy="345" r="105" fill="#ffffff" stroke="#1e3a8a" stroke-width="18"/>
                        <path d="M325 320l30 27 44-40" stroke="#0f172a" stroke-width="16" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                </div>
                <div>
                    <div class="brand-title-row">
                        <h1 class="brand-title">Programul de muncă</h1>
                        <span class="year-badge">2026 &amp; 2027</span>
                    </div>
                    <p class="brand-subtitle">Click pe orice celulă pentru editare • Click pe titlu pentru ecran 90°</p>
                </div>
            </button>

            <!-- Year + Week Navigation + Language Switcher -->
            <div class="week-navigator">
                <button type="button" id="prev-week-btn" class="btn btn-icon" title="Săptămâna anterioară">
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                        <polyline points="15 18 9 12 15 6"></polyline>
                    </svg>
                </button>

                <select id="year-select" class="select-control" aria-label="Selectează anul">
                    <option value="2026" selected>2026</option>
                    <option value="2027">2027</option>
                </select>

                <select id="week-select" class="select-control" aria-label="Selectează săptămâna"></select>

                <button type="button" id="next-week-btn" class="btn btn-icon" title="Săptămâna următoare">
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                        <polyline points="9 18 15 12 9 6"></polyline>
                    </svg>
                </button>

                <button type="button" id="week-47-btn" class="btn btn-soft-indigo" title="Mergi la Săpt. 47 (16–22 Nov 2026)">
                    Săpt. 47
                </button>

                <select id="lang-select" class="select-control" aria-label="Selectează limba">
                    <option value="ro">🇷🇴 Română</option>
                    <option value="de">🇩🇪 Deutsch</option>
                    <option value="en">🇬🇧 English</option>
                    <option value="ru">🇷🇺 Русский</option>
                    <option value="tr">🇹🇷 Türkçe</option>
                    <option value="nl">🇳🇱 Nederlands</option>
                </select>
            </div>

            <!-- Action Buttons -->
            <div class="header-actions">
                <button type="button" id="save-changes-btn" class="btn btn-save" title="Salvează toate modificările făcute în tabel">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M19 21H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h11l5 5v11a2 2 0 0 1-2 2z"></path>
                        <polyline points="17 21 17 13 7 13 7 21"></polyline>
                        <polyline points="7 3 7 8 15 8"></polyline>
                    </svg>
                    <span>Salvează modificările</span>
                </button>

                <button type="button" id="add-emp-btn" class="btn btn-primary">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                        <line x1="12" y1="5" x2="12" y2="19"></line>
                        <line x1="5" y1="12" x2="19" y2="12"></line>
                    </svg>
                    <span>+ Angajat</span>
                </button>

                <button type="button" id="copy-prev-week-btn" class="btn" title="Copiază programul din săptămâna anterioară">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect>
                        <path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path>
                    </svg>
                    <span>Copiază Săpt. Ant.</span>
                </button>

                <button type="button" id="fullscreen-90-btn" class="btn btn-soft-indigo" title="Vizualizare rotită la 90° pe tot ecranul">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <polyline points="15 3 21 3 21 9"></polyline>
                        <polyline points="9 21 3 21 3 15"></polyline>
                        <line x1="21" y1="3" x2="14" y2="10"></line>
                        <line x1="3" y1="21" x2="10" y2="14"></line>
                    </svg>
                    <span>Ecran 90°</span>
                </button>

                <button type="button" id="print-btn" class="btn" title="Printează sau salvează PDF">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <polyline points="6 9 6 2 18 2 18 9"></polyline>
                        <path d="M6 18H4a2 2 0 0 1-2-2v-5a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v5a2 2 0 0 1-2 2h-2"></path>
                        <rect x="6" y="14" width="12" height="8"></rect>
                    </svg>
                    <span>Printează</span>
                </button>
            </div>
        </div>
    </header>

    <!-- LEGEND, SHARE ACTIONS & STATS BAR -->
    <section class="sub-toolbar">
        <div class="legend-list">
            <span class="legend-pill shift-work"><span class="legend-dot" style="background:#059669"></span><span id="legend-work-text">Program (ex. 07:00 / 08:00 / 10:00)</span></span>
            <span class="legend-pill shift-extra"><span class="legend-dot" style="background:#d97706"></span><span id="legend-extra-text">Extra</span></span>
            <span class="legend-pill shift-vrij"><span class="legend-dot" style="background:#64748b"></span><span id="legend-vrij-text">Liber</span></span>
            <span class="legend-pill shift-vakantie"><span class="legend-dot" style="background:#e11d48"></span><span id="legend-vakantie-text">Vacanță</span></span>
        </div>

        <div class="right-toolbar-group">
            <div class="share-group">
                <button type="button" id="share-wa-btn" class="btn btn-whatsapp" title="Trimite săptămâna și imaginea tabelului pe WhatsApp">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.38 8.38 0 0 1-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.38 8.38 0 0 1 3.8-.9h.5a8.48 8.48 0 0 1 8 8v.5z"></path>
                    </svg>
                    <span>WhatsApp</span>
                </button>

                <button type="button" id="share-email-btn" class="btn btn-email" title="Trimite săptămâna și imaginea tabelului pe Email">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path>
                        <polyline points="22,6 12,13 2,6"></polyline>
                    </svg>
                    <span>Email</span>
                </button>

                <button type="button" id="copy-text-btn" class="btn" title="Copiază săptămâna curentă">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect>
                        <path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path>
                    </svg>
                    <span>Copiază Text</span>
                </button>
            </div>

            <div class="stats-bar">
                <span>Angajați: <strong id="stat-emp-count">0</strong></span>
                <span>•</span>
                <span>Zile lucrate / săpt.: <strong id="stat-total-days">0 zile</strong></span>
            </div>
        </div>
    </section>

    <!-- MAIN SCHEDULE WORKSPACE -->
    <main class="main-workspace">
        <div id="fullscreen-overlay-shell">
            <div id="fullscreen-rotated-stage">
                <div id="fullscreen-top-bar">
                    <div class="fs-title-group">
                        <span>Programul de muncă</span>
                        <span id="fs-week-label" style="color:#a5b4fc; font-weight:600;"></span>
                    </div>
                    <div class="fs-actions-group">
                        <button type="button" id="fs-save-btn" class="fs-btn fs-btn-save">💾 Salvează</button>
                        <button type="button" id="fs-wa-btn" class="fs-btn fs-btn-wa">WhatsApp</button>
                        <button type="button" id="fs-mail-btn" class="fs-btn fs-btn-mail">Email</button>
                        <button type="button" id="fs-prev-btn" class="fs-btn">◀ Săpt. ant.</button>
                        <button type="button" id="fs-next-btn" class="fs-btn">Săpt. urm. ▶</button>
                        <button type="button" id="fs-rotate-btn" class="fs-btn">↻ Rotește ±90°</button>
                        <button type="button" id="fs-exit-btn" class="fs-btn fs-btn-exit">✕ Ieșire (ESC)</button>
                    </div>
                </div>

                <div id="table-scroll-wrapper">
                    <table class="schedule-table">
                        <colgroup>
                            <col class="col-employee">
                            <col class="col-day">
                            <col class="col-day">
                            <col class="col-day">
                            <col class="col-day">
                            <col class="col-day">
                            <col class="col-day">
                            <col class="col-day">
                            <col class="col-days-cnt">
                        </colgroup>
                        <thead>
                            <tr id="table-head-row"></tr>
                        </thead>
                        <tbody id="table-body"></tbody>
                        <tfoot>
                            <tr id="table-foot-row"></tr>
                        </tfoot>
                    </table>
                </div>
            </div>
        </div>
    </main>

    <!-- MODAL 1: DAILY SHIFT / STATUS EDITOR -->
    <div id="shift-modal" class="modal-backdrop">
        <div class="modal-card">
            <div class="modal-header">
                <div>
                    <div class="modal-title" id="shift-modal-title">Setare Program Zilnic</div>
                    <div class="modal-subtitle" id="shift-modal-subtitle">Angajat • Ziua</div>
                </div>
                <button type="button" id="close-shift-modal-btn" class="modal-close" aria-label="Închide">✕</button>
            </div>

            <div class="modal-body">
                <div>
                    <div id="quick-presets-label" style="font-size:0.74rem; font-weight:700; color:var(--text-secondary); margin-bottom:6px;">
                        Alege rapid ora de începere sau statusul zilei:
                    </div>
                    <div class="preset-grid">
                        <button type="button" class="preset-btn" data-preset-type="work" data-preset-label="07:00" data-preset-extra="0">
                            <strong>07:00</strong>
                            <span>Zi lucrătoare</span>
                        </button>
                        <button type="button" class="preset-btn" data-preset-type="work" data-preset-label="08:00" data-preset-extra="0">
                            <strong>08:00</strong>
                            <span>Zi lucrătoare</span>
                        </button>
                        <button type="button" class="preset-btn" data-preset-type="work" data-preset-label="09:00" data-preset-extra="0">
                            <strong>09:00</strong>
                            <span>Zi lucrătoare</span>
                        </button>
                        <button type="button" class="preset-btn" data-preset-type="work" data-preset-label="10:00" data-preset-extra="0">
                            <strong>10:00</strong>
                            <span>Zi lucrătoare</span>
                        </button>
                        <button type="button" class="preset-btn" data-preset-type="extra" data-preset-label="07:00" data-preset-extra="1">
                            <strong>07:00 • Extra</strong>
                            <span>Zi lucrătoare suplimentară</span>
                        </button>
                        <button type="button" class="preset-btn" data-preset-type="extra" data-preset-label="08:00" data-preset-extra="1">
                            <strong>08:00 • Extra</strong>
                            <span>Zi lucrătoare suplimentară</span>
                        </button>
                        <button type="button" class="preset-btn" data-preset-type="vrij" data-preset-label="__VRIJ__" data-preset-extra="0">
                            <strong>Liber</strong>
                            <span>Zi liberă (nu se numără ca zi lucrată)</span>
                        </button>
                        <button type="button" class="preset-btn" data-preset-type="vakantie" data-preset-label="__VAKANTIE__" data-preset-extra="0">
                            <strong>Vacanță</strong>
                            <span>Concediu (nu se numără ca zi lucrată)</span>
                        </button>
                    </div>
                </div>

                <hr style="border:none; border-top:1px solid var(--border-color);">

                <div class="form-row">
                    <div class="form-group">
                        <label for="custom-label">Oră început sau status</label>
                        <input type="text" id="custom-label" class="form-input" placeholder="Ex: 07:00, 08:00, 10:00, Liber, Vacanță">
                    </div>
                    <div class="form-group">
                        <label for="custom-status-type">Tip zi</label>
                        <select id="custom-status-type" class="form-input">
                            <option value="work">Zi lucrătoare</option>
                            <option value="extra">Extra (suplimentar)</option>
                            <option value="vrij">Liber</option>
                            <option value="vakantie">Vacanță</option>
                        </select>
                    </div>
                </div>

                <div class="form-group">
                    <label for="custom-note">Mențiune opțională (ex: Extra, Grup A)</label>
                    <input type="text" id="custom-note" class="form-input" placeholder="Ex: Extra">
                </div>
            </div>

            <div class="modal-footer">
                <div style="display:flex; flex-wrap:wrap; gap:6px;">
                    <button type="button" id="clear-cell-btn" class="btn btn-danger-soft">Șterge</button>
                    <button type="button" id="add-extra-day-btn" class="btn btn-soft-amber">+ Adaugă zi Extra</button>
                    <button type="button" id="apply-mon-fri-btn" class="btn btn-soft-indigo">Aplică L–V</button>
                    <button type="button" id="reset-group-week-btn" class="btn" style="display:none;">Reaplică program grupă</button>
                </div>
                <div style="display:flex; flex-wrap:wrap; gap:6px;">
                    <button type="button" id="cancel-shift-btn" class="btn">Anulează</button>
                    <button type="button" id="save-shift-btn" class="btn btn-primary">Salvează</button>
                </div>
            </div>
        </div>
    </div>

    <!-- MODAL 2: ADD EMPLOYEE -->
    <div id="emp-modal" class="modal-backdrop">
        <div class="modal-card" style="max-width:400px;">
            <div class="modal-header">
                <div>
                    <div class="modal-title" id="add-emp-title">Adaugă Angajat Nou</div>
                    <div class="modal-subtitle" id="add-emp-subtitle">Va apărea imediat în tabelul săptămânal</div>
                </div>
                <button type="button" id="close-emp-modal-btn" class="modal-close" aria-label="Închide">✕</button>
            </div>
            <form id="add-emp-form">
                <div class="modal-body">
                    <div class="form-group">
                        <label for="new-emp-name">Nume și Prenume *</label>
                        <input type="text" id="new-emp-name" class="form-input" placeholder="Ex: Popescu Andrei" required>
                    </div>
                    <div class="form-group">
                        <label for="new-emp-role">Funcție / Grup (opțional)</label>
                        <input type="text" id="new-emp-role" class="form-input" placeholder="Ex: Grup A, Grup B, Grup C...">
                    </div>
                </div>
                <div class="modal-footer" style="justify-content:flex-end;">
                    <button type="button" id="cancel-emp-btn" class="btn">Anulează</button>
                    <button type="submit" id="submit-emp-btn" class="btn btn-primary">Adaugă în program</button>
                </div>
            </form>
        </div>
    </div>

    <!-- MODAL 3: PNG TABLE PREVIEW & SHARE -->
    <div id="share-image-modal" class="modal-backdrop">
        <div class="modal-card" style="max-width: 680px;">
            <div class="modal-header">
                <div>
                    <div class="modal-title" id="share-image-modal-title">Imagine Tabel Program (.PNG)</div>
                    <div class="modal-subtitle" id="share-image-modal-subtitle">Săpt. 47 (16 Nov – 22 Nov 2026) • Imagine PNG gata de trimis</div>
                </div>
                <button type="button" id="close-share-modal-btn" class="modal-close" aria-label="Închide">✕</button>
            </div>

            <div class="modal-body">
                <div class="share-helper-note" id="share-image-helper-text">
                    Se trimite săptămâna selectată împreună cu imaginea PNG a tabelului.
                </div>

                <div class="png-preview-box" id="png-preview-container">
                    <span style="font-size:0.8rem; color:var(--text-muted); font-weight:600;">Se generează imaginea tabelului...</span>
                </div>
            </div>

            <div class="modal-footer">
                <div style="display:flex; flex-wrap:wrap; gap:6px;">
                    <button type="button" id="download-png-btn" class="btn btn-soft-indigo">⬇ Descarcă PNG</button>
                    <button type="button" id="copy-png-btn" class="btn">📋 Copiază Imagine</button>
                    <button type="button" id="modal-copy-text-btn" class="btn">📄 Copiază Săptămâna</button>
                </div>
                <div style="display:flex; flex-wrap:wrap; gap:6px;">
                    <button type="button" id="modal-wa-text-btn" class="btn btn-whatsapp">WhatsApp (Săptămâna)</button>
                    <button type="button" id="modal-wa-image-btn" class="btn btn-whatsapp">WhatsApp (Imagine)</button>
                    <button type="button" id="modal-mail-image-btn" class="btn btn-email">Email</button>
                    <button type="button" id="close-share-footer-btn" class="btn">Închide</button>
                </div>
            </div>
        </div>
    </div>

    <!-- TOAST CONTAINER -->
    <div id="toast-container"></div>

    <script>
        /* =====================================================================
           1. MULTI-LAYER PERSISTENT STORAGE (LOCALSTORAGE + INDEXEDDB + WINDOW.NAME)
           ===================================================================== */
        const STORAGE_KEY = 'planificator_program_o_tura_2026_2027_v6';
        const LANG_STORAGE_KEY = 'planificator_program_lang_2026_2027_v1';
        const META_STORAGE_KEY = 'planificator_program_meta_2026_2027_v1';
        const IDB_DB_NAME = 'PlanificatorProgramDB_2026_2027';
        const IDB_STORE_NAME = 'kv_store';
        const WINDOW_NAME_PREFIX = 'PLANIFICATOR_PERSIST_V1::';

        const memoryStore = new Map();
        let idbReadyPromise = null;

        function getIndexedDB() {
            if (!idbReadyPromise) {
                idbReadyPromise = new Promise((resolve) => {
                    try {
                        const indexedDBRef = window.indexedDB || window.mozIndexedDB || window.webkitIndexedDB || window.msIndexedDB;
                        if (!indexedDBRef) {
                            resolve(null);
                            return;
                        }
                        const request = indexedDBRef.open(IDB_DB_NAME, 1);
                        request.onupgradeneeded = (event) => {
                            const db = event.target.result;
                            if (!db.objectStoreNames.contains(IDB_STORE_NAME)) {
                                db.createObjectStore(IDB_STORE_NAME);
                            }
                        };
                        request.onsuccess = (event) => resolve(event.target.result);
                        request.onerror = () => resolve(null);
                    } catch (err) {
                        resolve(null);
                    }
                });
            }
            return idbReadyPromise;
        }

        function readWindowNameMap() {
            try {
                if (typeof window.name === 'string' && window.name.startsWith(WINDOW_NAME_PREFIX)) {
                    const parsed = JSON.parse(window.name.slice(WINDOW_NAME_PREFIX.length));
                    if (parsed && typeof parsed === 'object') {
                        return parsed;
                    }
                }
            } catch (err) {
                // Ignore malformed window.name
            }
            return {};
        }

        function writeWindowNameEntry(key, val) {
            try {
                const map = readWindowNameMap();
                map[key] = val;
                const serialized = WINDOW_NAME_PREFIX + JSON.stringify(map);
                if (serialized.length < 1800000) {
                    window.name = serialized;
                }
            } catch (err) {
                // Ignore window.name quota errors
            }
        }

        function writeToIndexedDB(key, val) {
            getIndexedDB().then((db) => {
                if (!db) return;
                try {
                    const tx = db.transaction(IDB_STORE_NAME, 'readwrite');
                    const store = tx.objectStore(IDB_STORE_NAME);
                    store.put(val, key);
                } catch (err) {
                    // Ignore IDB write error
                }
            });
        }

        function safeGetStorage(key) {
            let lsVal = null;
            try {
                lsVal = window.localStorage.getItem(key);
            } catch (err) {
                lsVal = null;
            }

            if (lsVal !== null && lsVal !== undefined) {
                memoryStore.set(key, lsVal);
                writeWindowNameEntry(key, lsVal);
                return lsVal;
            }

            const wnMap = readWindowNameMap();
            if (Object.prototype.hasOwnProperty.call(wnMap, key) && wnMap[key] !== null && wnMap[key] !== undefined) {
                const wnVal = String(wnMap[key]);
                memoryStore.set(key, wnVal);
                try {
                    window.localStorage.setItem(key, wnVal);
                } catch (err) {}
                return wnVal;
            }

            if (memoryStore.has(key)) {
                return memoryStore.get(key);
            }

            return null;
        }

        function safeSetStorage(key, val) {
            const strVal = String(val);
            memoryStore.set(key, strVal);
            writeWindowNameEntry(key, strVal);
            writeToIndexedDB(key, strVal);

            try {
                window.localStorage.setItem(key, strVal);
            } catch (err) {
                // Fallback layers (IndexedDB + window.name + memory) remain active
            }
        }

        async function hydrateFromIndexedDBIfNeeded(onHydrated) {
            const db = await getIndexedDB();
            if (!db) return;

            const keys = [STORAGE_KEY, LANG_STORAGE_KEY, META_STORAGE_KEY];
            let updatedAny = false;

            await Promise.all(keys.map((key) => new Promise((resolve) => {
                try {
                    const tx = db.transaction(IDB_STORE_NAME, 'readonly');
                    const store = tx.objectStore(IDB_STORE_NAME);
                    const req = store.get(key);
                    req.onsuccess = () => {
                        const idbVal = req.result;
                        if (typeof idbVal === 'string' && idbVal.length > 0) {
                            const currentVal = safeGetStorage(key);
                            if (currentVal !== idbVal) {
                                memoryStore.set(key, idbVal);
                                writeWindowNameEntry(key, idbVal);
                                try {
                                    window.localStorage.setItem(key, idbVal);
                                } catch (err) {}
                                updatedAny = true;
                            }
                        }
                        resolve();
                    };
                    req.onerror = () => resolve();
                } catch (err) {
                    resolve();
                }
            })));

            if (updatedAny && typeof onHydrated === 'function') {
                onHydrated();
            }
        }

        /* =====================================================================
           2. MULTI-LANGUAGE DICTIONARY (RO, DE, EN, RU, TR, NL)
           ===================================================================== */
        const TRANSLATIONS = {
            ro: {
                pageTitle: 'Programul de muncă (2026 & 2027)',
                brandTitle: 'Programul de muncă',
                brandSubtitle: 'Click pe orice celulă pentru editare • Click pe titlu pentru ecran 90°',
                brandTooltip: 'Click pentru a deschide Programul de muncă rotit la 90° pe tot ecranul',
                prevWeekTitle: 'Săptămâna anterioară',
                nextWeekTitle: 'Săptămâna următoare',
                yearAria: 'Selectează anul',
                weekAria: 'Selectează săptămâna',
                langAria: 'Selectează limba',
                weekPrefix: 'Săpt.',
                week47Btn: 'Săpt. 47',
                week47Title: 'Mergi la Săpt. 47 (16–22 Nov 2026)',
                saveChangesBtn: 'Salvează modificările',
                saveChangesPending: 'Salvează modificările •',
                saveChangesTitle: 'Salvează toate modificările făcute în tabel',
                addEmployeeBtn: '+ Angajat',
                copyPrevWeekBtn: 'Copiază Săpt. Ant.',
                copyPrevWeekTitle: 'Copiază programul din săptămâna anterioară',
                fullscreen90Btn: 'Ecran 90°',
                fullscreen90Title: 'Vizualizare rotită la 90° pe tot ecranul',
                printBtn: 'Printează',
                printTitle: 'Printează sau salvează PDF',
                legendWork: 'Program (ex. 07:00 / 08:00 / 10:00)',
                legendExtra: 'Extra',
                legendVrij: 'Liber',
                legendVakantie: 'Vacanță',
                whatsappBtn: 'WhatsApp',
                whatsappTitle: 'Trimite săptămâna și imaginea tabelului pe WhatsApp',
                emailBtn: 'Email',
                emailTitle: 'Trimite săptămâna și imaginea tabelului pe Email',
                copyTextBtn: 'Copiază Text',
                copyTextTitle: 'Copiază săptămâna curentă',
                statsEmployees: 'Angajați:',
                statsWorkedDays: 'Zile lucrate / săpt.:',
                daySingular: 'zi',
                dayPlural: 'zile',
                fsSave: '💾 Salvează',
                fsPrevWeek: '◀ Săpt. ant.',
                fsNextWeek: 'Săpt. urm. ▶',
                fsRotate: '↻ Rotește ±90°',
                fsExit: '✕ Ieșire (ESC)',
                colEmployee: 'Angajat',
                colEmployeeDetails: 'ANGAJAT & DETALII',
                colDays: 'Zile',
                colDaysUpper: 'ZILE',
                presentPerDay: 'Prezenți / zi',
                noEmployeesTable: 'Nu există angajați adăugați. Apasă pe butonul <strong>+ Angajat</strong> pentru a începe.',
                noEmployeesCanvas: 'Nu există angajați adăugați pentru această săptămână.',
                removeEmployeeTitle: 'Elimină angajatul',
                setCellTitle: 'Click pentru a seta programul',
                days: ['Luni', 'Marți', 'Miercuri', 'Joi', 'Vineri', 'Sâmbătă', 'Duminică'],
                daysShort: ['Lu', 'Ma', 'Mi', 'Jo', 'Vi', 'Sâ', 'Du'],
                monthsShort: ['Ian', 'Feb', 'Mar', 'Apr', 'Mai', 'Iun', 'Iul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
                shiftModalTitleDay: 'Program • {day}',
                shiftModalSubtitle: '{name} ({date} {year})',
                closeModalAria: 'Închide',
                quickPresetsLabel: 'Alege rapid ora de începere sau statusul zilei:',
                presetWorkDesc: 'Zi lucrătoare',
                presetExtraTitle: '{time} • Extra',
                presetExtraDesc: 'Zi lucrătoare suplimentară',
                statusVrijLabel: 'Liber',
                presetVrijDesc: 'Zi liberă (nu se numără ca zi lucrată)',
                statusVakantieLabel: 'Vacanță',
                presetVakantieDesc: 'Concediu (nu se numără ca zi lucrată)',
                customLabelField: 'Oră început sau status',
                customLabelPlaceholder: 'Ex: 07:00, 08:00, 10:00, Liber, Vacanță',
                customTypeField: 'Tip zi',
                typeWorkOption: 'Zi lucrătoare',
                typeExtraOption: 'Extra (suplimentar)',
                typeVrijOption: 'Liber',
                typeVakantieOption: 'Vacanță',
                customNoteField: 'Mențiune opțională (ex: Extra, Grup A)',
                customNotePlaceholder: 'Ex: Extra',
                deleteCellBtn: 'Șterge',
                addExtraDayBtn: '+ Adaugă zi Extra',
                resetGroupWeekBtn: 'Reaplică program grupă',
                applyMonFriBtn: 'Aplică L–V',
                cancelBtn: 'Anulează',
                saveBtn: 'Salvează',
                addEmpModalTitle: 'Adaugă Angajat Nou',
                addEmpModalSubtitle: 'Va apărea imediat în tabelul săptămânal',
                empNameLabel: 'Nume și Prenume *',
                empNamePlaceholder: 'Ex: Popescu Andrei',
                empRoleLabel: 'Funcție / Grup (opțional)',
                empRolePlaceholder: 'Ex: Grup A, Grup B, Grup C...',
                empDefaultRole: 'Angajat',
                addEmpSubmitBtn: 'Adaugă în program',
                shareModalTitle: 'Trimite Săptămâna & Imaginea (.PNG)',
                shareModalSubtitle: 'Săpt. {week} ({range}) • Imagine PNG gata de trimis',
                shareError: 'Nu s-a putut genera imaginea PNG a tabelului.',
                shareHelperNative: 'Se trimite săptămâna selectată și imaginea PNG a tabelului prin WhatsApp sau Email.',
                shareHelperFallback: 'Se trimite săptămâna selectată și imaginea PNG a tabelului.',
                downloadPngBtn: '⬇ Descarcă PNG',
                copyImageBtn: '📋 Copiază Imagine',
                copyTextModalBtn: '📄 Copiază Săptămâna',
                waTextBtn: 'WhatsApp (Săptămâna)',
                waImageBtn: 'WhatsApp (Imagine)',
                mailImageBtn: 'Email',
                closeBtn: 'Închide',
                canvasBannerTitle: 'PROGRAMUL DE MUNCĂ • SĂPTĂMÂNA {week} ({range})',
                canvasBannerStats: 'Angajați: {count}   •   Total zile lucrate: {days} zile',
                canvasLegendWork: 'Program (ex. 07:00 / 08:00 / 10:00)',
                canvasLegendExtra: 'Extra',
                canvasLegendVrij: 'Liber',
                canvasLegendVakantie: 'Vacanță',
                shareTextTitle: 'PROGRAMUL DE MUNCĂ - Săpt. {week} ({range})',
                shareTextDaysLine: 'Zile: {daysLine}',
                shareTextNoEmp: 'Nu există angajați în program pentru această săptămână.',
                shareTextEmpLine: '{idx}. {name}{role} — {days} {dayWord}',
                shareTextPresentLine: 'Prezenți / zi: {presentLine}',
                shareTextTotalLine: 'Total zile lucrate în săptămână: {days} zile ({count} angajați)',
                shareAttachNote: '{title}',
                shareMailBody: '{title}',
                toastFirstWeek2026: 'Ai ajuns la prima săptămână din 2026.',
                toastLastWeek2027: 'Ai ajuns la ultima săptămână din 2027.',
                toastWeek47: 'Afișat Săpt. 47 (16 – 22 Noiembrie 2026).',
                toastChangesSaved: 'Toate modificările au fost salvate.',
                toastShiftSaved: 'Programul zilei a fost actualizat. Apasă „Salvează modificările” pentru confirmare.',
                toastExtraDayAdded: 'Zi Extra adăugată pentru {day}. Apasă „Salvează modificările” pentru a salva.',
                toastGroupReapplied: 'Programul grupei a fost reaplicat pe această săptămână.',
                toastAppliedMonFri: 'Program aplicat pentru Luni – Vineri.',
                toastCellCleared: 'Celula a fost golită.',
                toastEmpAdded: 'Angajatul {name} a fost adăugat.',
                toastEmpRemoved: 'Angajatul a fost eliminat din listă.',
                toastNoPrevWeek: 'Nu există o săptămână anterioară disponibilă.',
                toastPrevWeekEmpty: 'Săptămâna {week} nu are ture salvate.',
                toastWeekCopied: 'Programul din Săpt. {week} a fost copiat.',
                toastTextCopied: 'Săptămâna curentă a fost copiată.',
                toastTextCopyFail: 'Nu s-a putut copia automat; poți folosi butoanele WhatsApp sau Email.',
                toastPngNotReady: 'Imaginea PNG nu a putut fi pregătită.',
                toastPngDownloaded: 'Imaginea {filename} a fost descărcată.',
                toastPngOpenFail: 'Deschide imaginea din previzualizare pentru a o salva.',
                toastNoPng: 'Nu există o imagine PNG generată.',
                toastImgCopied: 'Imaginea tabelului a fost copiată în clipboard! O poți lipi direct în WhatsApp sau Email.',
                toastImgCopyFallback: 'Browserul nu permite copierea directă a imaginii; PNG-ul a fost descărcat pentru atașare.',
                toastNoPngGen: 'Nu s-a putut genera imaginea PNG.',
                toastSharedWa: 'Săptămâna și imaginea PNG au fost trimise către WhatsApp.',
                toastSharedMail: 'Săptămâna și imaginea PNG au fost trimise către Email.',
                toastShareCancelled: 'Partajarea a fost anulată.',
                toastOpenedWa: 'Săptămâna și imaginea PNG au fost pregătite pentru WhatsApp.',
                toastOpenedWaText: 'Săptămâna a fost trimisă către WhatsApp.',
                toastOpenedMail: 'Săptămâna a fost trimisă către Email.',
                toastFsActive: 'Ecran complet 90° activat • Apasă Înapoi pentru pagina principală.'
            },
            de: {
                pageTitle: 'Arbeitsplan & Schichten (2026 & 2027)',
                brandTitle: 'Arbeitsplan',
                brandSubtitle: 'Auf eine Zelle klicken zum Bearbeiten • Auf Titel klicken für 90°-Ansicht',
                brandTooltip: 'Klicken, um den Arbeitsplan um 90° gedreht im Vollbild zu öffnen',
                prevWeekTitle: 'Vorherige Woche',
                nextWeekTitle: 'Nächste Woche',
                yearAria: 'Jahr auswählen',
                weekAria: 'Woche auswählen',
                langAria: 'Sprache auswählen',
                weekPrefix: 'KW',
                week47Btn: 'KW 47',
                week47Title: 'Zu KW 47 wechseln (16.–22. Nov 2026)',
                saveChangesBtn: 'Änderungen speichern',
                saveChangesPending: 'Änderungen speichern •',
                saveChangesTitle: 'Alle Änderungen in der Tabelle speichern',
                addEmployeeBtn: '+ Mitarbeiter',
                copyPrevWeekBtn: 'Vorwoche kopieren',
                copyPrevWeekTitle: 'Plan der vorherigen Woche kopieren',
                fullscreen90Btn: 'Vollbild 90°',
                fullscreen90Title: 'Um 90° gedrehte Vollbildansicht',
                printBtn: 'Drucken',
                printTitle: 'Drucken oder als PDF speichern',
                legendWork: 'Arbeitszeit (z. B. 07:00 / 08:00 / 10:00)',
                legendExtra: 'Extra',
                legendVrij: 'Frei',
                legendVakantie: 'Urlaub',
                whatsappBtn: 'WhatsApp',
                whatsappTitle: 'Woche und Tabellenbild über WhatsApp teilen',
                emailBtn: 'E-Mail',
                emailTitle: 'Woche und Tabellenbild per E-Mail senden',
                copyTextBtn: 'Text kopieren',
                copyTextTitle: 'Aktuelle Woche kopieren',
                statsEmployees: 'Mitarbeiter:',
                statsWorkedDays: 'Arbeitstage / Wo.:',
                daySingular: 'Tag',
                dayPlural: 'Tage',
                fsSave: '💾 Speichern',
                fsPrevWeek: '◀ Vorwoche',
                fsNextWeek: 'Nächste Wo. ▶',
                fsRotate: '↻ Drehen ±90°',
                fsExit: '✕ Beenden (ESC)',
                colEmployee: 'Mitarbeiter',
                colEmployeeDetails: 'MITARBEITER & DETAILS',
                colDays: 'Tage',
                colDaysUpper: 'TAGE',
                presentPerDay: 'Anwesend / Tag',
                noEmployeesTable: 'Keine Mitarbeiter vorhanden. Klicken Sie auf <strong>+ Mitarbeiter</strong>, um zu starten.',
                noEmployeesCanvas: 'Für diese Woche sind keine Mitarbeiter eingetragen.',
                removeEmployeeTitle: 'Mitarbeiter entfernen',
                setCellTitle: 'Klicken, um Arbeitszeit festzulegen',
                days: ['Montag', 'Dienstag', 'Mittwoch', 'Donnerstag', 'Freitag', 'Samstag', 'Sonntag'],
                daysShort: ['Mo', 'Di', 'Mi', 'Do', 'Fr', 'Sa', 'So'],
                monthsShort: ['Jan', 'Feb', 'Mär', 'Apr', 'Mai', 'Jun', 'Jul', 'Aug', 'Sep', 'Okt', 'Nov', 'Dez'],
                shiftModalTitleDay: 'Plan • {day}',
                shiftModalSubtitle: '{name} ({date} {year})',
                closeModalAria: 'Schließen',
                quickPresetsLabel: 'Startzeit oder Status schnell wählen:',
                presetWorkDesc: 'Arbeitstag',
                presetExtraTitle: '{time} • Extra',
                presetExtraDesc: 'Zusätzlicher Arbeitstag',
                statusVrijLabel: 'Frei',
                presetVrijDesc: 'Freier Tag (zählt nicht als Arbeitstag)',
                statusVakantieLabel: 'Urlaub',
                presetVakantieDesc: 'Urlaub (zählt nicht als Arbeitstag)',
                customLabelField: 'Startzeit oder Status',
                customLabelPlaceholder: 'Z. B. 07:00, 08:00, 10:00, Frei, Urlaub',
                customTypeField: 'Tagestyp',
                typeWorkOption: 'Arbeitstag',
                typeExtraOption: 'Extra (zusätzlich)',
                typeVrijOption: 'Frei',
                typeVakantieOption: 'Urlaub',
                customNoteField: 'Optionale Notiz (z. B. Extra, Gruppe A)',
                customNotePlaceholder: 'Z. B. Extra',
                deleteCellBtn: 'Löschen',
                addExtraDayBtn: '+ Extra-Tag hinzufügen',
                resetGroupWeekBtn: 'Gruppenplan anwenden',
                applyMonFriBtn: 'Mo–Fr anwenden',
                cancelBtn: 'Abbrechen',
                saveBtn: 'Speichern',
                addEmpModalTitle: 'Neuen Mitarbeiter hinzufügen',
                addEmpModalSubtitle: 'Erscheint sofort im Wochenplan',
                empNameLabel: 'Vor- und Nachname *',
                empNamePlaceholder: 'Z. B. Max Mustermann',
                empRoleLabel: 'Funktion / Gruppe (optional)',
                empRolePlaceholder: 'Z. B. Gruppe A, Gruppe B...',
                empDefaultRole: 'Mitarbeiter',
                addEmpSubmitBtn: 'Zum Plan hinzufügen',
                shareModalTitle: 'Woche & Tabellenbild senden (.PNG)',
                shareModalSubtitle: 'KW {week} ({range}) • Bereit zum Teilen',
                shareError: 'Das PNG-Bild der Tabelle konnte nicht erstellt werden.',
                shareHelperNative: 'Die ausgewählte Woche und das PNG-Tabellenbild werden über WhatsApp oder E-Mail gesendet.',
                shareHelperFallback: 'Die ausgewählte Woche und das PNG-Tabellenbild werden gesendet.',
                downloadPngBtn: '⬇ PNG herunterladen',
                copyImageBtn: '📋 Bild kopieren',
                copyTextModalBtn: '📄 Woche kopieren',
                waTextBtn: 'WhatsApp (Woche)',
                waImageBtn: 'WhatsApp (Bild)',
                mailImageBtn: 'E-Mail',
                closeBtn: 'Schließen',
                canvasBannerTitle: 'ARBEITSPLAN • KALENDERWOCHE {week} ({range})',
                canvasBannerStats: 'Mitarbeiter: {count}   •   Arbeitstage gesamt: {days} Tage',
                canvasLegendWork: 'Arbeitszeit (z. B. 07:00 / 08:00 / 10:00)',
                canvasLegendExtra: 'Extra',
                canvasLegendVrij: 'Frei',
                canvasLegendVakantie: 'Urlaub',
                shareTextTitle: 'ARBEITSPLAN - KW {week} ({range})',
                shareTextDaysLine: 'Tage: {daysLine}',
                shareTextNoEmp: 'Keine Mitarbeiter für diese Woche eingetragen.',
                shareTextEmpLine: '{idx}. {name}{role} — {days} {dayWord}',
                shareTextPresentLine: 'Anwesend / Tag: {presentLine}',
                shareTextTotalLine: 'Arbeitstage gesamt in der Woche: {days} Tage ({count} Mitarbeiter)',
                shareAttachNote: '{title}',
                shareMailBody: '{title}',
                toastFirstWeek2026: 'Erste Woche von 2026 erreicht.',
                toastLastWeek2027: 'Letzte Woche von 2027 erreicht.',
                toastWeek47: 'KW 47 angezeigt (16.–22. November 2026).',
                toastChangesSaved: 'Alle Änderungen wurden gespeichert.',
                toastShiftSaved: 'Tagesplan aktualisiert. Klicken Sie auf „Änderungen speichern“ zur Bestätigung.',
                toastExtraDayAdded: 'Extra-Tag für {day} hinzugefügt.',
                toastGroupReapplied: 'Gruppenplan für diese Woche erneut angewendet.',
                toastAppliedMonFri: 'Plan auf Montag–Freitag angewendet.',
                toastCellCleared: 'Zelle geleert.',
                toastEmpAdded: 'Mitarbeiter {name} hinzugefügt.',
                toastEmpRemoved: 'Mitarbeiter aus der Liste entfernt.',
                toastNoPrevWeek: 'Keine vorherige Woche verfügbar.',
                toastPrevWeekEmpty: 'In KW {week} sind keine Einträge gespeichert.',
                toastWeekCopied: 'Plan aus KW {week} kopiert.',
                toastTextCopied: 'Aktuelle Woche kopiert.',
                toastTextCopyFail: 'Automatisches Kopieren nicht möglich; bitte WhatsApp oder E-Mail nutzen.',
                toastPngNotReady: 'PNG-Bild konnte nicht vorbereitet werden.',
                toastPngDownloaded: 'Bild {filename} heruntergeladen.',
                toastPngOpenFail: 'Öffnen Sie das Bild in der Vorschau, um es zu speichern.',
                toastNoPng: 'Kein PNG-Bild vorhanden.',
                toastImgCopied: 'Tabellenbild in die Zwischenablage kopiert!',
                toastImgCopyFallback: 'PNG wurde zum Anhängen heruntergeladen.',
                toastNoPngGen: 'PNG-Bild konnte nicht erzeugt werden.',
                toastSharedWa: 'Woche und PNG-Bild an WhatsApp gesendet.',
                toastSharedMail: 'Woche und PNG-Bild an E-Mail gesendet.',
                toastShareCancelled: 'Teilen abgebrochen.',
                toastOpenedWa: 'Woche und PNG-Bild für WhatsApp vorbereitet.',
                toastOpenedWaText: 'Woche an WhatsApp gesendet.',
                toastOpenedMail: 'Woche an E-Mail gesendet.',
                toastFsActive: '90°-Vollbild aktiv • Zurück drücken für Hauptansicht.'
            },
            en: {
                pageTitle: 'Work Schedule & Shifts (2026 & 2027)',
                brandTitle: 'Work Schedule',
                brandSubtitle: 'Click any cell to edit • Click title for 90° fullscreen',
                brandTooltip: 'Click to open Work Schedule rotated 90° in fullscreen',
                prevWeekTitle: 'Previous week',
                nextWeekTitle: 'Next week',
                yearAria: 'Select year',
                weekAria: 'Select week',
                langAria: 'Select language',
                weekPrefix: 'Week',
                week47Btn: 'Week 47',
                week47Title: 'Go to Week 47 (16–22 Nov 2026)',
                saveChangesBtn: 'Save changes',
                saveChangesPending: 'Save changes •',
                saveChangesTitle: 'Save all changes made in the table',
                addEmployeeBtn: '+ Employee',
                copyPrevWeekBtn: 'Copy Prev. Week',
                copyPrevWeekTitle: 'Copy schedule from previous week',
                fullscreen90Btn: '90° Screen',
                fullscreen90Title: '90° rotated fullscreen view',
                printBtn: 'Print',
                printTitle: 'Print or save as PDF',
                legendWork: 'Schedule (e.g. 07:00 / 08:00 / 10:00)',
                legendExtra: 'Extra',
                legendVrij: 'Off',
                legendVakantie: 'Vacation',
                whatsappBtn: 'WhatsApp',
                whatsappTitle: 'Share week and schedule image on WhatsApp',
                emailBtn: 'Email',
                emailTitle: 'Send week and schedule image by Email',
                copyTextBtn: 'Copy Text',
                copyTextTitle: 'Copy current week',
                statsEmployees: 'Employees:',
                statsWorkedDays: 'Worked days / wk:',
                daySingular: 'day',
                dayPlural: 'days',
                fsSave: '💾 Save',
                fsPrevWeek: '◀ Prev. wk',
                fsNextWeek: 'Next wk ▶',
                fsRotate: '↻ Rotate ±90°',
                fsExit: '✕ Exit (ESC)',
                colEmployee: 'Employee',
                colEmployeeDetails: 'EMPLOYEE & DETAILS',
                colDays: 'Days',
                colDaysUpper: 'DAYS',
                presentPerDay: 'Present / day',
                noEmployeesTable: 'No employees added yet. Click <strong>+ Employee</strong> to get started.',
                noEmployeesCanvas: 'No employees added for this week.',
                removeEmployeeTitle: 'Remove employee',
                setCellTitle: 'Click to set schedule',
                days: ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday'],
                daysShort: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'],
                monthsShort: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
                shiftModalTitleDay: 'Schedule • {day}',
                shiftModalSubtitle: '{name} ({date} {year})',
                closeModalAria: 'Close',
                quickPresetsLabel: 'Quickly pick start time or day status:',
                presetWorkDesc: 'Working day',
                presetExtraTitle: '{time} • Extra',
                presetExtraDesc: 'Extra working day',
                statusVrijLabel: 'Off',
                presetVrijDesc: 'Day off (not counted as worked day)',
                statusVakantieLabel: 'Vacation',
                presetVakantieDesc: 'Vacation (not counted as worked day)',
                customLabelField: 'Start time or status',
                customLabelPlaceholder: 'E.g. 07:00, 08:00, 10:00, Off, Vacation',
                customTypeField: 'Day type',
                typeWorkOption: 'Working day',
                typeExtraOption: 'Extra (additional)',
                typeVrijOption: 'Off',
                typeVakantieOption: 'Vacation',
                customNoteField: 'Optional note (e.g. Extra, Group A)',
                customNotePlaceholder: 'E.g. Extra',
                deleteCellBtn: 'Delete',
                addExtraDayBtn: '+ Add Extra day',
                resetGroupWeekBtn: 'Reapply group schedule',
                applyMonFriBtn: 'Apply Mon–Fri',
                cancelBtn: 'Cancel',
                saveBtn: 'Save',
                addEmpModalTitle: 'Add New Employee',
                addEmpModalSubtitle: 'Will appear immediately in the weekly table',
                empNameLabel: 'Full Name *',
                empNamePlaceholder: 'E.g. Alex Morgan',
                empRoleLabel: 'Role / Group (optional)',
                empRolePlaceholder: 'E.g. Group A, Group B, Group C...',
                empDefaultRole: 'Employee',
                addEmpSubmitBtn: 'Add to schedule',
                shareModalTitle: 'Send Week & Schedule Image (.PNG)',
                shareModalSubtitle: 'Week {week} ({range}) • Ready to share',
                shareError: 'Could not generate PNG image of the table.',
                shareHelperNative: 'Sends the selected week and the PNG schedule image via WhatsApp or Email.',
                shareHelperFallback: 'Sends the selected week and the PNG schedule image.',
                downloadPngBtn: '⬇ Download PNG',
                copyImageBtn: '📋 Copy Image',
                copyTextModalBtn: '📄 Copy Week',
                waTextBtn: 'WhatsApp (Week)',
                waImageBtn: 'WhatsApp (Image)',
                mailImageBtn: 'Email',
                closeBtn: 'Close',
                canvasBannerTitle: 'WORK SCHEDULE • WEEK {week} ({range})',
                canvasBannerStats: 'Employees: {count}   •   Total worked days: {days} days',
                canvasLegendWork: 'Schedule (e.g. 07:00 / 08:00 / 10:00)',
                canvasLegendExtra: 'Extra',
                canvasLegendVrij: 'Off',
                canvasLegendVakantie: 'Vacation',
                shareTextTitle: 'WORK SCHEDULE - Week {week} ({range})',
                shareTextDaysLine: 'Days: {daysLine}',
                shareTextNoEmp: 'No employees in schedule for this week.',
                shareTextEmpLine: '{idx}. {name}{role} — {days} {dayWord}',
                shareTextPresentLine: 'Present / day: {presentLine}',
                shareTextTotalLine: 'Total worked days this week: {days} days ({count} employees)',
                shareAttachNote: '{title}',
                shareMailBody: '{title}',
                toastFirstWeek2026: 'Reached the first week of 2026.',
                toastLastWeek2027: 'Reached the last week of 2027.',
                toastWeek47: 'Showing Week 47 (16 – 22 November 2026).',
                toastChangesSaved: 'All changes have been saved.',
                toastShiftSaved: 'Daily schedule updated. Click "Save changes" to confirm.',
                toastExtraDayAdded: 'Extra day added for {day}.',
                toastGroupReapplied: 'Group schedule reapplied for this week.',
                toastAppliedMonFri: 'Schedule applied to Monday – Friday.',
                toastCellCleared: 'Cell cleared.',
                toastEmpAdded: 'Employee {name} added.',
                toastEmpRemoved: 'Employee removed from list.',
                toastNoPrevWeek: 'No previous week available.',
                toastPrevWeekEmpty: 'Week {week} has no saved shifts.',
                toastWeekCopied: 'Copied schedule from Week {week}.',
                toastTextCopied: 'Current week copied.',
                toastTextCopyFail: 'Could not copy automatically; use WhatsApp or Email buttons.',
                toastPngNotReady: 'PNG image could not be prepared.',
                toastPngDownloaded: 'Image {filename} downloaded.',
                toastPngOpenFail: 'Open the image from preview to save it.',
                toastNoPng: 'No PNG image generated.',
                toastImgCopied: 'Table image copied to clipboard!',
                toastImgCopyFallback: 'PNG downloaded to attach.',
                toastNoPngGen: 'Could not generate PNG image.',
                toastSharedWa: 'Week and PNG image sent to WhatsApp.',
                toastSharedMail: 'Week and PNG image sent to Email.',
                toastShareCancelled: 'Sharing cancelled.',
                toastOpenedWa: 'Week and PNG image prepared for WhatsApp.',
                toastOpenedWaText: 'Week sent to WhatsApp.',
                toastOpenedMail: 'Week sent to Email.',
                toastFsActive: '90° fullscreen active • Press Back for main view.'
            },
            ru: {
                pageTitle: 'График работы и смен (2026 и 2027)',
                brandTitle: 'График работы',
                brandSubtitle: 'Нажмите на ячейку для правки • Нажмите на заголовок для поворота на 90°',
                brandTooltip: 'Нажмите, чтобы открыть график работы на весь экран с поворотом на 90°',
                prevWeekTitle: 'Предыдущая неделя',
                nextWeekTitle: 'Следующая неделя',
                yearAria: 'Выберите год',
                weekAria: 'Выберите неделю',
                langAria: 'Выберите язык',
                weekPrefix: 'Нед.',
                week47Btn: 'Нед. 47',
                week47Title: 'Перейти к неделе 47 (16–22 ноя 2026)',
                saveChangesBtn: 'Сохранить изменения',
                saveChangesPending: 'Сохранить изменения •',
                saveChangesTitle: 'Сохранить все изменения в таблице',
                addEmployeeBtn: '+ Сотрудник',
                copyPrevWeekBtn: 'Копия пред. нед.',
                copyPrevWeekTitle: 'Скопировать график с предыдущей недели',
                fullscreen90Btn: 'Экран 90°',
                fullscreen90Title: 'Полноэкранный режим с поворотом на 90°',
                printBtn: 'Печать',
                printTitle: 'Печать или сохранение в PDF',
                legendWork: 'График (напр. 07:00 / 08:00 / 10:00)',
                legendExtra: 'Extra',
                legendVrij: 'Выходной',
                legendVakantie: 'Отпуск',
                whatsappBtn: 'WhatsApp',
                whatsappTitle: 'Отправить неделю и картинку графика в WhatsApp',
                emailBtn: 'Email',
                emailTitle: 'Отправить неделю и картинку графика по Email',
                copyTextBtn: 'Копировать',
                copyTextTitle: 'Скопировать текущую неделю',
                statsEmployees: 'Сотрудники:',
                statsWorkedDays: 'Рабочих дней / нед.:',
                daySingular: 'день',
                dayPlural: 'дней',
                fsSave: '💾 Сохранить',
                fsPrevWeek: '◀ Пред. нед.',
                fsNextWeek: 'След. нед. ▶',
                fsRotate: '↻ Повернуть ±90°',
                fsExit: '✕ Выход (ESC)',
                colEmployee: 'Сотрудник',
                colEmployeeDetails: 'СОТРУДНИК И ДЕТАЛИ',
                colDays: 'Дни',
                colDaysUpper: 'ДНИ',
                presentPerDay: 'На смене / день',
                noEmployeesTable: 'Сотрудники не добавлены. Нажмите <strong>+ Сотрудник</strong>, чтобы начать.',
                noEmployeesCanvas: 'На эту неделю сотрудники не добавлены.',
                removeEmployeeTitle: 'Удалить сотрудника',
                setCellTitle: 'Нажмите, чтобы задать график',
                days: ['Понедельник', 'Вторник', 'Среда', 'Четверг', 'Пятница', 'Суббота', 'Воскресенье'],
                daysShort: ['Пн', 'Вт', 'Ср', 'Чт', 'Пт', 'Сб', 'Вс'],
                monthsShort: ['Янв', 'Фев', 'Мар', 'Апр', 'Май', 'Июн', 'Июл', 'Авг', 'Сен', 'Окт', 'Ноя', 'Дек'],
                shiftModalTitleDay: 'График • {day}',
                shiftModalSubtitle: '{name} ({date} {year})',
                closeModalAria: 'Закрыть',
                quickPresetsLabel: 'Быстрый выбор времени начала или статуса дня:',
                presetWorkDesc: 'Рабочий день',
                presetExtraTitle: '{time} • Extra',
                presetExtraDesc: 'Дополнительный рабочий день',
                statusVrijLabel: 'Выходной',
                presetVrijDesc: 'Выходной (не считается рабочим днём)',
                statusVakantieLabel: 'Отпуск',
                presetVakantieDesc: 'Отпуск (не считается рабочим днём)',
                customLabelField: 'Время начала или статус',
                customLabelPlaceholder: 'Напр.: 07:00, 08:00, 10:00, Выходной, Отпуск',
                customTypeField: 'Тип дня',
                typeWorkOption: 'Рабочий день',
                typeExtraOption: 'Extra (доп.)',
                typeVrijOption: 'Выходной',
                typeVakantieOption: 'Отпуск',
                customNoteField: 'Примечание (напр. Extra, Группа A)',
                customNotePlaceholder: 'Напр.: Extra',
                deleteCellBtn: 'Удалить',
                addExtraDayBtn: '+ Добавить день Extra',
                resetGroupWeekBtn: 'Вернуть график группы',
                applyMonFriBtn: 'На Пн–Пт',
                cancelBtn: 'Отмена',
                saveBtn: 'Сохранить',
                addEmpModalTitle: 'Добавить сотрудника',
                addEmpModalSubtitle: 'Сразу появится в недельном графике',
                empNameLabel: 'Имя и фамилия *',
                empNamePlaceholder: 'Напр.: Иван Петров',
                empRoleLabel: 'Должность / Группа (необязательно)',
                empRolePlaceholder: 'Напр.: Группа A, Группа B...',
                empDefaultRole: 'Сотрудник',
                addEmpSubmitBtn: 'Добавить в график',
                shareModalTitle: 'Отправить неделю и картинку (.PNG)',
                shareModalSubtitle: 'Нед. {week} ({range}) • Готово к отправке',
                shareError: 'Не удалось создать PNG-изображение таблицы.',
                shareHelperNative: 'Отправляются выбранная неделя и PNG-картинка таблицы через WhatsApp или Email.',
                shareHelperFallback: 'Отправляются выбранная неделя и PNG-картинка таблицы.',
                downloadPngBtn: '⬇ Скачать PNG',
                copyImageBtn: '📋 Копировать картинку',
                copyTextModalBtn: '📄 Копировать неделю',
                waTextBtn: 'WhatsApp (Неделя)',
                waImageBtn: 'WhatsApp (Картинка)',
                mailImageBtn: 'Email',
                closeBtn: 'Закрыть',
                canvasBannerTitle: 'ГРАФИК РАБОТЫ • НЕДЕЛЯ {week} ({range})',
                canvasBannerStats: 'Сотрудников: {count}   •   Всего рабочих дней: {days} дн.',
                canvasLegendWork: 'График (напр. 07:00 / 08:00 / 10:00)',
                canvasLegendExtra: 'Extra',
                canvasLegendVrij: 'Выходной',
                canvasLegendVakantie: 'Отпуск',
                shareTextTitle: 'ГРАФИК РАБОТЫ - Нед. {week} ({range})',
                shareTextDaysLine: 'Дни: {daysLine}',
                shareTextNoEmp: 'На эту неделю сотрудники не добавлены.',
                shareTextEmpLine: '{idx}. {name}{role} — {days} {dayWord}',
                shareTextPresentLine: 'На смене / день: {presentLine}',
                shareTextTotalLine: 'Всего рабочих дней за неделю: {days} дн. (сотрудников: {count})',
                shareAttachNote: '{title}',
                shareMailBody: '{title}',
                toastFirstWeek2026: 'Достигнута первая неделя 2026 года.',
                toastLastWeek2027: 'Достигнута последняя неделя 2027 года.',
                toastWeek47: 'Показана неделя 47 (16 – 22 ноября 2026).',
                toastChangesSaved: 'Все изменения сохранены.',
                toastShiftSaved: 'Дневной график обновлён. Нажмите «Сохранить изменения» для подтверждения.',
                toastExtraDayAdded: 'День Extra добавлен на {day}.',
                toastGroupReapplied: 'График группы повторно применён на эту неделю.',
                toastAppliedMonFri: 'График применён с понедельника по пятницу.',
                toastCellCleared: 'Ячейка очищена.',
                toastEmpAdded: 'Сотрудник {name} добавлен.',
                toastEmpRemoved: 'Сотрудник удалён из списка.',
                toastNoPrevWeek: 'Предыдущая неделя недоступна.',
                toastPrevWeekEmpty: 'В неделе {week} нет сохранённых смен.',
                toastWeekCopied: 'График с недели {week} скопирован.',
                toastTextCopied: 'Текущая неделя скопирована.',
                toastTextCopyFail: 'Автокопирование недоступно; используйте WhatsApp или Email.',
                toastPngNotReady: 'Не удалось подготовить PNG-изображение.',
                toastPngDownloaded: 'Изображение {filename} скачано.',
                toastPngOpenFail: 'Откройте изображение в предпросмотре, чтобы сохранить его.',
                toastNoPng: 'PNG-изображение не создано.',
                toastImgCopied: 'Изображение таблицы скопировано в буфер обмена!',
                toastImgCopyFallback: 'PNG скачан для отправки.',
                toastNoPngGen: 'Не удалось создать PNG-изображение.',
                toastSharedWa: 'Неделя и PNG-картинка отправлены в WhatsApp.',
                toastSharedMail: 'Неделя и PNG-картинка отправлены по Email.',
                toastShareCancelled: 'Отправка отменена.',
                toastOpenedWa: 'Неделя и PNG-картинка подготовлены для WhatsApp.',
                toastOpenedWaText: 'Неделя отправлена в WhatsApp.',
                toastOpenedMail: 'Неделя отправлена по Email.',
                toastFsActive: 'Полноэкранный режим 90° активен • Нажмите Назад для возврата.'
            },
            tr: {
                pageTitle: 'Çalışma Programı & Vardiyalar (2026 & 2027)',
                brandTitle: 'Çalışma Programı',
                brandSubtitle: 'Düzenlemek için hücreye tıklayın • 90° tam ekran için başlığa tıklayın',
                brandTooltip: 'Çalışma Programını 90° döndürülmüş tam ekranda açmak için tıklayın',
                prevWeekTitle: 'Önceki hafta',
                nextWeekTitle: 'Sonraki hafta',
                yearAria: 'Yıl seçin',
                weekAria: 'Hafta seçin',
                langAria: 'Dil seçin',
                weekPrefix: 'Hafta',
                week47Btn: 'Hafta 47',
                week47Title: '47. Haftaya git (16–22 Kas 2026)',
                saveChangesBtn: 'Değişiklikleri kaydet',
                saveChangesPending: 'Değişiklikleri kaydet •',
                saveChangesTitle: 'Tablodaki tüm değişiklikleri kaydet',
                addEmployeeBtn: '+ Çalışan',
                copyPrevWeekBtn: 'Önceki Haftayı Kopyala',
                copyPrevWeekTitle: 'Önceki haftanın programını kopyala',
                fullscreen90Btn: '90° Ekran',
                fullscreen90Title: '90° döndürülmüş tam ekran görünümü',
                printBtn: 'Yazdır',
                printTitle: 'Yazdır veya PDF olarak kaydet',
                legendWork: 'Program (örn. 07:00 / 08:00 / 10:00)',
                legendExtra: 'Extra',
                legendVrij: 'İzinli',
                legendVakantie: 'Tatil',
                whatsappBtn: 'WhatsApp',
                whatsappTitle: 'Haftayı ve tablo görselini WhatsApp’ta paylaş',
                emailBtn: 'E-posta',
                emailTitle: 'Haftayı ve tablo görselini E-posta ile gönder',
                copyTextBtn: 'Kopyala',
                copyTextTitle: 'Mevcut haftayı kopyala',
                statsEmployees: 'Çalışanlar:',
                statsWorkedDays: 'Çalışılan gün / hf.:',
                daySingular: 'gün',
                dayPlural: 'gün',
                fsSave: '💾 Kaydet',
                fsPrevWeek: '◀ Önceki hf.',
                fsNextWeek: 'Sonraki hf. ▶',
                fsRotate: '↻ Döndür ±90°',
                fsExit: '✕ Çıkış (ESC)',
                colEmployee: 'Çalışan',
                colEmployeeDetails: 'ÇALIŞAN & DETAYLAR',
                colDays: 'Gün',
                colDaysUpper: 'GÜN',
                presentPerDay: 'Mevcut / gün',
                noEmployeesTable: 'Henüz çalışan eklenmedi. Başlamak için <strong>+ Çalışan</strong> düğmesine tıklayın.',
                noEmployeesCanvas: 'Bu hafta için çalışan eklenmedi.',
                removeEmployeeTitle: 'Çalışanı kaldır',
                setCellTitle: 'Programı ayarlamak için tıklayın',
                days: ['Pazartesi', 'Salı', 'Çarşamba', 'Perşembe', 'Cuma', 'Cumartesi', 'Pazar'],
                daysShort: ['Pzt', 'Sal', 'Çar', 'Per', 'Cum', 'Cmt', 'Paz'],
                monthsShort: ['Oca', 'Şub', 'Mar', 'Nis', 'May', 'Haz', 'Tem', 'Ağu', 'Eyl', 'Eki', 'Kas', 'Ara'],
                shiftModalTitleDay: 'Program • {day}',
                shiftModalSubtitle: '{name} ({date} {year})',
                closeModalAria: 'Kapat',
                quickPresetsLabel: 'Başlangıç saatini veya gün durumunu hızlı seçin:',
                presetWorkDesc: 'Çalışma günü',
                presetExtraTitle: '{time} • Extra',
                presetExtraDesc: 'Ek çalışma günü',
                statusVrijLabel: 'İzinli',
                presetVrijDesc: 'İzin günü (çalışılan gün sayılmaz)',
                statusVakantieLabel: 'Tatil',
                presetVakantieDesc: 'Tatil (çalışılan gün sayılmaz)',
                customLabelField: 'Başlangıç saati veya durum',
                customLabelPlaceholder: 'Örn: 07:00, 08:00, 10:00, İzinli, Tatil',
                customTypeField: 'Gün türü',
                typeWorkOption: 'Çalışma günü',
                typeExtraOption: 'Extra (ek)',
                typeVrijOption: 'İzinli',
                typeVakantieOption: 'Tatil',
                customNoteField: 'İsteğe bağlı not (örn. Extra, Grup A)',
                customNotePlaceholder: 'Örn: Extra',
                deleteCellBtn: 'Sil',
                addExtraDayBtn: '+ Extra gün ekle',
                resetGroupWeekBtn: 'Grup programını uygula',
                applyMonFriBtn: 'Pzt–Cum uygula',
                cancelBtn: 'İptal',
                saveBtn: 'Kaydet',
                addEmpModalTitle: 'Yeni Çalışan Ekle',
                addEmpModalSubtitle: 'Haftalık tabloda hemen görünür',
                empNameLabel: 'Ad Soyad *',
                empNamePlaceholder: 'Örn: Ahmet Yılmaz',
                empRoleLabel: 'Görev / Grup (isteğe bağlı)',
                empRolePlaceholder: 'Örn: Grup A, Grup B, Grup C...',
                empDefaultRole: 'Çalışan',
                addEmpSubmitBtn: 'Programa ekle',
                shareModalTitle: 'Haftayı ve Tablo Görselini Gönder (.PNG)',
                shareModalSubtitle: 'Hafta {week} ({range}) • Paylaşıma hazır',
                shareError: 'Tablonun PNG görseli oluşturulamadı.',
                shareHelperNative: 'Seçilen hafta ve PNG tablo görseli WhatsApp veya E-posta ile gönderilir.',
                shareHelperFallback: 'Seçilen hafta ve PNG tablo görseli gönderilir.',
                downloadPngBtn: '⬇ PNG İndir',
                copyImageBtn: '📋 Görseli Kopyala',
                copyTextModalBtn: '📄 Haftayı Kopyala',
                waTextBtn: 'WhatsApp (Hafta)',
                waImageBtn: 'WhatsApp (Görsel)',
                mailImageBtn: 'E-posta',
                closeBtn: 'Kapat',
                canvasBannerTitle: 'ÇALIŞMA PROGRAMI • HAFTA {week} ({range})',
                canvasBannerStats: 'Çalışanlar: {count}   •   Toplam çalışılan gün: {days} gün',
                canvasLegendWork: 'Program (örn. 07:00 / 08:00 / 10:00)',
                canvasLegendExtra: 'Extra',
                canvasLegendVrij: 'İzinli',
                canvasLegendVakantie: 'Tatil',
                shareTextTitle: 'ÇALIŞMA PROGRAMI - Hafta {week} ({range})',
                shareTextDaysLine: 'Günler: {daysLine}',
                shareTextNoEmp: 'Bu hafta için çalışan bulunmuyor.',
                shareTextEmpLine: '{idx}. {name}{role} — {days} {dayWord}',
                shareTextPresentLine: 'Mevcut / gün: {presentLine}',
                shareTextTotalLine: 'Haftalık toplam çalışılan gün: {days} gün ({count} çalışan)',
                shareAttachNote: '{title}',
                shareMailBody: '{title}',
                toastFirstWeek2026: '2026 yılının ilk haftasına ulaştınız.',
                toastLastWeek2027: '2027 yılının son haftasına ulaştınız.',
                toastWeek47: '47. Hafta gösteriliyor (16 – 22 Kasım 2026).',
                toastChangesSaved: 'Tüm değişiklikler kaydedildi.',
                toastShiftSaved: 'Günlük program güncellendi. Onaylamak için „Değişiklikleri kaydet“ düğmesine tıklayın.',
                toastExtraDayAdded: '{day} için Extra gün eklendi.',
                toastGroupReapplied: 'Bu hafta için grup programı yeniden uygulandı.',
                toastAppliedMonFri: 'Program Pazartesi – Cuma günlerine uygulandı.',
                toastCellCleared: 'Hücre temizlendi.',
                toastEmpAdded: '{name} adlı çalışan eklendi.',
                toastEmpRemoved: 'Çalışan listeden kaldırıldı.',
                toastNoPrevWeek: 'Önceki hafta bulunamadı.',
                toastPrevWeekEmpty: '{week}. haftada kayıtlı vardiya yok.',
                toastWeekCopied: '{week}. haftanın programı kopyalandı.',
                toastTextCopied: 'Mevcut hafta kopyalandı.',
                toastTextCopyFail: 'Otomatik kopyalanamadı; WhatsApp veya E-posta düğmelerini kullanın.',
                toastPngNotReady: 'PNG görseli hazırlanamadı.',
                toastPngDownloaded: '{filename} görseli indirildi.',
                toastPngOpenFail: 'Kaydetmek için önizlemeden görseli açın.',
                toastNoPng: 'Oluşturulmuş PNG görseli yok.',
                toastImgCopied: 'Tablo görseli panoya kopyalandı!',
                toastImgCopyFallback: 'PNG eklemek için indirildi.',
                toastNoPngGen: 'PNG görseli oluşturulamadı.',
                toastSharedWa: 'Hafta ve PNG görseli WhatsApp’a gönderildi.',
                toastSharedMail: 'Hafta ve PNG görseli E-postaya gönderildi.',
                toastShareCancelled: 'Paylaşım iptal edildi.',
                toastOpenedWa: 'Hafta ve PNG görseli WhatsApp için hazırlandı.',
                toastOpenedWaText: 'Hafta WhatsApp’a gönderildi.',
                toastOpenedMail: 'Hafta E-postaya gönderildi.',
                toastFsActive: '90° tam ekran aktif • Ana görünüm için Geri tuşuna basın.'
            },
            nl: {
                pageTitle: 'Werkrooster & Diensten (2026 & 2027)',
                brandTitle: 'Werkrooster',
                brandSubtitle: 'Klik op een cel om te bewerken • Klik op titel voor 90° volledig scherm',
                brandTooltip: 'Klik om het werkrooster 90° gedraaid op volledig scherm te openen',
                prevWeekTitle: 'Vorige week',
                nextWeekTitle: 'Volgende week',
                yearAria: 'Selecteer jaar',
                weekAria: 'Selecteer week',
                langAria: 'Selecteer taal',
                weekPrefix: 'Week',
                week47Btn: 'Week 47',
                week47Title: 'Ga naar Week 47 (16–22 nov 2026)',
                saveChangesBtn: 'Wijzigingen opslaan',
                saveChangesPending: 'Wijzigingen opslaan •',
                saveChangesTitle: 'Alle wijzigingen in de tabel opslaan',
                addEmployeeBtn: '+ Medewerker',
                copyPrevWeekBtn: 'Kopieer Vorige Wk',
                copyPrevWeekTitle: 'Kopieer rooster van vorige week',
                fullscreen90Btn: 'Scherm 90°',
                fullscreen90Title: '90° gedraaide weergave op volledig scherm',
                printBtn: 'Afdrukken',
                printTitle: 'Afdrukken of opslaan als PDF',
                legendWork: 'Rooster (bijv. 07:00 / 08:00 / 10:00)',
                legendExtra: 'Extra',
                legendVrij: 'Vrij',
                legendVakantie: 'Vakantie',
                whatsappBtn: 'WhatsApp',
                whatsappTitle: 'Deel week en roosterafbeelding op WhatsApp',
                emailBtn: 'E-mail',
                emailTitle: 'Verstuur week en roosterafbeelding per e-mail',
                copyTextBtn: 'Kopieer',
                copyTextTitle: 'Kopieer huidige week',
                statsEmployees: 'Medewerkers:',
                statsWorkedDays: 'Gewerkte dagen / wk:',
                daySingular: 'dag',
                dayPlural: 'dagen',
                fsSave: '💾 Opslaan',
                fsPrevWeek: '◀ Vorige wk',
                fsNextWeek: 'Volgende wk ▶',
                fsRotate: '↻ Draai ±90°',
                fsExit: '✕ Sluiten (ESC)',
                colEmployee: 'Medewerker',
                colEmployeeDetails: 'MEDEWERKER & DETAILS',
                colDays: 'Dagen',
                colDaysUpper: 'DAGEN',
                presentPerDay: 'Aanwezig / dag',
                noEmployeesTable: 'Nog geen medewerkers toegevoegd. Klik op <strong>+ Medewerker</strong> om te beginnen.',
                noEmployeesCanvas: 'Geen medewerkers toegevoegd voor deze week.',
                removeEmployeeTitle: 'Verwijder medewerker',
                setCellTitle: 'Klik om rooster in te stellen',
                days: ['Maandag', 'Dinsdag', 'Woensdag', 'Donderdag', 'Vrijdag', 'Zaterdag', 'Zondag'],
                daysShort: ['Ma', 'Di', 'Wo', 'Do', 'Vr', 'Za', 'Zo'],
                monthsShort: ['Jan', 'Feb', 'Mrt', 'Apr', 'Mei', 'Jun', 'Jul', 'Aug', 'Sep', 'Okt', 'Nov', 'Dec'],
                shiftModalTitleDay: 'Rooster • {day}',
                shiftModalSubtitle: '{name} ({date} {year})',
                closeModalAria: 'Sluiten',
                quickPresetsLabel: 'Kies snel een begintijd of dagstatus:',
                presetWorkDesc: 'Werkdag',
                presetExtraTitle: '{time} • Extra',
                presetExtraDesc: 'Extra werkdag',
                statusVrijLabel: 'Vrij',
                presetVrijDesc: 'Vrije dag (telt niet als gewerkte dag)',
                statusVakantieLabel: 'Vakantie',
                presetVakantieDesc: 'Vakantie (telt niet als gewerkte dag)',
                customLabelField: 'Begintijd of status',
                customLabelPlaceholder: 'Bijv.: 07:00, 08:00, 10:00, Vrij, Vakantie',
                customTypeField: 'Dagtype',
                typeWorkOption: 'Werkdag',
                typeExtraOption: 'Extra (aanvullend)',
                typeVrijOption: 'Vrij',
                typeVakantieOption: 'Vakantie',
                customNoteField: 'Optionele notitie (bijv. Extra, Groep A)',
                customNotePlaceholder: 'Bijv.: Extra',
                deleteCellBtn: 'Verwijderen',
                addExtraDayBtn: '+ Extra dag toevoegen',
                resetGroupWeekBtn: 'Groepsrooster toepassen',
                applyMonFriBtn: 'Pas toe Ma–Vr',
                cancelBtn: 'Annuleren',
                saveBtn: 'Opslaan',
                addEmpModalTitle: 'Nieuwe Medewerker Toevoegen',
                addEmpModalSubtitle: 'Verschijnt direct in het weekrooster',
                empNameLabel: 'Voor- en achternaam *',
                empNamePlaceholder: 'Bijv.: Jan de Vries',
                empRoleLabel: 'Functie / Groep (optioneel)',
                empRolePlaceholder: 'Bijv.: Groep A, Groep B, Groep C...',
                empDefaultRole: 'Medewerker',
                addEmpSubmitBtn: 'Toevoegen aan rooster',
                shareModalTitle: 'Week & Roosterafbeelding Verzenden (.PNG)',
                shareModalSubtitle: 'Week {week} ({range}) • Klaar om te delen',
                shareError: 'Kon geen PNG-afbeelding van de tabel maken.',
                shareHelperNative: 'De geselecteerde week en de PNG-afbeelding worden via WhatsApp of E-mail verzonden.',
                shareHelperFallback: 'De geselecteerde week en de PNG-afbeelding worden verzonden.',
                downloadPngBtn: '⬇ Download PNG',
                copyImageBtn: '📋 Kopieer Afbeelding',
                copyTextModalBtn: '📄 Kopieer Week',
                waTextBtn: 'WhatsApp (Week)',
                waImageBtn: 'WhatsApp (Afbeelding)',
                mailImageBtn: 'E-mail',
                closeBtn: 'Sluiten',
                canvasBannerTitle: 'WERKROOSTER • WEEK {week} ({range})',
                canvasBannerStats: 'Medewerkers: {count}   •   Totaal gewerkte dagen: {days} dagen',
                canvasLegendWork: 'Rooster (bijv. 07:00 / 08:00 / 10:00)',
                canvasLegendExtra: 'Extra',
                canvasLegendVrij: 'Vrij',
                canvasLegendVakantie: 'Vakantie',
                shareTextTitle: 'WERKROOSTER - Week {week} ({range})',
                shareTextDaysLine: 'Dagen: {daysLine}',
                shareTextNoEmp: 'Geen medewerkers in het rooster voor deze week.',
                shareTextEmpLine: '{idx}. {name}{role} — {days} {dayWord}',
                shareTextPresentLine: 'Aanwezig / dag: {presentLine}',
                shareTextTotalLine: 'Totaal gewerkte dagen deze week: {days} dagen ({count} medewerkers)',
                shareAttachNote: '{title}',
                shareMailBody: '{title}',
                toastFirstWeek2026: 'Eerste week van 2026 bereikt.',
                toastLastWeek2027: 'Laatste week van 2027 bereikt.',
                toastWeek47: 'Week 47 weergegeven (16 – 22 november 2026).',
                toastChangesSaved: 'Alle wijzigingen zijn opgeslagen.',
                toastShiftSaved: 'Dagrooster bijgewerkt. Klik op „Wijzigingen opslaan“ om te bevestigen.',
                toastExtraDayAdded: 'Extra dag toegevoegd voor {day}.',
                toastGroupReapplied: 'Groepsrooster opnieuw toegepast voor deze week.',
                toastAppliedMonFri: 'Rooster toegepast op maandag – vrijdag.',
                toastCellCleared: 'Cel gewist.',
                toastEmpAdded: 'Medewerker {name} toegevoegd.',
                toastEmpRemoved: 'Medewerker uit de lijst verwijderd.',
                toastNoPrevWeek: 'Geen vorige week beschikbaar.',
                toastPrevWeekEmpty: 'Week {week} heeft geen opgeslagen diensten.',
                toastWeekCopied: 'Rooster van week {week} gekopieerd.',
                toastTextCopied: 'Huidige week gekopieerd.',
                toastTextCopyFail: 'Automatisch kopiëren mislukt; gebruik WhatsApp of E-mail.',
                toastPngNotReady: 'PNG-afbeelding kon niet worden voorbereid.',
                toastPngDownloaded: 'Afbeelding {filename} gedownload.',
                toastPngOpenFail: 'Open de afbeelding in het voorbeeld om deze op te slaan.',
                toastNoPng: 'Geen PNG-afbeelding gegenereerd.',
                toastImgCopied: 'Roosterafbeelding gekopieerd naar klembord!',
                toastImgCopyFallback: 'PNG gedownload om bij te voegen.',
                toastNoPngGen: 'Kon geen PNG-afbeelding genereren.',
                toastSharedWa: 'Week en PNG-afbeelding verzonden naar WhatsApp.',
                toastSharedMail: 'Week en PNG-afbeelding verzonden naar E-mail.',
                toastShareCancelled: 'Delen geannuleerd.',
                toastOpenedWa: 'Week en PNG-afbeelding voorbereid voor WhatsApp.',
                toastOpenedWaText: 'Week verzonden naar WhatsApp.',
                toastOpenedMail: 'Week verzonden naar E-mail.',
                toastFsActive: '90° volledig scherm actief • Druk op Terug voor hoofdweergave.'
            }
        };

        const ALL_VRIJ_WORDS = new Set(
            Object.values(TRANSLATIONS).map(d => (d.statusVrijLabel || '').trim().toUpperCase())
                .concat(['VRIJ', 'LIBER', 'OFF', 'DAY OFF'])
                .filter(Boolean)
        );

        const ALL_VAKANTIE_WORDS = new Set(
            Object.values(TRANSLATIONS).map(d => (d.statusVakantieLabel || '').trim().toUpperCase())
                .concat(['VACANȚĂ', 'VACANTA', 'URLAUB', 'VACATION', 'ОТПУСК', 'TATIL', 'VAKANTIE', 'CO', 'CM'])
                .filter(Boolean)
        );

        const ALL_DEFAULT_ROLES = new Set(
            Object.values(TRANSLATIONS).map(d => (d.empDefaultRole || '').trim().toUpperCase())
                .concat(['ANGAJAT', 'EMPLOYEE', 'MITARBEITER', 'СОТРУДНИК', 'ÇALIŞAN', 'MEDEWERKER'])
                .filter(Boolean)
        );

        const rawState = {
            year: 2026,
            week: 47,
            lang: 'ro',
            rotationClass: 'rotated-ccw',
            employees: [],
            schedules: {},
            manualOverrides: {},
            customData: {},
            hasPendingSave: false,
            editingCell: null,
            isFullscreen: false,
            pushedFullscreenState: false,
            lastPngDataUrl: '',
            lastPngBlob: null,
            lastPngFilename: ''
        };

        let persistDebounceTimer = null;

        function updateSaveButtonVisualState() {
            const saveBtn = document.getElementById('save-changes-btn');
            if (!saveBtn) return;
            const span = saveBtn.querySelector('span');
            if (state.hasPendingSave) {
                saveBtn.classList.add('has-unsaved');
                if (span) span.textContent = t('saveChangesPending');
            } else {
                saveBtn.classList.remove('has-unsaved');
                if (span) span.textContent = t('saveChangesBtn');
            }
        }

        function markPendingSave(pending = true) {
            state.hasPendingSave = Boolean(pending);
            updateSaveButtonVisualState();
        }

        function commitChangesExplicitly() {
            persistEverythingNow();
            markPendingSave(false);
            showToast(t('toastChangesSaved'));
        }

        function persistEverythingNow() {
            if (persistDebounceTimer) {
                clearTimeout(persistDebounceTimer);
                persistDebounceTimer = null;
            }
            const payload = JSON.stringify({
                employees: rawState.employees,
                schedules: rawState.schedules,
                manualOverrides: rawState.manualOverrides || {},
                customData: rawState.customData || {}
            });
            safeSetStorage(STORAGE_KEY, payload);
            safeSetStorage(LANG_STORAGE_KEY, rawState.lang);
            safeSetStorage(META_STORAGE_KEY, JSON.stringify({
                year: rawState.year,
                week: rawState.week,
                rotationClass: rawState.rotationClass || 'rotated-ccw'
            }));
        }

        function schedulePersistEverything() {
            if (persistDebounceTimer) {
                clearTimeout(persistDebounceTimer);
            }
            persistDebounceTimer = setTimeout(() => {
                persistDebounceTimer = null;
                persistEverythingNow();
            }, 30);
        }

        function createDeepReactiveProxy(target) {
            if (!target || typeof target !== 'object') return target;
            if (target.__isReactiveProxy) return target;

            const proxy = new Proxy(target, {
                get(obj, prop, receiver) {
                    if (prop === '__isReactiveProxy') return true;
                    const val = Reflect.get(obj, prop, receiver);
                    if (val && typeof val === 'object') {
                        return createDeepReactiveProxy(val);
                    }
                    return val;
                },
                set(obj, prop, value, receiver) {
                    const prev = Reflect.get(obj, prop, receiver);
                    const wrappedValue = (value && typeof value === 'object') ? createDeepReactiveProxy(value) : value;
                    const ok = Reflect.set(obj, prop, wrappedValue, receiver);
                    if (ok && prev !== value) {
                        schedulePersistEverything();
                    }
                    return ok;
                },
                deleteProperty(obj, prop) {
                    const hadKey = Object.prototype.hasOwnProperty.call(obj, prop);
                    const ok = Reflect.deleteProperty(obj, prop);
                    if (ok && hadKey) {
                        schedulePersistEverything();
                    }
                    return ok;
                }
            });

            return proxy;
        }

        const state = createDeepReactiveProxy(rawState);

        function t(key, params = {}) {
            const dict = TRANSLATIONS[state.lang] || TRANSLATIONS.ro;
            let str = Object.prototype.hasOwnProperty.call(dict, key) ? dict[key] : (TRANSLATIONS.ro[key] || key);
            Object.keys(params).forEach(paramKey => {
                str = str.replace(new RegExp(`\\{${paramKey}\\}`, 'g'), String(params[paramKey]));
            });
            return str;
        }

        function getDayNames() {
            return (TRANSLATIONS[state.lang] || TRANSLATIONS.ro).days;
        }

        function getDayShortNames() {
            return (TRANSLATIONS[state.lang] || TRANSLATIONS.ro).daysShort;
        }

        function getMonthShortNames() {
            return (TRANSLATIONS[state.lang] || TRANSLATIONS.ro).monthsShort;
        }

        function detectSlotKind(slot) {
            if (!slot || !slot.label) return 'empty';
            const rawType = (slot.type || '').toLowerCase();
            const upperLabel = slot.label.trim().toUpperCase();
            const upperNote = (slot.note || '').trim().toUpperCase();

            if (rawType === 'vakantie' || ALL_VAKANTIE_WORDS.has(upperLabel)) {
                return 'vakantie';
            }
            if (rawType === 'vrij' || ALL_VRIJ_WORDS.has(upperLabel)) {
                return 'vrij';
            }
            if (rawType === 'extra' || upperNote === 'EXTRA' || upperLabel.includes('EXTRA')) {
                return 'extra';
            }
            return 'work';
        }

        function getLocalizedSlotLabel(slot) {
            if (!slot || !slot.label) return '';
            const kind = detectSlotKind(slot);
            if (kind === 'vrij') return t('statusVrijLabel');
            if (kind === 'vakantie') return t('statusVakantieLabel');
            return slot.label;
        }

        function getLocalizedEmployeeRole(role) {
            if (!role) return '';
            if (ALL_DEFAULT_ROLES.has(role.trim().toUpperCase())) {
                return t('empDefaultRole');
            }
            return role;
        }

        function loadSavedMetaAndLanguage() {
            const savedLang = safeGetStorage(LANG_STORAGE_KEY);
            if (savedLang && Object.prototype.hasOwnProperty.call(TRANSLATIONS, savedLang)) {
                state.lang = savedLang;
            } else {
                state.lang = 'ro';
            }

            const savedMeta = safeGetStorage(META_STORAGE_KEY);
            if (savedMeta) {
                try {
                    const meta = JSON.parse(savedMeta);
                    if (meta && typeof meta === 'object') {
                        if (meta.year === 2026 || meta.year === 2027) {
                            state.year = meta.year;
                        }
                        if (typeof meta.week === 'number' && meta.week >= 1 && meta.week <= 53) {
                            state.week = meta.week;
                        }
                        if (meta.rotationClass === 'rotated-ccw' || meta.rotationClass === 'rotated-cw') {
                            state.rotationClass = meta.rotationClass;
                        }
                    }
                } catch (err) {
                    // Ignore malformed meta
                }
            }

            const select = document.getElementById('lang-select');
            if (select) select.value = state.lang;
            document.documentElement.lang = state.lang;
        }

        function applyStaticTranslations() {
            document.documentElement.lang = state.lang;
            document.title = t('pageTitle');

            const titleEl = document.querySelector('.brand-title');
            if (titleEl) titleEl.textContent = t('brandTitle');

            const subtitleEl = document.querySelector('.brand-subtitle');
            if (subtitleEl) subtitleEl.textContent = t('brandSubtitle');

            const brandTrigger = document.getElementById('brand-trigger-btn');
            if (brandTrigger) brandTrigger.setAttribute('title', t('brandTooltip'));

            const prevBtn = document.getElementById('prev-week-btn');
            if (prevBtn) prevBtn.setAttribute('title', t('prevWeekTitle'));

            const nextBtn = document.getElementById('next-week-btn');
            if (nextBtn) nextBtn.setAttribute('title', t('nextWeekTitle'));

            const yearSelect = document.getElementById('year-select');
            if (yearSelect) yearSelect.setAttribute('aria-label', t('yearAria'));

            const weekSelect = document.getElementById('week-select');
            if (weekSelect) weekSelect.setAttribute('aria-label', t('weekAria'));

            const langSelect = document.getElementById('lang-select');
            if (langSelect) {
                langSelect.value = state.lang;
                langSelect.setAttribute('aria-label', t('langAria'));
            }

            const w47Btn = document.getElementById('week-47-btn');
            if (w47Btn) {
                w47Btn.textContent = t('week47Btn');
                w47Btn.setAttribute('title', t('week47Title'));
            }

            const saveChangesBtn = document.getElementById('save-changes-btn');
            if (saveChangesBtn) {
                saveChangesBtn.setAttribute('title', t('saveChangesTitle'));
                updateSaveButtonVisualState();
            }

            const addEmpBtn = document.getElementById('add-emp-btn');
            if (addEmpBtn) {
                const span = addEmpBtn.querySelector('span');
                if (span) span.textContent = t('addEmployeeBtn');
            }

            const copyPrevBtn = document.getElementById('copy-prev-week-btn');
            if (copyPrevBtn) {
                const span = copyPrevBtn.querySelector('span');
                if (span) span.textContent = t('copyPrevWeekBtn');
                copyPrevBtn.setAttribute('title', t('copyPrevWeekTitle'));
            }

            const fs90Btn = document.getElementById('fullscreen-90-btn');
            if (fs90Btn) {
                const span = fs90Btn.querySelector('span');
                if (span) span.textContent = t('fullscreen90Btn');
                fs90Btn.setAttribute('title', t('fullscreen90Title'));
            }

            const printBtn = document.getElementById('print-btn');
            if (printBtn) {
                const span = printBtn.querySelector('span');
                if (span) span.textContent = t('printBtn');
                printBtn.setAttribute('title', t('printTitle'));
            }

            const legWork = document.getElementById('legend-work-text');
            if (legWork) legWork.textContent = t('legendWork');
            const legExtra = document.getElementById('legend-extra-text');
            if (legExtra) legExtra.textContent = t('legendExtra');
            const legVrij = document.getElementById('legend-vrij-text');
            if (legVrij) legVrij.textContent = t('legendVrij');
            const legVakantie = document.getElementById('legend-vakantie-text');
            if (legVakantie) legVakantie.textContent = t('legendVakantie');

            const waBtn = document.getElementById('share-wa-btn');
            if (waBtn) {
                const span = waBtn.querySelector('span');
                if (span) span.textContent = t('whatsappBtn');
                waBtn.setAttribute('title', t('whatsappTitle'));
            }

            const mailBtn = document.getElementById('share-email-btn');
            if (mailBtn) {
                const span = mailBtn.querySelector('span');
                if (span) span.textContent = t('emailBtn');
                mailBtn.setAttribute('title', t('emailTitle'));
            }

            const copyTextBtn = document.getElementById('copy-text-btn');
            if (copyTextBtn) {
                const span = copyTextBtn.querySelector('span');
                if (span) span.textContent = t('copyTextBtn');
                copyTextBtn.setAttribute('title', t('copyTextTitle'));
            }

            const statsBar = document.querySelector('.stats-bar');
            if (statsBar) {
                const spans = statsBar.querySelectorAll('span');
                if (spans[0]) {
                    const countVal = document.getElementById('stat-emp-count')?.textContent || '0';
                    spans[0].innerHTML = `${t('statsEmployees')} <strong id="stat-emp-count">${countVal}</strong>`;
                }
                if (spans[1]) {
                    const daysVal = document.getElementById('stat-total-days')?.textContent || `0 ${t('dayPlural')}`;
                    spans[1].innerHTML = `${t('statsWorkedDays')} <strong id="stat-total-days">${daysVal}</strong>`;
                }
            }

            const fsTitleSpan = document.querySelector('.fs-title-group > span:first-child');
            if (fsTitleSpan) fsTitleSpan.textContent = t('brandTitle');

            const fsSaveBtn = document.getElementById('fs-save-btn');
            if (fsSaveBtn) fsSaveBtn.textContent = t('fsSave');
            const fsWaBtn = document.getElementById('fs-wa-btn');
            if (fsWaBtn) fsWaBtn.textContent = t('whatsappBtn');
            const fsMailBtn = document.getElementById('fs-mail-btn');
            if (fsMailBtn) fsMailBtn.textContent = t('emailBtn');
            const fsPrevBtn = document.getElementById('fs-prev-btn');
            if (fsPrevBtn) fsPrevBtn.textContent = t('fsPrevWeek');
            const fsNextBtn = document.getElementById('fs-next-btn');
            if (fsNextBtn) fsNextBtn.textContent = t('fsNextWeek');
            const fsRotateBtn = document.getElementById('fs-rotate-btn');
            if (fsRotateBtn) fsRotateBtn.textContent = t('fsRotate');
            const fsExitBtn = document.getElementById('fs-exit-btn');
            if (fsExitBtn) fsExitBtn.textContent = t('fsExit');

            const shiftModal = document.getElementById('shift-modal');
            if (shiftModal) {
                const closeBtn = document.getElementById('close-shift-modal-btn');
                if (closeBtn) closeBtn.setAttribute('aria-label', t('closeModalAria'));

                const presetHeader = document.getElementById('quick-presets-label');
                if (presetHeader) presetHeader.textContent = t('quickPresetsLabel');

                const presetBtns = shiftModal.querySelectorAll('.preset-btn');
                const presetTimes = ['07:00', '08:00', '09:00', '10:00'];
                for (let i = 0; i < 4; i++) {
                    if (presetBtns[i]) {
                        presetBtns[i].innerHTML = `<strong>${presetTimes[i]}</strong><span>${t('presetWorkDesc')}</span>`;
                    }
                }
                if (presetBtns[4]) presetBtns[4].innerHTML = `<strong>${t('presetExtraTitle', { time: '07:00' })}</strong><span>${t('presetExtraDesc')}</span>`;
                if (presetBtns[5]) presetBtns[5].innerHTML = `<strong>${t('presetExtraTitle', { time: '08:00' })}</strong><span>${t('presetExtraDesc')}</span>`;
                if (presetBtns[6]) {
                    presetBtns[6].setAttribute('data-preset-label', t('statusVrijLabel'));
                    presetBtns[6].innerHTML = `<strong>${escapeHTML(t('statusVrijLabel'))}</strong><span>${t('presetVrijDesc')}</span>`;
                }
                if (presetBtns[7]) {
                    presetBtns[7].setAttribute('data-preset-label', t('statusVakantieLabel'));
                    presetBtns[7].innerHTML = `<strong>${escapeHTML(t('statusVakantieLabel'))}</strong><span>${t('presetVakantieDesc')}</span>`;
                }

                const labels = shiftModal.querySelectorAll('.form-group label');
                if (labels[0]) labels[0].textContent = t('customLabelField');
                if (labels[1]) labels[1].textContent = t('customTypeField');
                if (labels[2]) labels[2].textContent = t('customNoteField');

                const customLabelInput = document.getElementById('custom-label');
                if (customLabelInput) customLabelInput.setAttribute('placeholder', t('customLabelPlaceholder'));

                const customNoteInput = document.getElementById('custom-note');
                if (customNoteInput) customNoteInput.setAttribute('placeholder', t('customNotePlaceholder'));

                const typeSelect = document.getElementById('custom-status-type');
                if (typeSelect) {
                    const opts = typeSelect.querySelectorAll('option');
                    if (opts[0]) opts[0].textContent = t('typeWorkOption');
                    if (opts[1]) opts[1].textContent = t('typeExtraOption');
                    if (opts[2]) opts[2].textContent = t('typeVrijOption');
                    if (opts[3]) opts[3].textContent = t('typeVakantieOption');
                }

                const clearCellBtn = document.getElementById('clear-cell-btn');
                if (clearCellBtn) clearCellBtn.textContent = t('deleteCellBtn');
                const addExtraDayBtn = document.getElementById('add-extra-day-btn');
                if (addExtraDayBtn) addExtraDayBtn.textContent = t('addExtraDayBtn');
                const resetGroupWeekBtn = document.getElementById('reset-group-week-btn');
                if (resetGroupWeekBtn) resetGroupWeekBtn.textContent = t('resetGroupWeekBtn');
                const applyMonFriBtn = document.getElementById('apply-mon-fri-btn');
                if (applyMonFriBtn) applyMonFriBtn.textContent = t('applyMonFriBtn');
                const cancelShiftBtn = document.getElementById('cancel-shift-btn');
                if (cancelShiftBtn) cancelShiftBtn.textContent = t('cancelBtn');
                const saveShiftBtn = document.getElementById('save-shift-btn');
                if (saveShiftBtn) saveShiftBtn.textContent = t('saveBtn');

                if (state.editingCell) {
                    const emp = state.employees.find(e => e.id === state.editingCell.empId);
                    const days = getDatesOfISOWeek(state.year, state.week);
                    if (emp) {
                        document.getElementById('shift-modal-title').textContent = t('shiftModalTitleDay', { day: getDayNames()[state.editingCell.dayIndex] });
                        document.getElementById('shift-modal-subtitle').textContent = t('shiftModalSubtitle', {
                            name: emp.name,
                            date: formatShortDate(days[state.editingCell.dayIndex]),
                            year: state.year
                        });
                    }
                    const weekKey = getWeekKey(state.year, state.week);
                    const currentSlot = state.schedules[weekKey]?.[state.editingCell.empId]?.[state.editingCell.dayIndex];
                    if (currentSlot && currentSlot.label) {
                        document.getElementById('custom-label').value = getLocalizedSlotLabel(currentSlot);
                    }
                }
            }

            const empModal = document.getElementById('emp-modal');
            if (empModal) {
                const closeBtn = document.getElementById('close-emp-modal-btn');
                if (closeBtn) closeBtn.setAttribute('aria-label', t('closeModalAria'));

                const title = document.getElementById('add-emp-title');
                if (title) title.textContent = t('addEmpModalTitle');
                const sub = document.getElementById('add-emp-subtitle');
                if (sub) sub.textContent = t('addEmpModalSubtitle');

                const labels = empModal.querySelectorAll('.form-group label');
                if (labels[0]) labels[0].textContent = t('empNameLabel');
                if (labels[1]) labels[1].textContent = t('empRoleLabel');

                const nameInput = document.getElementById('new-emp-name');
                if (nameInput) nameInput.setAttribute('placeholder', t('empNamePlaceholder'));
                const roleInput = document.getElementById('new-emp-role');
                if (roleInput) roleInput.setAttribute('placeholder', t('empRolePlaceholder'));

                const cancelEmpBtn = document.getElementById('cancel-emp-btn');
                if (cancelEmpBtn) cancelEmpBtn.textContent = t('cancelBtn');
                const submitEmpBtn = document.getElementById('submit-emp-btn');
                if (submitEmpBtn) submitEmpBtn.textContent = t('addEmpSubmitBtn');
            }

            const shareModal = document.getElementById('share-image-modal');
            if (shareModal) {
                const closeBtn = document.getElementById('close-share-modal-btn');
                if (closeBtn) closeBtn.setAttribute('aria-label', t('closeModalAria'));

                const title = document.getElementById('share-image-modal-title');
                if (title) title.textContent = t('shareModalTitle');

                const dlBtn = document.getElementById('download-png-btn');
                if (dlBtn) dlBtn.textContent = t('downloadPngBtn');

                const cpBtn = document.getElementById('copy-png-btn');
                if (cpBtn) cpBtn.textContent = t('copyImageBtn');

                const cpTextBtn = document.getElementById('modal-copy-text-btn');
                if (cpTextBtn) cpTextBtn.textContent = t('copyTextModalBtn');

                const waTextBtn = document.getElementById('modal-wa-text-btn');
                if (waTextBtn) waTextBtn.textContent = t('waTextBtn');

                const waImgBtn = document.getElementById('modal-wa-image-btn');
                if (waImgBtn) waImgBtn.textContent = t('waImageBtn');

                const mailImgBtn = document.getElementById('modal-mail-image-btn');
                if (mailImgBtn) mailImgBtn.textContent = t('mailImageBtn');

                const closeFooterBtn = document.getElementById('close-share-footer-btn');
                if (closeFooterBtn) closeFooterBtn.textContent = t('closeBtn');
            }
        }

        function onLanguageChange(newLang) {
            if (!newLang || !Object.prototype.hasOwnProperty.call(TRANSLATIONS, newLang)) return;
            state.lang = newLang;
            saveAppState();
            applyStaticTranslations();
            populateWeekDropdown();
            renderScheduleTable();
            if (document.getElementById('share-image-modal').classList.contains('open')) {
                openShareImageModal(null);
            }
        }

        /* =====================================================================
           3. ISO CALENDAR UTILITIES (2026 & 2027)
           ===================================================================== */
        function getISOWeekInfo(date) {
            const d = new Date(Date.UTC(date.getFullYear(), date.getMonth(), date.getDate()));
            const dayNum = d.getUTCDay() || 7;
            d.setUTCDate(d.getUTCDate() + 4 - dayNum);
            const yearStart = new Date(Date.UTC(d.getUTCFullYear(), 0, 1));
            const week = Math.ceil((((d - yearStart) / 86400000) + 1) / 7);
            return { year: d.getUTCFullYear(), week: week };
        }

        function getWeeksCountInYear(year) {
            const dec28 = new Date(Date.UTC(year, 11, 28));
            return getISOWeekInfo(dec28).week;
        }

        function getDatesOfISOWeek(year, week) {
            const jan4 = new Date(Date.UTC(year, 0, 4));
            const jan4Day = jan4.getUTCDay() || 7;
            const mondayWeek1 = new Date(jan4);
            mondayWeek1.setUTCDate(jan4.getUTCDate() - (jan4Day - 1));

            const days = [];
            for (let i = 0; i < 7; i++) {
                const d = new Date(mondayWeek1);
                d.setUTCDate(mondayWeek1.getUTCDate() + (week - 1) * 7 + i);
                days.push(d);
            }
            return days;
        }

        function formatShortDate(utcDate) {
            const day = String(utcDate.getUTCDate()).padStart(2, '0');
            const month = getMonthShortNames()[utcDate.getUTCMonth()];
            return `${day} ${month}`;
        }

        function getWeekKey(year, week) {
            return `${year}-W${String(week).padStart(2, '0')}`;
        }

        function isTodayUTC(utcDate) {
            const now = new Date();
            return utcDate.getUTCFullYear() === now.getFullYear() &&
                   utcDate.getUTCMonth() === now.getMonth() &&
                   utcDate.getUTCDate() === now.getDate();
        }

        function getCurrentCalendarDaySignature() {
            const now = new Date();
            return `${now.getFullYear()}-${String(now.getMonth() + 1).padStart(2, '0')}-${String(now.getDate()).padStart(2, '0')}`;
        }

        /* =====================================================================
           4. GROUP ROTATION SCHEDULE FROM SHEET & MANUAL OVERRIDE SUPPORT
           ===================================================================== */
        function createSlot(type, label, note = '') {
            return { type, label, note };
        }

        const SHEET_PAIR_ROTATION_2026 = {
            1:  ['BC', 'AC', 'AC', 'AB', 'AB', 'AB', 'BC'],
            2:  ['BC', 'AC', 'AC', 'AB', 'AB', 'BC', 'BC'],
            3:  ['AC', 'AC', 'AB', 'AB', 'BC', 'BC', 'AC'],
            4:  ['AC', 'AB', 'AB', 'BC', 'BC', 'AC', 'AC'],
            5:  ['AB', 'AB', 'BC', 'BC', 'AC', 'AC', 'AB'],
            6:  ['AB', 'BC', 'BC', 'AC', 'AC', 'AB', 'AB'],
            7:  ['BC', 'BC', 'AC', 'AC', 'AB', 'AB', 'BC'],
            8:  ['BC', 'AC', 'AC', 'AB', 'AB', 'BC', 'BC'],
            9:  ['AC', 'AC', 'AB', 'AB', 'BC', 'BC', 'AC'],
            10: ['AC', 'AB', 'AB', 'BC', 'BC', 'AC', 'AC'],
            11: ['AB', 'AB', 'BC', 'BC', 'AC', 'AC', 'AB'],
            12: ['AB', 'BC', 'BC', 'AC', 'AC', 'AB', 'AB'],
            13: ['BC', 'BC', 'AC', 'AC', 'AB', 'AB', 'BC'],
            14: ['BC', 'AC', 'AC', 'AB', 'AB', 'BC', 'BC'],
            15: ['AC', 'AC', 'AB', 'AB', 'BC', 'BC', 'AC'],
            16: ['AC', 'AB', 'AB', 'BC', 'BC', 'AC', 'AC'],
            17: ['AB', 'AB', 'BC', 'BC', 'AC', 'AC', 'AB'],
            18: ['AB', 'BC', 'BC', 'AC', 'AC', 'AB', 'AB'],
            19: ['BC', 'BC', 'AC', 'AC', 'AB', 'AB', 'BC'],
            20: ['BC', 'AC', 'AC', 'AB', 'AB', 'BC', 'BC'],
            21: ['AC', 'AC', 'AB', 'AB', 'BC', 'BC', 'AC'],
            22: ['AC', 'AB', 'AB', 'BC', 'BC', 'AC', 'AC'],
            23: ['AB', 'AB', 'BC', 'BC', 'AC', 'AC', 'AB'],
            24: ['AB', 'BC', 'BC', 'AC', 'AC', 'AB', 'AB'],
            25: ['BC', 'BC', 'AC', 'AC', 'AB', 'AB', 'BC'],
            26: ['BC', 'AC', 'AC', 'AB', 'AB', 'BC', 'BC'],
            27: ['AC', 'AC', 'AB', 'AB', 'BC', 'BC', 'AC'],
            28: ['AC', 'AB', 'AB', 'BC', 'BC', 'AC', 'AC'],
            29: ['AB', 'AB', 'BC', 'BC', 'AC', 'AC', 'AB'],
            30: ['AB', 'BC', 'BC', 'AC', 'AC', 'AB', 'AB'],
            31: ['BC', 'BC', 'AC', 'AC', 'AB', 'AB', 'BC'],
            32: ['BC', 'AC', 'AC', 'AB', 'AB', 'BC', 'BC'],
            33: ['AC', 'AC', 'AB', 'AB', 'BC', 'BC', 'AC'],
            34: ['AC', 'AB', 'AB', 'BC', 'BC', 'AC', 'AC'],
            35: ['AB', 'AB', 'BC', 'BC', 'AC', 'AC', 'AB'],
            36: ['AB', 'BC', 'BC', 'AC', 'AC', 'AB', 'AB'],
            37: ['BC', 'BC', 'AC', 'AC', 'AB', 'AB', 'BC'],
            38: ['BC', 'AC', 'AC', 'AB', 'AB', 'BC', 'BC'],
            39: ['AC', 'AC', 'AB', 'AB', 'BC', 'BC', 'AC'],
            40: ['AC', 'AB', 'AB', 'BC', 'BC', 'AC', 'AC'],
            41: ['AB', 'AB', 'BC', 'BC', 'AC', 'AC', 'AB'],
            42: ['AB', 'BC', 'BC', 'AC', 'AC', 'AB', 'AB'],
            43: ['BC', 'BC', 'AC', 'AC', 'AB', 'AB', 'BC'],
            44: ['BC', 'AC', 'AC', 'AB', 'AB', 'BC', 'BC'],
            45: ['AC', 'AC', 'AB', 'AB', 'BC', 'BC', 'AC'],
            46: ['AC', 'AB', 'AB', 'BC', 'BC', 'AC', 'AC'],
            47: ['AB', 'AB', 'BC', 'BC', 'AC', 'AC', 'AB'],
            48: ['AB', 'BC', 'BC', 'AC', 'AC', 'AB', 'AB'],
            49: ['BC', 'BC', 'AC', 'AC', 'AB', 'AB', 'BC'],
            50: ['BC', 'AC', 'AC', 'AB', 'AB', 'BC', 'BC'],
            51: ['AC', 'AC', 'AB', 'AB', 'BC', 'BC', 'AC'],
            52: ['AC', 'AB', 'AB', 'BC', 'BC', 'AC', 'AC'],
            53: ['AB', 'AB', 'BC', 'BC', 'AC', 'AC', 'AB']
        };

        function extractGroupLetter(role) {
            if (!role) return null;
            const normalized = role.trim().toUpperCase();
            if (normalized === 'A' || normalized === 'GRUP A' || normalized === 'GRUPA A' || normalized.endsWith(' A')) {
                return 'A';
            }
            if (normalized === 'B' || normalized === 'GRUP B' || normalized === 'GRUPA B' || normalized.endsWith(' B')) {
                return 'B';
            }
            if (normalized === 'C' || normalized === 'GRUP C' || normalized === 'GRUPA C' || normalized.endsWith(' C')) {
                return 'C';
            }
            return null;
        }

        function getDayPairsForYearWeek(year, week) {
            if (year === 2026 && SHEET_PAIR_ROTATION_2026[week]) {
                return SHEET_PAIR_ROTATION_2026[week];
            }
            const refMonday = new Date(Date.UTC(2025, 11, 29));
            const days = getDatesOfISOWeek(year, week);
            const targetMonday = days[0];
            const diffWeeks = Math.round((targetMonday.getTime() - refMonday.getTime()) / (7 * 86400000));
            const cycleMod = ((diffWeeks % 3) + 3) % 3;
            return SHEET_PAIR_ROTATION_2026[cycleMod + 1];
        }

        function buildGroupScheduleForWeek(groupLetter, year, week, startTime = '07:00') {
            const pairs = getDayPairsForYearWeek(year, week);
            const empSched = {};
            for (let d = 0; d < 7; d++) {
                const activePair = pairs[d] || '';
                if (activePair.includes(groupLetter)) {
                    empSched[d] = createSlot('work', startTime);
                } else {
                    empSched[d] = createSlot('vrij', 'Liber');
                }
            }
            return empSched;
        }

        function markManualOverride(weekKey, empId, dayIndex) {
            if (!state.manualOverrides) state.manualOverrides = {};
            if (!state.manualOverrides[weekKey]) state.manualOverrides[weekKey] = {};
            if (!state.manualOverrides[weekKey][empId]) state.manualOverrides[weekKey][empId] = {};
            state.manualOverrides[weekKey][empId][dayIndex] = true;
        }

        function clearManualOverridesForEmpWeek(weekKey, empId) {
            if (state.manualOverrides && state.manualOverrides[weekKey] && state.manualOverrides[weekKey][empId]) {
                delete state.manualOverrides[weekKey][empId];
            }
        }

        function ensureWeekInitialized(year, week) {
            const weekKey = getWeekKey(year, week);
            if (!state.schedules[weekKey]) {
                state.schedules[weekKey] = {};
            }

            (state.employees || []).forEach(emp => {
                const grp = extractGroupLetter(emp.role);
                if (!grp) return;

                if (!state.schedules[weekKey][emp.id]) {
                    const defaultStart = emp.id === 'emp_iulian' ? '08:00' : '07:00';
                    state.schedules[weekKey][emp.id] = buildGroupScheduleForWeek(grp, year, week, defaultStart);
                    return;
                }

                const baseGroupSched = buildGroupScheduleForWeek(grp, year, week, '07:00');
                const overrides = state.manualOverrides?.[weekKey]?.[emp.id] || {};
                for (let d = 0; d < 7; d++) {
                    if (!overrides[d] && !state.schedules[weekKey][emp.id][d]) {
                        state.schedules[weekKey][emp.id][d] = { ...baseGroupSched[d] };
                    }
                }
            });
        }

        function getDefaultWorkbookSchedules() {
            const schedules = {};
            for (let w = 1; w <= 53; w++) {
                const wkKey = getWeekKey(2026, w);
                const weekMap = {
                    emp_daniel: {
                        0: createSlot('work', '07:00'),
                        1: createSlot('work', '07:00'),
                        2: createSlot('work', '07:00'),
                        3: createSlot('work', '07:00'),
                        4: createSlot('work', '07:00'),
                        5: createSlot('vrij', 'Liber'),
                        6: createSlot('vrij', 'Liber')
                    },
                    emp_druvis: {
                        0: createSlot('vrij', 'Liber'),
                        1: createSlot('work', '07:00'),
                        2: createSlot('work', '07:00'),
                        3: createSlot('work', '07:00'),
                        4: createSlot('work', '07:00'),
                        5: createSlot('work', w === 47 ? '09:00' : '07:00'),
                        6: createSlot('vrij', 'Liber')
                    },
                    emp_ghenadie: {
                        0: createSlot('work', '10:00'),
                        1: createSlot('work', '10:00'),
                        2: createSlot('work', '10:00'),
                        3: createSlot('work', '10:00'),
                        4: createSlot('work', '10:00'),
                        5: createSlot('vrij', 'Liber'),
                        6: createSlot('vrij', 'Liber')
                    },
                    emp_evelina: buildGroupScheduleForWeek('A', 2026, w, '07:00'),
                    emp_andrei: buildGroupScheduleForWeek('B', 2026, w, '07:00'),
                    emp_albert: w === 47
                        ? {
                            0: createSlot('vakantie', 'Vacanță'),
                            1: createSlot('vakantie', 'Vacanță'),
                            2: createSlot('vakantie', 'Vacanță'),
                            3: createSlot('vakantie', 'Vacanță'),
                            4: createSlot('vakantie', 'Vacanță'),
                            5: createSlot('vakantie', 'Vacanță'),
                            6: createSlot('vakantie', 'Vacanță')
                        }
                        : buildGroupScheduleForWeek('C', 2026, w, '07:00'),
                    emp_iulian: buildGroupScheduleForWeek('A', 2026, w, '08:00')
                };

                if (w === 47) {
                    weekMap.emp_andrei[5] = createSlot('extra', '07:00', 'Extra');
                    weekMap.emp_iulian[2] = createSlot('extra', '08:00', 'Extra');
                }

                schedules[wkKey] = weekMap;
            }

            return schedules;
        }

        function loadAppState() {
            state.year = 2026;
            state.week = 47;

            const defaultEmployees = [
                { id: 'emp_daniel', name: 'Daniel', role: '' },
                { id: 'emp_druvis', name: 'Druvis', role: '' },
                { id: 'emp_ghenadie', name: 'Ghenadie', role: '' },
                { id: 'emp_evelina', name: 'Evelina', role: 'Grup A' },
                { id: 'emp_andrei', name: 'Andrei', role: 'Grup B' },
                { id: 'emp_albert', name: 'Albert', role: 'Grup C' },
                { id: 'emp_iulian', name: 'Iulian', role: 'Grup A' }
            ];

            const raw = safeGetStorage(STORAGE_KEY);
            if (raw) {
                try {
                    const parsed = JSON.parse(raw);
                    if (parsed && Array.isArray(parsed.employees)) {
                        state.employees = parsed.employees;
                        state.schedules = (parsed.schedules && typeof parsed.schedules === 'object')
                            ? parsed.schedules
                            : getDefaultWorkbookSchedules();
                        state.manualOverrides = (parsed.manualOverrides && typeof parsed.manualOverrides === 'object')
                            ? parsed.manualOverrides
                            : {};
                        state.customData = (parsed.customData && typeof parsed.customData === 'object')
                            ? parsed.customData
                            : {};
                        markPendingSave(false);
                        return;
                    }
                } catch (err) {
                    // Fallback to default state
                }
            }

            state.employees = defaultEmployees;
            state.schedules = getDefaultWorkbookSchedules();
            state.manualOverrides = {};
            state.customData = {};
            markPendingSave(false);
            persistEverythingNow();
        }

        function saveAppState() {
            persistEverythingNow();
        }

        /* =====================================================================
           5. WEEK & YEAR NAVIGATION
           ===================================================================== */
        function populateWeekDropdown() {
            const yearSelect = document.getElementById('year-select');
            const weekSelect = document.getElementById('week-select');

            yearSelect.value = String(state.year);
            const totalWeeks = getWeeksCountInYear(state.year);
            if (state.week > totalWeeks) state.week = totalWeeks;

            weekSelect.innerHTML = '';
            for (let w = 1; w <= totalWeeks; w++) {
                const days = getDatesOfISOWeek(state.year, w);
                const opt = document.createElement('option');
                opt.value = String(w);
                opt.textContent = `${t('weekPrefix')} ${String(w).padStart(2, '0')} (${formatShortDate(days[0])} – ${formatShortDate(days[6])})`;
                if (w === state.week) opt.selected = true;
                weekSelect.appendChild(opt);
            }
        }

        function onYearChange() {
            state.year = parseInt(document.getElementById('year-select').value, 10);
            populateWeekDropdown();
            ensureWeekInitialized(state.year, state.week);
            saveAppState();
            renderScheduleTable();
        }

        function onWeekChange() {
            state.week = parseInt(document.getElementById('week-select').value, 10);
            ensureWeekInitialized(state.year, state.week);
            saveAppState();
            renderScheduleTable();
        }

        function changeWeek(delta) {
            let y = state.year;
            let w = state.week + delta;

            if (w < 1) {
                if (y > 2026) {
                    y -= 1;
                    w = getWeeksCountInYear(y);
                } else {
                    showToast(t('toastFirstWeek2026'));
                    return;
                }
            } else {
                const maxW = getWeeksCountInYear(y);
                if (w > maxW) {
                    if (y < 2027) {
                        y += 1;
                        w = 1;
                    } else {
                        showToast(t('toastLastWeek2027'));
                        return;
                    }
                }
            }

            state.year = y;
            state.week = w;
            populateWeekDropdown();
            ensureWeekInitialized(state.year, state.week);
            saveAppState();
            renderScheduleTable();
        }

        function goToWeek47() {
            state.year = 2026;
            state.week = 47;
            populateWeekDropdown();
            ensureWeekInitialized(state.year, state.week);
            saveAppState();
            renderScheduleTable();
            showToast(t('toastWeek47'));
        }

        /* =====================================================================
           6. TABLE RENDERING
           ===================================================================== */
        function escapeHTML(str) {
            return String(str)
                .replace(/&/g, '&amp;')
                .replace(/</g, '&lt;')
                .replace(/>/g, '&gt;')
                .replace(/"/g, '&quot;');
        }

        function isWorkingDaySlot(slot) {
            if (!slot || !slot.label) return false;
            const kind = detectSlotKind(slot);
            return kind === 'work' || kind === 'extra';
        }

        function renderScheduleTable() {
            ensureWeekInitialized(state.year, state.week);
            const days = getDatesOfISOWeek(state.year, state.week);
            const weekKey = getWeekKey(state.year, state.week);
            const weekData = state.schedules[weekKey] || {};
            const dayNames = getDayNames();

            const fsLabel = document.getElementById('fs-week-label');
            if (fsLabel) {
                fsLabel.textContent = `${t('weekPrefix')} ${String(state.week).padStart(2, '0')} • ${formatShortDate(days[0])} – ${formatShortDate(days[6])} ${state.year}`;
            }

            const headRow = document.getElementById('table-head-row');
            let headHTML = `<th class="sticky-col" dir="ltr">${escapeHTML(t('colEmployee'))}</th>`;

            for (let i = 0; i < 7; i++) {
                const isWeekend = (i === 5 || i === 6);
                const isToday = isTodayUTC(days[i]);
                let cls = '';
                if (isToday) cls = 'today-col';
                else if (isWeekend) cls = 'weekend-col';

                const todayDotHTML = isToday ? `<span class="today-red-dot" aria-hidden="true"></span>` : '';

                headHTML += `
                    <th class="${cls}">
                        <span class="day-name-row"><span class="day-name">${escapeHTML(dayNames[i])}</span>${todayDotHTML}</span>
                        <span class="day-date">${formatShortDate(days[i])}</span>
                    </th>
                `;
            }

            headHTML += `<th>${escapeHTML(t('colDays'))}</th>`;
            headRow.innerHTML = headHTML;

            const tbody = document.getElementById('table-body');
            let bodyHTML = '';
            let grandTotalDays = 0;
            const dailyWorkingCount = [0, 0, 0, 0, 0, 0, 0];

            if (state.employees.length === 0) {
                bodyHTML = `
                    <tr>
                        <td colspan="9" style="padding:36px 16px; text-align:center; color:var(--text-muted);">
                            ${t('noEmployeesTable')}
                        </td>
                    </tr>
                `;
            } else {
                state.employees.forEach(emp => {
                    const empSchedule = weekData[emp.id] || {};
                    let empWorkedDays = 0;
                    const displayRole = getLocalizedEmployeeRole(emp.role);

                    let cellsHTML = `
                        <td class="sticky-col" dir="ltr">
                            <div class="emp-cell-wrap" dir="ltr">
                                <div class="emp-info" dir="ltr">
                                    <div class="emp-name" dir="ltr" title="${escapeHTML(emp.name)}">${escapeHTML(emp.name)}</div>
                                    ${displayRole ? `<div class="emp-role" dir="ltr" title="${escapeHTML(displayRole)}">${escapeHTML(displayRole)}</div>` : ''}
                                </div>
                                <button type="button" class="emp-del-btn" data-delete-emp="${escapeHTML(emp.id)}" title="${escapeHTML(t('removeEmployeeTitle'))}">✕</button>
                            </div>
                        </td>
                    `;

                    for (let d = 0; d < 7; d++) {
                        const isWeekend = (d === 5 || d === 6);
                        const slot = empSchedule[d];
                        const tdClass = isWeekend ? 'weekend-cell' : '';

                        if (slot && slot.label) {
                            const kind = detectSlotKind(slot);
                            const worked = (kind === 'work' || kind === 'extra');
                            if (worked) {
                                empWorkedDays += 1;
                                dailyWorkingCount[d] += 1;
                            }

                            const typeClass = `shift-${kind}`;
                            const displayLabel = getLocalizedSlotLabel(slot);
                            const subText = slot.note ? slot.note : '';

                            cellsHTML += `
                                <td class="${tdClass}">
                                    <div class="shift-slot ${typeClass}" data-emp-id="${escapeHTML(emp.id)}" data-day-index="${d}">
                                        <span class="shift-title">${escapeHTML(displayLabel)}</span>
                                        ${subText ? `<span class="shift-sub">${escapeHTML(subText)}</span>` : ''}
                                    </div>
                                </td>
                            `;
                        } else {
                            cellsHTML += `
                                <td class="${tdClass}">
                                    <div class="shift-slot shift-empty" data-emp-id="${escapeHTML(emp.id)}" data-day-index="${d}" title="${escapeHTML(t('setCellTitle'))}">
                                        +
                                    </div>
                                </td>
                            `;
                        }
                    }

                    grandTotalDays += empWorkedDays;
                    const dayWord = empWorkedDays === 1 ? t('daySingular') : t('dayPlural');

                    cellsHTML += `
                        <td>
                            <span class="days-count-badge">${empWorkedDays} ${escapeHTML(dayWord)}</span>
                        </td>
                    `;

                    bodyHTML += `<tr>${cellsHTML}</tr>`;
                });
            }

            tbody.innerHTML = bodyHTML;

            const footRow = document.getElementById('table-foot-row');
            let footHTML = `<td class="sticky-col" dir="ltr">${escapeHTML(t('presentPerDay'))}</td>`;
            for (let d = 0; d < 7; d++) {
                footHTML += `<td>${dailyWorkingCount[d]}</td>`;
            }
            footHTML += `<td>${grandTotalDays}</td>`;
            footRow.innerHTML = footHTML;

            document.getElementById('stat-emp-count').textContent = String(state.employees.length);
            document.getElementById('stat-total-days').textContent = `${grandTotalDays} ${t('dayPlural')}`;
            updateSaveButtonVisualState();
        }

        /* =====================================================================
           7. SHIFT MODAL, EXTRA DAY & EMPLOYEE MANAGEMENT
           ===================================================================== */
        function openShiftModal(empId, dayIndex) {
            const emp = state.employees.find(e => e.id === empId);
            if (!emp) return;

            state.editingCell = { empId, dayIndex };
            const days = getDatesOfISOWeek(state.year, state.week);
            const weekKey = getWeekKey(state.year, state.week);
            const currentSlot = state.schedules[weekKey]?.[empId]?.[dayIndex];

            document.getElementById('shift-modal-title').textContent = t('shiftModalTitleDay', { day: getDayNames()[dayIndex] });
            document.getElementById('shift-modal-subtitle').textContent = t('shiftModalSubtitle', {
                name: emp.name,
                date: formatShortDate(days[dayIndex]),
                year: state.year
            });

            const resetGroupBtn = document.getElementById('reset-group-week-btn');
            if (resetGroupBtn) {
                resetGroupBtn.style.display = extractGroupLetter(emp.role) ? 'inline-flex' : 'none';
            }

            if (currentSlot && currentSlot.label) {
                const kind = detectSlotKind(currentSlot);
                document.getElementById('custom-label').value = getLocalizedSlotLabel(currentSlot);
                document.getElementById('custom-status-type').value = kind === 'empty' ? 'work' : kind;
                document.getElementById('custom-note').value = currentSlot.note || (kind === 'extra' ? 'Extra' : '');
            } else {
                document.getElementById('custom-label').value = '07:00';
                document.getElementById('custom-status-type').value = 'work';
                document.getElementById('custom-note').value = '';
            }

            document.getElementById('shift-modal').classList.add('open');
        }

        function closeShiftModal() {
            document.getElementById('shift-modal').classList.remove('open');
            state.editingCell = null;
        }

        function selectPreset(type, label, isExtra) {
            let resolvedLabel = label;
            if (label === '__VRIJ__') resolvedLabel = t('statusVrijLabel');
            if (label === '__VAKANTIE__') resolvedLabel = t('statusVakantieLabel');

            document.getElementById('custom-status-type').value = type;
            document.getElementById('custom-label').value = resolvedLabel;
            document.getElementById('custom-note').value = isExtra ? 'Extra' : '';
        }

        function getModalShiftObject() {
            let label = document.getElementById('custom-label').value.trim() || '07:00';
            let note = document.getElementById('custom-note').value.trim();
            let type = document.getElementById('custom-status-type').value;

            const upper = label.toUpperCase();
            if (ALL_VRIJ_WORDS.has(upper)) {
                type = 'vrij';
                label = t('statusVrijLabel');
            } else if (ALL_VAKANTIE_WORDS.has(upper)) {
                type = 'vakantie';
                label = t('statusVakantieLabel');
            } else if (type === 'extra' || note.toUpperCase() === 'EXTRA' || upper.includes('EXTRA')) {
                type = 'extra';
                if (!note) note = 'Extra';
            }

            return { type, label, note };
        }

        function saveShiftModal() {
            if (!state.editingCell) return;
            const { empId, dayIndex } = state.editingCell;
            const weekKey = getWeekKey(state.year, state.week);

            if (!state.schedules[weekKey]) state.schedules[weekKey] = {};
            if (!state.schedules[weekKey][empId]) state.schedules[weekKey][empId] = {};

            state.schedules[weekKey][empId][dayIndex] = getModalShiftObject();
            markManualOverride(weekKey, empId, dayIndex);
            markPendingSave(true);
            saveAppState();
            closeShiftModal();
            renderScheduleTable();
            showToast(t('toastShiftSaved'));
        }

        function addExtraDayFromModal() {
            if (!state.editingCell) return;
            const { empId, dayIndex } = state.editingCell;
            const weekKey = getWeekKey(state.year, state.week);

            if (!state.schedules[weekKey]) state.schedules[weekKey] = {};
            if (!state.schedules[weekKey][empId]) state.schedules[weekKey][empId] = {};

            const currentSlot = state.schedules[weekKey][empId][dayIndex];
            let targetDay = dayIndex;
            if (currentSlot && isWorkingDaySlot(currentSlot)) {
                for (let d = 0; d < 7; d++) {
                    const s = state.schedules[weekKey][empId][d];
                    if (!s || !isWorkingDaySlot(s)) {
                        targetDay = d;
                        break;
                    }
                }
            }

            let startLabel = document.getElementById('custom-label').value.trim();
            if (!startLabel || ALL_VRIJ_WORDS.has(startLabel.toUpperCase()) || ALL_VAKANTIE_WORDS.has(startLabel.toUpperCase())) {
                startLabel = '07:00';
            }

            state.schedules[weekKey][empId][targetDay] = {
                type: 'extra',
                label: startLabel,
                note: 'Extra'
            };
            markManualOverride(weekKey, empId, targetDay);
            markPendingSave(true);
            saveAppState();
            closeShiftModal();
            renderScheduleTable();
            showToast(t('toastExtraDayAdded', { day: getDayNames()[targetDay] }));
        }

        function reapplyGroupScheduleForEditingEmp() {
            if (!state.editingCell) return;
            const { empId } = state.editingCell;
            const emp = state.employees.find(e => e.id === empId);
            if (!emp) return;
            const grp = extractGroupLetter(emp.role);
            if (!grp) return;

            const weekKey = getWeekKey(state.year, state.week);
            clearManualOverridesForEmpWeek(weekKey, empId);
            if (!state.schedules[weekKey]) state.schedules[weekKey] = {};
            state.schedules[weekKey][empId] = buildGroupScheduleForWeek(grp, state.year, state.week, '07:00');
            markPendingSave(true);
            saveAppState();
            closeShiftModal();
            renderScheduleTable();
            showToast(t('toastGroupReapplied'));
        }

        function applyToMonFri() {
            if (!state.editingCell) return;
            const { empId } = state.editingCell;
            const weekKey = getWeekKey(state.year, state.week);
            const shiftObj = getModalShiftObject();

            if (!state.schedules[weekKey]) state.schedules[weekKey] = {};
            if (!state.schedules[weekKey][empId]) state.schedules[weekKey][empId] = {};

            for (let d = 0; d < 5; d++) {
                state.schedules[weekKey][empId][d] = { ...shiftObj };
                markManualOverride(weekKey, empId, d);
            }
            markPendingSave(true);
            saveAppState();
            closeShiftModal();
            renderScheduleTable();
            showToast(t('toastAppliedMonFri'));
        }

        function clearCurrentCell() {
            if (!state.editingCell) return;
            const { empId, dayIndex } = state.editingCell;
            const weekKey = getWeekKey(state.year, state.week);

            if (state.schedules[weekKey]?.[empId]) {
                delete state.schedules[weekKey][empId][dayIndex];
            }
            markManualOverride(weekKey, empId, dayIndex);
            markPendingSave(true);
            saveAppState();
            closeShiftModal();
            renderScheduleTable();
            showToast(t('toastCellCleared'));
        }

        function openAddEmployeeModal() {
            document.getElementById('new-emp-name').value = '';
            document.getElementById('new-emp-role').value = '';
            document.getElementById('emp-modal').classList.add('open');
            setTimeout(() => document.getElementById('new-emp-name').focus(), 50);
        }

        function closeAddEmployeeModal() {
            document.getElementById('emp-modal').classList.remove('open');
        }

        function submitNewEmployee(event) {
            event.preventDefault();
            const nameInput = document.getElementById('new-emp-name');
            const roleInput = document.getElementById('new-emp-role');
            const name = nameInput.value.trim();
            if (!name) return;

            const newEmp = {
                id: 'emp_' + Date.now() + '_' + Math.random().toString(36).slice(2, 6),
                name: name,
                role: roleInput.value.trim() || t('empDefaultRole')
            };

            state.employees.push(newEmp);
            ensureWeekInitialized(state.year, state.week);
            markPendingSave(true);
            saveAppState();
            closeAddEmployeeModal();
            renderScheduleTable();
            showToast(t('toastEmpAdded', { name: name }));
        }

        function deleteEmployee(empId) {
            state.employees = state.employees.filter(e => e.id !== empId);
            Object.keys(state.schedules || {}).forEach(wk => {
                if (state.schedules[wk] && Object.prototype.hasOwnProperty.call(state.schedules[wk], empId)) {
                    delete state.schedules[wk][empId];
                }
            });
            Object.keys(state.manualOverrides || {}).forEach(wk => {
                if (state.manualOverrides[wk] && Object.prototype.hasOwnProperty.call(state.manualOverrides[wk], empId)) {
                    delete state.manualOverrides[wk][empId];
                }
            });
            markPendingSave(true);
            saveAppState();
            renderScheduleTable();
            showToast(t('toastEmpRemoved'));
        }

        function copyPreviousWeek() {
            let prevY = state.year;
            let prevW = state.week - 1;
            if (prevW < 1) {
                if (prevY > 2026) {
                    prevY -= 1;
                    prevW = getWeeksCountInYear(prevY);
                } else {
                    showToast(t('toastNoPrevWeek'));
                    return;
                }
            }

            const prevKey = getWeekKey(prevY, prevW);
            const currKey = getWeekKey(state.year, state.week);
            const prevData = state.schedules[prevKey];

            if (!prevData || Object.keys(prevData).length === 0) {
                showToast(t('toastPrevWeekEmpty', { week: String(prevW).padStart(2, '0') }));
                return;
            }

            state.schedules[currKey] = JSON.parse(JSON.stringify(prevData));
            if (state.manualOverrides?.[prevKey]) {
                state.manualOverrides[currKey] = JSON.parse(JSON.stringify(state.manualOverrides[prevKey]));
            }
            markPendingSave(true);
            saveAppState();
            renderScheduleTable();
            showToast(t('toastWeekCopied', { week: String(prevW).padStart(2, '0') }));
        }

        /* =====================================================================
           8. WEEK-ONLY SHARE TEXT, CANVAS PNG RENDERING & WHATSAPP / EMAIL SHARE
           ===================================================================== */
        function buildScheduleShareText() {
            const days = getDatesOfISOWeek(state.year, state.week);
            const weekNumStr = String(state.week).padStart(2, '0');
            const rangeStr = `${formatShortDate(days[0])} – ${formatShortDate(days[6])} ${state.year}`;
            return t('shareTextTitle', { week: weekNumStr, range: rangeStr });
        }

        function copyTextFallback(text) {
            try {
                const ta = document.createElement('textarea');
                ta.value = text;
                ta.setAttribute('readonly', '');
                ta.style.position = 'fixed';
                ta.style.top = '-9999px';
                ta.style.left = '-9999px';
                document.body.appendChild(ta);
                ta.focus();
                ta.select();
                const ok = document.execCommand('copy');
                document.body.removeChild(ta);
                return ok;
            } catch (err) {
                return false;
            }
        }

        async function copyScheduleTextToClipboard(silent = false) {
            const text = buildScheduleShareText();
            let copied = false;
            try {
                if (navigator.clipboard && typeof navigator.clipboard.writeText === 'function') {
                    await navigator.clipboard.writeText(text);
                    copied = true;
                }
            } catch (err) {
                copied = false;
            }
            if (!copied) {
                copied = copyTextFallback(text);
            }
            if (!silent) {
                if (copied) {
                    showToast(t('toastTextCopied'));
                } else {
                    showToast(t('toastTextCopyFail'));
                }
            }
            return copied;
        }

        function isAndroidWebView() {
            const ua = (navigator.userAgent || '').toLowerCase();
            return ua.includes('wv') || (ua.includes('android') && ua.includes('version/'));
        }

        function triggerAnchorNavigation(url, newTab = false) {
            try {
                const a = document.createElement('a');
                a.href = url;
                if (newTab) {
                    a.target = '_blank';
                    a.rel = 'noopener noreferrer';
                }
                a.style.display = 'none';
                document.body.appendChild(a);
                a.click();
                document.body.removeChild(a);
                return true;
            } catch (err) {
                return false;
            }
        }

        async function openWhatsAppWithTextSafe(title, weekLabelText) {
            await copyScheduleTextToClipboard(true);

            if (typeof navigator !== 'undefined' && typeof navigator.share === 'function') {
                try {
                    await navigator.share({
                        title: title,
                        text: weekLabelText
                    });
                    showToast(t('toastOpenedWaText'));
                    return;
                } catch (err) {
                    if (err && err.name === 'AbortError') {
                        showToast(t('toastShareCancelled'));
                        return;
                    }
                }
            }

            const encodedText = encodeURIComponent(weekLabelText);

            if (isAndroidWebView() || /android/i.test(navigator.userAgent || '')) {
                const fallbackWaWeb = encodeURIComponent(`https://wa.me/?text=${encodedText}`);
                const androidIntentUrl = `intent://send?text=${encodedText}#Intent;scheme=whatsapp;package=com.whatsapp;S.browser_fallback_url=${fallbackWaWeb};end`;
                if (triggerAnchorNavigation(androidIntentUrl, false)) {
                    showToast(t('toastOpenedWaText'));
                    return;
                }
            }

            const waUrl = `https://wa.me/?text=${encodedText}`;
            const win = window.open(waUrl, '_blank', 'noopener,noreferrer');
            if (!win) {
                triggerAnchorNavigation(waUrl, true);
            }
            showToast(t('toastOpenedWaText'));
        }

        async function shareScheduleTextOnWhatsApp() {
            const days = getDatesOfISOWeek(state.year, state.week);
            const weekNumStr = String(state.week).padStart(2, '0');
            const rangeStr = `${formatShortDate(days[0])} – ${formatShortDate(days[6])} ${state.year}`;
            const title = t('shareTextTitle', { week: weekNumStr, range: rangeStr });
            const weekOnlyText = buildScheduleShareText();

            await openWhatsAppWithTextSafe(title, weekOnlyText);
        }

        function getSlotColors(kind) {
            if (kind === 'work') {
                return { bg: '#ecfdf5', border: '#a7f3d0', text: '#065f46', sub: '#047857' };
            }
            if (kind === 'extra') {
                return { bg: '#fffbeb', border: '#fde68a', text: '#92400e', sub: '#b45309' };
            }
            if (kind === 'vakantie') {
                return { bg: '#fff1f2', border: '#fecdd3', text: '#be123c', sub: '#e11d48' };
            }
            if (kind === 'vrij') {
                return { bg: '#f1f5f9', border: '#cbd5e1', text: '#475569', sub: '#64748b' };
            }
            return { bg: '#f8fafc', border: '#e2e8f0', text: '#94a3b8', sub: '#94a3b8' };
        }

        function drawRoundedRect(ctx, x, y, w, h, r) {
            const radius = Math.min(r, w / 2, h / 2);
            ctx.beginPath();
            ctx.moveTo(x + radius, y);
            ctx.arcTo(x + w, y, x + w, y + h, radius);
            ctx.arcTo(x + w, y + h, x, y + h, radius);
            ctx.arcTo(x, y + h, x, y, radius);
            ctx.arcTo(x, y, x + w, y, radius);
            ctx.closePath();
        }

        function renderScheduleToPNG() {
            try {
                ensureWeekInitialized(state.year, state.week);
                const days = getDatesOfISOWeek(state.year, state.week);
                const weekKey = getWeekKey(state.year, state.week);
                const weekData = state.schedules[weekKey] || {};
                const weekNumStr = String(state.week).padStart(2, '0');
                const rangeStr = `${formatShortDate(days[0])} – ${formatShortDate(days[6])} ${state.year}`;
                const dayNames = getDayNames();

                const padX = 24;
                const padTop = 22;
                const bannerHeight = 68;
                const tableTop = padTop + bannerHeight + 14;
                const headerHeight = 52;
                const rowHeight = 56;
                const footerHeight = 44;
                const legendHeight = 36;

                const empRowsCount = Math.max(state.employees.length, 1);
                const tableHeight = headerHeight + (empRowsCount * rowHeight) + footerHeight;
                const totalWidth = 1140;
                const totalHeight = tableTop + tableHeight + legendHeight + 24;

                const rawArea = totalWidth * totalHeight;
                const scale = rawArea > 3500000 ? 1 : 2;

                const canvas = document.createElement('canvas');
                canvas.width = Math.round(totalWidth * scale);
                canvas.height = Math.round(totalHeight * scale);

                const ctx = canvas.getContext('2d', { alpha: false });
                if (!ctx) return null;

                ctx.save();
                ctx.scale(scale, scale);

                ctx.globalAlpha = 1;
                ctx.fillStyle = '#f8fafc';
                ctx.fillRect(0, 0, totalWidth, totalHeight);

                ctx.fillStyle = '#0f172a';
                drawRoundedRect(ctx, padX, padTop, totalWidth - padX * 2, bannerHeight, 12);
                ctx.fill();

                ctx.fillStyle = '#ffffff';
                ctx.font = '800 20px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                ctx.textAlign = 'left';
                ctx.textBaseline = 'middle';
                ctx.fillText(t('canvasBannerTitle', { week: weekNumStr, range: rangeStr }), padX + 18, padTop + 25);

                let grandTotalDays = 0;
                const dailyWorkingCount = [0, 0, 0, 0, 0, 0, 0];

                state.employees.forEach(emp => {
                    const empSchedule = weekData[emp.id] || {};
                    for (let d = 0; d < 7; d++) {
                        const slot = empSchedule[d];
                        if (slot && slot.label && isWorkingDaySlot(slot)) {
                            grandTotalDays += 1;
                            dailyWorkingCount[d] += 1;
                        }
                    }
                });

                ctx.fillStyle = '#cbd5e1';
                ctx.font = '600 13px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                ctx.fillText(
                    t('canvasBannerStats', { count: state.employees.length, days: grandTotalDays }),
                    padX + 18,
                    padTop + 49
                );

                const innerW = totalWidth - padX * 2;
                const empColW = Math.round(innerW * 0.21);
                const daysCntColW = Math.round(innerW * 0.09);
                const dayColW = Math.floor((innerW - empColW - daysCntColW) / 7);
                const adjustedDaysCntW = innerW - empColW - (dayColW * 7);

                const colX = [padX];
                for (let i = 0; i < 7; i++) {
                    colX.push(colX[colX.length - 1] + dayColW);
                }
                colX.push(colX[colX.length - 1] + adjustedDaysCntW);

                const colWidths = [empColW, dayColW, dayColW, dayColW, dayColW, dayColW, dayColW, dayColW, adjustedDaysCntW];

                ctx.fillStyle = '#ffffff';
                drawRoundedRect(ctx, padX, tableTop, innerW, tableHeight, 12);
                ctx.fill();

                for (let c = 0; c < 9; c++) {
                    const x = colX[c];
                    const w = colWidths[c];
                    const isTodayCol = (c >= 1 && c <= 7) ? isTodayUTC(days[c - 1]) : false;

                    if (c === 0) {
                        ctx.fillStyle = '#4f46e5';
                    } else if (c === 6 || c === 7) {
                        ctx.fillStyle = '#fef3c7';
                    } else if (isTodayCol) {
                        ctx.fillStyle = '#e0e7ff';
                    } else {
                        ctx.fillStyle = '#f1f5f9';
                    }

                    ctx.fillRect(x, tableTop, w, headerHeight);
                    ctx.strokeStyle = '#cbd5e1';
                    ctx.lineWidth = 1;
                    ctx.strokeRect(x, tableTop, w, headerHeight);

                    if (c === 0) {
                        ctx.fillStyle = '#ffffff';
                        ctx.font = '800 13px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                        ctx.textAlign = 'left';
                        ctx.textBaseline = 'middle';
                        ctx.fillText(t('colEmployeeDetails'), x + 12, tableTop + headerHeight / 2);
                    } else if (c >= 1 && c <= 7) {
                        const dayIdx = c - 1;
                        const labelText = dayNames[dayIdx];
                        ctx.fillStyle = (c === 6 || c === 7) ? '#92400e' : '#0f172a';
                        ctx.font = '800 13px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                        ctx.textAlign = 'center';
                        ctx.textBaseline = 'middle';
                        ctx.fillText(labelText, x + w / 2, tableTop + 19);

                        if (isTodayCol) {
                            const textW = ctx.measureText(labelText).width;
                            const dotX = x + w / 2 + textW / 2 + 8;
                            ctx.fillStyle = '#e11d48';
                            ctx.beginPath();
                            ctx.arc(dotX, tableTop + 19, 4.5, 0, Math.PI * 2);
                            ctx.fill();
                        }

                        ctx.fillStyle = (c === 6 || c === 7) ? '#b45309' : '#64748b';
                        ctx.font = '600 11px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                        ctx.fillText(formatShortDate(days[dayIdx]), x + w / 2, tableTop + 37);
                    } else {
                        ctx.fillStyle = '#0f172a';
                        ctx.font = '800 13px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                        ctx.textAlign = 'center';
                        ctx.textBaseline = 'middle';
                        ctx.fillText(t('colDaysUpper'), x + w / 2, tableTop + headerHeight / 2);
                    }
                }

                if (state.employees.length === 0) {
                    const y = tableTop + headerHeight;
                    ctx.fillStyle = '#ffffff';
                    ctx.fillRect(padX, y, innerW, rowHeight);
                    ctx.strokeStyle = '#e2e8f0';
                    ctx.strokeRect(padX, y, innerW, rowHeight);
                    ctx.fillStyle = '#64748b';
                    ctx.font = '600 14px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                    ctx.textAlign = 'center';
                    ctx.textBaseline = 'middle';
                    ctx.fillText(t('noEmployeesCanvas'), padX + innerW / 2, y + rowHeight / 2);
                } else {
                    state.employees.forEach((emp, rIdx) => {
                        const y = tableTop + headerHeight + rIdx * rowHeight;
                        const empSchedule = weekData[emp.id] || {};
                        let empWorkedDays = 0;
                        const displayRole = getLocalizedEmployeeRole(emp.role);

                        ctx.fillStyle = rIdx % 2 === 0 ? '#ffffff' : '#f8fafc';
                        ctx.fillRect(colX[0], y, colWidths[0], rowHeight);
                        ctx.strokeStyle = '#e2e8f0';
                        ctx.strokeRect(colX[0], y, colWidths[0], rowHeight);

                        ctx.fillStyle = '#4f46e5';
                        ctx.fillRect(colX[0], y, 4, rowHeight);

                        ctx.fillStyle = '#0f172a';
                        ctx.font = '800 14px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                        ctx.textAlign = 'left';
                        ctx.textBaseline = 'middle';
                        const nameY = displayRole ? y + 20 : y + rowHeight / 2;
                        ctx.fillText(emp.name, colX[0] + 12, nameY);

                        if (displayRole) {
                            ctx.fillStyle = '#4f46e5';
                            ctx.font = '700 11px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                            ctx.fillText(displayRole, colX[0] + 12, y + 38);
                        }

                        for (let d = 0; d < 7; d++) {
                            const cx = colX[d + 1];
                            const cw = colWidths[d + 1];
                            const slot = empSchedule[d];

                            ctx.fillStyle = (d === 5 || d === 6) ? '#fffbeb' : (rIdx % 2 === 0 ? '#ffffff' : '#f8fafc');
                            ctx.fillRect(cx, y, cw, rowHeight);
                            ctx.strokeStyle = '#e2e8f0';
                            ctx.strokeRect(cx, y, cw, rowHeight);

                            const kind = detectSlotKind(slot);
                            const isWorked = (kind === 'work' || kind === 'extra');
                            if (isWorked) empWorkedDays += 1;

                            const colors = getSlotColors(kind);
                            const badgePad = 5;
                            const bx = cx + badgePad;
                            const by = y + badgePad;
                            const bw = cw - badgePad * 2;
                            const bh = rowHeight - badgePad * 2;

                            ctx.fillStyle = colors.bg;
                            ctx.strokeStyle = colors.border;
                            ctx.lineWidth = 1;
                            drawRoundedRect(ctx, bx, by, bw, bh, 8);
                            ctx.fill();
                            ctx.stroke();

                            if (slot && slot.label) {
                                const displayLabel = getLocalizedSlotLabel(slot);
                                const hasNote = Boolean(slot.note);
                                ctx.fillStyle = colors.text;
                                ctx.font = '800 13px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                                ctx.textAlign = 'center';
                                ctx.textBaseline = 'middle';
                                ctx.fillText(displayLabel, bx + bw / 2, hasNote ? by + bh / 2 - 7 : by + bh / 2);

                                if (hasNote) {
                                    ctx.fillStyle = colors.sub;
                                    ctx.font = '700 10px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                                    ctx.fillText(slot.note, bx + bw / 2, by + bh / 2 + 8);
                                }
                            } else {
                                ctx.fillStyle = '#94a3b8';
                                ctx.font = '700 13px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                                ctx.textAlign = 'center';
                                ctx.textBaseline = 'middle';
                                ctx.fillText('—', bx + bw / 2, by + bh / 2);
                            }
                        }

                        const cntX = colX[8];
                        const cntW = colWidths[8];
                        ctx.fillStyle = rIdx % 2 === 0 ? '#ffffff' : '#f8fafc';
                        ctx.fillRect(cntX, y, cntW, rowHeight);
                        ctx.strokeStyle = '#e2e8f0';
                        ctx.strokeRect(cntX, y, cntW, rowHeight);

                        ctx.fillStyle = '#eef2ff';
                        ctx.strokeStyle = '#c7d2fe';
                        drawRoundedRect(ctx, cntX + 8, y + 12, cntW - 16, rowHeight - 24, 7);
                        ctx.fill();
                        ctx.stroke();

                        const dayWord = empWorkedDays === 1 ? t('daySingular') : t('dayPlural');
                        ctx.fillStyle = '#4338ca';
                        ctx.font = '800 12px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                        ctx.textAlign = 'center';
                        ctx.textBaseline = 'middle';
                        ctx.fillText(`${empWorkedDays} ${dayWord}`, cntX + cntW / 2, y + rowHeight / 2);
                    });
                }

                const footY = tableTop + headerHeight + empRowsCount * rowHeight;
                for (let c = 0; c < 9; c++) {
                    const fx = colX[c];
                    const fw = colWidths[c];
                    ctx.fillStyle = '#f1f5f9';
                    ctx.fillRect(fx, footY, fw, footerHeight);
                    ctx.strokeStyle = '#cbd5e1';
                    ctx.strokeRect(fx, footY, fw, footerHeight);

                    ctx.fillStyle = '#0f172a';
                    ctx.font = '800 12px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                    ctx.textBaseline = 'middle';

                    if (c === 0) {
                        ctx.textAlign = 'left';
                        ctx.fillText(t('presentPerDay'), fx + 12, footY + footerHeight / 2);
                    } else if (c >= 1 && c <= 7) {
                        ctx.textAlign = 'center';
                        ctx.fillText(String(dailyWorkingCount[c - 1]), fx + fw / 2, footY + footerHeight / 2);
                    } else {
                        ctx.textAlign = 'center';
                        ctx.fillText(String(grandTotalDays), fx + fw / 2, footY + footerHeight / 2);
                    }
                }

                const legY = tableTop + tableHeight + 14;
                const legendItems = [
                    { text: t('canvasLegendWork'), color: '#059669' },
                    { text: t('canvasLegendExtra'), color: '#d97706' },
                    { text: t('canvasLegendVrij'), color: '#64748b' },
                    { text: t('canvasLegendVakantie'), color: '#e11d48' }
                ];

                let lx = padX + 4;
                ctx.textBaseline = 'middle';
                ctx.textAlign = 'left';
                ctx.font = '600 12px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, sans-serif';
                legendItems.forEach(item => {
                    ctx.fillStyle = item.color;
                    ctx.beginPath();
                    ctx.arc(lx + 5, legY + 10, 5, 0, Math.PI * 2);
                    ctx.fill();

                    ctx.fillStyle = '#475569';
                    ctx.fillText(item.text, lx + 15, legY + 10);
                    lx += ctx.measureText(item.text).width + 32;
                });

                ctx.restore();

                const dataUrl = canvas.toDataURL('image/png');
                if (!dataUrl || !dataUrl.startsWith('data:image/png;base64,') || dataUrl.length < 200) {
                    return null;
                }

                const filename = `program-munca-${state.year}-W${weekNumStr}-${state.lang}.png`;
                state.lastPngDataUrl = dataUrl;
                state.lastPngFilename = filename;

                const byteString = atob(dataUrl.split(',')[1]);
                const ab = new ArrayBuffer(byteString.length);
                const ia = new Uint8Array(ab);
                for (let i = 0; i < byteString.length; i++) {
                    ia[i] = byteString.charCodeAt(i);
                }
                const blob = new Blob([ab], { type: 'image/png' });
                if (!blob || blob.size === 0) {
                    return null;
                }
                state.lastPngBlob = blob;

                return { dataUrl, blob, filename };
            } catch (err) {
                return null;
            }
        }

        function openShareImageModal(preferredChannel = null) {
            const rendered = renderScheduleToPNG();
            const container = document.getElementById('png-preview-container');
            const helper = document.getElementById('share-image-helper-text');
            const subtitle = document.getElementById('share-image-modal-subtitle');

            const days = getDatesOfISOWeek(state.year, state.week);
            const weekNumStr = String(state.week).padStart(2, '0');
            const rangeStr = `${formatShortDate(days[0])} – ${formatShortDate(days[6])} ${state.year}`;
            subtitle.textContent = t('shareModalSubtitle', { week: weekNumStr, range: rangeStr });

            if (!rendered || !rendered.dataUrl) {
                container.innerHTML = `<span style="font-size:0.8rem; color:#be123c; font-weight:700;">${escapeHTML(t('shareError'))}</span>`;
            } else {
                container.innerHTML = `<img src="${rendered.dataUrl}" alt="${escapeHTML(t('shareModalTitle'))}" class="png-preview-img">`;
            }

            const canShareTextOrFile = typeof navigator !== 'undefined' && typeof navigator.share === 'function';
            helper.textContent = canShareTextOrFile ? t('shareHelperNative') : t('shareHelperFallback');
            document.getElementById('share-image-modal').classList.add('open');

            if (preferredChannel === 'whatsapp') {
                shareRenderedScheduleImage('whatsapp');
            } else if (preferredChannel === 'email') {
                shareRenderedScheduleImage('email');
            }
        }

        function closeShareImageModal() {
            document.getElementById('share-image-modal').classList.remove('open');
        }

        function downloadRenderedSchedulePNG() {
            const rendered = (state.lastPngBlob && state.lastPngFilename)
                ? { blob: state.lastPngBlob, dataUrl: state.lastPngDataUrl, filename: state.lastPngFilename }
                : renderScheduleToPNG();

            if (!rendered || (!rendered.blob && !rendered.dataUrl)) {
                showToast(t('toastPngNotReady'));
                return;
            }

            try {
                const objectUrl = rendered.blob ? URL.createObjectURL(rendered.blob) : rendered.dataUrl;
                const link = document.createElement('a');
                link.href = objectUrl;
                link.download = rendered.filename;
                document.body.appendChild(link);
                link.click();
                document.body.removeChild(link);
                if (rendered.blob) {
                    setTimeout(() => URL.revokeObjectURL(objectUrl), 5000);
                }
                showToast(t('toastPngDownloaded', { filename: rendered.filename }));
            } catch (err) {
                showToast(t('toastPngOpenFail'));
            }
        }

        async function copyRenderedScheduleImage() {
            const rendered = (state.lastPngBlob)
                ? { blob: state.lastPngBlob }
                : renderScheduleToPNG();

            if (!rendered || !rendered.blob) {
                showToast(t('toastNoPng'));
                return;
            }

            try {
                if (navigator.clipboard && typeof ClipboardItem !== 'undefined') {
                    const item = new ClipboardItem({ 'image/png': rendered.blob });
                    await navigator.clipboard.write([item]);
                    showToast(t('toastImgCopied'));
                    return;
                }
            } catch (err) {
                // Fallback to download
            }

            downloadRenderedSchedulePNG();
            showToast(t('toastImgCopyFallback'));
        }

        async function shareRenderedScheduleImage(channel = 'whatsapp') {
            const rendered = renderScheduleToPNG();
            const days = getDatesOfISOWeek(state.year, state.week);
            const weekNumStr = String(state.week).padStart(2, '0');
            const rangeStr = `${formatShortDate(days[0])} – ${formatShortDate(days[6])} ${state.year}`;
            const title = t('shareTextTitle', { week: weekNumStr, range: rangeStr });
            const weekOnlyText = buildScheduleShareText();

            // Trimite săptămâna + imaginea PNG a tabelului
            if (rendered && rendered.blob && typeof navigator !== 'undefined' && typeof navigator.share === 'function' && typeof File !== 'undefined') {
                try {
                    const pngFile = new File([rendered.blob], rendered.filename, { type: 'image/png' });
                    if (!navigator.canShare || navigator.canShare({ files: [pngFile] })) {
                        await navigator.share({
                            title: title,
                            text: weekOnlyText,
                            files: [pngFile]
                        });
                        showToast(channel === 'whatsapp' ? t('toastSharedWa') : t('toastSharedMail'));
                        return;
                    }
                } catch (err) {
                    if (err && err.name === 'AbortError') {
                        showToast(t('toastShareCancelled'));
                        return;
                    }
                }
            }

            // Fallback nativ: doar eticheta săptămânii
            if (typeof navigator !== 'undefined' && typeof navigator.share === 'function') {
                try {
                    await navigator.share({
                        title: title,
                        text: weekOnlyText
                    });
                    showToast(channel === 'whatsapp' ? t('toastOpenedWaText') : t('toastOpenedMail'));
                    return;
                } catch (err) {
                    if (err && err.name === 'AbortError') {
                        showToast(t('toastShareCancelled'));
                        return;
                    }
                }
            }

            if (channel === 'whatsapp') {
                await openWhatsAppWithTextSafe(title, weekOnlyText);
            } else {
                const mailtoUrl = `mailto:?subject=${encodeURIComponent(title)}&body=${encodeURIComponent(weekOnlyText)}`;
                triggerAnchorNavigation(mailtoUrl, false);
                showToast(t('toastOpenedMail'));
            }
        }

        /* =====================================================================
           9. 90-DEGREE FULLSCREEN MODE & PORTALS
           ===================================================================== */
        function syncPortalsToFullscreenStage(intoStage) {
            const stage = document.getElementById('fullscreen-rotated-stage');
            const shiftModal = document.getElementById('shift-modal');
            const empModal = document.getElementById('emp-modal');
            const shareImageModal = document.getElementById('share-image-modal');
            const toastContainer = document.getElementById('toast-container');

            if (intoStage && stage) {
                if (shiftModal && shiftModal.parentElement !== stage) stage.appendChild(shiftModal);
                if (empModal && empModal.parentElement !== stage) stage.appendChild(empModal);
                if (shareImageModal && shareImageModal.parentElement !== stage) stage.appendChild(shareImageModal);
                if (toastContainer && toastContainer.parentElement !== stage) stage.appendChild(toastContainer);
            } else {
                if (shiftModal && shiftModal.parentElement !== document.body) document.body.appendChild(shiftModal);
                if (empModal && empModal.parentElement !== document.body) document.body.appendChild(empModal);
                if (shareImageModal && shareImageModal.parentElement !== document.body) document.body.appendChild(shareImageModal);
                if (toastContainer && toastContainer.parentElement !== document.body) document.body.appendChild(toastContainer);
            }
        }

        function enterFullscreenSchedule() {
            if (state.isFullscreen) return;
            state.isFullscreen = true;
            state.pushedFullscreenState = false;

            try {
                window.history.pushState(
                    { scheduleFullscreen90: true, year: state.year, week: state.week },
                    '',
                    window.location.href
                );
                state.pushedFullscreenState = true;
            } catch (err) {
                state.pushedFullscreenState = false;
            }

            document.body.classList.add('fullscreen-schedule-active');
            const shell = document.getElementById('fullscreen-overlay-shell');
            shell.classList.add('active', state.rotationClass);
            syncPortalsToFullscreenStage(true);
            showToast(t('toastFsActive'));
        }

        function exitFullscreenSchedule(fromPopState = false) {
            if (!state.isFullscreen) return;

            if (document.getElementById('shift-modal').classList.contains('open')) {
                closeShiftModal();
            }
            if (document.getElementById('emp-modal').classList.contains('open')) {
                closeAddEmployeeModal();
            }
            if (document.getElementById('share-image-modal').classList.contains('open')) {
                closeShareImageModal();
            }

            const hadPushedState = state.pushedFullscreenState;
            state.isFullscreen = false;
            state.pushedFullscreenState = false;

            syncPortalsToFullscreenStage(false);
            document.body.classList.remove('fullscreen-schedule-active');
            const shell = document.getElementById('fullscreen-overlay-shell');
            shell.classList.remove('active', 'rotated-ccw', 'rotated-cw');

            if (!fromPopState && hadPushedState) {
                try {
                    window.history.back();
                } catch (err) {
                    // Ignore history errors
                }
            }
        }

        function toggleRotationDirection() {
            const shell = document.getElementById('fullscreen-overlay-shell');
            shell.classList.remove(state.rotationClass);
            state.rotationClass = (state.rotationClass === 'rotated-ccw') ? 'rotated-cw' : 'rotated-ccw';
            shell.classList.add(state.rotationClass);
            saveAppState();
        }

        /* =====================================================================
           10. TOASTS, EVENT BINDING & BOOTSTRAP
           ===================================================================== */
        function showToast(message) {
            const container = document.getElementById('toast-container');
            const el = document.createElement('div');
            el.className = 'toast-item';
            el.textContent = message;
            container.appendChild(el);
            setTimeout(() => {
                el.style.opacity = '0';
                el.style.transition = 'opacity 0.25s ease';
                setTimeout(() => el.remove(), 260);
            }, 2600);
        }

        function bindEvents() {
            document.getElementById('brand-trigger-btn').addEventListener('click', enterFullscreenSchedule);
            document.getElementById('prev-week-btn').addEventListener('click', () => changeWeek(-1));
            document.getElementById('next-week-btn').addEventListener('click', () => changeWeek(1));
            document.getElementById('year-select').addEventListener('change', onYearChange);
            document.getElementById('week-select').addEventListener('change', onWeekChange);
            document.getElementById('week-47-btn').addEventListener('click', goToWeek47);
            document.getElementById('lang-select').addEventListener('change', (e) => onLanguageChange(e.target.value));

            document.getElementById('save-changes-btn').addEventListener('click', commitChangesExplicitly);
            document.getElementById('add-emp-btn').addEventListener('click', openAddEmployeeModal);
            document.getElementById('copy-prev-week-btn').addEventListener('click', copyPreviousWeek);
            document.getElementById('fullscreen-90-btn').addEventListener('click', enterFullscreenSchedule);
            document.getElementById('print-btn').addEventListener('click', () => window.print());

            document.getElementById('share-wa-btn').addEventListener('click', () => openShareImageModal('whatsapp'));
            document.getElementById('share-email-btn').addEventListener('click', () => openShareImageModal('email'));
            document.getElementById('copy-text-btn').addEventListener('click', () => copyScheduleTextToClipboard(false));

            document.getElementById('fs-save-btn').addEventListener('click', commitChangesExplicitly);
            document.getElementById('fs-wa-btn').addEventListener('click', () => openShareImageModal('whatsapp'));
            document.getElementById('fs-mail-btn').addEventListener('click', () => openShareImageModal('email'));
            document.getElementById('fs-prev-btn').addEventListener('click', () => changeWeek(-1));
            document.getElementById('fs-next-btn').addEventListener('click', () => changeWeek(1));
            document.getElementById('fs-rotate-btn').addEventListener('click', toggleRotationDirection);
            document.getElementById('fs-exit-btn').addEventListener('click', () => exitFullscreenSchedule(false));

            document.getElementById('fullscreen-rotated-stage').addEventListener('dblclick', () => {
                if (state.isFullscreen && window.innerWidth < 768) {
                    exitFullscreenSchedule(false);
                }
            });

            // Delegated click handling for table shift cells and employee delete buttons
            document.getElementById('table-body').addEventListener('click', (e) => {
                const delBtn = e.target.closest('[data-delete-emp]');
                if (delBtn) {
                    e.stopPropagation();
                    deleteEmployee(delBtn.getAttribute('data-delete-emp'));
                    return;
                }

                const slotEl = e.target.closest('.shift-slot[data-emp-id]');
                if (slotEl) {
                    const empId = slotEl.getAttribute('data-emp-id');
                    const dayIndex = parseInt(slotEl.getAttribute('data-day-index'), 10);
                    if (empId && !Number.isNaN(dayIndex)) {
                        openShiftModal(empId, dayIndex);
                    }
                }
            });

            // Shift modal controls
            document.getElementById('shift-modal').addEventListener('click', (e) => {
                if (e.target === e.currentTarget) closeShiftModal();
            });
            document.getElementById('close-shift-modal-btn').addEventListener('click', closeShiftModal);
            document.getElementById('cancel-shift-btn').addEventListener('click', closeShiftModal);
            document.getElementById('save-shift-btn').addEventListener('click', saveShiftModal);
            document.getElementById('add-extra-day-btn').addEventListener('click', addExtraDayFromModal);
            document.getElementById('reset-group-week-btn').addEventListener('click', reapplyGroupScheduleForEditingEmp);
            document.getElementById('apply-mon-fri-btn').addEventListener('click', applyToMonFri);
            document.getElementById('clear-cell-btn').addEventListener('click', clearCurrentCell);

            document.querySelectorAll('#shift-modal .preset-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    const pType = btn.getAttribute('data-preset-type') || 'work';
                    const pLabel = btn.getAttribute('data-preset-label') || '07:00';
                    const pExtra = btn.getAttribute('data-preset-extra') === '1';
                    selectPreset(pType, pLabel, pExtra);
                });
            });

            // Add employee modal controls
            document.getElementById('emp-modal').addEventListener('click', (e) => {
                if (e.target === e.currentTarget) closeAddEmployeeModal();
            });
            document.getElementById('close-emp-modal-btn').addEventListener('click', closeAddEmployeeModal);
            document.getElementById('cancel-emp-btn').addEventListener('click', closeAddEmployeeModal);
            document.getElementById('add-emp-form').addEventListener('submit', submitNewEmployee);

            // Share image modal controls
            document.getElementById('share-image-modal').addEventListener('click', (e) => {
                if (e.target === e.currentTarget) closeShareImageModal();
            });
            document.getElementById('close-share-modal-btn').addEventListener('click', closeShareImageModal);
            document.getElementById('close-share-footer-btn').addEventListener('click', closeShareImageModal);
            document.getElementById('download-png-btn').addEventListener('click', downloadRenderedSchedulePNG);
            document.getElementById('copy-png-btn').addEventListener('click', copyRenderedScheduleImage);
            document.getElementById('modal-copy-text-btn').addEventListener('click', () => copyScheduleTextToClipboard(false));
            document.getElementById('modal-wa-text-btn').addEventListener('click', shareScheduleTextOnWhatsApp);
            document.getElementById('modal-wa-image-btn').addEventListener('click', () => shareRenderedScheduleImage('whatsapp'));
            document.getElementById('modal-mail-image-btn').addEventListener('click', () => shareRenderedScheduleImage('email'));

            window.addEventListener('pagehide', persistEverythingNow);
            window.addEventListener('beforeunload', persistEverythingNow);
            document.addEventListener('visibilitychange', () => {
                if (document.visibilityState === 'hidden') {
                    persistEverythingNow();
                } else {
                    renderScheduleTable();
                }
            });

            window.addEventListener('popstate', () => {
                if (document.getElementById('shift-modal').classList.contains('open')) {
                    closeShiftModal();
                    if (state.isFullscreen) {
                        try {
                            window.history.pushState({ scheduleFullscreen90: true, year: state.year, week: state.week }, '', window.location.href);
                            state.pushedFullscreenState = true;
                        } catch (err) {}
                    }
                    return;
                }

                if (document.getElementById('emp-modal').classList.contains('open')) {
                    closeAddEmployeeModal();
                    if (state.isFullscreen) {
                        try {
                            window.history.pushState({ scheduleFullscreen90: true, year: state.year, week: state.week }, '', window.location.href);
                            state.pushedFullscreenState = true;
                        } catch (err) {}
                    }
                    return;
                }

                if (document.getElementById('share-image-modal').classList.contains('open')) {
                    closeShareImageModal();
                    if (state.isFullscreen) {
                        try {
                            window.history.pushState({ scheduleFullscreen90: true, year: state.year, week: state.week }, '', window.location.href);
                            state.pushedFullscreenState = true;
                        } catch (err) {}
                    }
                    return;
                }

                if (state.isFullscreen) {
                    exitFullscreenSchedule(true);
                }
            });

            document.addEventListener('keydown', (e) => {
                if (e.key === 'Escape') {
                    if (document.getElementById('shift-modal').classList.contains('open')) {
                        closeShiftModal();
                    } else if (document.getElementById('emp-modal').classList.contains('open')) {
                        closeAddEmployeeModal();
                    } else if (document.getElementById('share-image-modal').classList.contains('open')) {
                        closeShareImageModal();
                    } else if (state.isFullscreen) {
                        exitFullscreenSchedule(false);
                    }
                }
            });

            let lastKnownDaySig = getCurrentCalendarDaySignature();
            setInterval(() => {
                const currentDaySig = getCurrentCalendarDaySignature();
                if (currentDaySig !== lastKnownDaySig) {
                    lastKnownDaySig = currentDaySig;
                    renderScheduleTable();
                }
            }, 30000);
        }

        function initApp() {
            loadAppState();
            loadSavedMetaAndLanguage();
            bindEvents();
            applyStaticTranslations();
            populateWeekDropdown();
            renderScheduleTable();
            hydrateFromIndexedDBIfNeeded(() => {
                loadAppState();
                loadSavedMetaAndLanguage();
                applyStaticTranslations();
                populateWeekDropdown();
                renderScheduleTable();
            });
        }

        if (document.readyState === 'loading') {
            window.addEventListener('DOMContentLoaded', initApp);
        } else {
            initApp();
        }
    </script>
</body>
</html>

