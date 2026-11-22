<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SmartWork - Programul de muncă (PC)</title>

    <meta name="application-name" content="SmartWork">
    <meta name="apple-mobile-web-app-title" content="SmartWork">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="theme-color" content="#1d4ed8">

    <link id="app-favicon" rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 512 512'%3E%3Cdefs%3E%3ClinearGradient id='bg' x1='0' y1='0' x2='1' y2='1'%3E%3Cstop offset='0%25' stop-color='%232563eb'/%3E%3Cstop offset='100%25' stop-color='%231e3a8a'/%3E%3C/linearGradient%3E%3C/defs%3E%3Crect width='512' height='512' rx='112' fill='url(%23bg)'/%3E%3Cg transform='rotate(-7 240 245)'%3E%3Crect x='92' y='112' width='284' height='256' rx='36' fill='%23f8fafc'/%3E%3Cpath d='M92 148c0-20 16-36 36-36h212c20 0 36 16 36 36v42H92v-42z' fill='%231d4ed8'/%3E%3Crect x='152' y='84' width='24' height='54' rx='12' fill='%230f172a'/%3E%3Crect x='292' y='84' width='24' height='54' rx='12' fill='%230f172a'/%3E%3Crect x='132' y='214' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='188' y='214' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='244' y='214' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='300' y='214' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='132' y='266' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='188' y='266' width='40' height='36' rx='8' fill='%232563eb'/%3E%3Cpath d='M198 284l7 7 15-15' stroke='%23ffffff' stroke-width='6' fill='none' stroke-linecap='round' stroke-linejoin='round'/%3E%3Crect x='244' y='266' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3C/g%3E%3Cpath d='M402 92l26-26M420 124l36-10M426 158l32 8' stroke='%23ffffff' stroke-width='12' stroke-linecap='round'/%3E%3Crect x='66' y='324' width='156' height='118' rx='24' fill='%23f8fafc' stroke='%231e3a8a' stroke-width='8'/%3E%3Cpath d='M116 324v-20c0-10 8-18 18-18h20c10 0 18 8 18 18v20' fill='none' stroke='%230f172a' stroke-width='12'/%3E%3Cpath d='M66 366c48 22 108 22 156 0' fill='none' stroke='%231e3a8a' stroke-width='8'/%3E%3Crect x='128' y='362' width='32' height='34' rx='8' fill='%231e3a8a'/%3E%3Ccircle cx='352' cy='346' r='104' fill='%23f8fafc' stroke='%231e3a8a' stroke-width='18'/%3E%3Cpath d='M352 266v14M352 412v14M272 346h14M418 346h14' stroke='%231e3a8a' stroke-width='10' stroke-linecap='round'/%3E%3Cpath d='M324 322l28 26 42-38' fill='none' stroke='%230f172a' stroke-width='14' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E">
    <link id="apple-touch-icon" rel="apple-touch-icon" href="">
    <link id="pwa-manifest" rel="manifest" href="">

    <script>
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

                const grad = ctx.createLinearGradient(0, 0, 512, 512);
                grad.addColorStop(0, '#2563eb');
                grad.addColorStop(1, '#1e3a8a');
                ctx.fillStyle = grad;
                roundRect(ctx, 0, 0, 512, 512, 112);
                ctx.fill();

                ctx.strokeStyle = '#ffffff';
                ctx.lineWidth = 13;
                ctx.lineCap = 'round';
                ctx.beginPath();
                ctx.moveTo(398, 94); ctx.lineTo(426, 66);
                ctx.moveTo(418, 128); ctx.lineTo(456, 116);
                ctx.moveTo(424, 164); ctx.lineTo(458, 172);
                ctx.stroke();

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

                ctx.fillStyle = '#0f172a';
                roundRect(ctx, 152, 82, 24, 54, 12);
                ctx.fill();
                roundRect(ctx, 290, 82, 24, 54, 12);
                ctx.fill();

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

                ctx.fillStyle = '#f8fafc';
                ctx.beginPath();
                ctx.arc(352, 346, 102, 0, Math.PI * 2);
                ctx.fill();
                ctx.strokeStyle = '#1e3a8a';
                ctx.lineWidth = 18;
                ctx.stroke();

                ctx.strokeStyle = '#1e3a8a';
                ctx.lineWidth = 10;
                ctx.beginPath();
                ctx.moveTo(352, 268); ctx.lineTo(352, 282);
                ctx.moveTo(352, 410); ctx.lineTo(352, 424);
                ctx.moveTo(274, 346); ctx.lineTo(288, 346);
                ctx.moveTo(416, 346); ctx.lineTo(430, 346);
                ctx.stroke();

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
           1. DESIGN TOKENS & FULL-SCREEN PC LAYOUT
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
            width: 100vw;
            height: 100vh;
            overflow: hidden;
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
        }

        button, select, input {
            font-family: inherit;
        }

        ::-webkit-scrollbar {
            width: 9px;
            height: 9px;
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
            padding: 10px 18px;
            flex-shrink: 0;
            width: 100%;
        }

        .header-inner {
            width: 100%;
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
            padding: 5px 10px;
            border-radius: 12px;
            transition: background-color 0.2s ease;
            user-select: none;
            background: transparent;
            border: none;
            text-align: left;
        }

        .brand-trigger:hover {
            background-color: var(--indigo-50);
        }

        .brand-icon {
            width: 40px;
            height: 40px;
            border-radius: 11px;
            background: linear-gradient(135deg, #2563eb, #1e3a8a);
            color: #ffffff;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
            box-shadow: 0 4px 10px rgba(37, 99, 235, 0.28);
        }

        .brand-title-row {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .brand-title {
            font-size: 1.15rem;
            font-weight: 800;
            color: var(--text-main);
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
            font-size: 0.74rem;
            color: var(--text-muted);
        }

        .week-navigator {
            display: flex;
            align-items: center;
            gap: 6px;
            background: var(--bg-subtle);
            padding: 4px 6px;
            border-radius: 12px;
            border: 1px solid var(--border-color);
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
            padding: 8px 13px;
            border-radius: 10px;
            font-size: 0.82rem;
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

        .btn-icon {
            padding: 7px 10px;
            font-size: 0.85rem;
            font-weight: 700;
        }

        .btn-primary {
            background: var(--indigo-600);
            color: #ffffff;
            border-color: var(--indigo-600);
        }

        .btn-primary:hover {
            background: var(--indigo-700);
            border-color: var(--indigo-700);
        }

        .btn-save {
            background: #059669;
            color: #ffffff;
            border-color: #047857;
        }

        .btn-save:hover {
            background: #047857;
        }

        .btn-save.has-unsaved {
            background: #d97706;
            border-color: #b45309;
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
        }

        .btn-whatsapp:hover {
            background: #15803d;
        }

        .btn-email {
            background: #0284c7;
            color: #ffffff;
            border-color: #0369a1;
        }

        .btn-email:hover {
            background: #0369a1;
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
            padding: 7px 11px;
            border-radius: 10px;
            border: 1px solid var(--border-strong);
            background: #ffffff;
            color: var(--text-main);
            font-size: 0.82rem;
            font-weight: 700;
            cursor: pointer;
            outline: none;
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
            width: 100%;
            padding: 10px 18px;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 12px;
            flex-shrink: 0;
            background: var(--bg-body);
            border-bottom: 1px solid var(--border-color);
        }

        .legend-list {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 8px;
            font-size: 0.78rem;
        }

        .legend-pill {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            padding: 5px 11px;
            border-radius: 9px;
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
            gap: 10px;
        }

        .share-group {
            display: inline-flex;
            align-items: center;
            gap: 6px;
        }

        .stats-bar {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.82rem;
            color: var(--text-secondary);
            background: #ffffff;
            padding: 7px 14px;
            border-radius: 10px;
            border: 1px solid var(--border-color);
        }

        .stats-bar strong {
            color: var(--text-main);
            font-weight: 800;
        }

        /* =====================================================================
           4. LARGE FIXED SCHEDULE TABLE (NO ROTATION, 100% FULL WIDTH/HEIGHT)
           ===================================================================== */
        .main-workspace {
            flex: 1 1 auto;
            width: 100vw;
            height: 100%;
            min-height: 0;
            padding: 12px 18px 16px;
            display: flex;
            flex-direction: column;
        }

        #fullscreen-overlay-shell {
            flex: 1 1 auto;
            width: 100%;
            height: 100%;
            min-height: 0;
            display: flex;
            flex-direction: column;
        }

        #fullscreen-overlay-shell.expanded-mode {
            position: fixed;
            inset: 0;
            z-index: 50;
            width: 100vw;
            height: 100vh;
            background: #0f172a;
            padding: 10px;
        }

        #fullscreen-rotated-stage {
            flex: 1 1 auto;
            width: 100%;
            height: 100%;
            min-height: 0;
            display: flex;
            flex-direction: column;
            background: var(--bg-card);
            border: 1px solid var(--border-strong);
            border-radius: 14px;
            box-shadow: var(--shadow-md);
            overflow: hidden;
            transform: none !important;
        }

        #fullscreen-top-bar {
            display: none;
            align-items: center;
            justify-content: space-between;
            gap: 12px;
            padding: 9px 16px;
            background: #0f172a;
            color: #ffffff;
            border-bottom: 1px solid #334155;
            flex-shrink: 0;
        }

        #fullscreen-overlay-shell.expanded-mode #fullscreen-top-bar {
            display: flex;
        }

        .fs-title-group {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.9rem;
            font-weight: 700;
        }

        .fs-actions-group {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .fs-btn {
            padding: 6px 12px;
            border-radius: 8px;
            font-size: 0.8rem;
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

        .fs-btn-exit {
            background: #e11d48;
            border-color: #e11d48;
            color: #ffffff;
        }

        #table-scroll-wrapper {
            width: 100%;
            height: 100%;
            flex: 1 1 auto;
            overflow: auto;
        }

        table.schedule-table {
            width: 100%;
            height: 100%;
            border-collapse: separate;
            border-spacing: 0;
            table-layout: fixed;
            min-width: 1040px;
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
            padding: 13px 8px;
            text-align: center;
            font-size: 0.88rem;
            font-weight: 800;
            color: var(--text-main);
        }

        .schedule-table thead th.sticky-col {
            position: sticky;
            top: 0;
            left: 0;
            z-index: 25;
            text-align: left;
            padding-left: 16px;
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
            width: 9px;
            height: 9px;
            border-radius: 50%;
            background-color: #e11d48;
            box-shadow: 0 0 0 2px rgba(225, 29, 72, 0.22);
            margin-left: 6px;
            vertical-align: middle;
        }

        .day-name-row {
            display: inline-flex;
            align-items: center;
            justify-content: center;
        }

        .day-name {
            font-size: 0.9rem;
            font-weight: 800;
        }

        .day-date {
            display: block;
            font-size: 0.76rem;
            font-weight: 600;
            opacity: 0.88;
            margin-top: 2px;
        }

        .schedule-table tbody td {
            border-bottom: 1px solid var(--border-color);
            border-right: 1px solid var(--border-color);
            padding: 8px 6px;
            vertical-align: middle;
            text-align: center;
            height: 82px;
            background: #ffffff;
        }

        .schedule-table tbody tr:hover td {
            background-color: #f8fafc;
        }

        .schedule-table tbody td.sticky-col {
            position: sticky;
            left: 0;
            z-index: 20;
            text-align: left;
            padding: 8px 12px 8px 16px;
            background: #ffffff;
            border-left: 4px solid var(--indigo-600);
            border-right: 2px solid var(--indigo-200);
            box-shadow: 2px 0 6px rgba(79, 70, 229, 0.06);
        }

        .schedule-table tbody tr:hover td.sticky-col {
            background: var(--indigo-50);
        }

        .emp-cell-wrap {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 8px;
        }

        .emp-info {
            min-width: 0;
            flex: 1;
        }

        .emp-name {
            font-size: 1.02rem;
            font-weight: 800;
            color: #1e1b4b;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .emp-role {
            display: inline-block;
            font-size: 0.72rem;
            font-weight: 700;
            color: #ffffff;
            background: var(--indigo-600);
            border-radius: 6px;
            padding: 2px 8px;
            margin-top: 4px;
            max-width: 100%;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .emp-del-btn {
            background: var(--rose-50);
            color: var(--rose-600);
            border: 1px solid var(--rose-200);
            border-radius: 7px;
            width: 26px;
            height: 26px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            flex-shrink: 0;
            font-size: 0.78rem;
            font-weight: 700;
        }

        .emp-del-btn:hover {
            background: var(--rose-100);
        }

        .schedule-table tbody td.weekend-cell {
            background-color: rgba(254, 243, 199, 0.28);
        }

        .shift-slot {
            width: 100%;
            height: 100%;
            min-height: 62px;
            border-radius: 10px;
            padding: 6px 5px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            border: 1px solid transparent;
            transition: transform 0.1s ease, box-shadow 0.15s ease;
            user-select: none;
        }

        .shift-slot:hover {
            transform: translateY(-1px);
            box-shadow: 0 3px 8px rgba(15, 23, 42, 0.08);
        }

        .shift-empty {
            border: 1px dashed #cbd5e1;
            color: #94a3b8;
            background: rgba(255, 255, 255, 0.8);
            font-size: 0.8rem;
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
            font-size: 0.9rem;
            font-weight: 800;
            line-height: 1.2;
        }

        .shift-sub {
            font-size: 0.72rem;
            font-weight: 700;
            opacity: 0.92;
            margin-top: 3px;
        }

        .days-count-badge {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 6px 11px;
            border-radius: 9px;
            font-size: 0.85rem;
            font-weight: 800;
            background: var(--indigo-50);
            color: var(--indigo-700);
            border: 1px solid var(--indigo-200);
        }

        .schedule-table tfoot td {
            position: sticky;
            bottom: 0;
            z-index: 15;
            background: #f8fafc;
            border-top: 2px solid var(--border-strong);
            border-right: 1px solid var(--border-color);
            padding: 11px 8px;
            text-align: center;
            font-size: 0.82rem;
            font-weight: 700;
            color: var(--text-secondary);
        }

        .schedule-table tfoot td.sticky-col {
            position: sticky;
            bottom: 0;
            left: 0;
            z-index: 25;
            background: #f1f5f9;
            text-align: left;
            padding-left: 16px;
            color: var(--text-main);
            border-right: 2px solid var(--border-strong);
        }

        /* =====================================================================
           5. MODALS & TOAST
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
            padding: 20px;
        }

        .modal-backdrop.open {
            display: flex;
        }

        .modal-card {
            background: #ffffff;
            border-radius: 16px;
            width: 100%;
            max-width: 540px;
            box-shadow: var(--shadow-xl);
            border: 1px solid var(--border-color);
            overflow: hidden;
        }

        .modal-card.modal-wide {
            max-width: 780px;
        }

        .modal-header {
            padding: 14px 20px;
            border-bottom: 1px solid var(--border-color);
            display: flex;
            align-items: center;
            justify-content: space-between;
            background: #f8fafc;
        }

        .modal-title {
            font-size: 1rem;
            font-weight: 800;
            color: var(--text-main);
        }

        .modal-subtitle {
            font-size: 0.76rem;
            color: var(--text-muted);
            margin-top: 2px;
        }

        .modal-close {
            width: 32px;
            height: 32px;
            border-radius: 8px;
            border: 1px solid var(--border-color);
            background: #ffffff;
            color: var(--text-secondary);
            cursor: pointer;
            font-weight: 700;
        }

        .modal-body {
            padding: 18px 20px;
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
            padding: 10px 12px;
            border-radius: 10px;
            border: 1px solid var(--border-color);
            background: #ffffff;
            text-align: left;
            cursor: pointer;
        }

        .preset-btn:hover {
            border-color: var(--indigo-600);
            background: var(--indigo-50);
        }

        .preset-btn strong {
            display: block;
            font-size: 0.82rem;
            color: var(--text-main);
        }

        .preset-btn span {
            font-size: 0.72rem;
            color: var(--text-muted);
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 5px;
        }

        .form-group label {
            font-size: 0.76rem;
            font-weight: 700;
            color: var(--text-secondary);
        }

        .form-input {
            padding: 9px 12px;
            border-radius: 10px;
            border: 1px solid var(--border-strong);
            font-size: 0.86rem;
            color: var(--text-main);
            outline: none;
        }

        .form-input:focus {
            border-color: var(--indigo-600);
            box-shadow: 0 0 0 3px rgba(79, 70, 229, 0.14);
        }

        .modal-footer {
            padding: 12px 20px;
            border-top: 1px solid var(--border-color);
            background: #f8fafc;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 10px;
        }

        .png-preview-box {
            background: #f1f5f9;
            border: 1px solid var(--border-strong);
            border-radius: 12px;
            padding: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 200px;
            max-height: 50vh;
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
            padding: 10px 14px;
            font-size: 0.78rem;
            font-weight: 600;
        }

        #toast-container {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 80;
            display: flex;
            flex-direction: column;
            gap: 8px;
            pointer-events: none;
        }

        .toast-item {
            background: #0f172a;
            color: #ffffff;
            padding: 11px 16px;
            border-radius: 12px;
            font-size: 0.82rem;
            font-weight: 600;
            box-shadow: var(--shadow-md);
        }
    </style>
</head>
<body>

    <header class="app-header">
        <div class="header-inner">
            <button type="button" class="brand-trigger" onclick="goToCurrentWeek()" title="Mergi la săptămâna curentă">
                <div class="brand-icon" aria-hidden="true">
                    <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <rect x="3" y="4" width="18" height="18" rx="3"></rect>
                        <line x1="16" y1="2" x2="16" y2="6"></line>
                        <line x1="8" y1="2" x2="8" y2="6"></line>
                        <line x1="3" y1="10" x2="21" y2="10"></line>
                    </svg>
                </div>
                <div>
                    <div class="brand-title-row">
                        <span class="brand-title">SmartWork</span>
                        <span class="year-badge" id="current-year-badge">2026</span>
                    </div>
                    <div class="brand-subtitle" id="week-range-label">Program săptămânal de lucru</div>
                </div>
            </button>

            <div class="week-navigator">
                <button type="button" class="btn btn-icon" onclick="shiftWeek(-1)" title="Săptămâna anterioară">←</button>
                <select id="week-select" class="select-control" onchange="onWeekSelectChange(this.value)" aria-label="Selectează săptămâna"></select>
                <button type="button" class="btn btn-icon" onclick="shiftWeek(1)" title="Săptămâna următoare">→</button>
                <button type="button" class="btn btn-soft-indigo" onclick="goToCurrentWeek()">Azi</button>
            </div>

            <div class="header-actions">
                <button type="button" class="btn btn-primary" onclick="openEmployeeModal()">+ Adaugă angajat</button>
                <button type="button" id="btn-save" class="btn btn-save" onclick="saveSchedule()">💾 Salvează</button>
                <button type="button" class="btn btn-soft-indigo" onclick="toggleExpandedView()" title="Comută tot ecranul">⇄ Tot ecranul</button>
                <button type="button" class="btn btn-danger-soft" onclick="openResetModal()">↺ Reset</button>
            </div>
        </div>
    </header>

    <div class="sub-toolbar">
        <div class="legend-list">
            <span class="legend-pill shift-work"><span class="legend-dot" style="background:#059669"></span>Schimb normal</span>
            <span class="legend-pill shift-extra"><span class="legend-dot" style="background:#d97706"></span>Suplimentar</span>
            <span class="legend-pill shift-vrij"><span class="legend-dot" style="background:#64748b"></span>Liber (Vrij)</span>
            <span class="legend-pill shift-vakantie"><span class="legend-dot" style="background:#e11d48"></span>Concediu</span>
        </div>

        <div class="right-toolbar-group">
            <div class="share-group">
                <button type="button" class="btn btn-soft-amber" onclick="openPngPreviewModal()">🖼 Export PNG</button>
                <button type="button" class="btn btn-whatsapp" onclick="shareViaWhatsApp()">💬 WhatsApp</button>
                <button type="button" class="btn btn-email" onclick="shareViaEmail()">✉️ Email</button>
            </div>
            <div class="stats-bar" id="stats-summary">
                <span>Angajați: <strong>0</strong></span>
                <span>•</span>
                <span>Zile lucrate: <strong>0</strong></span>
            </div>
        </div>
    </div>

    <main class="main-workspace">
        <div id="fullscreen-overlay-shell">
            <div id="fullscreen-rotated-stage">
                <div id="fullscreen-top-bar">
                    <div class="fs-title-group">
                        <span>SmartWork — Mod Ecran Complet</span>
                        <span id="fs-week-label" style="color:#93c5fd;"></span>
                    </div>
                    <div class="fs-actions-group">
                        <button type="button" class="fs-btn fs-btn-save" onclick="saveSchedule()">💾 Salvează</button>
                        <button type="button" class="fs-btn" onclick="shareViaWhatsApp()">💬 WhatsApp</button>
                        <button type="button" class="fs-btn" onclick="shareViaEmail()">✉️ Email</button>
                        <button type="button" class="fs-btn fs-btn-exit" onclick="toggleExpandedView()">⇄ Ieși din tot ecranul</button>
                    </div>
                </div>

                <div id="table-scroll-wrapper">
                    <table class="schedule-table" id="schedule-table">
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
                            <tr id="schedule-thead-row"></tr>
                        </thead>
                        <tbody id="schedule-tbody"></tbody>
                        <tfoot>
                            <tr id="schedule-tfoot-row"></tr>
                        </tfoot>
                    </table>
                </div>
            </div>
        </div>
    </main>

    <!-- Modal editare tură -->
    <div id="shift-modal" class="modal-backdrop" role="dialog" aria-modal="true" aria-labelledby="shift-modal-title">
        <div class="modal-card">
            <div class="modal-header">
                <div>
                    <div id="shift-modal-title" class="modal-title">Editează schimbul</div>
                    <div id="shift-modal-subtitle" class="modal-subtitle"></div>
                </div>
                <button type="button" class="modal-close" onclick="closeShiftModal()">✕</button>
            </div>
            <div class="modal-body">
                <div>
                    <div style="font-size:0.76rem;font-weight:700;color:var(--text-secondary);margin-bottom:6px;">Șabloane rapide:</div>
                    <div class="preset-grid">
                        <button type="button" class="preset-btn" onclick="applyShiftPreset('work', '06:00 - 14:30', 'Schimb 1')">
                            <strong>06:00 - 14:30</strong>
                            <span>Schimb normal (8.5h)</span>
                        </button>
                        <button type="button" class="preset-btn" onclick="applyShiftPreset('work', '14:00 - 22:30', 'Schimb 2')">
                            <strong>14:00 - 22:30</strong>
                            <span>Schimb normal (8.5h)</span>
                        </button>
                        <button type="button" class="preset-btn" onclick="applyShiftPreset('extra', '08:00 - 17:00', 'Extra')">
                            <strong>08:00 - 17:00</strong>
                            <span>Schimb suplimentar</span>
                        </button>
                        <button type="button" class="preset-btn" onclick="applyShiftPreset('vrij', 'VRIJ', 'Zi liberă')">
                            <strong>VRIJ</strong>
                            <span>Zi liberă</span>
                        </button>
                        <button type="button" class="preset-btn" onclick="applyShiftPreset('vakantie', 'CONCEDIU', 'Vakantie')">
                            <strong>CONCEDIU</strong>
                            <span>Concediu / Absență</span>
                        </button>
                        <button type="button" class="preset-btn" onclick="applyShiftPreset('work', '08:00 - 16:30', 'Zi')">
                            <strong>08:00 - 16:30</strong>
                            <span>Program standard</span>
                        </button>
                    </div>
                </div>

                <div class="form-row">
                    <div class="form-group">
                        <label for="shift-type-input">Tip</label>
                        <select id="shift-type-input" class="form-input">
                            <option value="work">Schimb normal</option>
                            <option value="extra">Suplimentar</option>
                            <option value="vrij">Liber (Vrij)</option>
                            <option value="vakantie">Concediu</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="shift-label-input">Interval / Etichetă</label>
                        <input type="text" id="shift-label-input" class="form-input" placeholder="ex: 07:00 - 15:30">
                    </div>
                </div>

                <div class="form-group">
                    <label for="shift-note-input">Notă opțională</label>
                    <input type="text" id="shift-note-input" class="form-input" placeholder="ex: Depozit A, Livrări...">
                </div>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-danger-soft" onclick="clearCurrentShift()">Șterge celula</button>
                <div style="display:flex;gap:8px;">
                    <button type="button" class="btn" onclick="closeShiftModal()">Anulează</button>
                    <button type="button" class="btn btn-primary" onclick="saveShiftFromModal()">Aplică</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Modal adăugare angajat -->
    <div id="employee-modal" class="modal-backdrop" role="dialog" aria-modal="true" aria-labelledby="employee-modal-title">
        <div class="modal-card">
            <div class="modal-header">
                <div>
                    <div id="employee-modal-title" class="modal-title">Adaugă angajat nou</div>
                    <div class="modal-subtitle">Va apărea în tabelul săptămânal</div>
                </div>
                <button type="button" class="modal-close" onclick="closeEmployeeModal()">✕</button>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="emp-name-input">Nume și prenume</label>
                    <input type="text" id="emp-name-input" class="form-input" placeholder="ex: Andrei Popescu">
                </div>
                <div class="form-group">
                    <label for="emp-role-input">Post / Rol</label>
                    <input type="text" id="emp-role-input" class="form-input" placeholder="ex: Operator, Șofer, Logistică">
                </div>
            </div>
            <div class="modal-footer">
                <div></div>
                <div style="display:flex;gap:8px;">
                    <button type="button" class="btn" onclick="closeEmployeeModal()">Anulează</button>
                    <button type="button" class="btn btn-primary" onclick="addEmployeeFromModal()">Adaugă</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Modal export PNG -->
    <div id="png-preview-modal" class="modal-backdrop" role="dialog" aria-modal="true" aria-labelledby="png-modal-title">
        <div class="modal-card modal-wide">
            <div class="modal-header">
                <div>
                    <div id="png-modal-title" class="modal-title">Export program ca imagine PNG</div>
                    <div class="modal-subtitle">Previzualizare tabel pentru săptămâna selectată</div>
                </div>
                <button type="button" class="modal-close" onclick="closePngPreviewModal()">✕</button>
            </div>
            <div class="modal-body">
                <div class="share-helper-note">
                    Poți descărca imaginea direct pe PC sau o poți trimite colegilor pe WhatsApp / Email.
                </div>
                <div class="png-preview-box" id="png-preview-container">
                    <span style="color:var(--text-muted);font-size:0.84rem;">Se generează imaginea...</span>
                </div>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn" onclick="closePngPreviewModal()">Închide</button>
                <div style="display:flex;gap:8px;">
                    <button type="button" class="btn btn-whatsapp" onclick="shareViaWhatsApp()">💬 Trimite pe WhatsApp</button>
                    <button type="button" class="btn btn-primary" id="btn-download-png">⬇ Descarcă PNG</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Modal confirmare reset -->
    <div id="reset-confirm-modal" class="modal-backdrop" role="dialog" aria-modal="true" aria-labelledby="reset-modal-title">
        <div class="modal-card">
            <div class="modal-header">
                <div>
                    <div id="reset-modal-title" class="modal-title">Resetează datele salvate?</div>
                    <div class="modal-subtitle">Se va restaura lista inițială de angajați și ture</div>
                </div>
                <button type="button" class="modal-close" onclick="closeResetModal()">✕</button>
            </div>
            <div class="modal-body">
                <p style="font-size:0.86rem;color:var(--text-secondary);">
                    Ești sigur că vrei să ștergi modificările locale și să revii la programul implicit?
                </p>
            </div>
            <div class="modal-footer">
                <div></div>
                <div style="display:flex;gap:8px;">
                    <button type="button" class="btn" onclick="closeResetModal()">Anulează</button>
                    <button type="button" class="btn btn-danger-soft" onclick="confirmResetSchedule()">Da, resetează</button>
                </div>
            </div>
        </div>
    </div>

    <div id="toast-container" aria-live="polite"></div>

    <script>
        const STORAGE_KEY = 'smartwork_schedule_pc_v2';
        const DAYS_RO = ['Luni', 'Marți', 'Miercuri', 'Joi', 'Vineri', 'Sâmbătă', 'Duminică'];

        const DEFAULT_EMPLOYEES = [
            { id: 'emp-1', name: 'Alexandru Marin', role: 'Coordonator' },
            { id: 'emp-2', name: 'Elena Radu', role: 'Operator' },
            { id: 'emp-3', name: 'Mihai Ionescu', role: 'Logistică' },
            { id: 'emp-4', name: 'Cristina Stoica', role: 'Asistent' }
        ];

        function getMondayOfWeek(dateInput) {
            const d = new Date(dateInput.getFullYear(), dateInput.getMonth(), dateInput.getDate());
            const day = d.getDay();
            const diff = day === 0 ? -6 : 1 - day;
            d.setDate(d.getDate() + diff);
            d.setHours(0, 0, 0, 0);
            return d;
        }

        function formatIsoDate(dateObj) {
            const y = dateObj.getFullYear();
            const m = String(dateObj.getMonth() + 1).padStart(2, '0');
            const d = String(dateObj.getDate()).padStart(2, '0');
            return `${y}-${m}-${d}`;
        }

        function formatShortRo(dateObj) {
            return dateObj.toLocaleDateString('ro-RO', { day: '2-digit', month: '2-digit' });
        }

        function getIsoWeekNumber(mondayDate) {
            const target = new Date(mondayDate.valueOf());
            const dayNr = (mondayDate.getDay() + 6) % 7;
            target.setDate(target.getDate() - dayNr + 3);
            const firstThursday = target.valueOf();
            target.setMonth(0, 1);
            if (target.getDay() !== 4) {
                target.setMonth(0, 1 + ((4 - target.getDay()) + 7) % 7);
            }
            return 1 + Math.ceil((firstThursday - target) / 604800000);
        }

        let state = {
            currentMonday: getMondayOfWeek(new Date()),
            employees: [],
            shifts: {},
            hasUnsaved: false,
            editingCell: null,
            expandedView: false,
            generatedPngUrl: null
        };

        function showToast(msg) {
            const container = document.getElementById('toast-container');
            const el = document.createElement('div');
            el.className = 'toast-item';
            el.textContent = msg;
            container.appendChild(el);
            setTimeout(() => {
                el.style.opacity = '0';
                el.style.transition = 'opacity 0.2s ease';
                setTimeout(() => el.remove(), 220);
            }, 2400);
        }

        function markUnsaved(flag = true) {
            state.hasUnsaved = flag;
            const btn = document.getElementById('btn-save');
            if (btn) {
                btn.classList.toggle('has-unsaved', flag);
                btn.textContent = flag ? '💾 Salvează *' : '💾 Salvează';
            }
        }

        function loadState() {
            try {
                const raw = localStorage.getItem(STORAGE_KEY);
                if (raw) {
                    const parsed = JSON.parse(raw);
                    state.employees = Array.isArray(parsed.employees) && parsed.employees.length > 0
                        ? parsed.employees
                        : [...DEFAULT_EMPLOYEES];
                    state.shifts = parsed.shifts && typeof parsed.shifts === 'object' ? parsed.shifts : {};
                } else {
                    state.employees = [...DEFAULT_EMPLOYEES];
                    seedInitialCurrentWeek();
                }
            } catch (e) {
                state.employees = [...DEFAULT_EMPLOYEES];
                seedInitialCurrentWeek();
            }
            markUnsaved(false);
        }

        function seedInitialCurrentWeek() {
            const wk = formatIsoDate(getMondayOfWeek(new Date()));
            state.employees.forEach((emp, idx) => {
                for (let d = 0; d < 5; d++) {
                    state.shifts[`${wk}_${emp.id}_${d}`] = {
                        type: 'work',
                        label: idx % 2 === 0 ? '08:00 - 16:30' : '09:00 - 17:30',
                        note: ''
                    };
                }
                state.shifts[`${wk}_${emp.id}_5`] = { type: 'vrij', label: 'VRIJ', note: '' };
                state.shifts[`${wk}_${emp.id}_6`] = { type: 'vrij', label: 'VRIJ', note: '' };
            });
        }

        function saveSchedule() {
            try {
                localStorage.setItem(STORAGE_KEY, JSON.stringify({
                    employees: state.employees,
                    shifts: state.shifts
                }));
                markUnsaved(false);
                showToast('Programul a fost salvat.');
            } catch (e) {
                showToast('Eroare la salvare.');
            }
        }

        function populateWeekSelect() {
            const select = document.getElementById('week-select');
            const currentIso = formatIsoDate(state.currentMonday);
            select.innerHTML = '';

            const baseMonday = getMondayOfWeek(new Date());
            for (let offset = -16; offset <= 24; offset++) {
                const m = new Date(baseMonday);
                m.setDate(baseMonday.getDate() + offset * 7);
                const sun = new Date(m);
                sun.setDate(m.getDate() + 6);
                const iso = formatIsoDate(m);
                const wkNum = getIsoWeekNumber(m);
                const opt = document.createElement('option');
                opt.value = iso;
                opt.textContent = `Săpt. ${wkNum} (${formatShortRo(m)} - ${formatShortRo(sun)})`;
                if (iso === currentIso) opt.selected = true;
                select.appendChild(opt);
            }

            if (!select.value) {
                const sun = new Date(state.currentMonday);
                sun.setDate(state.currentMonday.getDate() + 6);
                const wkNum = getIsoWeekNumber(state.currentMonday);
                const customOpt = document.createElement('option');
                customOpt.value = currentIso;
                customOpt.textContent = `Săpt. ${wkNum} (${formatShortRo(state.currentMonday)} - ${formatShortRo(sun)})`;
                customOpt.selected = true;
                select.prepend(customOpt);
            }
        }

        function shiftWeek(deltaWeeks) {
            const next = new Date(state.currentMonday);
            next.setDate(next.getDate() + deltaWeeks * 7);
            state.currentMonday = getMondayOfWeek(next);
            renderAll();
        }

        function onWeekSelectChange(isoVal) {
            const parts = isoVal.split('-').map(Number);
            if (parts.length === 3) {
                state.currentMonday = getMondayOfWeek(new Date(parts[0], parts[1] - 1, parts[2]));
                renderAll();
            }
        }

        function goToCurrentWeek() {
            state.currentMonday = getMondayOfWeek(new Date());
            renderAll();
            showToast('Săptămâna curentă.');
        }

        function renderHeaderLabels() {
            const sun = new Date(state.currentMonday);
            sun.setDate(state.currentMonday.getDate() + 6);
            const wkNum = getIsoWeekNumber(state.currentMonday);
            const year = state.currentMonday.getFullYear();

            document.getElementById('current-year-badge').textContent = `${year}`;
            const labelText = `Săptămâna ${wkNum} • ${formatShortRo(state.currentMonday)} – ${formatShortRo(sun)} ${year}`;
            document.getElementById('week-range-label').textContent = labelText;
            const fsLabel = document.getElementById('fs-week-label');
            if (fsLabel) fsLabel.textContent = labelText;
        }

        function renderTable() {
            const wkIso = formatIsoDate(state.currentMonday);
            const todayIso = formatIsoDate(new Date());
            const theadRow = document.getElementById('schedule-thead-row');
            const tbody = document.getElementById('schedule-tbody');
            const tfootRow = document.getElementById('schedule-tfoot-row');

            let thHtml = `<th class="sticky-col">Angajat (${state.employees.length})</th>`;
            for (let d = 0; d < 7; d++) {
                const dayDate = new Date(state.currentMonday);
                dayDate.setDate(state.currentMonday.getDate() + d);
                const dIso = formatIsoDate(dayDate);
                const isWeekend = d >= 5;
                const isToday = dIso === todayIso;
                const cls = [isWeekend ? 'weekend-col' : '', isToday ? 'today-col' : ''].filter(Boolean).join(' ');
                thHtml += `
                    <th class="${cls}">
                        <div class="day-name-row">
                            <span class="day-name">${DAYS_RO[d]}</span>
                            ${isToday ? '<span class="today-red-dot" title="Azi"></span>' : ''}
                        </div>
                        <span class="day-date">${formatShortRo(dayDate)}</span>
                    </th>
                `;
            }
            thHtml += `<th>Zile</th>`;
            theadRow.innerHTML = thHtml;

            let totalWorkedAll = 0;
            const dailyCounts = Array(7).fill(0);

            let bodyHtml = '';
            state.employees.forEach((emp) => {
                let empWorkedDays = 0;
                bodyHtml += `<tr>`;
                bodyHtml += `
                    <td class="sticky-col">
                        <div class="emp-cell-wrap">
                            <div class="emp-info">
                                <div class="emp-name" title="${escapeHtml(emp.name)}">${escapeHtml(emp.name)}</div>
                                <span class="emp-role" title="${escapeHtml(emp.role || 'Angajat')}">${escapeHtml(emp.role || 'Angajat')}</span>
                            </div>
                            <button type="button" class="emp-del-btn" onclick="deleteEmployee('${emp.id}')" title="Șterge angajatul">✕</button>
                        </div>
                    </td>
                `;

                for (let d = 0; d < 7; d++) {
                    const key = `${wkIso}_${emp.id}_${d}`;
                    const shift = state.shifts[key];
                    const isWeekend = d >= 5;
                    if (shift && (shift.type === 'work' || shift.type === 'extra')) {
                        empWorkedDays++;
                        dailyCounts[d]++;
                        totalWorkedAll++;
                    }

                    let slotClass = 'shift-slot shift-empty';
                    let slotContent = `<span>+ Tură</span>`;

                    if (shift) {
                        if (shift.type === 'work') slotClass = 'shift-slot shift-work';
                        else if (shift.type === 'extra') slotClass = 'shift-slot shift-extra';
                        else if (shift.type === 'vrij') slotClass = 'shift-slot shift-vrij';
                        else if (shift.type === 'vakantie') slotClass = 'shift-slot shift-vakantie';

                        slotContent = `
                            <span class="shift-title">${escapeHtml(shift.label || '')}</span>
                            ${shift.note ? `<span class="shift-sub">${escapeHtml(shift.note)}</span>` : ''}
                        `;
                    }

                    bodyHtml += `
                        <td class="${isWeekend ? 'weekend-cell' : ''}">
                            <div class="${slotClass}" onclick="openShiftModal('${emp.id}', ${d})" title="Click pentru a edita">
                                ${slotContent}
                            </div>
                        </td>
                    `;
                }

                bodyHtml += `<td><span class="days-count-badge">${empWorkedDays}</span></td>`;
                bodyHtml += `</tr>`;
            });

            if (state.employees.length === 0) {
                bodyHtml = `
                    <tr>
                        <td colspan="9" style="padding:36px;color:var(--text-muted);font-size:0.95rem;">
                            Niciun angajat adăugat. Apasă pe <strong>+ Adaugă angajat</strong>.
                        </td>
                    </tr>
                `;
            }

            tbody.innerHTML = bodyHtml;

            let footHtml = `<td class="sticky-col">Activitate / zi</td>`;
            for (let d = 0; d < 7; d++) {
                footHtml += `<td>${dailyCounts[d]} activi</td>`;
            }
            footHtml += `<td><strong>${totalWorkedAll}</strong></td>`;
            tfootRow.innerHTML = footHtml;

            document.getElementById('stats-summary').innerHTML = `
                <span>Angajați: <strong>${state.employees.length}</strong></span>
                <span>•</span>
                <span>Zile lucrate: <strong>${totalWorkedAll}</strong></span>
            `;
        }

        function escapeHtml(str) {
            return String(str)
                .replace(/&/g, '&amp;')
                .replace(/</g, '&lt;')
                .replace(/>/g, '&gt;')
                .replace(/"/g, '&quot;');
        }

        function renderAll() {
            renderHeaderLabels();
            populateWeekSelect();
            renderTable();
        }

        function toggleExpandedView() {
            const shell = document.getElementById('fullscreen-overlay-shell');
            state.expandedView = !state.expandedView;
            shell.classList.toggle('expanded-mode', state.expandedView);
        }

        function openShiftModal(empId, dayIdx) {
            const emp = state.employees.find(e => e.id === empId);
            if (!emp) return;
            const wkIso = formatIsoDate(state.currentMonday);
            const key = `${wkIso}_${empId}_${dayIdx}`;
            const existing = state.shifts[key] || { type: 'work', label: '08:00 - 16:30', note: '' };

            state.editingCell = { empId, dayIdx, key };

            const dayDate = new Date(state.currentMonday);
            dayDate.setDate(state.currentMonday.getDate() + dayIdx);

            document.getElementById('shift-modal-title').textContent = `${emp.name} — ${DAYS_RO[dayIdx]}`;
            document.getElementById('shift-modal-subtitle').textContent = `${formatShortRo(dayDate)} • ${emp.role || 'Angajat'}`;
            document.getElementById('shift-type-input').value = existing.type || 'work';
            document.getElementById('shift-label-input').value = existing.label || '';
            document.getElementById('shift-note-input').value = existing.note || '';

            document.getElementById('shift-modal').classList.add('open');
            document.getElementById('shift-label-input').focus();
        }

        function closeShiftModal() {
            document.getElementById('shift-modal').classList.remove('open');
            state.editingCell = null;
        }

        function applyShiftPreset(type, label, note) {
            document.getElementById('shift-type-input').value = type;
            document.getElementById('shift-label-input').value = label;
            document.getElementById('shift-note-input').value = note;
        }

        function saveShiftFromModal() {
            if (!state.editingCell) return;
            const type = document.getElementById('shift-type-input').value;
            const label = document.getElementById('shift-label-input').value.trim();
            const note = document.getElementById('shift-note-input').value.trim();

            if (!label && !note) {
                delete state.shifts[state.editingCell.key];
            } else {
                state.shifts[state.editingCell.key] = {
                    type,
                    label: label || (type === 'vrij' ? 'VRIJ' : type === 'vakantie' ? 'CONCEDIU' : 'Program'),
                    note
                };
            }
            markUnsaved(true);
            closeShiftModal();
            renderTable();
        }

        function clearCurrentShift() {
            if (!state.editingCell) return;
            delete state.shifts[state.editingCell.key];
            markUnsaved(true);
            closeShiftModal();
            renderTable();
        }

        function openEmployeeModal() {
            document.getElementById('emp-name-input').value = '';
            document.getElementById('emp-role-input').value = '';
            document.getElementById('employee-modal').classList.add('open');
            document.getElementById('emp-name-input').focus();
        }

        function closeEmployeeModal() {
            document.getElementById('employee-modal').classList.remove('open');
        }

        function addEmployeeFromModal() {
            const name = document.getElementById('emp-name-input').value.trim();
            const role = document.getElementById('emp-role-input').value.trim() || 'Angajat';
            if (!name) {
                showToast('Introdu numele angajatului.');
                return;
            }
            state.employees.push({
                id: 'emp-' + Date.now(),
                name,
                role
            });
            markUnsaved(true);
            closeEmployeeModal();
            renderTable();
            showToast(`${name} a fost adăugat.`);
        }

        function deleteEmployee(empId) {
            const emp = state.employees.find(e => e.id === empId);
            if (!emp) return;
            state.employees = state.employees.filter(e => e.id !== empId);
            Object.keys(state.shifts).forEach(k => {
                if (k.includes(`_${empId}_`)) delete state.shifts[k];
            });
            markUnsaved(true);
            renderTable();
            showToast(`${emp.name} a fost eliminat.`);
        }

        function openResetModal() {
            document.getElementById('reset-confirm-modal').classList.add('open');
        }

        function closeResetModal() {
            document.getElementById('reset-confirm-modal').classList.remove('open');
        }

        function confirmResetSchedule() {
            localStorage.removeItem(STORAGE_KEY);
            state.employees = [...DEFAULT_EMPLOYEES];
            state.shifts = {};
            seedInitialCurrentWeek();
            markUnsaved(false);
            closeResetModal();
            renderAll();
            showToast('Programul a fost resetat.');
        }

        function buildScheduleSummaryText() {
            const wkIso = formatIsoDate(state.currentMonday);
            const sun = new Date(state.currentMonday);
            sun.setDate(state.currentMonday.getDate() + 6);
            const wkNum = getIsoWeekNumber(state.currentMonday);

            let lines = [
                `SmartWork — Program Săptămâna ${wkNum} (${formatShortRo(state.currentMonday)} - ${formatShortRo(sun)})`,
                ''
            ];

            state.employees.forEach(emp => {
                const dayParts = [];
                for (let d = 0; d < 7; d++) {
                    const sh = state.shifts[`${wkIso}_${emp.id}_${d}`];
                    if (sh && sh.label) {
                        dayParts.push(`${DAYS_RO[d].slice(0, 3)}: ${sh.label}`);
                    }
                }
                lines.push(`• ${emp.name} (${emp.role}): ${dayParts.length ? dayParts.join(' | ') : 'Necompletat'}`);
            });

            return lines.join('\n');
        }

        function shareViaWhatsApp() {
            const text = buildScheduleSummaryText();
            window.open(`https://wa.me/?text=${encodeURIComponent(text)}`, '_blank', 'noopener,noreferrer');
        }

        function shareViaEmail() {
            const wkNum = getIsoWeekNumber(state.currentMonday);
            const subject = encodeURIComponent(`SmartWork - Program Săptămâna ${wkNum}`);
            const body = encodeURIComponent(buildScheduleSummaryText());
            window.location.href = `mailto:?subject=${subject}&body=${body}`;
        }

        function generateSchedulePngDataUrl() {
            const wkIso = formatIsoDate(state.currentMonday);
            const sun = new Date(state.currentMonday);
            sun.setDate(state.currentMonday.getDate() + 6);
            const wkNum = getIsoWeekNumber(state.currentMonday);

            const rowsCount = Math.max(1, state.employees.length);
            const colWidths = [240, 130, 130, 130, 130, 130, 130, 130, 90];
            const totalWidth = colWidths.reduce((a, b) => a + b, 0) + 40;
            const totalHeight = 84 + (rowsCount + 1) * 54 + 44;

            const canvas = document.createElement('canvas');
            canvas.width = totalWidth;
            canvas.height = totalHeight;
            const ctx = canvas.getContext('2d');

            ctx.fillStyle = '#ffffff';
            ctx.fillRect(0, 0, totalWidth, totalHeight);

            ctx.fillStyle = '#0f172a';
            ctx.font = 'bold 18px sans-serif';
            ctx.fillText(`SmartWork — Săptămâna ${wkNum} (${formatShortRo(state.currentMonday)} - ${formatShortRo(sun)})`, 20, 28);

            let y = 44;
            let x = 20;
            const headers = ['Angajat', ...DAYS_RO.map((d, idx) => {
                const dt = new Date(state.currentMonday);
                dt.setDate(state.currentMonday.getDate() + idx);
                return `${d} (${formatShortRo(dt)})`;
            }), 'Zile'];

            headers.forEach((h, i) => {
                ctx.fillStyle = i === 0 ? '#4f46e5' : '#f1f5f9';
                ctx.fillRect(x, y, colWidths[i], 36);
                ctx.strokeStyle = '#cbd5e1';
                ctx.strokeRect(x, y, colWidths[i], 36);
                ctx.fillStyle = i === 0 ? '#ffffff' : '#0f172a';
                ctx.font = 'bold 12px sans-serif';
                ctx.fillText(h.slice(0, 19), x + 8, y + 22);
                x += colWidths[i];
            });

            y += 36;
            state.employees.forEach((emp) => {
                x = 20;
                let worked = 0;

                ctx.fillStyle = '#ffffff';
                ctx.fillRect(x, y, colWidths[0], 54);
                ctx.strokeStyle = '#e2e8f0';
                ctx.strokeRect(x, y, colWidths[0], 54);
                ctx.fillStyle = '#0f172a';
                ctx.font = 'bold 13px sans-serif';
                ctx.fillText(emp.name.slice(0, 25), x + 8, y + 22);
                ctx.fillStyle = '#64748b';
                ctx.font = '11px sans-serif';
                ctx.fillText((emp.role || 'Angajat').slice(0, 25), x + 8, y + 40);
                x += colWidths[0];

                for (let d = 0; d < 7; d++) {
                    const sh = state.shifts[`${wkIso}_${emp.id}_${d}`];
                    if (sh && (sh.type === 'work' || sh.type === 'extra')) worked++;

                    let bg = '#f8fafc';
                    let fg = '#94a3b8';
                    let txt = '-';
                    if (sh) {
                        txt = sh.label || '';
                        if (sh.type === 'work') { bg = '#ecfdf5'; fg = '#065f46'; }
                        else if (sh.type === 'extra') { bg = '#fffbeb'; fg = '#92400e'; }
                        else if (sh.type === 'vrij') { bg = '#f1f5f9'; fg = '#475569'; }
                        else if (sh.type === 'vakantie') { bg = '#fff1f2'; fg = '#be123c'; }
                    }

                    ctx.fillStyle = bg;
                    ctx.fillRect(x, y, colWidths[d + 1], 54);
                    ctx.strokeStyle = '#e2e8f0';
                    ctx.strokeRect(x, y, colWidths[d + 1], 54);
                    ctx.fillStyle = fg;
                    ctx.font = 'bold 12px sans-serif';
                    ctx.fillText(txt.slice(0, 16), x + 6, y + 31);
                    x += colWidths[d + 1];
                }

                ctx.fillStyle = '#eef2ff';
                ctx.fillRect(x, y, colWidths[8], 54);
                ctx.strokeStyle = '#e2e8f0';
                ctx.strokeRect(x, y, colWidths[8], 54);
                ctx.fillStyle = '#4338ca';
                ctx.font = 'bold 13px sans-serif';
                ctx.fillText(`${worked}`, x + 30, y + 31);

                y += 54;
            });

            return canvas.toDataURL('image/png');
        }

        function openPngPreviewModal() {
            const modal = document.getElementById('png-preview-modal');
            const box = document.getElementById('png-preview-container');
            modal.classList.add('open');
            box.innerHTML = '<span style="color:var(--text-muted);font-size:0.84rem;">Se generează imaginea...</span>';

            setTimeout(() => {
                const dataUrl = generateSchedulePngDataUrl();
                state.generatedPngUrl = dataUrl;
                box.innerHTML = `<img src="${dataUrl}" alt="Previzualizare program PNG" class="png-preview-img">`;
            }, 50);
        }

        function closePngPreviewModal() {
            document.getElementById('png-preview-modal').classList.remove('open');
        }

        document.getElementById('btn-download-png').addEventListener('click', () => {
            if (!state.generatedPngUrl) state.generatedPngUrl = generateSchedulePngDataUrl();
            const wkNum = getIsoWeekNumber(state.currentMonday);
            const link = document.createElement('a');
            link.download = `SmartWork-Saptamana-${wkNum}.png`;
            link.href = state.generatedPngUrl;
            link.click();
            showToast('Imaginea PNG a fost descărcată.');
        });

        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape') {
                closeShiftModal();
                closeEmployeeModal();
                closePngPreviewModal();
                closeResetModal();
            }
        });

        loadState();
        renderAll();
    </script>
</body>
</html>
