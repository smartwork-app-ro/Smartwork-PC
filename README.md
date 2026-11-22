```html
<!DOCTYPE html>
<html lang="ro" dir="ltr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SmartWork Desktop — Programul de muncă (2026 &amp; 2027)</title>

    <!-- Pictogramă Desktop Favicon -->
    <meta name="application-name" content="SmartWork Desktop">
    <meta name="theme-color" content="#1d4ed8">
    <link id="app-favicon" rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 512 512'%3E%3Cdefs%3E%3ClinearGradient id='bg' x1='0' y1='0' x2='1' y2='1'%3E%3Cstop offset='0%25' stop-color='%232563eb'/%3E%3Cstop offset='100%25' stop-color='%231e3a8a'/%3E%3C/linearGradient%3E%3C/defs%3E%3Crect width='512' height='512' rx='112' fill='url(%23bg)'/%3E%3Cg transform='rotate(-7 240 245)'%3E%3Crect x='92' y='112' width='284' height='256' rx='36' fill='%23f8fafc'/%3E%3Cpath d='M92 148c0-20 16-36 36-36h212c20 0 36 16 36 36v42H92v-42z' fill='%231d4ed8'/%3E%3Crect x='152' y='84' width='24' height='54' rx='12' fill='%230f172a'/%3E%3Crect x='292' y='84' width='24' height='54' rx='12' fill='%230f172a'/%3E%3Crect x='132' y='214' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='188' y='214' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='244' y='214' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='300' y='214' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='132' y='266' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3Crect x='188' y='266' width='40' height='36' rx='8' fill='%232563eb'/%3E%3Cpath d='M198 284l7 7 15-15' stroke='%23ffffff' stroke-width='6' fill='none' stroke-linecap='round' stroke-linejoin='round'/%3E%3Crect x='244' y='266' width='40' height='36' rx='8' fill='%23cbd5e1'/%3E%3C/g%3E%3Ccircle cx='352' cy='346' r='104' fill='%23f8fafc' stroke='%231e3a8a' stroke-width='18'/%3E%3Cpath d='M324 322l28 26 42-38' fill='none' stroke='%230f172a' stroke-width='14' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E">

    <style>
        /* =====================================================================
           1. DESIGN TOKENS & DESKTOP BASE STYLES
           ===================================================================== */
        :root {
            --bg-body: #f1f5f9;
            --bg-card: #ffffff;
            --bg-subtle: #f8fafc;
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
            --shadow-md: 0 4px 14px rgba(15, 23, 42, 0.07);
            --shadow-xl: 0 22px 40px -12px rgba(15, 23, 42, 0.28);
        }

        *, *::before, *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html, body {
            height: 100%;
            direction: ltr;
            font-family: "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, Helvetica, Arial, sans-serif;
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

        body.desktop-fullscreen-active {
            overflow: hidden !important;
        }

        button, select, input {
            font-family: inherit;
        }

        ::-webkit-scrollbar {
            width: 8px;
            height: 8px;
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
           2. DESKTOP HEADER & NAVIGATION CONTROLS
           ===================================================================== */
        .app-header {
            background: var(--bg-card);
            border-bottom: 1px solid var(--border-color);
            box-shadow: var(--shadow-sm);
            position: sticky;
            top: 0;
            z-index: 30;
            padding: 12px 24px;
        }

        .header-inner {
            max-width: 1800px;
            margin: 0 auto;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 14px;
        }

        .brand-trigger {
            display: flex;
            align-items: center;
            gap: 12px;
            cursor: pointer;
            padding: 6px 12px;
            margin-left: -12px;
            border-radius: 14px;
            transition: background-color 0.18s ease, transform 0.12s ease;
            user-select: none;
            background: transparent;
            border: none;
            text-align: left;
        }

        .brand-trigger:hover {
            background-color: var(--indigo-50);
        }

        .brand-icon {
            width: 44px;
            height: 44px;
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
        }

        .brand-title {
            font-size: 1.2rem;
            font-weight: 800;
            color: var(--text-main);
            letter-spacing: -0.015em;
        }

        .brand-trigger:hover .brand-title {
            color: var(--indigo-700);
        }

        .year-badge {
            display: inline-flex;
            align-items: center;
            padding: 2px 9px;
            border-radius: 999px;
            font-size: 0.74rem;
            font-weight: 700;
            background: var(--indigo-50);
            color: var(--indigo-700);
            border: 1px solid var(--indigo-200);
        }

        .desktop-badge {
            display: inline-flex;
            align-items: center;
            padding: 2px 8px;
            border-radius: 6px;
            font-size: 0.68rem;
            font-weight: 800;
            background: #0f172a;
            color: #f8fafc;
            letter-spacing: 0.04em;
        }

        .brand-subtitle {
            font-size: 0.76rem;
            color: var(--text-muted);
            margin-top: 2px;
        }

        .week-navigator {
            display: flex;
            align-items: center;
            gap: 6px;
            background: var(--bg-subtle);
            padding: 5px 7px;
            border-radius: 12px;
            border: 1px solid var(--border-color);
            flex-wrap: wrap;
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
            transition: all 0.14s ease;
            white-space: nowrap;
        }

        .btn:hover {
            background: #f8fafc;
            border-color: var(--border-strong);
            box-shadow: 0 2px 5px rgba(15, 23, 42, 0.05);
        }

        .btn:active {
            transform: translateY(1px);
        }

        .btn-icon {
            padding: 8px 9px;
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
            padding: 7px 11px;
            border-radius: 10px;
            border: 1px solid var(--border-strong);
            background: #ffffff;
            color: var(--text-main);
            font-size: 0.83rem;
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
           3. DESKTOP TOOLBAR (LEGEND, EXPORT/IMPORT, SHARE & STATS)
           ===================================================================== */
        .sub-toolbar {
            max-width: 1800px;
            width: 100%;
            margin: 14px auto 0;
            padding: 0 24px;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 12px;
        }

        .legend-list {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 8px;
            font-size: 0.76rem;
        }

        .legend-pill {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            padding: 5px 11px;
            border-radius: 8px;
            font-weight: 600;
            border: 1px solid transparent;
        }

        .legend-dot {
            width: 9px;
            height: 9px;
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
            flex-wrap: wrap;
        }

        .toolbar-divider {
            width: 1px;
            height: 24px;
            background: var(--border-strong);
            margin: 0 2px;
        }

        .stats-bar {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 0.82rem;
            color: var(--text-secondary);
            background: #ffffff;
            padding: 7px 14px;
            border-radius: 12px;
            border: 1px solid var(--border-color);
            box-shadow: var(--shadow-sm);
        }

        .stats-bar strong {
            color: var(--text-main);
            font-weight: 800;
        }

        /* =====================================================================
           4. DESKTOP WIDESCREEN SCHEDULE TABLE
           ===================================================================== */
        .main-workspace {
            flex: 1;
            max-width: 1800px;
            width: 100%;
            margin: 14px auto 12px;
            padding: 0 24px;
            display: flex;
            flex-direction: column;
        }

        #fullscreen-overlay-shell {
            flex: 1;
            display: flex;
            flex-direction: column;
        }

        #fullscreen-desktop-stage {
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

        /* Desktop Fullscreen Mode (Standard Widescreen, No Mobile Rotation) */
        #fullscreen-overlay-shell.active {
            position: fixed;
            inset: 0;
            z-index: 50;
            width: 100vw;
            height: 100vh;
            background: #0f172a;
            padding: 0;
        }

        #fullscreen-overlay-shell.active #fullscreen-desktop-stage {
            border-radius: 0;
            border: none;
            width: 100%;
            height: 100%;
        }

        #fullscreen-top-bar {
            display: none;
            align-items: center;
            justify-content: space-between;
            gap: 12px;
            padding: 10px 20px;
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
            gap: 12px;
            font-size: 0.95rem;
            font-weight: 700;
        }

        .fs-actions-group {
            display: flex;
            align-items: center;
            gap: 8px;
            flex-wrap: wrap;
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
            gap: 6px;
            transition: background 0.14s ease;
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
            min-width: 980px;
            direction: ltr;
        }

        col.col-employee { width: 20%; }
        col.col-day      { width: 10.28%; }
        col.col-days-cnt { width: 8%; }

        .schedule-table thead th {
            position: sticky;
            top: 0;
            z-index: 15;
            background: #f1f5f9;
            border-bottom: 2px solid var(--border-strong);
            border-right: 1px solid var(--border-color);
            padding: 12px 6px;
            text-align: center;
            font-size: 0.85rem;
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
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background-color: #e11d48;
            box-shadow: 0 0 0 2px rgba(225, 29, 72, 0.22);
            margin-left: 5px;
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
            font-size: 0.88rem;
            font-weight: 800;
            letter-spacing: -0.01em;
        }

        .day-date {
            display: block;
            font-size: 0.74rem;
            font-weight: 600;
            opacity: 0.85;
            margin-top: 2px;
        }

        .schedule-table tbody td {
            border-bottom: 1px solid var(--border-color);
            border-right: 1px solid var(--border-color);
            padding: 6px;
            vertical-align: middle;
            text-align: center;
            height: 72px;
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
            padding: 8px 12px 8px 16px;
            background: #ffffff;
            border-left: 4px solid var(--indigo-600);
            border-right: 2px solid var(--indigo-200);
            box-shadow: 2px 0 8px rgba(79, 70, 229, 0.06);
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
            gap: 8px;
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
            font-size: 1rem;
            font-weight: 800;
            letter-spacing: -0.01em;
            color: #1e1b4b;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            line-height: 1.25;
        }

        .emp-role {
            display: inline-block;
            direction: ltr;
            unicode-bidi: isolate;
            text-align: left;
            font-size: 0.7rem;
            font-weight: 700;
            color: #ffffff;
            background: var(--indigo-600);
            border: 1px solid var(--indigo-700);
            border-radius: 6px;
            padding: 1px 8px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-top: 4px;
            max-width: 100%;
        }

        .emp-del-btn {
            opacity: 0;
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
            transition: opacity 0.15s ease, background 0.15s ease;
        }

        .emp-del-btn:hover {
            background: var(--rose-100);
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
            min-height: 54px;
            border-radius: 10px;
            padding: 6px 6px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            border: 1.5px solid transparent;
            transition: transform 0.1s ease, box-shadow 0.15s ease, border-color 0.15s ease;
            user-select: none;
            outline: none;
        }

        .shift-slot:hover {
            transform: translateY(-1px);
            box-shadow: 0 4px 10px rgba(15, 23, 42, 0.09);
        }

        .shift-slot.selected-cell,
        .shift-slot:focus-visible {
            border-color: var(--indigo-600) !important;
            box-shadow: 0 0 0 3px rgba(79, 70, 229, 0.22);
        }

        .shift-empty {
            border: 1.5px dashed #cbd5e1;
            color: #94a3b8;
            background: rgba(255, 255, 255, 0.7);
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
            font-size: 0.88rem;
            font-weight: 800;
            line-height: 1.2;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            max-width: 100%;
        }

        .shift-sub {
            font-size: 0.68rem;
            font-weight: 700;
            opacity: 0.9;
            margin-top: 2px;
            white-space: nowrap;
        }

        .days-count-badge {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 5px 10px;
            border-radius: 8px;
            font-size: 0.8rem;
            font-weight: 800;
            background: var(--indigo-50);
            color: var(--indigo-700);
            border: 1px solid var(--indigo-200);
        }

        .schedule-table tfoot td {
            background: #f8fafc;
            border-top: 2px solid var(--border-strong);
            border-right: 1px solid var(--border-color);
            padding: 10px 6px;
            text-align: center;
            font-size: 0.8rem;
            font-weight: 800;
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
            padding-left: 16px;
            color: var(--text-main);
            border-right: 2px solid var(--border-strong);
        }

        /* =====================================================================
           5. DESKTOP STATUS BAR & RIGHT-CLICK CONTEXT MENU
           ===================================================================== */
        .desktop-status-bar {
            max-width: 1800px;
            width: 100%;
            margin: 0 auto 14px;
            padding: 0 24px;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 10px;
            font-size: 0.74rem;
            color: var(--text-muted);
        }

        .kbd-hints {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 12px;
        }

        .kbd-chip {
            display: inline-flex;
            align-items: center;
            gap: 5px;
        }

        kbd {
            display: inline-block;
            padding: 1px 6px;
            font-size: 0.68rem;
            font-weight: 700;
            color: var(--text-main);
            background: #ffffff;
            border: 1px solid var(--border-strong);
            border-bottom-width: 2px;
            border-radius: 5px;
            font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
        }

        .context-menu {
            position: fixed;
            z-index: 95;
            min-width: 220px;
            background: #ffffff;
            border: 1px solid var(--border-strong);
            border-radius: 12px;
            box-shadow: 0 14px 30px rgba(15, 23, 42, 0.2);
            padding: 6px;
            display: none;
            flex-direction: column;
            gap: 2px;
        }

        .context-menu.open {
            display: flex;
        }

        .ctx-header {
            padding: 6px 10px;
            font-size: 0.72rem;
            font-weight: 800;
            color: var(--text-muted);
            border-bottom: 1px solid var(--border-color);
            margin-bottom: 4px;
        }

        .ctx-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 12px;
            width: 100%;
            padding: 7px 10px;
            border: none;
            background: transparent;
            border-radius: 8px;
            font-size: 0.8rem;
            font-weight: 600;
            color: var(--text-main);
            cursor: pointer;
            text-align: left;
            transition: background 0.1s ease;
        }

        .ctx-item:hover:not(:disabled) {
            background: var(--indigo-50);
            color: var(--indigo-700);
        }

        .ctx-item:disabled {
            opacity: 0.45;
            cursor: not-allowed;
        }

        .ctx-item.danger:hover {
            background: var(--rose-50);
            color: var(--rose-700);
        }

        .ctx-sep {
            height: 1px;
            background: var(--border-color);
            margin: 4px 6px;
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
            padding: 20px;
        }

        .modal-backdrop.open {
            display: flex;
        }

        .modal-card {
            background: #ffffff;
            border-radius: 18px;
            width: 100%;
            max-width: 560px;
            box-shadow: var(--shadow-xl);
            border: 1px solid var(--border-color);
            overflow: hidden;
            animation: modalPop 0.15s ease-out;
        }

        @keyframes modalPop {
            from { opacity: 0; transform: scale(0.96); }
            to   { opacity: 1; transform: scale(1); }
        }

        .modal-header {
            padding: 16px 20px;
            border-bottom: 1px solid var(--border-color);
            display: flex;
            align-items: center;
            justify-content: space-between;
            background: #f8fafc;
        }

        .modal-title {
            font-size: 1.02rem;
            font-weight: 800;
            color: var(--text-main);
        }

        .modal-subtitle {
            font-size: 0.78rem;
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
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
        }

        .modal-close:hover {
            background: #f1f5f9;
        }

        .modal-body {
            padding: 18px 20px;
            display: flex;
            flex-direction: column;
            gap: 15px;
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
            transition: all 0.12s ease;
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
            font-size: 0.7rem;
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
            padding: 9px 11px;
            border-radius: 10px;
            border: 1px solid var(--border-strong);
            font-size: 0.85rem;
            color: var(--text-main);
            outline: none;
        }

        .form-input:focus {
            border-color: var(--indigo-600);
            box-shadow: 0 0 0 3px rgba(79, 70, 229, 0.14);
        }

        .modal-footer {
            padding: 14px 20px;
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
            padding: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 220px;
            max-height: 52vh;
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
            padding: 9px 13px;
            font-size: 0.78rem;
            font-weight: 600;
            line-height: 1.4;
        }

        #toast-container {
            position: fixed;
            bottom: 20px;
            right: 24px;
            z-index: 100;
            display: flex;
            flex-direction: column;
            gap: 8px;
            pointer-events: none;
            max-width: 400px;
        }

        .toast-item {
            background: #0f172a;
            color: #ffffff;
            padding: 11px 16px;
            border-radius: 12px;
            font-size: 0.82rem;
            font-weight: 600;
            box-shadow: var(--shadow-md);
            animation: slideUp 0.2s ease-out;
        }

        @keyframes slideUp {
            from { opacity: 0; transform: translateY(10px); }
            to   { opacity: 1; transform: translateY(0); }
        }

        /* =====================================================================
           7. PRINT STYLES (OPTIMIZED FOR DESKTOP A4 LANDSCAPE)
           ===================================================================== */
        @page {
            size: A4 landscape;
            margin: 10mm;
        }

        @media print {
            .app-header, .sub-toolbar, .desktop-status-bar, .emp-del-btn, #fullscreen-top-bar, .context-menu {
                display: none !important;
            }
            body {
                background: #ffffff !important;
            }
            .main-workspace {
                margin: 0;
                padding: 0;
                max-width: none;
            }
            #fullscreen-desktop-stage {
                box-shadow: none;
                border: none;
            }
            table.schedule-table {
                min-width: 0 !important;
                width: 100% !important;
            }
            .schedule-table tbody td.sticky-col,
            .schedule-table thead th.sticky-col,
            .schedule-table tfoot td.sticky-col {
                position: static;
                box-shadow: none;
            }
            .shift-slot {
                min-height: 38px;
                padding: 3px;
                -webkit-print-color-adjust: exact;
                print-color-adjust: exact;
            }
        }
    </style>
</head>
<body>
    <!-- TOP HEADER BAR -->
    <header class="app-header">
        <div class="header-inner">
            <button type="button" id="brand-trigger-btn" class="brand-trigger" title="Click pentru a comuta modul Ecran Complet Desktop">
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
                        <span class="desktop-badge">PC DESKTOP</span>
                    </div>
                    <p class="brand-subtitle">Click stânga pentru editare • Click dreapta pentru meniu rapid • Ctrl+S pentru salvare</p>
                </div>
            </button>

            <!-- Year + Week Navigation + Language Switcher -->
            <div class="week-navigator">
                <button type="button" id="prev-week-btn" class="btn btn-icon" title="Săptămâna anterioară (Alt + ←)">
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                        <polyline points="15 18 9 12 15 6"></polyline>
                    </svg>
                </button>

                <select id="year-select" class="select-control" aria-label="Selectează anul">
                    <option value="2026" selected>2026</option>
                    <option value="2027">2027</option>
                </select>

                <select id="week-select" class="select-control" aria-label="Selectează săptămâna"></select>

                <button type="button" id="next-week-btn" class="btn btn-icon" title="Săptămâna următoare (Alt + →)">
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

            <!-- Desktop Action Buttons -->
            <div class="header-actions">
                <button type="button" id="save-changes-btn" class="btn btn-save" title="Salvează toate modificările (Ctrl+S)">
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

                <button type="button" id="fullscreen-desktop-btn" class="btn btn-soft-indigo" title="Extinde tabelul pe tot monitorul PC">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <polyline points="15 3 21 3 21 9"></polyline>
                        <polyline points="9 21 3 21 3 15"></polyline>
                        <line x1="21" y1="3" x2="14" y2="10"></line>
                        <line x1="3" y1="21" x2="10" y2="14"></line>
                    </svg>
                    <span>Ecran Complet</span>
                </button>

                <button type="button" id="print-btn" class="btn" title="Printează A4 Landscape sau salvează PDF (Ctrl+P)">
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

    <!-- LEGEND, DESKTOP EXPORT/IMPORT, SHARE ACTIONS & STATS BAR -->
    <section class="sub-toolbar">
        <div class="legend-list">
            <span class="legend-pill shift-work"><span class="legend-dot" style="background:#059669"></span><span id="legend-work-text">Program (ex. 07:00 / 08:00 / 10:00)</span></span>
            <span class="legend-pill shift-extra"><span class="legend-dot" style="background:#d97706"></span><span id="legend-extra-text">Extra</span></span>
            <span class="legend-pill shift-vrij"><span class="legend-dot" style="background:#64748b"></span><span id="legend-vrij-text">Liber</span></span>
            <span class="legend-pill shift-vakantie"><span class="legend-dot" style="background:#e11d48"></span><span id="legend-vakantie-text">Vacanță</span></span>
        </div>

        <div class="right-toolbar-group">
            <div class="share-group">
                <button type="button" id="export-csv-btn" class="btn" title="Exportă săptămâna curentă în format CSV pentru Microsoft Excel">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
                        <polyline points="14 2 14 8 20 8"></polyline>
                        <line x1="8" y1="13" x2="16" y2="13"></line>
                        <line x1="8" y1="17" x2="16" y2="17"></line>
                    </svg>
                    <span>Excel (CSV)</span>
                </button>

                <button type="button" id="backup-export-btn" class="btn" title="Descarcă copie de siguranță JSON pe PC">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path>
                        <polyline points="7 10 12 15 17 10"></polyline>
                        <line x1="12" y1="15" x2="12" y2="3"></line>
                    </svg>
                    <span>Backup PC</span>
                </button>

                <button type="button" id="backup-import-btn" class="btn" title="Încarcă o copie de siguranță JSON de pe PC">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path>
                        <polyline points="17 8 12 3 7 8"></polyline>
                        <line x1="12" y1="3" x2="12" y2="15"></line>
                    </svg>
                    <span>Restaurare</span>
                </button>
                <input type="file" id="backup-file-input" accept=".json,application/json" style="display:none;">

                <div class="toolbar-divider"></div>

                <button type="button" id="share-wa-btn" class="btn btn-whatsapp" title="Deschide WhatsApp Web și copiază imaginea PNG pentru Ctrl+V">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.38 8.38 0 0 1-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.38 8.38 0 0 1 3.8-.9h.5a8.48 8.48 0 0 1 8 8v.5z"></path>
                    </svg>
                    <span>WhatsApp Web</span>
                </button>

                <button type="button" id="share-email-btn" class="btn btn-email" title="Pregătește imaginea PNG și deschide clientul de Email">
                    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path>
                        <polyline points="22,6 12,13 2,6"></polyline>
                    </svg>
                    <span>Email</span>
                </button>

                <button type="button" id="copy-text-btn" class="btn" title="Copiază săptămâna curentă în clipboard">
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

    <!-- MAIN DESKTOP SCHEDULE WORKSPACE -->
    <main class="main-workspace">
        <div id="fullscreen-overlay-shell">
            <div id="fullscreen-desktop-stage">
                <div id="fullscreen-top-bar">
                    <div class="fs-title-group">
                        <span>SmartWork Desktop — Programul de muncă</span>
                        <span id="fs-week-label" style="color:#a5b4fc; font-weight:600;"></span>
                    </div>
                    <div class="fs-actions-group">
                        <button type="button" id="fs-save-btn" class="fs-btn fs-btn-save">💾 Salvează (Ctrl+S)</button>
                        <button type="button" id="fs-wa-btn" class="fs-btn fs-btn-wa">WhatsApp Web</button>
                        <button type="button" id="fs-mail-btn" class="fs-btn fs-btn-mail">Email</button>
                        <button type="button" id="fs-prev-btn" class="fs-btn">◀ Săpt. ant.</button>
                        <button type="button" id="fs-next-btn" class="fs-btn">Săpt. urm. ▶</button>
                        <button type="button" id="fs-exit-btn" class="fs-btn fs-btn-exit">✕ Ieșire Ecran Complet (ESC)</button>
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

    <!-- DESKTOP KEYBOARD & MOUSE STATUS BAR -->
    <footer class="desktop-status-bar">
        <div class="kbd-hints">
            <span class="kbd-chip"><kbd>Click stânga</kbd> Editare celulă</span>
            <span class="kbd-chip"><kbd>Click dreapta</kbd> Meniu rapid</span>
            <span class="kbd-chip"><kbd>Ctrl</kbd>+<kbd>C</kbd> / <kbd>Ctrl</kbd>+<kbd>V</kbd> Copiază / Lipește celula</span>
            <span class="kbd-chip"><kbd>Delete</kbd> Golește celula</span>
            <span class="kbd-chip"><kbd>Ctrl</kbd>+<kbd>S</kbd> Salvează</span>
            <span class="kbd-chip"><kbd>Alt</kbd>+<kbd>←</kbd>/<kbd>→</kbd> Schimbă săptămâna</span>
        </div>
        <div id="desktop-storage-status" style="font-weight: 600;">
            Stocare locală PC activă (Auto-Sync)
        </div>
    </footer>

    <!-- DESKTOP RIGHT-CLICK CONTEXT MENU -->
    <div id="cell-context-menu" class="context-menu" role="menu">
        <div class="ctx-header" id="ctx-menu-header">Acțiuni rapide celulă</div>
        <button type="button" class="ctx-item" data-ctx-action="set" data-type="work" data-label="07:00" data-note="">
            <span>🟢 Program 07:00</span><kbd>07:00</kbd>
        </button>
        <button type="button" class="ctx-item" data-ctx-action="set" data-type="work" data-label="08:00" data-note="">
            <span>🟢 Program 08:00</span><kbd>08:00</kbd>
        </button>
        <button type="button" class="ctx-item" data-ctx-action="set" data-type="work" data-label="09:00" data-note="">
            <span>🟢 Program 09:00</span><kbd>09:00</kbd>
        </button>
        <button type="button" class="ctx-item" data-ctx-action="set" data-type="work" data-label="10:00" data-note="">
            <span>🟢 Program 10:00</span><kbd>10:00</kbd>
        </button>
        <button type="button" class="ctx-item" data-ctx-action="set" data-type="extra" data-label="07:00" data-note="Extra">
            <span>🟠 07:00 • Extra</span><kbd>Extra</kbd>
        </button>
        <button type="button" class="ctx-item" data-ctx-action="set" data-type="vrij" data-label="__VRIJ__" data-note="">
            <span id="ctx-vrij-label">⚪ Liber</span>
        </button>
        <button type="button" class="ctx-item" data-ctx-action="set" data-type="vakantie" data-label="__VAKANTIE__" data-note="">
            <span id="ctx-vakantie-label">🔴 Vacanță</span>
        </button>
        <div class="ctx-sep"></div>
        <button type="button" class="ctx-item" data-ctx-action="copy">
            <span>📋 Copiază celula</span><kbd>Ctrl+C</kbd>
        </button>
        <button type="button" class="ctx-item" id="ctx-paste-btn" data-ctx-action="paste">
            <span>📥 Lipește celula</span><kbd>Ctrl+V</kbd>
        </button>
        <button type="button" class="ctx-item" data-ctx-action="edit">
            <span>✏️ Editare detaliată...</span><kbd>Enter</kbd>
        </button>
        <div class="ctx-sep"></div>
        <button type="button" class="ctx-item danger" data-ctx-action="clear">
            <span>🗑️ Șterge celula</span><kbd>Del</kbd>
        </button>
    </div>

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
                    <div id="quick-presets-label" style="font-size:0.76rem; font-weight:700; color:var(--text-secondary); margin-bottom:8px;">
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
                    <button type="button" id="save-shift-btn" class="btn btn-primary">Salvează (Enter)</button>
                </div>
            </div>
        </div>
    </div>

    <!-- MODAL 2: ADD EMPLOYEE -->
    <div id="emp-modal" class="modal-backdrop">
        <div class="modal-card" style="max-width:420px;">
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

    <!-- MODAL 3: PNG TABLE PREVIEW & DESKTOP SHARE -->
    <div id="share-image-modal" class="modal-backdrop">
        <div class="modal-card" style="max-width: 780px;">
            <div class="modal-header">
                <div>
                    <div class="modal-title" id="share-image-modal-title">Imagine Tabel Program (.PNG)</div>
                    <div class="modal-subtitle" id="share-image-modal-subtitle">Săpt. 47 (16 Nov – 22 Nov 2026) • Imagine PNG gata de trimis</div>
                </div>
                <button type="button" id="close-share-modal-btn" class="modal-close" aria-label="Închide">✕</button>
            </div>

            <div class="modal-body">
                <div class="share-helper-note" id="share-image-helper-text">
                    Pe PC: Apasă „Copiază Imagine”, apoi deschide WhatsApp Web sau Email și apasă Ctrl+V pentru a lipi tabelul direct în mesaj.
                </div>

                <div class="png-preview-box" id="png-preview-container">
                    <span style="font-size:0.82rem; color:var(--text-muted); font-weight:600;">Se generează imaginea tabelului...</span>
                </div>
            </div>

            <div class="modal-footer">
                <div style="display:flex; flex-wrap:wrap; gap:6px;">
                    <button type="button" id="download-png-btn" class="btn btn-soft-indigo">⬇ Descarcă PNG</button>
                    <button type="button" id="copy-png-btn" class="btn">📋 Copiază Imagine (Ctrl+V)</button>
                    <button type="button" id="modal-copy-text-btn" class="btn">📄 Copiază Text</button>
                </div>
                <div style="display:flex; flex-wrap:wrap; gap:6px;">
                    <button type="button" id="modal-wa-text-btn" class="btn btn-whatsapp">WhatsApp Web</button>
                    <button type="button" id="modal-mail-image-btn" class="btn btn-email">Client Email</button>
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
            } catch (err) {}
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
            } catch (err) {}
        }

        function writeToIndexedDB(key, val) {
            getIndexedDB().then((db) => {
                if (!db) return;
                try {
                    const tx = db.transaction(IDB_STORE_NAME, 'readwrite');
                    const store = tx.objectStore(IDB_STORE_NAME);
                    store.put(val, key);
                } catch (err) {}
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
            } catch (err) {}
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
                pageTitle: 'SmartWork Desktop — Programul de muncă (2026 & 2027)',
                brandTitle: 'Programul de muncă',
                brandSubtitle: 'Click stânga pentru editare • Click dreapta pentru meniu rapid • Ctrl+S pentru salvare',
                brandTooltip: 'Click pentru a comuta Ecran Complet Desktop',
                prevWeekTitle: 'Săptămâna anterioară (Alt + ←)',
                nextWeekTitle: 'Săptămâna următoare (Alt + →)',
                yearAria: 'Selectează anul',
                weekAria: 'Selectează săptămâna',
                langAria: 'Selectează limba',
                weekPrefix: 'Săpt.',
                week47Btn: 'Săpt. 47',
                week47Title: 'Mergi la Săpt. 47 (16–22 Nov 2026)',
                saveChangesBtn: 'Salvează modificările',
                saveChangesPending: 'Salvează modificările •',
                saveChangesTitle: 'Salvează toate modificările făcute în tabel (Ctrl+S)',
                addEmployeeBtn: '+ Angajat',
                copyPrevWeekBtn: 'Copiază Săpt. Ant.',
                copyPrevWeekTitle: 'Copiază programul din săptămâna anterioară',
                fullscreenBtn: 'Ecran Complet',
                fullscreenTitle: 'Extinde tabelul pe tot monitorul PC',
                printBtn: 'Printează',
                printTitle: 'Printează A4 Landscape sau salvează PDF (Ctrl+P)',
                legendWork: 'Program (ex. 07:00 / 08:00 / 10:00)',
                legendExtra: 'Extra',
                legendVrij: 'Liber',
                legendVakantie: 'Vacanță',
                whatsappBtn: 'WhatsApp Web',
                whatsappTitle: 'Deschide WhatsApp Web și copiază imaginea PNG pentru Ctrl+V',
                emailBtn: 'Email',
                emailTitle: 'Pregătește imaginea PNG și deschide clientul de Email',
                copyTextBtn: 'Copiază Text',
                copyTextTitle: 'Copiază săptămâna curentă',
                statsEmployees: 'Angajați:',
                statsWorkedDays: 'Zile lucrate / săpt.:',
                daySingular: 'zi',
                dayPlural: 'zile',
                fsSave: '💾 Salvează (Ctrl+S)',
                fsPrevWeek: '◀ Săpt. ant.',
                fsNextWeek: 'Săpt. urm. ▶',
                fsExit: '✕ Ieșire Ecran Complet (ESC)',
                colEmployee: 'Angajat',
                colEmployeeDetails: 'ANGAJAT & DETALII',
                colDays: 'Zile',
                colDaysUpper: 'ZILE',
                presentPerDay: 'Prezenți / zi',
                noEmployeesTable: 'Nu există angajați adăugați. Apasă pe butonul <strong>+ Angajat</strong> pentru a începe.',
                noEmployeesCanvas: 'Nu există angajați adăugați pentru această săptămână.',
                removeEmployeeTitle: 'Elimină angajatul',
                setCellTitle: 'Click stânga pentru editare • Click dreapta pentru meniu rapid',
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
                saveBtn: 'Salvează (Enter)',
                addEmpModalTitle: 'Adaugă Angajat Nou',
                addEmpModalSubtitle: 'Va apărea imediat în tabelul săptămânal',
                empNameLabel: 'Nume și Prenume *',
                empNamePlaceholder: 'Ex: Popescu Andrei',
                empRoleLabel: 'Funcție / Grup (opțional)',
                empRolePlaceholder: 'Ex: Grup A, Grup B, Grup C...',
                empDefaultRole: 'Angajat',
                addEmpSubmitBtn: 'Adaugă în program',
                shareModalTitle: 'Trimite Săptămâna & Imaginea (.PNG) pe PC',
                shareModalSubtitle: 'Săpt. {week} ({range}) • Imagine PNG gata de lipit cu Ctrl+V',
                shareError: 'Nu s-a putut genera imaginea PNG a tabelului.',
                shareHelperDesktop: 'Pe PC: Apasă „Copiază Imagine (Ctrl+V)”, apoi deschide WhatsApp Web sau clientul de Email și apasă Ctrl+V pentru a lipi tabelul direct în mesaj.',
                downloadPngBtn: '⬇ Descarcă PNG',
                copyImageBtn: '📋 Copiază Imagine (Ctrl+V)',
                copyTextModalBtn: '📄 Copiază Text',
                waTextBtn: 'WhatsApp Web',
                mailImageBtn: 'Client Email',
                closeBtn: 'Închide',
                canvasBannerTitle: 'PROGRAMUL DE MUNCĂ • SĂPTĂMÂNA {week} ({range})',
                canvasBannerStats: 'Angajați: {count}   •   Total zile lucrate: {days} zile',
                canvasLegendWork: 'Program (ex. 07:00 / 08:00 / 10:00)',
                canvasLegendExtra: 'Extra',
                canvasLegendVrij: 'Liber',
                canvasLegendVakantie: 'Vacanță',
                shareTextTitle: 'PROGRAMUL DE MUNCĂ - Săpt. {week} ({range})',
                toastFirstWeek2026: 'Ai ajuns la prima săptămână din 2026.',
                toastLastWeek2027: 'Ai ajuns la ultima săptămână din 2027.',
                toastWeek47: 'Afișat Săpt. 47 (16 – 22 Noiembrie 2026).',
                toastChangesSaved: 'Toate modificările au fost salvate pe PC.',
                toastShiftSaved: 'Programul zilei a fost actualizat. Apasă Ctrl+S pentru confirmare.',
                toastExtraDayAdded: 'Zi Extra adăugată pentru {day}.',
                toastGroupReapplied: 'Programul grupei a fost reaplicat pe această săptămână.',
                toastAppliedMonFri: 'Program aplicat pentru Luni – Vineri.',
                toastCellCleared: 'Celula a fost golită.',
                toastCellCopied: 'Celula a fost copiată (Ctrl+V pentru lipire).',
                toastCellPasted: 'Programul copiat a fost lipit în celulă.',
                toastEmpAdded: 'Angajatul {name} a fost adăugat.',
                toastEmpRemoved: 'Angajatul a fost eliminat din listă.',
                toastNoPrevWeek: 'Nu există o săptămână anterioară disponibilă.',
                toastPrevWeekEmpty: 'Săptămâna {week} nu are ture salvate.',
                toastWeekCopied: 'Programul din Săpt. {week} a fost copiat.',
                toastTextCopied: 'Textul săptămânii a fost copiat în clipboard.',
                toastTextCopyFail: 'Nu s-a putut copia automat; folosește butoanele WhatsApp Web sau Email.',
                toastPngNotReady: 'Imaginea PNG nu a putut fi pregătită.',
                toastPngDownloaded: 'Imaginea {filename} a fost descărcată.',
                toastPngOpenFail: 'Deschide imaginea din previzualizare pentru a o salva.',
                toastNoPng: 'Nu există o imagine PNG generată.',
                toastImgCopied: 'Imaginea tabelului a fost copiată! Apasă Ctrl+V în WhatsApp Web sau Email.',
                toastImgCopyFallback: 'Browserul nu permite copierea directă a imaginii; PNG-ul a fost descărcat.',
                toastOpenedWaText: 'WhatsApp Web a fost deschis. Poți lipi imaginea cu Ctrl+V.',
                toastOpenedMail: 'Clientul de Email a fost deschis.',
                toastFsActive: 'Ecran complet desktop activ • Apasă ESC pentru a reveni.',
                toastCsvExported: 'Fișierul Excel (CSV) pentru Săpt. {week} a fost descărcat.',
                toastBackupExported: 'Copia de siguranță JSON a fost descărcată pe PC.',
                toastBackupRestored: 'Datele din copia de siguranță au fost restaurate cu succes!',
                toastBackupInvalid: 'Fișierul selectat nu este o copie de siguranță validă SmartWork.'
            },
            de: {
                pageTitle: 'SmartWork Desktop — Arbeitsplan & Schichten (2026 & 2027)',
                brandTitle: 'Arbeitsplan',
                brandSubtitle: 'Linksklick zum Bearbeiten • Rechtsklick für Schnellmenü • Strg+S zum Speichern',
                brandTooltip: 'Klicken, um Desktop-Vollbild umzuschalten',
                prevWeekTitle: 'Vorherige Woche (Alt + ←)',
                nextWeekTitle: 'Nächste Woche (Alt + →)',
                yearAria: 'Jahr auswählen',
                weekAria: 'Woche auswählen',
                langAria: 'Sprache auswählen',
                weekPrefix: 'KW',
                week47Btn: 'KW 47',
                week47Title: 'Zu KW 47 wechseln (16.–22. Nov 2026)',
                saveChangesBtn: 'Änderungen speichern',
                saveChangesPending: 'Änderungen speichern •',
                saveChangesTitle: 'Alle Änderungen speichern (Strg+S)',
                addEmployeeBtn: '+ Mitarbeiter',
                copyPrevWeekBtn: 'Vorwoche kopieren',
                copyPrevWeekTitle: 'Plan der vorherigen Woche kopieren',
                fullscreenBtn: 'Vollbild',
                fullscreenTitle: 'Tabelle auf den gesamten Monitor erweitern',
                printBtn: 'Drucken',
                printTitle: 'A4 Querformat drucken oder als PDF speichern',
                legendWork: 'Arbeitszeit (z. B. 07:00 / 08:00 / 10:00)',
                legendExtra: 'Extra',
                legendVrij: 'Frei',
                legendVakantie: 'Urlaub',
                whatsappBtn: 'WhatsApp Web',
                whatsappTitle: 'WhatsApp Web öffnen und PNG-Bild für Strg+V kopieren',
                emailBtn: 'E-Mail',
                emailTitle: 'PNG-Bild vorbereiten und E-Mail-Programm öffnen',
                copyTextBtn: 'Text kopieren',
                copyTextTitle: 'Aktuelle Woche kopieren',
                statsEmployees: 'Mitarbeiter:',
                statsWorkedDays: 'Arbeitstage / Wo.:',
                daySingular: 'Tag',
                dayPlural: 'Tage',
                fsSave: '💾 Speichern (Strg+S)',
                fsPrevWeek: '◀ Vorwoche',
                fsNextWeek: 'Nächste Wo. ▶',
                fsExit: '✕ Vollbild beenden (ESC)',
                colEmployee: 'Mitarbeiter',
                colEmployeeDetails: 'MITARBEITER & DETAILS',
                colDays: 'Tage',
                colDaysUpper: 'TAGE',
                presentPerDay: 'Anwesend / Tag',
                noEmployeesTable: 'Keine Mitarbeiter vorhanden. Klicken Sie auf <strong>+ Mitarbeiter</strong>, um zu starten.',
                noEmployeesCanvas: 'Für diese Woche sind keine Mitarbeiter eingetragen.',
                removeEmployeeTitle: 'Mitarbeiter entfernen',
                setCellTitle: 'Linksklick zum Bearbeiten • Rechtsklick für Schnellmenü',
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
                saveBtn: 'Speichern (Enter)',
                addEmpModalTitle: 'Neuen Mitarbeiter hinzufügen',
                addEmpModalSubtitle: 'Erscheint sofort im Wochenplan',
                empNameLabel: 'Vor- und Nachname *',
                empNamePlaceholder: 'Z. B. Max Mustermann',
                empRoleLabel: 'Funktion / Gruppe (optional)',
                empRolePlaceholder: 'Z. B. Gruppe A, Gruppe B...',
                empDefaultRole: 'Mitarbeiter',
                addEmpSubmitBtn: 'Zum Plan hinzufügen',
                shareModalTitle: 'Woche & Tabellenbild senden (.PNG)',
                shareModalSubtitle: 'KW {week} ({range}) • Bereit zum Einfügen mit Strg+V',
                shareError: 'Das PNG-Bild der Tabelle konnte nicht erstellt werden.',
                shareHelperDesktop: 'Am PC: Klicken Sie auf „Bild kopieren (Strg+V)“, öffnen Sie WhatsApp Web oder E-Mail und drücken Sie Strg+V.',
                downloadPngBtn: '⬇ PNG herunterladen',
                copyImageBtn: '📋 Bild kopieren (Strg+V)',
                copyTextModalBtn: '📄 Text kopieren',
                waTextBtn: 'WhatsApp Web',
                mailImageBtn: 'E-Mail-Client',
                closeBtn: 'Schließen',
                canvasBannerTitle: 'ARBEITSPLAN • KALENDERWOCHE {week} ({range})',
                canvasBannerStats: 'Mitarbeiter: {count}   •   Arbeitstage gesamt: {days} Tage',
                canvasLegendWork: 'Arbeitszeit (z. B. 07:00 / 08:00 / 10:00)',
                canvasLegendExtra: 'Extra',
                canvasLegendVrij: 'Frei',
                canvasLegendVakantie: 'Urlaub',
                shareTextTitle: 'ARBEITSPLAN - KW {week} ({range})',
                toastFirstWeek2026: 'Erste Woche von 2026 erreicht.',
                toastLastWeek2027: 'Letzte Woche von 2027 erreicht.',
                toastWeek47: 'KW 47 angezeigt (16.–22. November 2026).',
                toastChangesSaved: 'Alle Änderungen wurden auf dem PC gespeichert.',
                toastShiftSaved: 'Tagesplan aktualisiert. Drücken Sie Strg+S zur Bestätigung.',
                toastExtraDayAdded: 'Extra-Tag für {day} hinzugefügt.',
                toastGroupReapplied: 'Gruppenplan für diese Woche erneut angewendet.',
                toastAppliedMonFri: 'Plan auf Montag–Freitag angewendet.',
                toastCellCleared: 'Zelle geleert.',
                toastCellCopied: 'Zelle kopiert (Strg+V zum Einfügen).',
                toastCellPasted: 'Kopierter Plan in Zelle eingefügt.',
                toastEmpAdded: 'Mitarbeiter {name} hinzugefügt.',
                toastEmpRemoved: 'Mitarbeiter aus der Liste entfernt.',
                toastNoPrevWeek: 'Keine vorherige Woche verfügbar.',
                toastPrevWeekEmpty: 'In KW {week} sind keine Einträge gespeichert.',
                toastWeekCopied: 'Plan aus KW {week} kopiert.',
                toastTextCopied: 'Wochentext in die Zwischenablage kopiert.',
                toastTextCopyFail: 'Automatisches Kopieren nicht möglich.',
                toastPngNotReady: 'PNG-Bild konnte nicht vorbereitet werden.',
                toastPngDownloaded: 'Bild {filename} heruntergeladen.',
                toastPngOpenFail: 'Öffnen Sie das Bild in der Vorschau, um es zu speichern.',
                toastNoPng: 'Kein PNG-Bild vorhanden.',
                toastImgCopied: 'Tabellenbild kopiert! Drücken Sie Strg+V in WhatsApp Web oder E-Mail.',
                toastImgCopyFallback: 'PNG wurde zum Anhängen heruntergeladen.',
                toastOpenedWaText: 'WhatsApp Web geöffnet. Bild mit Strg+V einfügen.',
                toastOpenedMail: 'E-Mail-Programm geöffnet.',
                toastFsActive: 'Desktop-Vollbild aktiv • ESC drücken zum Beenden.',
                toastCsvExported: 'Excel-Datei (CSV) für KW {week} heruntergeladen.',
                toastBackupExported: 'JSON-Backup auf den PC heruntergeladen.',
                toastBackupRestored: 'Daten aus Backup erfolgreich wiederhergestellt!',
                toastBackupInvalid: 'Die ausgewählte Datei ist kein gültiges SmartWork-Backup.'
            },
            en: {
                pageTitle: 'SmartWork Desktop — Work Schedule & Shifts (2026 & 2027)',
                brandTitle: 'Work Schedule',
                brandSubtitle: 'Left-click to edit • Right-click for quick menu • Ctrl+S to save',
                brandTooltip: 'Click to toggle Desktop Fullscreen',
                prevWeekTitle: 'Previous week (Alt + ←)',
                nextWeekTitle: 'Next week (Alt + →)',
                yearAria: 'Select year',
                weekAria: 'Select week',
                langAria: 'Select language',
                weekPrefix: 'Week',
                week47Btn: 'Week 47',
                week47Title: 'Go to Week 47 (16–22 Nov 2026)',
                saveChangesBtn: 'Save changes',
                saveChangesPending: 'Save changes •',
                saveChangesTitle: 'Save all changes made in the table (Ctrl+S)',
                addEmployeeBtn: '+ Employee',
                copyPrevWeekBtn: 'Copy Prev. Week',
                copyPrevWeekTitle: 'Copy schedule from previous week',
                fullscreenBtn: 'Fullscreen',
                fullscreenTitle: 'Expand schedule across the entire PC monitor',
                printBtn: 'Print',
                printTitle: 'Print A4 Landscape or save as PDF (Ctrl+P)',
                legendWork: 'Schedule (e.g. 07:00 / 08:00 / 10:00)',
                legendExtra: 'Extra',
                legendVrij: 'Off',
                legendVakantie: 'Vacation',
                whatsappBtn: 'WhatsApp Web',
                whatsappTitle: 'Open WhatsApp Web and copy PNG image for Ctrl+V',
                emailBtn: 'Email',
                emailTitle: 'Prepare PNG image and open Email client',
                copyTextBtn: 'Copy Text',
                copyTextTitle: 'Copy current week',
                statsEmployees: 'Employees:',
                statsWorkedDays: 'Worked days / wk:',
                daySingular: 'day',
                dayPlural: 'days',
                fsSave: '💾 Save (Ctrl+S)',
                fsPrevWeek: '◀ Prev. wk',
                fsNextWeek: 'Next wk ▶',
                fsExit: '✕ Exit Fullscreen (ESC)',
                colEmployee: 'Employee',
                colEmployeeDetails: 'EMPLOYEE & DETAILS',
                colDays: 'Days',
                colDaysUpper: 'DAYS',
                presentPerDay: 'Present / day',
                noEmployeesTable: 'No employees added yet. Click <strong>+ Employee</strong> to get started.',
                noEmployeesCanvas: 'No employees added for this week.',
                removeEmployeeTitle: 'Remove employee',
                setCellTitle: 'Left-click to edit • Right-click for quick menu',
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
                saveBtn: 'Save (Enter)',
                addEmpModalTitle: 'Add New Employee',
                addEmpModalSubtitle: 'Will appear immediately in the weekly table',
                empNameLabel: 'Full Name *',
                empNamePlaceholder: 'E.g. Alex Morgan',
                empRoleLabel: 'Role / Group (optional)',
                empRolePlaceholder: 'E.g. Group A, Group B, Group C...',
                empDefaultRole: 'Employee',
                addEmpSubmitBtn: 'Add to schedule',
                shareModalTitle: 'Send Week & Schedule Image (.PNG) on PC',
                shareModalSubtitle: 'Week {week} ({range}) • Ready to paste with Ctrl+V',
                shareError: 'Could not generate PNG image of the table.',
                shareHelperDesktop: 'On PC: Click "Copy Image (Ctrl+V)", then open WhatsApp Web or your Email client and press Ctrl+V to paste the schedule directly.',
                downloadPngBtn: '⬇ Download PNG',
                copyImageBtn: '📋 Copy Image (Ctrl+V)',
                copyTextModalBtn: '📄 Copy Text',
                waTextBtn: 'WhatsApp Web',
                mailImageBtn: 'Email Client',
                closeBtn: 'Close',
                canvasBannerTitle: 'WORK SCHEDULE • WEEK {week} ({range})',
                canvasBannerStats: 'Employees: {count}   •   Total worked days: {days} days',
                canvasLegendWork: 'Schedule (e.g. 07:00 / 08:00 / 10:00)',
                canvasLegendExtra: 'Extra',
                canvasLegendVrij: 'Off',
                canvasLegendVakantie: 'Vacation',
                shareTextTitle: 'WORK SCHEDULE - Week {week} ({range})',
                toastFirstWeek2026: 'Reached the first week of 2026.',
                toastLastWeek2027: 'Reached the last week of 2027.',
                toastWeek47: 'Showing Week 47 (16 – 22 November 2026).',
                toastChangesSaved: 'All changes have been saved on PC.',
                toastShiftSaved: 'Daily schedule updated. Press Ctrl+S to confirm.',
                toastExtraDayAdded: 'Extra day added for {day}.',
                toastGroupReapplied: 'Group schedule reapplied for this week.',
                toastAppliedMonFri: 'Schedule applied to Monday – Friday.',
                toastCellCleared: 'Cell cleared.',
                toastCellCopied: 'Cell copied (Ctrl+V to paste).',
                toastCellPasted: 'Copied schedule pasted into cell.',
                toastEmpAdded: 'Employee {name} added.',
                toastEmpRemoved: 'Employee removed from list.',
                toastNoPrevWeek: 'No previous week available.',
                toastPrevWeekEmpty: 'Week {week} has no saved shifts.',
                toastWeekCopied: 'Copied schedule from Week {week}.',
                toastTextCopied: 'Week text copied to clipboard.',
                toastTextCopyFail: 'Could not copy automatically; use WhatsApp Web or Email buttons.',
                toastPngNotReady: 'PNG image could not be prepared.',
                toastPngDownloaded: 'Image {filename} downloaded.',
                toastPngOpenFail: 'Open the image from preview to save it.',
                toastNoPng: 'No PNG image generated.',
                toastImgCopied: 'Table image copied! Press Ctrl+V in WhatsApp Web or Email.',
                toastImgCopyFallback: 'PNG downloaded to attach.',
                toastOpenedWaText: 'WhatsApp Web opened. Paste the image with Ctrl+V.',
                toastOpenedMail: 'Email client opened.',
                toastFsActive: 'Desktop fullscreen active • Press ESC to exit.',
                toastCsvExported: 'Excel (CSV) file for Week {week} downloaded.',
                toastBackupExported: 'JSON backup downloaded to your PC.',
                toastBackupRestored: 'Backup data restored successfully!',
                toastBackupInvalid: 'Selected file is not a valid SmartWork backup.'
            },
            ru: {
                pageTitle: 'SmartWork Desktop — График работы и смен (2026 и 2027)',
                brandTitle: 'График работы',
                brandSubtitle: 'ЛКМ — редактировать • ПКМ — быстрое меню • Ctrl+S — сохранить',
                brandTooltip: 'Нажмите для полноэкранного режима на ПК',
                prevWeekTitle: 'Предыдущая неделя (Alt + ←)',
                nextWeekTitle: 'Следующая неделя (Alt + →)',
                yearAria: 'Выберите год',
                weekAria: 'Выберите неделю',
                langAria: 'Выберите язык',
                weekPrefix: 'Нед.',
                week47Btn: 'Нед. 47',
                week47Title: 'Перейти к неделе 47 (16–22 ноя 2026)',
                saveChangesBtn: 'Сохранить изменения',
                saveChangesPending: 'Сохранить изменения •',
                saveChangesTitle: 'Сохранить все изменения в таблице (Ctrl+S)',
                addEmployeeBtn: '+ Сотрудник',
                copyPrevWeekBtn: 'Копия пред. нед.',
                copyPrevWeekTitle: 'Скопировать график с предыдущей недели',
                fullscreenBtn: 'Полный экран',
                fullscreenTitle: 'Развернуть таблицу на весь монитор ПК',
                printBtn: 'Печать',
                printTitle: 'Печать A4 альбомная или PDF (Ctrl+P)',
                legendWork: 'График (напр. 07:00 / 08:00 / 10:00)',
                legendExtra: 'Extra',
                legendVrij: 'Выходной',
                legendVakantie: 'Отпуск',
                whatsappBtn: 'WhatsApp Web',
                whatsappTitle: 'Открыть WhatsApp Web и скопировать PNG для Ctrl+V',
                emailBtn: 'Email',
                emailTitle: 'Подготовить PNG и открыть почтовый клиент',
                copyTextBtn: 'Копировать',
                copyTextTitle: 'Скопировать текущую неделю',
                statsEmployees: 'Сотрудники:',
                statsWorkedDays: 'Рабочих дней / нед.:',
                daySingular: 'день',
                dayPlural: 'дней',
                fsSave: '💾 Сохранить (Ctrl+S)',
                fsPrevWeek: '◀ Пред. нед.',
                fsNextWeek: 'След. нед. ▶',
                fsExit: '✕ Выход из полноэкранного режима (ESC)',
                colEmployee: 'Сотрудник',
                colEmployeeDetails: 'СОТРУДНИК И ДЕТАЛИ',
                colDays: 'Дни',
                colDaysUpper: 'ДНИ',
                presentPerDay: 'На смене / день',
                noEmployeesTable: 'Сотрудники не добавлены. Нажмите <strong>+ Сотрудник</strong>, чтобы начать.',
                noEmployeesCanvas: 'На эту неделю сотрудники не добавлены.',
                removeEmployeeTitle: 'Удалить сотрудника',
                setCellTitle: 'ЛКМ — редактировать • ПКМ — быстрое меню',
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
                saveBtn: 'Сохранить (Enter)',
                addEmpModalTitle: 'Добавить сотрудника',
                addEmpModalSubtitle: 'Сразу появится в недельном графике',
                empNameLabel: 'Имя и фамилия *',
                empNamePlaceholder: 'Напр.: Иван Петров',
                empRoleLabel: 'Должность / Группа (необязательно)',
                empRolePlaceholder: 'Напр.: Группа A, Группа B...',
                empDefaultRole: 'Сотрудник',
                addEmpSubmitBtn: 'Добавить в график',
                shareModalTitle: 'Отправить неделю и картинку (.PNG) на ПК',
                shareModalSubtitle: 'Нед. {week} ({range}) • Готово для вставки через Ctrl+V',
                shareError: 'Не удалось создать PNG-изображение таблицы.',
                shareHelperDesktop: 'На ПК: Нажмите «Копировать картинку (Ctrl+V)», откройте WhatsApp Web или Email и нажмите Ctrl+V.',
                downloadPngBtn: '⬇ Скачать PNG',
                copyImageBtn: '📋 Копировать картинку (Ctrl+V)',
                copyTextModalBtn: '📄 Копировать текст',
                waTextBtn: 'WhatsApp Web',
                mailImageBtn: 'Почтовый клиент',
                closeBtn: 'Закрыть',
                canvasBannerTitle: 'ГРАФИК РАБОТЫ • НЕДЕЛЯ {week} ({range})',
                canvasBannerStats: 'Сотрудников: {count}   •   Всего рабочих дней: {days} дн.',
                canvasLegendWork: 'График (напр. 07:00 / 08:00 / 10:00)',
                canvasLegendExtra: 'Extra',
                canvasLegendVrij: 'Выходной',
                canvasLegendVakantie: 'Отпуск',
                shareTextTitle: 'ГРАФИК РАБОТЫ - Нед. {week} ({range})',
                toastFirstWeek2026: 'Достигнута первая неделя 2026 года.',
                toastLastWeek2027: 'Достигнута последняя неделя 2027 года.',
                toastWeek47: 'Показана неделя 47 (16 – 22 ноября 2026).',
                toastChangesSaved: 'Все изменения сохранены на ПК.',
                toastShiftSaved: 'Дневной график обновлён. Нажмите Ctrl+S для подтверждения.',
                toastExtraDayAdded: 'День Extra добавлен на {day}.',
                toastGroupReapplied: 'График группы повторно применён на эту неделю.',
                toastAppliedMonFri: 'График применён с понедельника по пятницу.',
                toastCellCleared: 'Ячейка очищена.',
                toastCellCopied: 'Ячейка скопирована (Ctrl+V для вставки).',
                toastCellPasted: 'Скопированный график вставлен в ячейку.',
                toastEmpAdded: 'Сотрудник {name} добавлен.',
                toastEmpRemoved: 'Сотрудник удалён из списка.',
                toastNoPrevWeek: 'Предыдущая неделя недоступна.',
                toastPrevWeekEmpty: 'В неделе {week} нет сохранённых смен.',
                toastWeekCopied: 'График с недели {week} скопирован.',
                toastTextCopied: 'Текст недели скопирован в буфер обмена.',
                toastTextCopyFail: 'Автокопирование недоступно; используйте WhatsApp Web или Email.',
                toastPngNotReady: 'Не удалось подготовить PNG-изображение.',
                toastPngDownloaded: 'Изображение {filename} скачано.',
                toastPngOpenFail: 'Откройте изображение в предпросмотре, чтобы сохранить его.',
                toastNoPng: 'PNG-изображение не создано.',
                toastImgCopied: 'Картинка скопирована! Нажмите Ctrl+V в WhatsApp Web или Email.',
                toastImgCopyFallback: 'PNG скачан для отправки.',
                toastOpenedWaText: 'WhatsApp Web открыт. Вставьте картинку через Ctrl+V.',
                toastOpenedMail: 'Почтовый клиент открыт.',
                toastFsActive: 'Полноэкранный режим ПК активен • Нажмите ESC для выхода.',
                toastCsvExported: 'Файл Excel (CSV) за неделю {week} скачан.',
                toastBackupExported: 'Резервная копия JSON скачана на ПК.',
                toastBackupRestored: 'Данные из резервной копии успешно восстановлены!',
                toastBackupInvalid: 'Выбранный файл не является корректной копией SmartWork.'
            },
            tr: {
                pageTitle: 'SmartWork Desktop — Çalışma Programı & Vardiyalar (2026 & 2027)',
                brandTitle: 'Çalışma Programı',
                brandSubtitle: 'Düzenlemek için sol tık • Hızlı menü için sağ tık • Kaydetmek için Ctrl+S',
                brandTooltip: 'Masaüstü Tam Ekran modunu açmak/kapatmak için tıklayın',
                prevWeekTitle: 'Önceki hafta (Alt + ←)',
                nextWeekTitle: 'Sonraki hafta (Alt + →)',
                yearAria: 'Yıl seçin',
                weekAria: 'Hafta seçin',
                langAria: 'Dil seçin',
                weekPrefix: 'Hafta',
                week47Btn: 'Hafta 47',
                week47Title: '47. Haftaya git (16–22 Kas 2026)',
                saveChangesBtn: 'Değişiklikleri kaydet',
                saveChangesPending: 'Değişiklikleri kaydet •',
                saveChangesTitle: 'Tablodaki tüm değişiklikleri kaydet (Ctrl+S)',
                addEmployeeBtn: '+ Çalışan',
                copyPrevWeekBtn: 'Önceki Haftayı Kopyala',
                copyPrevWeekTitle: 'Önceki haftanın programını kopyala',
                fullscreenBtn: 'Tam Ekran',
                fullscreenTitle: 'Tabloyu tüm PC monitörüne genişlet',
                printBtn: 'Yazdır',
                printTitle: 'A4 Yatay yazdır veya PDF olarak kaydet (Ctrl+P)',
                legendWork: 'Program (örn. 07:00 / 08:00 / 10:00)',
                legendExtra: 'Extra',
                legendVrij: 'İzinli',
                legendVakantie: 'Tatil',
                whatsappBtn: 'WhatsApp Web',
                whatsappTitle: 'WhatsApp Web aç ve Ctrl+V için PNG görselini kopyala',
                emailBtn: 'E-posta',
                emailTitle: 'PNG görselini hazırla ve E-posta istemcisini aç',
                copyTextBtn: 'Kopyala',
                copyTextTitle: 'Mevcut haftayı kopyala',
                statsEmployees: 'Çalışanlar:',
                statsWorkedDays: 'Çalışılan gün / hf.:',
                daySingular: 'gün',
                dayPlural: 'gün',
                fsSave: '💾 Kaydet (Ctrl+S)',
                fsPrevWeek: '◀ Önceki hf.',
                fsNextWeek: 'Sonraki hf. ▶',
                fsExit: '✕ Tam Ekrandan Çık (ESC)',
                colEmployee: 'Çalışan',
                colEmployeeDetails: 'ÇALIŞAN & DETAYLAR',
                colDays: 'Gün',
                colDaysUpper: 'GÜN',
                presentPerDay: 'Mevcut / gün',
                noEmployeesTable: 'Henüz çalışan eklenmedi. Başlamak için <strong>+ Çalışan</strong> düğmesine tıklayın.',
                noEmployeesCanvas: 'Bu hafta için çalışan eklenmedi.',
                removeEmployeeTitle: 'Çalışanı kaldır',
                setCellTitle: 'Düzenlemek için sol tık • Hızlı menü için sağ tık',
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
                saveBtn: 'Kaydet (Enter)',
                addEmpModalTitle: 'Yeni Çalışan Ekle',
                addEmpModalSubtitle: 'Haftalık tabloda hemen görünür',
                empNameLabel: 'Ad Soyad *',
                empNamePlaceholder: 'Örn: Ahmet Yılmaz',
                empRoleLabel: 'Görev / Grup (isteğe bağlı)',
                empRolePlaceholder: 'Örn: Grup A, Grup B, Grup C...',
                empDefaultRole: 'Çalışan',
                addEmpSubmitBtn: 'Programa ekle',
                shareModalTitle: 'Haftayı ve Tablo Görselini Gönder (.PNG)',
                shareModalSubtitle: 'Hafta {week} ({range}) • Ctrl+V ile yapıştırmaya hazır',
                shareError: 'Tablonun PNG görseli oluşturulamadı.',
                shareHelperDesktop: 'PC’de: „Görseli Kopyala (Ctrl+V)“ düğmesine tıklayın, WhatsApp Web veya E-posta istemcisini açıp Ctrl+V ile yapıştırın.',
                downloadPngBtn: '⬇ PNG İndir',
                copyImageBtn: '📋 Görseli Kopyala (Ctrl+V)',
                copyTextModalBtn: '📄 Metni Kopyala',
                waTextBtn: 'WhatsApp Web',
                mailImageBtn: 'E-posta İstemcisi',
                closeBtn: 'Kapat',
                canvasBannerTitle: 'ÇALIŞMA PROGRAMI • HAFTA {week} ({range})',
                canvasBannerStats: 'Çalışanlar: {count}   •   Toplam çalışılan gün: {days} gün',
                canvasLegendWork: 'Program (örn. 07:00 / 08:00 / 10:00)',
                canvasLegendExtra: 'Extra',
                canvasLegendVrij: 'İzinli',
                canvasLegendVakantie: 'Tatil',
                shareTextTitle: 'ÇALIŞMA PROGRAMI - Hafta {week} ({range})',
                toastFirstWeek2026: '2026 yılının ilk haftasına ulaştınız.',
                toastLastWeek2027: '2027 yılının son haftasına ulaştınız.',
                toastWeek47: '47. Hafta gösteriliyor (16 – 22 Kasım 2026).',
                toastChangesSaved: 'Tüm değişiklikler PC’ye kaydedildi.',
                toastShiftSaved: 'Günlük program güncellendi. Onaylamak için Ctrl+S tuşuna basın.',
                toastExtraDayAdded: '{day} için Extra gün eklendi.',
                toastGroupReapplied: 'Bu hafta için grup programı yeniden uygulandı.',
                toastAppliedMonFri: 'Program Pazartesi – Cuma günlerine uygulandı.',
                toastCellCleared: 'Hücre temizlendi.',
                toastCellCopied: 'Hücre kopyalandı (yapıştırmak için Ctrl+V).',
                toastCellPasted: 'Kopyalanan program hücreye yapıştırıldı.',
                toastEmpAdded: '{name} adlı çalışan eklendi.',
                toastEmpRemoved: 'Çalışan listeden kaldırıldı.',
                toastNoPrevWeek: 'Önceki hafta bulunamadı.',
                toastPrevWeekEmpty: '{week}. haftada kayıtlı vardiya yok.',
                toastWeekCopied: '{week}. haftanın programı kopyalandı.',
                toastTextCopied: 'Hafta metni panoya kopyalandı.',
                toastTextCopyFail: 'Otomatik kopyalanamadı.',
                toastPngNotReady: 'PNG görseli hazırlanamadı.',
                toastPngDownloaded: '{filename} görseli indirildi.',
                toastPngOpenFail: 'Kaydetmek için önizlemeden görseli açın.',
                toastNoPng: 'Oluşturulmuş PNG görseli yok.',
                toastImgCopied: 'Tablo görseli kopyalandı! WhatsApp Web veya E-posta’da Ctrl+V yapın.',
                toastImgCopyFallback: 'PNG eklemek için indirildi.',
                toastOpenedWaText: 'WhatsApp Web açıldı. Görseli Ctrl+V ile yapıştırabilirsiniz.',
                toastOpenedMail: 'E-posta istemcisi açıldı.',
                toastFsActive: 'Masaüstü tam ekran aktif • Çıkmak için ESC tuşuna basın.',
                toastCsvExported: '{week}. hafta için Excel (CSV) dosyası indirildi.',
                toastBackupExported: 'JSON yedek dosyası PC’ye indirildi.',
                toastBackupRestored: 'Yedek veriler başarıyla geri yüklendi!',
                toastBackupInvalid: 'Seçilen dosya geçerli bir SmartWork yedeği değil.'
            },
            nl: {
                pageTitle: 'SmartWork Desktop — Werkrooster & Diensten (2026 & 2027)',
                brandTitle: 'Werkrooster',
                brandSubtitle: 'Linksklik om te bewerken • Rechtsklik voor snelmenu • Ctrl+S om op te slaan',
                brandTooltip: 'Klik om Desktop Volledig Scherm te wisselen',
                prevWeekTitle: 'Vorige week (Alt + ←)',
                nextWeekTitle: 'Volgende week (Alt + →)',
                yearAria: 'Selecteer jaar',
                weekAria: 'Selecteer week',
                langAria: 'Selecteer taal',
                weekPrefix: 'Week',
                week47Btn: 'Week 47',
                week47Title: 'Ga naar Week 47 (16–22 nov 2026)',
                saveChangesBtn: 'Wijzigingen opslaan',
                saveChangesPending: 'Wijzigingen opslaan •',
                saveChangesTitle: 'Alle wijzigingen in de tabel opslaan (Ctrl+S)',
                addEmployeeBtn: '+ Medewerker',
                copyPrevWeekBtn: 'Kopieer Vorige Wk',
                copyPrevWeekTitle: 'Kopieer rooster van vorige week',
                fullscreenBtn: 'Volledig Scherm',
                fullscreenTitle: 'Tabel uitbreiden over het volledige PC-scherm',
                printBtn: 'Afdrukken',
                printTitle: 'Afdrukken op A4 liggend of opslaan als PDF (Ctrl+P)',
                legendWork: 'Rooster (bijv. 07:00 / 08:00 / 10:00)',
                legendExtra: 'Extra',
                legendVrij: 'Vrij',
                legendVakantie: 'Vakantie',
                whatsappBtn: 'WhatsApp Web',
                whatsappTitle: 'Open WhatsApp Web en kopieer PNG-afbeelding voor Ctrl+V',
                emailBtn: 'E-mail',
                emailTitle: 'Bereid PNG-afbeelding voor en open E-mailclient',
                copyTextBtn: 'Kopieer',
                copyTextTitle: 'Kopieer huidige week',
                statsEmployees: 'Medewerkers:',
                statsWorkedDays: 'Gewerkte dagen / wk:',
                daySingular: 'dag',
                dayPlural: 'dagen',
                fsSave: '💾 Opslaan (Ctrl+S)',
                fsPrevWeek: '◀ Vorige wk',
                fsNextWeek: 'Volgende wk ▶',
                fsExit: '✕ Volledig scherm sluiten (ESC)',
                colEmployee: 'Medewerker',
                colEmployeeDetails: 'MEDEWERKER & DETAILS',
                colDays: 'Dagen',
                colDaysUpper: 'DAGEN',
                presentPerDay: 'Aanwezig / dag',
                noEmployeesTable: 'Nog geen medewerkers toegevoegd. Klik op <strong>+ Medewerker</strong> om te beginnen.',
                noEmployeesCanvas: 'Geen medewerkers toegevoegd voor deze week.',
                removeEmployeeTitle: 'Verwijder medewerker',
                setCellTitle: 'Linksklik om te bewerken • Rechtsklik voor snelmenu',
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
                saveBtn: 'Opslaan (Enter)',
                addEmpModalTitle: 'Nieuwe Medewerker Toevoegen',
                addEmpModalSubtitle: 'Verschijnt direct in het weekrooster',
                empNameLabel: 'Voor- en achternaam *',
                empNamePlaceholder: 'Bijv.: Jan de Vries',
                empRoleLabel: 'Functie / Groep (optioneel)',
                empRolePlaceholder: 'Bijv.: Groep A, Groep B, Groep C...',
                empDefaultRole: 'Medewerker',
                addEmpSubmitBtn: 'Toevoegen aan rooster',
                shareModalTitle: 'Week & Roosterafbeelding Verzenden (.PNG) op PC',
                shareModalSubtitle: 'Week {week} ({range}) • Klaar om te plakken met Ctrl+V',
                shareError: 'Kon geen PNG-afbeelding van de tabel maken.',
                shareHelperDesktop: 'Op PC: Klik op „Kopieer Afbeelding (Ctrl+V)“, open WhatsApp Web of E-mail en druk op Ctrl+V.',
                downloadPngBtn: '⬇ Download PNG',
                copyImageBtn: '📋 Kopieer Afbeelding (Ctrl+V)',
                copyTextModalBtn: '📄 Kopieer Tekst',
                waTextBtn: 'WhatsApp Web',
                mailImageBtn: 'E-mailclient',
                closeBtn: 'Sluiten',
                canvasBannerTitle: 'WERKROOSTER • WEEK {week} ({range})',
                canvasBannerStats: 'Medewerkers: {count}   •   Totaal gewerkte dagen: {days} dagen',
                canvasLegendWork: 'Rooster (bijv. 07:00 / 08:00 / 10:00)',
                canvasLegendExtra: 'Extra',
                canvasLegendVrij: 'Vrij',
                canvasLegendVakantie: 'Vakantie',
                shareTextTitle: 'WERKROOSTER - Week {week} ({range})',
                toastFirstWeek2026: 'Eerste week van 2026 bereikt.',
                toastLastWeek2027: 'Laatste week van 2027 bereikt.',
                toastWeek47: 'Week 47 weergegeven (16 – 22 november 2026).',
                toastChangesSaved: 'Alle wijzigingen zijn opgeslagen op PC.',
                toastShiftSaved: 'Dagrooster bijgewerkt. Druk op Ctrl+S om te bevestigen.',
                toastExtraDayAdded: 'Extra dag toegevoegd voor {day}.',
                toastGroupReapplied: 'Groepsrooster opnieuw toegepast voor deze week.',
                toastAppliedMonFri: 'Rooster toegepast op maandag – vrijdag.',
                toastCellCleared: 'Cel gewist.',
                toastCellCopied: 'Cel gekopieerd (Ctrl+V om te plakken).',
                toastCellPasted: 'Gekopieerd rooster in cel geplakt.',
                toastEmpAdded: 'Medewerker {name} toegevoegd.',
                toastEmpRemoved: 'Medewerker uit de lijst verwijderd.',
                toastNoPrevWeek: 'Geen vorige week beschikbaar.',
                toastPrevWeekEmpty: 'Week {week} heeft geen opgeslagen diensten.',
                toastWeekCopied: 'Rooster van week {week} gekopieerd.',
                toastTextCopied: 'Weektekst gekopieerd naar klembord.',
                toastTextCopyFail: 'Automatisch kopiëren mislukt.',
                toastPngNotReady: 'PNG-afbeelding kon niet worden voorbereid.',
                toastPngDownloaded: 'Afbeelding {filename} gedownload.',
                toastPngOpenFail: 'Open de afbeelding in het voorbeeld om deze op te slaan.',
                toastNoPng: 'Geen PNG-afbeelding gegenereerd.',
                toastImgCopied: 'Roosterafbeelding gekopieerd! Druk op Ctrl+V in WhatsApp Web of E-mail.',
                toastImgCopyFallback: 'PNG gedownload om bij te voegen.',
                toastOpenedWaText: 'WhatsApp Web geopend. Plak de afbeelding met Ctrl+V.',
                toastOpenedMail: 'E-mailclient geopend.',
                toastFsActive: 'Desktop volledig scherm actief • Druk op ESC om te sluiten.',
                toastCsvExported: 'Excel (CSV)-bestand voor Week {week} gedownload.',
                toastBackupExported: 'JSON-back-up gedownload naar PC.',
                toastBackupRestored: 'Back-upgegevens succesvol hersteld!',
                toastBackupInvalid: 'Geselecteerd bestand is geen geldige SmartWork-back-up.'
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
            employees: [],
            schedules: {},
            manualOverrides: {},
            customData: {},
            hasPendingSave: false,
            editingCell: null,
            selectedCell: null,
            copiedCellSlot: null,
            contextTargetCell: null,
            isFullscreen: false,
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
                week: rawState.week
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

            return new Proxy(target, {
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
                    }
                } catch (err) {}
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

            const fsBtn = document.getElementById('fullscreen-desktop-btn');
            if (fsBtn) {
                const span = fsBtn.querySelector('span');
                if (span) span.textContent = t('fullscreenBtn');
                fsBtn.setAttribute('title', t('fullscreenTitle'));
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

            const ctxVrij = document.getElementById('ctx-vrij-label');
            if (ctxVrij) ctxVrij.textContent = `⚪ ${t('statusVrijLabel')}`;
            const ctxVak = document.getElementById('ctx-vakantie-label');
            if (ctxVak) ctxVak.textContent = `🔴 ${t('statusVakantieLabel')}`;

            const statsBar = document.querySelector('.stats-bar');
            if (statsBar) {
                const spans = statsBar.querySelectorAll('span');
                if (spans[0]) {
                    const countVal = document.getElementById('stat-emp-count')?.textContent || '0';
                    spans[0].innerHTML = `${t('statsEmployees')} <strong id="stat-emp-count">${countVal}</strong>`;
                }
                if (spans[2]) {
                    const daysVal = document.getElementById('stat-total-days')?.textContent || `0 ${t('dayPlural')}`;
                    spans[2].innerHTML = `${t('statsWorkedDays')} <strong id="stat-total-days">${daysVal}</strong>`;
                }
            }

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

                const helper = document.getElementById('share-image-helper-text');
                if (helper) helper.textContent = t('shareHelperDesktop');

                const dlBtn = document.getElementById('download-png-btn');
                if (dlBtn) dlBtn.textContent = t('downloadPngBtn');

                const cpBtn = document.getElementById('copy-png-btn');
                if (cpBtn) cpBtn.textContent = t('copyImageBtn');

                const cpTextBtn = document.getElementById('modal-copy-text-btn');
                if (cpTextBtn) cpTextBtn.textContent = t('copyTextModalBtn');

                const waTextBtn = document.getElementById('modal-wa-text-btn');
                if (waTextBtn) waTextBtn.textContent = t('waTextBtn');

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
           4. GROUP ROTATION SCHEDULE (2026 & 2027) & DEFAULT EMPLOYEES
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
                } catch (err) {}
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
           6. TABLE RENDERING & CELL SELECTION
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

        function setSelectedCell(empId, dayIndex) {
            state.selectedCell = { empId, dayIndex };
            document.querySelectorAll('.shift-slot.selected-cell').forEach(el => el.classList.remove('selected-cell'));
            const target = document.querySelector(`.shift-slot[data-emp-id="${CSS.escape(empId)}"][data-day-index="${dayIndex}"]`);
            if (target) {
                target.classList.add('selected-cell');
            }
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
                        <td colspan="9" style="padding:42px 16px; text-align:center; color:var(--text-muted);">
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
                        const isSelected = state.selectedCell && state.selectedCell.empId === emp.id && state.selectedCell.dayIndex === d;
                        const selCls = isSelected ? ' selected-cell' : '';

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
                                    <div tabindex="0" class="shift-slot ${typeClass}${selCls}" data-emp-id="${escapeHTML(emp.id)}" data-day-index="${d}" title="${escapeHTML(t('setCellTitle'))}">
                                        <span class="shift-title">${escapeHTML(displayLabel)}</span>
                                        ${subText ? `<span class="shift-sub">${escapeHTML(subText)}</span>` : ''}
                                    </div>
                                </td>
                            `;
                        } else {
                            cellsHTML += `
                                <td class="${tdClass}">
                                    <div tabindex="0" class="shift-slot shift-empty${selCls}" data-emp-id="${escapeHTML(emp.id)}" data-day-index="${d}" title="${escapeHTML(t('setCellTitle'))}">
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
           7. DESKTOP RIGHT-CLICK CONTEXT MENU & CELL CLIPBOARD
           ===================================================================== */
        function openCellContextMenu(x, y, empId, dayIndex) {
            const emp = state.employees.find(e => e.id === empId);
            if (!emp) return;

            setSelectedCell(empId, dayIndex);
            state.contextTargetCell = { empId, dayIndex };

            const menu = document.getElementById('cell-context-menu');
            const header = document.getElementById('ctx-menu-header');
            const pasteBtn = document.getElementById('ctx-paste-btn');

            header.textContent = `${emp.name} • ${getDayNames()[dayIndex]}`;
            pasteBtn.disabled = !state.copiedCellSlot;

            menu.classList.add('open');
            const rect = menu.getBoundingClientRect();
            const safeX = Math.min(x, window.innerWidth - rect.width - 12);
            const safeY = Math.min(y, window.innerHeight - rect.height - 12);
            menu.style.left = `${Math.max(8, safeX)}px`;
            menu.style.top = `${Math.max(8, safeY)}px`;
        }

        function closeCellContextMenu() {
            document.getElementById('cell-context-menu').classList.remove('open');
            state.contextTargetCell = null;
        }

        function applyQuickCellData(empId, dayIndex, slotObj) {
            const weekKey = getWeekKey(state.year, state.week);
            if (!state.schedules[weekKey]) state.schedules[weekKey] = {};
            if (!state.schedules[weekKey][empId]) state.schedules[weekKey][empId] = {};

            if (slotObj === null) {
                delete state.schedules[weekKey][empId][dayIndex];
            } else {
                state.schedules[weekKey][empId][dayIndex] = { ...slotObj };
            }

            markManualOverride(weekKey, empId, dayIndex);
            markPendingSave(true);
            saveAppState();
            renderScheduleTable();
        }

        function copySelectedCellSlot(targetCell = null) {
            const cell = targetCell || state.selectedCell;
            if (!cell) return;
            const weekKey = getWeekKey(state.year, state.week);
            const slot = state.schedules[weekKey]?.[cell.empId]?.[cell.dayIndex];
            state.copiedCellSlot = slot ? { ...slot } : { type: 'empty', label: '', note: '' };
            showToast(t('toastCellCopied'));
        }

        function pasteToSelectedCellSlot(targetCell = null) {
            const cell = targetCell || state.selectedCell;
            if (!cell || !state.copiedCellSlot) return;

            if (!state.copiedCellSlot.label) {
                applyQuickCellData(cell.empId, cell.dayIndex, null);
            } else {
                applyQuickCellData(cell.empId, cell.dayIndex, state.copiedCellSlot);
            }
            showToast(t('toastCellPasted'));
        }

        /* =====================================================================
           8. SHIFT MODAL, EXTRA DAY & EMPLOYEE MANAGEMENT
           ===================================================================== */
        function openShiftModal(empId, dayIndex) {
            const emp = state.employees.find(e => e.id === empId);
            if (!emp) return;

            setSelectedCell(empId, dayIndex);
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
            setTimeout(() => document.getElementById('custom-label').focus(), 40);
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
            applyQuickCellData(empId, dayIndex, getModalShiftObject());
            closeShiftModal();
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
            applyQuickCellData(empId, dayIndex, null);
            closeShiftModal();
            showToast(t('toastCellCleared'));
        }

        function openAddEmployeeModal() {
            document.getElementById('new-emp-name').value = '';
            document.getElementById('new-emp-role').value = '';
            document.getElementById('emp-modal').classList.add('open');
            setTimeout(() => document.getElementById('new-emp-name').focus(), 40);
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
           9. DESKTOP EXPORT / IMPORT (CSV EXCEL & JSON BACKUP)
           ===================================================================== */
        function exportWeekToCSV() {
            ensureWeekInitialized(state.year, state.week);
            const days = getDatesOfISOWeek(state.year, state.week);
            const weekKey = getWeekKey(state.year, state.week);
            const weekData = state.schedules[weekKey] || {};
            const dayNames = getDayNames();
            const weekNumStr = String(state.week).padStart(2, '0');

            const headers = [
                t('colEmployee'),
                'Grup / Functie',
                ...dayNames.map((dn, i) => `${dn} (${formatShortDate(days[i])})`),
                t('colDays')
            ];

            const rows = [headers];

            state.employees.forEach(emp => {
                const empSchedule = weekData[emp.id] || {};
                let workedCount = 0;
                const dayCells = [];

                for (let d = 0; d < 7; d++) {
                    const slot = empSchedule[d];
                    if (slot && slot.label) {
                        if (isWorkingDaySlot(slot)) workedCount += 1;
                        const lbl = getLocalizedSlotLabel(slot);
                        dayCells.push(slot.note ? `${lbl} (${slot.note})` : lbl);
                    } else {
                        dayCells.push('');
                    }
                }

                rows.push([
                    emp.name,
                    getLocalizedEmployeeRole(emp.role),
                    ...dayCells,
                    String(workedCount)
                ]);
            });

            const csvContent = '\uFEFF' + rows.map(row =>
                row.map(cell => `"${String(cell || '').replace(/"/g, '""')}"`).join(';')
            ).join('\r\n');

            const blob = new Blob([csvContent], { type: 'text/csv;charset=utf-8;' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = `SmartWork-${state.year}-Sapt${weekNumStr}.csv`;
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            setTimeout(() => URL.revokeObjectURL(url), 4000);
            showToast(t('toastCsvExported', { week: weekNumStr }));
        }

        function exportJSONBackup() {
            persistEverythingNow();
            const backupObj = {
                app: 'SmartWork Desktop',
                version: 6,
                exportedAt: new Date().toISOString(),
                employees: rawState.employees,
                schedules: rawState.schedules,
                manualOverrides: rawState.manualOverrides || {},
                customData: rawState.customData || {}
            };

            const blob = new Blob([JSON.stringify(backupObj, null, 2)], { type: 'application/json' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            const dateStamp = new Date().toISOString().slice(0, 10);
            a.href = url;
            a.download = `SmartWork-Backup-${dateStamp}.json`;
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            setTimeout(() => URL.revokeObjectURL(url), 4000);
            showToast(t('toastBackupExported'));
        }

        function importJSONBackup(file) {
            if (!file) return;
            const reader = new FileReader();
            reader.onload = (e) => {
                try {
                    const parsed = JSON.parse(String(e.target.result || ''));
                    if (!parsed || !Array.isArray(parsed.employees) || typeof parsed.schedules !== 'object') {
                        showToast(t('toastBackupInvalid'));
                        return;
                    }
                    state.employees = parsed.employees;
                    state.schedules = parsed.schedules;
                    state.manualOverrides = parsed.manualOverrides || {};
                    state.customData = parsed.customData || {};
                    persistEverythingNow();
                    markPendingSave(false);
                    renderScheduleTable();
                    showToast(t('toastBackupRestored'));
                } catch (err) {
                    showToast(t('toastBackupInvalid'));
                }
            };
            reader.readAsText(file);
        }

        /* =====================================================================
           10. DESKTOP PNG RENDERING, CLIPBOARD & WHATSAPP WEB / EMAIL SHARE
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

                const scale = 2;
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
                ctx.font = '800 20px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
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
                ctx.font = '600 13px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
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
                        ctx.font = '800 13px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
                        ctx.textAlign = 'left';
                        ctx.textBaseline = 'middle';
                        ctx.fillText(t('colEmployeeDetails'), x + 12, tableTop + headerHeight / 2);
                    } else if (c >= 1 && c <= 7) {
                        const dayIdx = c - 1;
                        const labelText = dayNames[dayIdx];
                        ctx.fillStyle = (c === 6 || c === 7) ? '#92400e' : '#0f172a';
                        ctx.font = '800 13px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
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
                        ctx.font = '600 11px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
                        ctx.fillText(formatShortDate(days[dayIdx]), x + w / 2, tableTop + 37);
                    } else {
                        ctx.fillStyle = '#0f172a';
                        ctx.font = '800 13px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
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
                    ctx.font = '600 14px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
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
                        ctx.font = '800 14px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
                        ctx.textAlign = 'left';
                        ctx.textBaseline = 'middle';
                        const nameY = displayRole ? y + 20 : y + rowHeight / 2;
                        ctx.fillText(emp.name, colX[0] + 12, nameY);

                        if (displayRole) {
                            ctx.fillStyle = '#4f46e5';
                            ctx.font = '700 11px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
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
                                ctx.font = '800 13px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
                                ctx.textAlign = 'center';
                                ctx.textBaseline = 'middle';
                                ctx.fillText(displayLabel, bx + bw / 2, hasNote ? by + bh / 2 - 7 : by + bh / 2);

                                if (hasNote) {
                                    ctx.fillStyle = colors.sub;
                                    ctx.font = '700 10px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
                                    ctx.fillText(slot.note, bx + bw / 2, by + bh / 2 + 8);
                                }
                            } else {
                                ctx.fillStyle = '#94a3b8';
                                ctx.font = '700 13px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
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
                        ctx.font = '800 12px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
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
                    ctx.font = '800 12px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
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
                ctx.font = '600 12px "Segoe UI", -apple-system, BlinkMacSystemFont, Roboto, Inter, sans-serif';
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

                const filename = `SmartWork-${state.year}-Sapt${weekNumStr}-${state.lang}.png`;
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

        async function openShareImageModal(autoChannel = null) {
            const rendered = renderScheduleToPNG();
            const container = document.getElementById('png-preview-container');
            const subtitle = document.getElementById('share-image-modal-subtitle');

            const days = getDatesOfISOWeek(state.year, state.week);
            const weekNumStr = String(state.week).padStart(2, '0');
            const rangeStr = `${formatShortDate(days[0])} – ${formatShortDate(days[6])} ${state.year}`;
            subtitle.textContent = t('shareModalSubtitle', { week: weekNumStr, range: rangeStr });

            if (!rendered || !rendered.dataUrl) {
                container.innerHTML = `<span style="font-size:0.82rem; color:#be123c; font-weight:700;">${escapeHTML(t('shareError'))}</span>`;
            } else {
                container.innerHTML = `<img src="${rendered.dataUrl}" alt="${escapeHTML(t('shareModalTitle'))}" class="png-preview-img">`;
            }

            document.getElementById('share-image-modal').classList.add('open');

            if (autoChannel === 'whatsapp') {
                await copyRenderedScheduleImage(true);
                openWhatsAppWebDesktop();
            } else if (autoChannel === 'email') {
                await copyRenderedScheduleImage(true);
                openEmailDesktopClient();
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

        async function copyRenderedScheduleImage(silent = false) {
            const rendered = (state.lastPngBlob)
                ? { blob: state.lastPngBlob }
                : renderScheduleToPNG();

            if (!rendered || !rendered.blob) {
                if (!silent) showToast(t('toastNoPng'));
                return false;
            }

            try {
                if (navigator.clipboard && typeof ClipboardItem !== 'undefined') {
                    const item = new ClipboardItem({ 'image/png': rendered.blob });
                    await navigator.clipboard.write([item]);
                    if (!silent) showToast(t('toastImgCopied'));
                    return true;
                }
            } catch (err) {}

            if (!silent) {
                downloadRenderedSchedulePNG();
                showToast(t('toastImgCopyFallback'));
            }
            return false;
        }

        function openWhatsAppWebDesktop() {
            const weekOnlyText = buildScheduleShareText();
            const waUrl = `https://web.whatsapp.com/send?text=${encodeURIComponent(weekOnlyText)}`;
            window.open(waUrl, '_blank', 'noopener,noreferrer');
            showToast(t('toastOpenedWaText'));
        }

        function openEmailDesktopClient() {
            const days = getDatesOfISOWeek(state.year, state.week);
            const weekNumStr = String(state.week).padStart(2, '0');
            const rangeStr = `${formatShortDate(days[0])} – ${formatShortDate(days[6])} ${state.year}`;
            const title = t('shareTextTitle', { week: weekNumStr, range: rangeStr });
            const mailtoUrl = `mailto:?subject=${encodeURIComponent(title)}&body=${encodeURIComponent(title)}`;
            window.location.href = mailtoUrl;
            showToast(t('toastOpenedMail'));
        }

        /* =====================================================================
           11. DESKTOP FULLSCREEN MODE (STANDARD WIDESCREEN, NO ROTATION)
           ===================================================================== */
        function toggleDesktopFullscreen() {
            if (state.isFullscreen) {
                exitDesktopFullscreen();
            } else {
                enterDesktopFullscreen();
            }
        }

        function enterDesktopFullscreen() {
            if (state.isFullscreen) return;
            state.isFullscreen = true;
            document.body.classList.add('desktop-fullscreen-active');
            document.getElementById('fullscreen-overlay-shell').classList.add('active');

            if (document.documentElement.requestFullscreen && !document.fullscreenElement) {
                document.documentElement.requestFullscreen().catch(() => {});
            }
            showToast(t('toastFsActive'));
        }

        function exitDesktopFullscreen() {
            if (!state.isFullscreen) return;
            state.isFullscreen = false;
            document.body.classList.remove('desktop-fullscreen-active');
            document.getElementById('fullscreen-overlay-shell').classList.remove('active');

            if (document.fullscreenElement && document.exitFullscreen) {
                document.exitFullscreen().catch(() => {});
            }
        }

        /* =====================================================================
           12. TOASTS, DESKTOP KEYBOARD SHORTCUTS & EVENT BINDING
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
            }, 2800);
        }

        function isAnyModalOpen() {
            return document.getElementById('shift-modal').classList.contains('open') ||
                   document.getElementById('emp-modal').classList.contains('open') ||
                   document.getElementById('share-image-modal').classList.contains('open');
        }

        function bindEvents() {
            document.getElementById('brand-trigger-btn').addEventListener('click', toggleDesktopFullscreen);
            document.getElementById('prev-week-btn').addEventListener('click', () => changeWeek(-1));
            document.getElementById('next-week-btn').addEventListener('click', () => changeWeek(1));
            document.getElementById('year-select').addEventListener('change', onYearChange);
            document.getElementById('week-select').addEventListener('change', onWeekChange);
            document.getElementById('week-47-btn').addEventListener('click', goToWeek47);
            document.getElementById('lang-select').addEventListener('change', (e) => onLanguageChange(e.target.value));

            document.getElementById('save-changes-btn').addEventListener('click', commitChangesExplicitly);
            document.getElementById('add-emp-btn').addEventListener('click', openAddEmployeeModal);
            document.getElementById('copy-prev-week-btn').addEventListener('click', copyPreviousWeek);
            document.getElementById('fullscreen-desktop-btn').addEventListener('click', toggleDesktopFullscreen);
            document.getElementById('print-btn').addEventListener('click', () => window.print());

            document.getElementById('export-csv-btn').addEventListener('click', exportWeekToCSV);
            document.getElementById('backup-export-btn').addEventListener('click', exportJSONBackup);
            document.getElementById('backup-import-btn').addEventListener('click', () => {
                document.getElementById('backup-file-input').click();
            });
            document.getElementById('backup-file-input').addEventListener('change', (e) => {
                const file = e.target.files && e.target.files[0];
                if (file) {
                    importJSONBackup(file);
                    e.target.value = '';
                }
            });

            document.getElementById('share-wa-btn').addEventListener('click', () => openShareImageModal('whatsapp'));
            document.getElementById('share-email-btn').addEventListener('click', () => openShareImageModal('email'));
            document.getElementById('copy-text-btn').addEventListener('click', () => copyScheduleTextToClipboard(false));

            document.getElementById('fs-save-btn').addEventListener('click', commitChangesExplicitly);
            document.getElementById('fs-wa-btn').addEventListener('click', () => openShareImageModal('whatsapp'));
            document.getElementById('fs-mail-btn').addEventListener('click', () => openShareImageModal('email'));
            document.getElementById('fs-prev-btn').addEventListener('click', () => changeWeek(-1));
            document.getElementById('fs-next-btn').addEventListener('click', () => changeWeek(1));
            document.getElementById('fs-exit-btn').addEventListener('click', exitDesktopFullscreen);

            // Table Left-Click (Edit / Select) & Right-Click (Quick Context Menu)
            const tbody = document.getElementById('table-body');
            tbody.addEventListener('click', (e) => {
                closeCellContextMenu();
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

            tbody.addEventListener('contextmenu', (e) => {
                const slotEl = e.target.closest('.shift-slot[data-emp-id]');
                if (!slotEl) return;
                e.preventDefault();
                const empId = slotEl.getAttribute('data-emp-id');
                const dayIndex = parseInt(slotEl.getAttribute('data-day-index'), 10);
                if (empId && !Number.isNaN(dayIndex)) {
                    openCellContextMenu(e.clientX, e.clientY, empId, dayIndex);
                }
            });

            // Context Menu Item Actions
            document.getElementById('cell-context-menu').addEventListener('click', (e) => {
                const btn = e.target.closest('.ctx-item');
                if (!btn || btn.disabled || !state.contextTargetCell) return;

                const { empId, dayIndex } = state.contextTargetCell;
                const action = btn.getAttribute('data-ctx-action');

                if (action === 'set') {
                    const type = btn.getAttribute('data-type') || 'work';
                    let label = btn.getAttribute('data-label') || '07:00';
                    const note = btn.getAttribute('data-note') || '';
                    if (label === '__VRIJ__') label = t('statusVrijLabel');
                    if (label === '__VAKANTIE__') label = t('statusVakantieLabel');
                    applyQuickCellData(empId, dayIndex, { type, label, note });
                    showToast(t('toastShiftSaved'));
                } else if (action === 'copy') {
                    copySelectedCellSlot({ empId, dayIndex });
                } else if (action === 'paste') {
                    pasteToSelectedCellSlot({ empId, dayIndex });
                } else if (action === 'edit') {
                    openShiftModal(empId, dayIndex);
                } else if (action === 'clear') {
                    applyQuickCellData(empId, dayIndex, null);
                    showToast(t('toastCellCleared'));
                }

                closeCellContextMenu();
            });

            document.addEventListener('click', (e) => {
                if (!e.target.closest('#cell-context-menu')) {
                    closeCellContextMenu();
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
            document.getElementById('copy-png-btn').addEventListener('click', () => copyRenderedScheduleImage(false));
            document.getElementById('modal-copy-text-btn').addEventListener('click', () => copyScheduleTextToClipboard(false));
            document.getElementById('modal-wa-text-btn').addEventListener('click', openWhatsAppWebDesktop);
            document.getElementById('modal-mail-image-btn').addEventListener('click', openEmailDesktopClient);

            // Desktop Global Keyboard Shortcuts
            document.addEventListener('keydown', (e) => {
                const activeTag = document.activeElement ? document.activeElement.tagName.toUpperCase() : '';
                const isTypingInInput = (activeTag === 'INPUT' || activeTag === 'TEXTAREA' || activeTag === 'SELECT');

                // Ctrl+S / Cmd+S -> Save Changes
                if ((e.ctrlKey || e.metaKey) && e.key.toLowerCase() === 's') {
                    e.preventDefault();
                    commitChangesExplicitly();
                    return;
                }

                // Escape -> Close context menu, modals, or exit fullscreen
                if (e.key === 'Escape') {
                    if (document.getElementById('cell-context-menu').classList.contains('open')) {
                        closeCellContextMenu();
                        return;
                    }
                    if (document.getElementById('shift-modal').classList.contains('open')) {
                        closeShiftModal();
                        return;
                    }
                    if (document.getElementById('emp-modal').classList.contains('open')) {
                        closeAddEmployeeModal();
                        return;
                    }
                    if (document.getElementById('share-image-modal').classList.contains('open')) {
                        closeShareImageModal();
                        return;
                    }
                    if (state.isFullscreen) {
                        exitDesktopFullscreen();
                    }
                    return;
                }

                // Enter inside Shift Modal -> Save Shift
                if (e.key === 'Enter' && document.getElementById('shift-modal').classList.contains('open')) {
                    e.preventDefault();
                    saveShiftModal();
                    return;
                }

                if (isAnyModalOpen() || isTypingInInput) return;

                // Alt + Left / Right -> Previous / Next Week
                if (e.altKey && e.key === 'ArrowLeft') {
                    e.preventDefault();
                    changeWeek(-1);
                    return;
                }
                if (e.altKey && e.key === 'ArrowRight') {
                    e.preventDefault();
                    changeWeek(1);
                    return;
                }

                // Cell keyboard shortcuts when a cell is selected
                if (state.selectedCell) {
                    if ((e.ctrlKey || e.metaKey) && e.key.toLowerCase() === 'c') {
                        e.preventDefault();
                        copySelectedCellSlot();
                        return;
                    }
                    if ((e.ctrlKey || e.metaKey) && e.key.toLowerCase() === 'v') {
                        e.preventDefault();
                        pasteToSelectedCellSlot();
                        return;
                    }
                    if (e.key === 'Delete' || e.key === 'Backspace') {
                        e.preventDefault();
                        applyQuickCellData(state.selectedCell.empId, state.selectedCell.dayIndex, null);
                        showToast(t('toastCellCleared'));
                        return;
                    }
                    if (e.key === 'Enter') {
                        e.preventDefault();
                        openShiftModal(state.selectedCell.empId, state.selectedCell.dayIndex);
                    }
                }
            });

            document.addEventListener('fullscreenchange', () => {
                if (!document.fullscreenElement && state.isFullscreen) {
                    state.isFullscreen = false;
                    document.body.classList.remove('desktop-fullscreen-active');
                    document.getElementById('fullscreen-overlay-shell').classList.remove('active');
                }
            });

            window.addEventListener('pagehide', persistEverythingNow);
            window.addEventListener('beforeunload', persistEverythingNow);
            document.addEventListener('visibilitychange', () => {
                if (document.visibilityState === 'hidden') {
                    persistEverythingNow();
                } else {
                    renderScheduleTable();
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
```
