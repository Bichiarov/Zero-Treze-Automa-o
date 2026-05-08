<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Zero13 Automação Comercial - PDV, suporte técnico, equipamentos, redes e soluções para comércio." />
  <title>Zero13 Automação Comercial</title>
  <!-- Versão responsiva atualizada - layout full screen -->

  <style>
    :root {
      --preto: #111111;
      --preto-profundo: #050505;
      --azul: #008ee8;
      --azul-claro: #18a8ff;
      --prata: #d7dde5;
      --prata-escuro: #8d99a8;
      --branco: #ffffff;
      --cinza: #b6beca;
      --borda: rgba(215, 221, 229, 0.16);
      --card: rgba(255, 255, 255, 0.045);
      --whatsapp: #25d366;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      color: var(--branco);
      background: var(--preto);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      max-width: 100%;
      display: block;
    }

    .container {
      width: min(1180px, calc(100% - 40px));
      margin: 0 auto;
    }

    .topbar {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(17, 17, 17, 0.92);
      border-bottom: 1px solid var(--borda);
      backdrop-filter: blur(14px);
    }

    .navbar {
      min-height: 82px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 28px;
    }

    .logo-nav {
      width: 220px;
      height: auto;
      filter: drop-shadow(0 0 12px rgba(0, 142, 232, 0.22));
    }

    .menu {
      display: flex;
      align-items: center;
      gap: 24px;
      color: var(--cinza);
      font-size: 0.95rem;
    }

    .menu a {
      transition: color 0.2s ease;
    }

    .menu a:hover {
      color: var(--branco);
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      border-radius: 12px;
      padding: 13px 18px;
      border: 1px solid transparent;
      font-weight: 800;
      transition: 0.2s ease;
      cursor: pointer;
      white-space: nowrap;
    }

    .btn-primary {
      background: var(--azul);
      color: #00111f;
      box-shadow: 0 12px 28px rgba(0, 142, 232, 0.25);
    }

    .btn-primary:hover {
      background: var(--azul-claro);
      transform: translateY(-2px);
    }

    .btn-outline {
      border-color: var(--borda);
      color: var(--prata);
      background: rgba(255, 255, 255, 0.04);
    }

    .btn-outline:hover {
      border-color: rgba(0, 142, 232, 0.55);
      background: rgba(0, 142, 232, 0.1);
    }

    .btn-whatsapp {
      background: var(--whatsapp);
      color: #04140a;
    }

    .whatsapp-float {
      position: fixed;
      right: 22px;
      bottom: 22px;
      z-index: 300;
      display: inline-flex;
      align-items: center;
      gap: 12px;
      color: #04140a;
      font-weight: 900;
      filter: drop-shadow(0 16px 24px rgba(0, 0, 0, 0.38));
    }

    .whatsapp-label {
      background: var(--branco);
      color: #111111;
      border-radius: 999px;
      padding: 11px 15px;
      border: 1px solid rgba(0, 0, 0, 0.08);
    }

    .whatsapp-icon {
      width: 58px;
      height: 58px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      background: var(--whatsapp);
      color: #04140a;
      font-size: 1.75rem;
      border: 3px solid rgba(255, 255, 255, 0.85);
      animation: pulseWhatsApp 1.8s ease-in-out infinite;
    }

    @keyframes pulseWhatsApp {
      0%, 100% { transform: scale(1); box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.44); }
      50% { transform: scale(1.06); box-shadow: 0 0 0 12px rgba(37, 211, 102, 0); }
    }

    .top-video-hero {
      position: relative;
      width: 100%;
      padding: 0;
      background: #000000;
      overflow: hidden;
      border-bottom: 1px solid var(--borda);
      box-shadow: 0 18px 52px rgba(0, 0, 0, 0.44);
    }

    .top-video-hero::after {
      content: "";
      position: absolute;
      inset: 0;
      pointer-events: none;
      background:
        radial-gradient(circle at 50% 100%, rgba(0, 142, 232, 0.10), transparent 55%);
    }

    .top-video {
      position: relative;
      z-index: 1;
      display: block;
      width: min(1400px, 100%);
      height: 220px;
      margin: 0 auto;
      object-fit: contain;
      object-position: center center;
      background: #000000;
      border: none;
      border-radius: 0;
      box-shadow: none;
    }

    .hero {
      position: relative;
      min-height: auto;
      display: grid;
      grid-template-columns: 1fr;
      align-items: center;
      gap: 54px;
      padding: 82px 0;
      overflow: hidden;
    }

    .hero::before {
      content: "";
      position: absolute;
      inset: 0;
      background:
        radial-gradient(circle at 15% 18%, rgba(0, 142, 232, 0.20), transparent 30%),
        radial-gradient(circle at 78% 35%, rgba(215, 221, 229, 0.10), transparent 30%);
      pointer-events: none;
    }

    .hero > * {
      position: relative;
      z-index: 2;
    }

    .tag {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      color: var(--prata);
      background: rgba(0, 142, 232, 0.10);
      border: 1px solid rgba(0, 142, 232, 0.35);
      padding: 8px 12px;
      border-radius: 999px;
      font-size: 0.92rem;
      margin-bottom: 22px;
    }

    .tag::before {
      content: "";
      width: 9px;
      height: 9px;
      border-radius: 50%;
      background: var(--azul-claro);
      box-shadow: 0 0 12px var(--azul-claro);
    }

    h1 {
      font-size: clamp(2.5rem, 5.6vw, 5.5rem);
      line-height: 0.96;
      letter-spacing: -0.07em;
      margin-bottom: 24px;
    }

    .hero p {
      color: var(--cinza);
      font-size: 1.16rem;
      max-width: 640px;
      margin-bottom: 30px;
    }

    .hero-actions {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
      margin-bottom: 34px;
    }

    .hero-points {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
      max-width: 680px;
    }

    .point {
      border: 1px solid var(--borda);
      background: var(--card);
      border-radius: 18px;
      padding: 15px;
    }

    .point strong {
      display: block;
      color: var(--branco);
      font-size: 1rem;
      margin-bottom: 4px;
    }

    .point span {
      color: var(--prata-escuro);
      font-size: 0.9rem;
    }

    .live-panel {
      max-width: 980px;
      width: 100%;
      margin-top: 18px;
      border: 1px solid rgba(0, 142, 232, 0.28);
      background:
        linear-gradient(135deg, rgba(0, 142, 232, 0.12), rgba(255, 255, 255, 0.035)),
        rgba(255, 255, 255, 0.035);
      border-radius: 22px;
      padding: 18px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
      align-items: center;
    }

    .live-date {
      color: var(--prata);
      font-size: 0.98rem;
      margin-bottom: 4px;
      text-transform: capitalize;
    }

    .live-time {
      font-size: clamp(2rem, 4vw, 3.2rem);
      line-height: 1;
      letter-spacing: -0.05em;
      font-weight: 900;
      color: var(--branco);
    }

    .live-weather {
      border-left: 1px solid var(--borda);
      padding-left: 16px;
    }

    .live-weather strong {
      display: block;
      font-size: 1.45rem;
      color: var(--azul-claro);
      margin-bottom: 3px;
    }

    .live-weather span {
      display: block;
      color: var(--cinza);
      font-size: 0.92rem;
    }

    .live-economy {
      border-left: 1px solid var(--borda);
      padding-left: 16px;
    }

    .live-economy .live-economy-label {
      display: block;
      color: var(--prata);
      font-size: 0.88rem;
      font-weight: 800;
      margin-bottom: 4px;
    }

    .live-economy strong {
      display: block;
      color: var(--azul-claro);
      font-size: clamp(1.85rem, 3vw, 2.85rem);
      line-height: 1.05;
      letter-spacing: -0.04em;
      white-space: nowrap;
      text-shadow: 0 0 18px rgba(0, 142, 232, 0.25);
    }

    .live-economy span {
      display: block;
      color: var(--cinza);
      font-size: 0.92rem;
      margin-top: 5px;
    }

    .live-status {
      margin-top: 8px;
      color: var(--prata-escuro);
      font-size: 0.82rem;
    }

    .logo-panel {
      border: 1px solid var(--borda);
      background:
        linear-gradient(145deg, rgba(255, 255, 255, 0.07), rgba(255, 255, 255, 0.015)),
        var(--preto-profundo);
      border-radius: 28px;
      min-height: 360px;
      display: grid;
      place-items: center;
      padding: 42px;
      box-shadow: 0 24px 80px rgba(0, 0, 0, 0.42);
      overflow: hidden;
    }

    .logo-hero {
      width: min(100%, 680px);
      filter:
        drop-shadow(0 22px 26px rgba(0, 0, 0, 0.65))
        drop-shadow(0 0 24px rgba(0, 142, 232, 0.22));
    }

    .logo-hero-video {
      width: min(100%, 680px);
      display: block;
      margin: 0 auto;
      border-radius: 18px;
      object-fit: contain;
      background: transparent;
      filter:
        drop-shadow(0 22px 26px rgba(0, 0, 0, 0.65))
        drop-shadow(0 0 24px rgba(0, 142, 232, 0.22));
    }

    section {
      padding: 82px 0;
    }

    .section-title {
      max-width: 820px;
      margin-bottom: 34px;
    }

    .section-title span {
      display: block;
      color: var(--azul-claro);
      font-size: 0.82rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      font-weight: 900;
      margin-bottom: 10px;
    }

    .section-title h2 {
      font-size: clamp(2rem, 4vw, 3.1rem);
      line-height: 1.06;
      letter-spacing: -0.055em;
      margin-bottom: 12px;
    }

    .section-title p {
      color: var(--cinza);
      font-size: 1.05rem;
    }

    .grid-3 {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .grid-4 {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 16px;
    }

    .card {
      min-height: 230px;
      border: 1px solid var(--borda);
      background: var(--card);
      border-radius: 24px;
      padding: 24px;
      transition: 0.22s ease;
    }

    .card:hover {
      transform: translateY(-4px);
      border-color: rgba(0, 142, 232, 0.48);
      background: rgba(0, 142, 232, 0.075);
    }

    .icon {
      width: 50px;
      height: 50px;
      border-radius: 15px;
      display: grid;
      place-items: center;
      background: rgba(0, 142, 232, 0.13);
      border: 1px solid rgba(0, 142, 232, 0.22);
      font-size: 1.45rem;
      margin-bottom: 18px;
    }

    .card h3 {
      font-size: 1.24rem;
      margin-bottom: 9px;
    }

    .card p {
      color: var(--cinza);
    }

    .segment-card {
      min-height: 0;
      padding: 0;
      overflow: hidden;
      display: flex;
      flex-direction: column;
    }

    .segment-image-wrap {
      position: relative;
      aspect-ratio: 4 / 3;
      overflow: hidden;
      background: #0a0a0a;
      border-bottom: 1px solid rgba(255, 255, 255, 0.06);
    }

    .segment-image {
      width: 100%;
      height: 100%;
      display: block;
      object-fit: cover;
      transition: transform 0.35s ease;
    }

    .segment-card:hover .segment-image {
      transform: scale(1.03);
    }

    .segment-body {
      padding: 20px 22px 24px;
    }

    .segment-body h3 {
      font-size: 1.2rem;
      margin-bottom: 9px;
      color: var(--branco);
    }

    .segment-body p {
      color: var(--cinza);
    }


    .equipment-gallery {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .equipment-card {
      border: 1px solid var(--borda);
      background: var(--card);
      border-radius: 26px;
      overflow: hidden;
      transition: 0.22s ease;
      box-shadow: 0 18px 55px rgba(0, 0, 0, 0.28);
    }

    .equipment-card:hover {
      transform: translateY(-5px);
      border-color: rgba(0, 142, 232, 0.52);
      background: rgba(0, 142, 232, 0.075);
    }

    .equipment-image {
      width: 100%;
      aspect-ratio: 4 / 5;
      object-fit: cover;
      background: var(--preto-profundo);
      border-bottom: 1px solid var(--borda);
    }

    .equipment-content {
      padding: 20px;
    }

    .equipment-content h3 {
      font-size: 1.18rem;
      line-height: 1.15;
      margin-bottom: 8px;
      color: var(--branco);
    }

    .equipment-content p {
      color: var(--cinza);
      font-size: 0.95rem;
    }

    .feature-box {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
    }

    .feature-column {
      border: 1px solid var(--borda);
      background: var(--card);
      border-radius: 26px;
      padding: 28px;
    }

    .feature-column h3 {
      font-size: 1.45rem;
      margin-bottom: 16px;
    }

    .feature-list {
      list-style: none;
      display: grid;
      gap: 12px;
    }

    .feature-list li {
      position: relative;
      color: var(--prata);
      padding-left: 28px;
    }

    .feature-list li::before {
      content: "✓";
      position: absolute;
      left: 0;
      color: var(--azul-claro);
      font-weight: 900;
    }

    .split {
      display: grid;
      grid-template-columns: 0.9fr 1.1fr;
      gap: 40px;
      align-items: start;
    }

    .steps {
      display: grid;
      gap: 14px;
    }

    .step {
      display: grid;
      grid-template-columns: 48px 1fr;
      gap: 14px;
      padding: 18px;
      border: 1px solid var(--borda);
      background: var(--card);
      border-radius: 20px;
    }

    .step-number {
      width: 44px;
      height: 44px;
      border-radius: 14px;
      display: grid;
      place-items: center;
      color: #00111f;
      background: linear-gradient(135deg, var(--azul), var(--prata));
      font-weight: 950;
    }

    .step p {
      color: var(--cinza);
    }

    .security {
      border: 1px solid rgba(0, 142, 232, 0.28);
      background:
        linear-gradient(135deg, rgba(0, 142, 232, 0.12), rgba(255, 255, 255, 0.035)),
        var(--preto-profundo);
      border-radius: 28px;
      padding: 34px;
    }

    .security h3 {
      font-size: 1.85rem;
      line-height: 1.1;
      margin-bottom: 12px;
      letter-spacing: -0.04em;
    }

    .security p {
      color: var(--cinza);
      margin-bottom: 20px;
    }

    .security ul {
      list-style: none;
      display: grid;
      gap: 10px;
    }

    .security li {
      border: 1px solid var(--borda);
      background: rgba(255, 255, 255, 0.035);
      border-radius: 14px;
      padding: 12px 14px;
      color: var(--prata);
    }

    .cta {
      border: 1px solid var(--borda);
      background:
        radial-gradient(circle at 0% 0%, rgba(0, 142, 232, 0.24), transparent 32%),
        var(--preto-profundo);
      border-radius: 30px;
      padding: 44px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 30px;
    }

    .cta h2 {
      font-size: clamp(1.8rem, 3.4vw, 2.85rem);
      line-height: 1.08;
      letter-spacing: -0.05em;
      margin-bottom: 10px;
    }

    .cta p {
      color: var(--cinza);
      max-width: 730px;
    }

    footer {
      border-top: 1px solid var(--borda);
      padding: 30px 0;
      color: var(--prata-escuro);
    }

    .footer-content {
      display: flex;
      justify-content: space-between;
      gap: 18px;
      flex-wrap: wrap;
    }

    @media (max-width: 980px) {
      .hero,
      .split,
  
    .equipment-gallery {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .equipment-card {
      border: 1px solid var(--borda);
      background: var(--card);
      border-radius: 26px;
      overflow: hidden;
      transition: 0.22s ease;
      box-shadow: 0 18px 55px rgba(0, 0, 0, 0.28);
    }

    .equipment-card:hover {
      transform: translateY(-5px);
      border-color: rgba(0, 142, 232, 0.52);
      background: rgba(0, 142, 232, 0.075);
    }

    .equipment-image {
      width: 100%;
      aspect-ratio: 4 / 5;
      object-fit: cover;
      background: var(--preto-profundo);
      border-bottom: 1px solid var(--borda);
    }

    .equipment-content {
      padding: 20px;
    }

    .equipment-content h3 {
      font-size: 1.18rem;
      line-height: 1.15;
      margin-bottom: 8px;
      color: var(--branco);
    }

    .equipment-content p {
      color: var(--cinza);
      font-size: 0.95rem;
    }

    .feature-box {
        grid-template-columns: 1fr;
      }

      .menu {
        display: none;
      }

      .grid-3,
      .grid-4,
      .equipment-gallery {
        grid-template-columns: 1fr 1fr;
      }

      .cta {
        flex-direction: column;
        align-items: flex-start;
      }
    }

    @media (max-width: 980px) {
      .top-video {
        height: 170px;
      }
    }

    @media (max-width: 640px) {
      .container {
        width: min(100% - 28px, 1180px);
      }

      .navbar {
        min-height: auto;
        padding: 16px 0;
        align-items: flex-start;
        flex-direction: column;
      }

      .logo-nav {
        width: 190px;
      }

      .hero {
        padding: 56px 0;
      }

      .top-video {
        width: 100%;
        height: 120px;
        border-radius: 0;
      }

      .hero-actions,
      .hero-points,
      .grid-3,
      .grid-4,
      .equipment-gallery {
        display: grid;
        grid-template-columns: 1fr;
      }

      .btn {
        width: 100%;
      }

      .logo-panel {
        min-height: 260px;
        padding: 24px;
      }

      .live-panel {
        grid-template-columns: 1fr;
      }

      .live-economy {
        border-left: none;
        border-top: 1px solid var(--borda);
        padding-left: 0;
        padding-top: 14px;
      }

      .live-economy strong {
        white-space: normal;
      }

      .cta {
        padding: 28px;
      }

      .whatsapp-float {
        right: 14px;
        bottom: 14px;
      }

      .whatsapp-label {
        display: none;
      }

      .whatsapp-icon {
        width: 56px;
        height: 56px;
      }
    }


    /* ===== AJUSTES RESPONSIVOS ZERO13 ===== */
    html,
    body {
      max-width: 100%;
      overflow-x: hidden;
    }

    .container {
      width: min(1180px, calc(100% - clamp(28px, 5vw, 48px)));
    }

    .logo-nav {
      max-width: min(220px, 68vw);
    }

    h1 {
      font-size: clamp(2.15rem, 8vw, 5.5rem);
    }

    section {
      padding: clamp(54px, 7vw, 82px) 0;
    }

    .hero {
      padding: clamp(48px, 7vw, 82px) 0;
    }

    .hero-actions,
    .hero-points,
    .grid-3,
    .grid-4,
    .equipment-gallery,
    .feature-box,
    .split {
      width: 100%;
    }

    .grid-3 {
      grid-template-columns: repeat(auto-fit, minmax(min(100%, 270px), 1fr));
    }

    .grid-4,
    .equipment-gallery {
      grid-template-columns: repeat(auto-fit, minmax(min(100%, 245px), 1fr));
    }

    .feature-box,
    .split {
      grid-template-columns: repeat(auto-fit, minmax(min(100%, 360px), 1fr));
    }

    .hero-points {
      grid-template-columns: repeat(auto-fit, minmax(min(100%, 190px), 1fr));
    }

    .live-panel {
      grid-template-columns: repeat(auto-fit, minmax(min(100%, 240px), 1fr));
    }

    .card,
    .equipment-card,
    .segment-card {
      height: 100%;
    }

    .segment-image-wrap {
      aspect-ratio: 16 / 10;
    }

    .equipment-image {
      aspect-ratio: 4 / 3;
    }

    @media (max-width: 1024px) {
      .navbar {
        min-height: auto;
        padding: 16px 0;
        flex-wrap: wrap;
        align-items: center;
      }

      .menu {
        display: flex;
        order: 3;
        width: 100%;
        gap: 14px;
        overflow-x: auto;
        padding: 8px 0 2px;
        scrollbar-width: thin;
      }

      .menu a {
        flex: 0 0 auto;
        padding: 8px 10px;
        border: 1px solid var(--borda);
        border-radius: 999px;
        background: rgba(255, 255, 255, 0.035);
      }

      .navbar > .btn {
        margin-left: auto;
      }

      .cta {
        flex-direction: column;
        align-items: flex-start;
      }
    }

    @media (max-width: 720px) {
      .container {
        width: min(100% - 28px, 1180px);
      }

      .topbar {
        position: sticky;
        top: 0;
      }

      .navbar {
        align-items: stretch;
        gap: 14px;
      }

      .navbar > a:first-child {
        display: flex;
        justify-content: center;
      }

      .logo-nav {
        width: min(210px, 72vw);
        margin: 0 auto;
      }

      .navbar > .btn {
        width: 100%;
        margin-left: 0;
      }

      .menu {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 8px;
        overflow: visible;
      }

      .menu a {
        text-align: center;
        font-size: 0.88rem;
        padding: 9px 8px;
      }

      .hero-actions {
        display: grid;
        grid-template-columns: 1fr;
      }

      .hero-actions .btn,
      .cta .btn {
        width: 100%;
      }

      .live-panel {
        grid-template-columns: 1fr;
      }

      .live-economy {
        border-left: none;
        border-top: 1px solid var(--borda);
        padding-left: 0;
        padding-top: 14px;
      }

      .live-economy strong {
        white-space: normal;
      }

      .section-title h2 {
        font-size: clamp(1.85rem, 8vw, 2.65rem);
      }

      .card,
      .feature-column,
      .security,
      .cta {
        border-radius: 22px;
      }

      .footer-content {
        flex-direction: column;
        text-align: center;
        align-items: center;
      }
    }

    @media (max-width: 460px) {
      .container {
        width: min(100% - 22px, 1180px);
      }

      .menu {
        grid-template-columns: 1fr;
      }

      .tag {
        font-size: 0.92rem;
        align-items: flex-start;
      }

      .hero p,
      .section-title p {
        font-size: 1rem;
      }

      .live-time {
        font-size: clamp(2rem, 13vw, 2.8rem);
      }

      .card,
      .feature-column,
      .security,
      .cta,
      .equipment-content,
      .segment-body {
        padding: 20px;
      }

      .step {
        grid-template-columns: 1fr;
      }

      .step-number {
        width: 42px;
        height: 42px;
      }

      .whatsapp-float {
        right: 14px;
        bottom: 14px;
      }

      .whatsapp-label {
        display: none;
      }

      .whatsapp-icon {
        width: 56px;
        height: 56px;
      }
    }


    /* Ajuste para ocupar melhor telas grandes */
    @media (min-width: 981px) {
      .container {
        width: min(1560px, calc(100% - 96px));
      }

      .navbar {
        width: min(1560px, calc(100% - 96px));
      }

      .hero.container {
        width: 100%;
        max-width: none;
        margin: 0;
        min-height: calc(100vh - 82px);
        padding-left: clamp(56px, 8vw, 176px);
        padding-right: clamp(56px, 8vw, 176px);
      }

      .hero > div {
        width: min(980px, 100%);
      }

      .hero p {
        max-width: 760px;
      }

      .hero-points,
      .live-panel {
        max-width: 900px;
      }

      .section-title {
        max-width: 980px;
      }

      .equipment-gallery,
      .grid-4 {
        gap: 24px;
      }
    }

    @media (min-width: 1500px) {
      .hero.container {
        padding-left: max(96px, calc((100vw - 1560px) / 2));
        padding-right: max(96px, calc((100vw - 1560px) / 2));
      }
    }


    /* ===== MOBILE PREMIUM: mantém a identidade visual do desktop no smartphone ===== */
    @media (max-width: 820px) {
      body {
        background:
          radial-gradient(circle at 8% 0%, rgba(0, 142, 232, 0.18), transparent 34%),
          radial-gradient(circle at 92% 20%, rgba(215, 221, 229, 0.08), transparent 28%),
          var(--preto);
      }

      .container {
        width: min(100% - 24px, 1180px);
      }

      .topbar {
        background: rgba(8, 8, 8, 0.94);
        border-bottom: 1px solid rgba(0, 142, 232, 0.20);
      }

      .navbar {
        display: grid;
        grid-template-columns: 1fr;
        gap: 12px;
        min-height: auto;
        padding: 14px 0 16px;
      }

      .navbar > a:first-child {
        justify-self: center;
      }

      .logo-nav {
        width: min(245px, 74vw);
        margin: 0 auto;
      }

      .menu {
        order: 2;
        display: flex;
        width: 100%;
        gap: 8px;
        overflow-x: auto;
        padding: 4px 0 2px;
        scrollbar-width: none;
        -webkit-overflow-scrolling: touch;
      }

      .menu::-webkit-scrollbar {
        display: none;
      }

      .menu a {
        flex: 0 0 auto;
        text-align: center;
        font-size: 0.86rem;
        padding: 9px 12px;
        border: 1px solid rgba(0, 142, 232, 0.24);
        border-radius: 999px;
        background: rgba(0, 142, 232, 0.07);
        color: var(--prata);
      }

      .navbar > .btn {
        order: 3;
        width: 100%;
        min-height: 48px;
        border-radius: 14px;
      }

      .hero.container {
        width: 100%;
        max-width: none;
        margin: 0;
        padding: 46px 14px 54px;
        min-height: auto;
      }

      .hero::before {
        background:
          radial-gradient(circle at 0% 0%, rgba(0, 142, 232, 0.23), transparent 34%),
          radial-gradient(circle at 100% 18%, rgba(215, 221, 229, 0.09), transparent 30%);
      }

      .hero > div {
        width: 100%;
        max-width: 680px;
        margin: 0 auto;
      }

      .tag {
        max-width: 100%;
        font-size: 0.92rem;
        line-height: 1.35;
        padding: 8px 11px;
        margin-bottom: 20px;
      }

      h1 {
        font-size: clamp(2.35rem, 11vw, 4.25rem);
        line-height: 0.96;
        letter-spacing: -0.072em;
        margin-bottom: 20px;
      }

      .hero p {
        max-width: 100%;
        font-size: 1.03rem;
        line-height: 1.65;
        margin-bottom: 24px;
        color: #d4dce8;
      }

      .hero-actions {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 10px;
        margin-bottom: 22px;
      }

      .hero-actions .btn {
        width: 100%;
        min-height: 50px;
        padding: 12px 13px;
        border-radius: 14px;
        font-size: 0.94rem;
      }

      .hero-points {
        display: grid;
        grid-template-columns: 1fr;
        gap: 10px;
        max-width: none;
      }

      .point {
        border-radius: 18px;
        padding: 16px;
        background: rgba(255, 255, 255, 0.052);
        box-shadow: 0 12px 30px rgba(0, 0, 0, 0.22);
      }

      .live-panel {
        max-width: none;
        margin-top: 12px;
        grid-template-columns: 1fr;
        border-radius: 22px;
        padding: 18px;
        box-shadow: 0 18px 44px rgba(0, 0, 0, 0.28);
      }

      .live-date {
        font-size: 0.94rem;
      }

      .live-time {
        font-size: clamp(2.35rem, 13vw, 3.4rem);
      }

      .live-weather {
        border-left: 0;
        border-top: 1px solid var(--borda);
        padding-left: 0;
        padding-top: 14px;
      }

      section {
        padding: 58px 0;
      }

      .section-title {
        margin-bottom: 24px;
      }

      .section-title h2 {
        font-size: clamp(2rem, 8.6vw, 3rem);
        letter-spacing: -0.058em;
      }

      .section-title p {
        font-size: 1rem;
        line-height: 1.65;
      }

      .grid-3,
      .grid-4,
      .equipment-gallery,
      .feature-box,
      .split {
        display: grid;
        grid-template-columns: 1fr;
        gap: 16px;
      }

      .card,
      .equipment-card,
      .segment-card,
      .feature-column,
      .security,
      .step,
      .cta {
        border-radius: 24px;
        box-shadow: 0 18px 46px rgba(0, 0, 0, 0.24);
      }

      .card,
      .feature-column,
      .security,
      .cta {
        padding: 22px;
      }

      .equipment-image,
      .segment-image-wrap {
        aspect-ratio: 16 / 10;
      }

      .equipment-image,
      .segment-image {
        object-fit: cover;
      }

      .equipment-content,
      .segment-body {
        padding: 20px;
      }

      .equipment-content h3,
      .segment-body h3,
      .card h3 {
        font-size: 1.24rem;
      }

      .equipment-content p,
      .segment-body p,
      .card p {
        font-size: 0.98rem;
        line-height: 1.58;
      }

      .step {
        grid-template-columns: 46px 1fr;
      }

      .cta {
        gap: 22px;
      }

      .cta .btn {
        width: 100%;
      }

      .footer-content {
        flex-direction: column;
        text-align: center;
        align-items: center;
      }

      .whatsapp-float {
        right: 14px;
        bottom: 14px;
      }

      .whatsapp-label {
        display: none;
      }

      .whatsapp-icon {
        width: 58px;
        height: 58px;
      }
    }

    @media (max-width: 380px) {
      .container {
        width: min(100% - 18px, 1180px);
      }

      .hero.container {
        padding-left: 10px;
        padding-right: 10px;
      }

      .hero-actions {
        grid-template-columns: 1fr;
      }

      h1 {
        font-size: clamp(2.15rem, 12vw, 3.15rem);
      }

      .menu a {
        font-size: 0.82rem;
        padding: 8px 10px;
      }
    }




    /* Área Quem Somos */
    .about-section {
      position: relative;
      overflow: hidden;
      padding-top: 88px;
      padding-bottom: 88px;
    }

    .about-section::before {
      content: "";
      position: absolute;
      inset: 0;
      pointer-events: none;
      background:
        radial-gradient(circle at 8% 12%, rgba(0, 142, 232, 0.16), transparent 34%),
        radial-gradient(circle at 90% 70%, rgba(215, 221, 229, 0.08), transparent 34%);
    }

    .about-section > .container {
      position: relative;
      z-index: 2;
    }

    .about-panel {
      display: grid;
      grid-template-columns: 1.05fr 0.95fr;
      gap: 26px;
      align-items: stretch;
      margin-top: 30px;
    }

    .about-story {
      border: 1px solid rgba(215, 221, 229, 0.16);
      border-radius: 30px;
      padding: 34px;
      background:
        linear-gradient(145deg, rgba(255, 255, 255, 0.07), rgba(255, 255, 255, 0.018)),
        rgba(255, 255, 255, 0.045);
      box-shadow: 0 26px 72px rgba(0, 0, 0, 0.26);
    }

    .about-story h3 {
      font-size: clamp(1.65rem, 3vw, 2.35rem);
      line-height: 1.08;
      letter-spacing: -0.045em;
      margin-bottom: 18px;
      color: var(--branco);
    }

    .about-story p {
      color: var(--cinza);
      font-size: 1.05rem;
      margin-bottom: 16px;
    }

    .about-story p:last-child {
      margin-bottom: 0;
    }

    .about-highlight {
      color: var(--azul-claro);
      font-weight: 900;
    }

    .about-values {
      display: grid;
      gap: 16px;
    }

    .about-value-card {
      border: 1px solid rgba(215, 221, 229, 0.16);
      border-radius: 24px;
      padding: 24px;
      background:
        linear-gradient(145deg, rgba(0, 142, 232, 0.10), rgba(255, 255, 255, 0.02)),
        rgba(255, 255, 255, 0.04);
      transition: 0.22s ease;
    }

    .about-value-card:hover {
      transform: translateY(-3px);
      border-color: rgba(0, 142, 232, 0.48);
      background:
        linear-gradient(145deg, rgba(0, 142, 232, 0.16), rgba(255, 255, 255, 0.025)),
        rgba(255, 255, 255, 0.05);
    }

    .about-value-card span {
      display: inline-flex;
      width: 46px;
      height: 46px;
      border-radius: 15px;
      align-items: center;
      justify-content: center;
      background: rgba(0, 142, 232, 0.14);
      border: 1px solid rgba(0, 142, 232, 0.28);
      color: var(--azul-claro);
      font-weight: 950;
      margin-bottom: 14px;
    }

    .about-value-card strong {
      display: block;
      color: var(--branco);
      font-size: 1.13rem;
      margin-bottom: 8px;
    }

    .about-value-card p {
      color: var(--cinza);
      font-size: 0.96rem;
    }

    .about-motto {
      margin-top: 24px;
      border: 1px solid rgba(0, 142, 232, 0.38);
      border-radius: 24px;
      padding: 22px 24px;
      background:
        radial-gradient(circle at 0% 0%, rgba(0, 142, 232, 0.22), transparent 40%),
        rgba(0, 142, 232, 0.08);
      color: var(--prata);
      font-size: 1.18rem;
      font-weight: 900;
      letter-spacing: -0.02em;
    }

    @media (max-width: 980px) {
      .about-panel {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 640px) {
      .about-section {
        padding-top: 62px;
        padding-bottom: 62px;
      }

      .about-story {
        padding: 26px 22px;
        border-radius: 26px;
      }

      .about-story p {
        font-size: 1rem;
      }

      .about-value-card {
        padding: 20px;
      }

      .about-motto {
        font-size: 1.05rem;
      }
    }


    /* Área de depoimentos */
    .testimonials-section {
      position: relative;
      overflow: hidden;
    }

    .testimonials-section::before {
      content: "";
      position: absolute;
      inset: 0;
      pointer-events: none;
      background:
        radial-gradient(circle at 15% 12%, rgba(0, 142, 232, 0.14), transparent 34%),
        radial-gradient(circle at 85% 70%, rgba(0, 142, 232, 0.08), transparent 32%);
    }

    .testimonials-section > .container {
      position: relative;
      z-index: 2;
    }

    .testimonials-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 18px;
      margin-top: 28px;
    }

    .testimonial-card {
      position: relative;
      min-height: 300px;
      border: 1px solid rgba(215, 221, 229, 0.16);
      border-radius: 26px;
      padding: 26px;
      background:
        linear-gradient(145deg, rgba(255, 255, 255, 0.065), rgba(255, 255, 255, 0.018)),
        rgba(255, 255, 255, 0.045);
      box-shadow: 0 22px 60px rgba(0, 0, 0, 0.22);
      overflow: hidden;
      transition: opacity 0.28s ease, transform 0.28s ease, border-color 0.24s ease, background 0.24s ease;
    }

    .testimonial-card:hover {
      transform: translateY(-4px);
      border-color: rgba(0, 142, 232, 0.48);
      background:
        linear-gradient(145deg, rgba(0, 142, 232, 0.12), rgba(255, 255, 255, 0.025)),
        rgba(255, 255, 255, 0.045);
    }

    .testimonial-card::before {
      content: "“";
      position: absolute;
      right: 20px;
      top: -24px;
      color: rgba(0, 142, 232, 0.18);
      font-size: 8.5rem;
      line-height: 1;
      font-family: Georgia, serif;
      font-weight: 900;
    }

    .testimonial-stars {
      color: var(--azul-claro);
      letter-spacing: 0.12em;
      font-size: 0.96rem;
      margin-bottom: 18px;
      text-shadow: 0 0 16px rgba(0, 142, 232, 0.34);
    }

    .testimonial-text {
      position: relative;
      z-index: 2;
      color: var(--prata);
      font-size: 1.02rem;
      line-height: 1.72;
      margin-bottom: 24px;
    }

    .testimonial-author {
      display: flex;
      align-items: center;
      gap: 13px;
      margin-top: auto;
    }

    .testimonial-avatar {
      width: 48px;
      height: 48px;
      border-radius: 16px;
      display: grid;
      place-items: center;
      color: #00111f;
      background: linear-gradient(135deg, var(--azul), var(--prata));
      font-weight: 950;
      box-shadow: 0 12px 28px rgba(0, 142, 232, 0.24);
      flex: 0 0 auto;
    }

    .testimonial-author strong {
      display: block;
      color: var(--branco);
      line-height: 1.2;
    }

    .testimonial-author span {
      display: block;
      color: var(--prata-escuro);
      font-size: 0.9rem;
      margin-top: 3px;
    }

    .testimonial-note {
      display: none;
      margin-top: 18px;
      color: var(--prata-escuro);
      font-size: 0.9rem;
    }

    .testimonial-card {
      display: flex;
      flex-direction: column;
    }

    .testimonial-card.is-fading {
      opacity: 0;
      transform: translateY(8px);
    }

    .testimonials-controls {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      margin-top: 22px;
    }

    .testimonial-dot {
      width: 9px;
      height: 9px;
      border-radius: 999px;
      background: rgba(215, 221, 229, 0.26);
      transition: 0.25s ease;
    }

    .testimonial-dot.is-active {
      width: 30px;
      background: var(--azul-claro);
      box-shadow: 0 0 18px rgba(0, 142, 232, 0.48);
    }

    @media (max-width: 980px) {
      .testimonials-grid {
        grid-template-columns: 1fr 1fr;
      }
    }

    @media (max-width: 640px) {
      .testimonials-grid {
        grid-template-columns: 1fr;
        gap: 16px;
      }

      .testimonial-card {
        min-height: auto;
        padding: 22px;
        border-radius: 24px;
      }

      .testimonial-text {
        font-size: 0.98rem;
      }
    }


    /* Área de economia / economômetro */
    .economy-section {
      position: relative;
      overflow: hidden;
      padding-top: 82px;
      padding-bottom: 82px;
    }

    .economy-section::before {
      content: "";
      position: absolute;
      inset: 0;
      pointer-events: none;
      background:
        radial-gradient(circle at 18% 18%, rgba(0, 142, 232, 0.16), transparent 34%),
        radial-gradient(circle at 82% 75%, rgba(37, 211, 102, 0.09), transparent 32%);
    }

    .economy-section > .container {
      position: relative;
      z-index: 2;
    }

    .economy-panel {
      margin-top: 30px;
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(360px, 0.9fr);
      gap: 22px;
      align-items: stretch;
    }

    .economy-counter-card,
    .economy-calculator-card {
      border: 1px solid rgba(215, 221, 229, 0.16);
      border-radius: 30px;
      background:
        linear-gradient(145deg, rgba(0, 142, 232, 0.12), rgba(255, 255, 255, 0.026)),
        rgba(255, 255, 255, 0.045);
      box-shadow: 0 24px 70px rgba(0, 0, 0, 0.28);
      padding: 32px;
      overflow: hidden;
    }

    .economy-label {
      display: inline-flex;
      align-items: center;
      gap: 9px;
      color: var(--prata);
      background: rgba(37, 211, 102, 0.10);
      border: 1px solid rgba(37, 211, 102, 0.32);
      padding: 8px 12px;
      border-radius: 999px;
      font-size: 0.88rem;
      font-weight: 800;
      margin-bottom: 18px;
    }

    .economy-label::before {
      content: "";
      width: 9px;
      height: 9px;
      border-radius: 50%;
      background: var(--whatsapp);
      box-shadow: 0 0 14px rgba(37, 211, 102, 0.75);
    }

    .economy-counter {
      font-size: clamp(2.4rem, 6vw, 5.4rem);
      line-height: 0.96;
      letter-spacing: -0.07em;
      font-weight: 950;
      color: var(--branco);
      text-shadow: 0 0 28px rgba(0, 142, 232, 0.28);
      margin-bottom: 14px;
      white-space: nowrap;
    }

    .economy-counter-card p {
      color: var(--cinza);
      font-size: 1.05rem;
      max-width: 760px;
    }

    .economy-kpis {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 14px;
      margin-top: 26px;
    }

    .economy-kpi {
      border: 1px solid rgba(215, 221, 229, 0.14);
      border-radius: 20px;
      background: rgba(0, 0, 0, 0.20);
      padding: 18px;
    }

    .economy-kpi strong {
      display: block;
      color: var(--azul-claro);
      font-size: 1.5rem;
      line-height: 1.1;
      margin-bottom: 5px;
    }

    .economy-kpi span {
      color: var(--prata-escuro);
      font-size: 0.9rem;
    }

    .economy-calculator-card h3 {
      font-size: 1.55rem;
      letter-spacing: -0.04em;
      margin-bottom: 10px;
    }

    .economy-calculator-card > p {
      color: var(--cinza);
      margin-bottom: 20px;
      font-size: 0.98rem;
    }

    .economy-form {
      display: grid;
      gap: 13px;
    }

    .economy-field {
      display: grid;
      gap: 7px;
    }

    .economy-field label {
      color: var(--prata);
      font-size: 0.9rem;
      font-weight: 800;
    }

    .economy-field input {
      width: 100%;
      border: 1px solid rgba(215, 221, 229, 0.18);
      border-radius: 14px;
      background: rgba(0, 0, 0, 0.28);
      color: var(--branco);
      padding: 12px 14px;
      font-size: 1rem;
      outline: none;
    }

    .economy-field input:focus {
      border-color: rgba(0, 142, 232, 0.65);
      box-shadow: 0 0 0 3px rgba(0, 142, 232, 0.12);
    }

    .economy-results {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
      margin-top: 18px;
    }

    .economy-result {
      border: 1px solid rgba(0, 142, 232, 0.26);
      border-radius: 18px;
      background: rgba(0, 142, 232, 0.08);
      padding: 16px;
    }

    .economy-result strong {
      display: block;
      color: var(--branco);
      font-size: 1.28rem;
      line-height: 1.1;
      margin-bottom: 5px;
    }

    .economy-result span {
      color: var(--prata-escuro);
      font-size: 0.86rem;
    }

    .economy-note {
      margin-top: 16px;
      color: var(--prata-escuro);
      font-size: 0.86rem;
    }

    @media (max-width: 1100px) {
      .economy-panel {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 760px) {
      .economy-section {
        padding-top: 62px;
        padding-bottom: 62px;
      }

      .economy-counter-card,
      .economy-calculator-card {
        padding: 24px;
        border-radius: 26px;
      }

      .economy-counter {
        white-space: normal;
        font-size: clamp(2.25rem, 12vw, 3.4rem);
      }

      .economy-kpis,
      .economy-results {
        grid-template-columns: 1fr;
      }
    }

  </style>
</head>
<body>
  <header class="topbar">
    <div class="container navbar">
      <a href="#inicio" aria-label="Página inicial da Zero13 Automação Comercial">
        <img class="logo-nav" src="assets/logo-zero13-cartao.png" alt="Zero13 Automação Comercial" />
      </a>

      <nav class="menu" aria-label="Menu principal">
        <a href="#servicos">Serviços</a>
        <a href="#quem-somos">Quem somos</a>
        <a href="#equipamentos">Equipamentos</a>
        <a href="#segmentos">Segmentos</a>
        <a href="#depoimentos">Depoimentos</a>
        <a href="#funcionalidades">Funcionalidades</a>
        <a href="#seguranca">Segurança</a>
        <a href="#contato">Contato</a>
      </nav>

      <a class="btn btn-primary" href="https://wa.me/5513988229261?text=Ol%C3%A1%2C%20gostaria%20de%20falar%20com%20Alexander%20da%20Zero13." target="_blank" rel="noopener noreferrer" data-whatsapp-rotate="true">
        Solicitar demonstração
      </a>
    </div>
  </header>

  <main id="inicio">
    <section class="container hero">
      <div>
        <div class="tag">Automação comercial para empresas que não podem parar</div>
        <h1>PDV, suporte e gestão para o seu comércio.</h1>
        <p>
          A Zero13 Automação Comercial oferece soluções para frente de caixa, retaguarda, equipamentos,
          redes, suporte técnico e organização da operação comercial.
        </p>

        <div class="hero-actions">
          <a class="btn btn-primary" href="#contato">Solicitar demonstração</a>
          <a class="btn btn-outline" href="#servicos">Conhecer soluções</a>
        </div>

        <div class="hero-points">
          <div class="point">
            <strong>PDV e retaguarda</strong>
            <span>Venda, controle e gestão</span>
          </div>
          <div class="point">
            <strong>Equipamentos</strong>
            <span>Impressoras, leitores e balanças</span>
          </div>
          <div class="point">
            <strong>Suporte técnico</strong>
            <span>Implantação e manutenção</span>
          </div>
        </div>

        
      </div>

    </section>


    <section id="quem-somos" class="about-section">
      <div class="container">
        <div class="section-title">
          <span>Quem somos</span>
          <h2>Uma empresa nascida da experiência real no suporte à automação comercial.</h2>
          <p>
            A 013 Automação Comercial une experiência especializada, atendimento próximo e compromisso com o pós-venda.
          </p>
        </div>

        <div class="about-panel">
          <div class="about-story">
            <h3>Da RRSYSTEM à 013 Automação Comercial.</h3>
            <p>
              A <strong>013 Automação Comercial</strong> nasceu originalmente como <strong>RRSYSTEM</strong>.
              A empresa surgiu depois que dois analistas com mais de 20 anos de experiência, após atuarem por muitos anos em diversas empresas do setor,
              passaram a observar deficiências recorrentes nos atendimentos e, principalmente, nas questões de suporte e pós-venda.
            </p>
            <p>
              A partir dessa experiência prática, nasceu a RRSYSTEM, hoje <strong>013 Automação Comercial</strong>,
              com o objetivo de entregar um atendimento mais próximo, claro e responsável para empresas que dependem
              da tecnologia para vender, controlar e manter sua operação funcionando.
            </p>
            <p>
              Nosso princípio é simples: <span class="about-highlight">atender bem para atender sempre</span>,
              trabalhando com honestidade, responsabilidade profissional e preço justo.
            </p>

            <div class="about-motto">
              “Atender bem para atender sempre, com honestidade e preço justo.”
            </div>
          </div>

          <div class="about-values" aria-label="Princípios da 013 Automação Comercial">
            <article class="about-value-card">
              <span>01</span>
              <strong>Experiência de campo</strong>
              <p>Conhecimento adquirido em anos de atendimento especializado, implantação de sistemas e suporte em ambientes comerciais reais.</p>
            </article>

            <article class="about-value-card">
              <span>02</span>
              <strong>Suporte e pós-venda</strong>
              <p>Foco em acompanhar o cliente depois da implantação, reduzindo dúvidas, falhas operacionais e paradas no atendimento.</p>
            </article>

            <article class="about-value-card">
              <span>03</span>
              <strong>Honestidade e preço justo</strong>
              <p>Atendimento transparente, soluções adequadas à necessidade do cliente e compromisso com relações de longo prazo.</p>
            </article>
          </div>
        </div>
      </div>
    </section>


    <section id="servicos">
      <div class="container">
        <div class="section-title">
          <span>Serviços</span>
          <h2>Soluções para organizar, vender e controlar melhor.</h2>
          <p>
            Uma estrutura pensada para pequenos e médios comércios que precisam de caixa rápido,
            operação estável e suporte confiável.
          </p>
        </div>

        <div class="grid-3">
          <article class="card">
            <div class="icon">🖥️</div>
            <h3>Sistemas de PDV</h3>
            <p>Instalação, configuração e suporte para frente de caixa, comandas, vendas, operadores e fechamento de caixa.</p>
          </article>

          <article class="card">
            <div class="icon">📦</div>
            <h3>Retaguarda e estoque</h3>
            <p>Cadastro de produtos, grupos, preços, fornecedores, estoque, relatórios e organização da gestão comercial.</p>
          </article>

          <article class="card">
            <div class="icon">🧾</div>
            <h3>Equipamentos comerciais</h3>
            <p>Configuração de impressoras, leitores de código de barras, balanças, pin pad, gavetas e terminais.</p>
          </article>

          <article class="card">
            <div class="icon">🌐</div>
            <h3>Redes e infraestrutura</h3>
            <p>Organização de rede local, computadores, internet, pontos de venda e ambiente técnico da operação.</p>
          </article>

          <article class="card">
            <div class="icon">🛠️</div>
            <h3>Suporte técnico</h3>
            <p>Diagnóstico, manutenção preventiva, atendimento remoto, atendimento presencial e orientação operacional.</p>
          </article>

          <article class="card">
            <div class="icon">🔐</div>
            <h3>Segurança da operação</h3>
            <p>Boas práticas para senhas, usuários, permissões, backup, logs e redução de riscos no ambiente comercial.</p>
          </article>
        </div>
      </div>
    </section>


    <section id="equipamentos">
      <div class="container">
        <div class="section-title">
          <span>Equipamentos</span>
          <h2>Tecnologia para deixar sua operação mais rápida e profissional.</h2>
          <p>
            Além do sistema, a Zero13 apoia sua empresa na escolha, configuração e integração de equipamentos
            de automação comercial para frente de caixa, atendimento, pesagem e emissão de comprovantes.
          </p>
        </div>

        <div class="equipment-gallery" aria-label="Galeria de equipamentos de automação comercial">
          <article class="equipment-card">
            <img class="equipment-image" src="assets/totem-autoatendimento.webp" alt="Totem de autoatendimento para automação comercial" loading="lazy" />
            <div class="equipment-content">
              <h3>Totens de autoatendimento</h3>
              <p>Agilizam pedidos, reduzem filas e modernizam o atendimento em lojas, restaurantes e operações de alto fluxo.</p>
            </div>
          </article>

          <article class="equipment-card">
            <img class="equipment-image" src="assets/impressora-termica.webp" alt="Impressora térmica imprimindo comprovante" loading="lazy" />
            <div class="equipment-content">
              <h3>Impressoras térmicas</h3>
              <p>Essenciais para cupons, pedidos de cozinha, senhas, comandas e comprovantes de venda.</p>
            </div>
          </article>

          <article class="equipment-card">
            <img class="equipment-image" src="assets/balanca-comercial.webp" alt="Balança comercial digital para mercados e varejo" loading="lazy" />
            <div class="equipment-content">
              <h3>Balanças comerciais</h3>
              <p>Integração para pesagem, etiquetas, preço por quilo e rotinas de atendimento em mercados e padarias.</p>
            </div>
          </article>

          <article class="equipment-card">
            <img class="equipment-image" src="assets/pdv-completo.webp" alt="Conjunto de equipamentos de PDV com monitor, leitor, impressora e pin pad" loading="lazy" />
            <div class="equipment-content">
              <h3>PDV completo</h3>
              <p>Monitor, gaveta, leitor, pin pad e periféricos configurados para uma operação estável e integrada.</p>
            </div>
          </article>
        </div>
      </div>
    </section>


    <section id="segmentos">
      <div class="container">
        <div class="section-title">
          <span>Segmentos</span>
          <h2>Atendimento para diferentes tipos de comércio.</h2>
          <p>
            O projeto pode ser adaptado conforme o fluxo de venda, os equipamentos e o nível de controle necessário.
          </p>
        </div>

        <div class="grid-4">
          <article class="card segment-card">
            <div class="segment-image-wrap">
              <img class="segment-image" src="assets/segmento-mercados.png" alt="Ambiente de mercado com PDV, balança e automação comercial" loading="lazy" />
            </div>
            <div class="segment-body">
              <h3>Mercados</h3>
              <p>PDV, balança, etiquetas, estoque e controle de preços.</p>
            </div>
          </article>
          <article class="card segment-card">
            <div class="segment-image-wrap">
              <img class="segment-image" src="assets/segmento-padarias.png" alt="Padaria moderna com balcão, caixa e impressora" loading="lazy" />
            </div>
            <div class="segment-body">
              <h3>Padarias</h3>
              <p>Balcão, comandas, impressoras e vendas rápidas.</p>
            </div>
          </article>
          <article class="card segment-card">
            <div class="segment-image-wrap">
              <img class="segment-image" src="assets/segmento-bares-restaurantes.png" alt="Bar ou restaurante com sistema de automação e terminal de atendimento" loading="lazy" />
            </div>
            <div class="segment-body">
              <h3>Bares e restaurantes</h3>
              <p>Mesas, comandas, cozinha, delivery e pagamentos.</p>
            </div>
          </article>
          <article class="card segment-card">
            <div class="segment-image-wrap">
              <img class="segment-image" src="assets/segmento-lojas.png" alt="Loja moderna com PDV, leitor e organização de estoque" loading="lazy" />
            </div>
            <div class="segment-body">
              <h3>Lojas</h3>
              <p>Produtos, estoque, operadores, caixa e relatórios.</p>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="funcionalidades">
      <div class="container">
        <div class="section-title">
          <span>Funcionalidades</span>
          <h2>O essencial para uma operação comercial moderna.</h2>
          <p>
            Um bom ambiente de automação deve unir velocidade no atendimento, controle de gestão e segurança operacional.
          </p>
        </div>

        <div class="feature-box">
          <div class="feature-column">
            <h3>Frente de caixa</h3>
            <ul class="feature-list">
              <li>Venda rápida no balcão.</li>
              <li>Controle de caixa e operadores.</li>
              <li>Comandas, mesas e pedidos.</li>
              <li>Integração com impressoras e leitores.</li>
              <li>Pagamentos por cartão, Pix e TEF quando disponível.</li>
            </ul>
          </div>

          <div class="feature-column">
            <h3>Gestão e retaguarda</h3>
            <ul class="feature-list">
              <li>Cadastro de produtos e preços.</li>
              <li>Controle de estoque e fornecedores.</li>
              <li>Relatórios de venda e fechamento.</li>
              <li>Organização de grupos e subgrupos.</li>
              <li>Permissões de usuários e trilhas de auditoria.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section id="seguranca">
      <div class="container split">
        <div class="security">
          <h3>Boas práticas alinhadas à ISO/IEC 27001</h3>
          <p>
            Segurança aplicada ao ambiente comercial para reduzir riscos de parada, perda de dados e acesso indevido.
          </p>

          <ul>
            <li>Controle de acesso por função.</li>
            <li>Uso de credenciais individuais.</li>
            <li>Backup com validação de restauração.</li>
            <li>Registro de alterações críticas.</li>
            <li>Separação entre usuários administrativos e operacionais.</li>
          </ul>
        </div>

        <div class="section-title">
          <span>Segurança</span>
          <h2>Automação comercial precisa ser rápida e protegida.</h2>
          <p>
            Sistemas de venda lidam com informações sensíveis, fluxo financeiro, cadastros e relatórios.
            Por isso, o projeto deve considerar controle de acesso, backup, documentação e rastreabilidade.
          </p>
        </div>
      </div>
    </section>

    <section id="processo">
      <div class="container split">
        <div class="section-title">
          <span>Processo</span>
          <h2>Como a implantação acontece.</h2>
          <p>
            O atendimento pode começar por uma demonstração, seguida de diagnóstico, configuração,
            implantação e acompanhamento da operação.
          </p>
        </div>

        <div class="steps">
          <div class="step">
            <div class="step-number">1</div>
            <div>
              <h3>Demonstração</h3>
              <p>Apresentação da solução e entendimento inicial da operação.</p>
            </div>
          </div>
          <div class="step">
            <div class="step-number">2</div>
            <div>
              <h3>Diagnóstico</h3>
              <p>Levantamento de sistema, equipamentos, rede e necessidades.</p>
            </div>
          </div>
          <div class="step">
            <div class="step-number">3</div>
            <div>
              <h3>Implantação</h3>
              <p>Configuração de PDV, equipamentos, usuários e retaguarda.</p>
            </div>
          </div>
          <div class="step">
            <div class="step-number">4</div>
            <div>
              <h3>Suporte</h3>
              <p>Acompanhamento, ajustes e apoio técnico após a implantação.</p>
            </div>
          </div>
        </div>
      </div>
    </section>



    <section id="depoimentos" class="testimonials-section">
      <div class="container">
        <div class="section-title">
          <span>Depoimentos</span>
          <h2>Relatos que mostram como a automação melhora a rotina.</h2>
          <p>
            Relatos de cenários comerciais para demonstrar como a automação pode melhorar caixa, atendimento, estoque e pós-venda.
          </p>
        </div>

        <div class="testimonials-grid" aria-live="polite">
          <article class="testimonial-card" data-testimonial-card>
            <div class="testimonial-stars" data-testimonial-stars>★★★★★</div>
            <p class="testimonial-text" data-testimonial-text>
              A implantação do PDV deixou nosso caixa muito mais rápido. A equipe conseguiu operar com menos erro e o suporte ajudou bastante nos primeiros dias.
            </p>
            <div class="testimonial-author">
              <div class="testimonial-avatar" data-testimonial-avatar>ME</div>
              <div>
                <strong data-testimonial-business>Mercado Estrela Azul</strong>
                <span data-testimonial-meta>Marcelo Ribeiro • Mercado de bairro</span>
              </div>
            </div>
          </article>

          <article class="testimonial-card" data-testimonial-card>
            <div class="testimonial-stars" data-testimonial-stars>★★★★★</div>
            <p class="testimonial-text" data-testimonial-text>
              Organizamos o balcão, impressora, comandas e fechamento de caixa. O atendimento ficou mais fluido e ganhamos mais controle da rotina da padaria.
            </p>
            <div class="testimonial-author">
              <div class="testimonial-avatar" data-testimonial-avatar>PV</div>
              <div>
                <strong data-testimonial-business>Padaria Pão da Vila</strong>
                <span data-testimonial-meta>Carla Pereira • Padaria e confeitaria</span>
              </div>
            </div>
          </article>

          <article class="testimonial-card" data-testimonial-card>
            <div class="testimonial-stars" data-testimonial-stars>★★★★★</div>
            <p class="testimonial-text" data-testimonial-text>
              A automação ajudou muito nas comandas, mesas e pedidos. Hoje conseguimos acompanhar melhor o movimento e reduzir atrasos no atendimento.
            </p>
            <div class="testimonial-author">
              <div class="testimonial-avatar" data-testimonial-avatar>P13</div>
              <div>
                <strong data-testimonial-business>Restaurante Porto 13</strong>
                <span data-testimonial-meta>Renato Silva • Bar e restaurante</span>
              </div>
            </div>
          </article>
        </div>

        <div class="testimonials-controls" aria-label="Indicador de depoimentos">
          <span class="testimonial-dot is-active" data-testimonial-dot></span>
          <span class="testimonial-dot" data-testimonial-dot></span>
          <span class="testimonial-dot" data-testimonial-dot></span>
          <span class="testimonial-dot" data-testimonial-dot></span>
        </div>
      </div>
    </section>

    <section id="contato">
      <div class="container">
        <div class="cta">
          <div>
            <h2>Solicite uma demonstração da Zero13.</h2>
            <p>
              Fale pelo WhatsApp comercial para avaliar PDV, equipamentos, rede,
              suporte técnico, retaguarda, comandas e organização da sua operação comercial. O atendimento é distribuído alternadamente entre Rafael e Alexander.
            </p>
          </div>
          <a class="btn btn-whatsapp" href="https://wa.me/5513988229261?text=Ol%C3%A1%2C%20gostaria%20de%20falar%20com%20Alexander%20da%20Zero13." target="_blank" rel="noopener noreferrer" data-whatsapp-rotate="true">
            Chamar no WhatsApp
          </a>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-content">
      <p>© <span id="anoAtual"></span> Zero13 Automação Comercial. Todos os direitos reservados.</p>
      <p>PDV • Suporte • Equipamentos • Redes • Retaguarda</p>
    </div>
  </footer>

  <a
    class="whatsapp-float"
    href="https://wa.me/5513988229261?text=Ol%C3%A1%2C%20gostaria%20de%20falar%20com%20Alexander%20da%20Zero13."
    target="_blank"
    rel="noopener noreferrer"
    aria-label="Falar com Rafael ou Alexander da Zero13 pelo WhatsApp"
   data-whatsapp-rotate="true">
    <span class="whatsapp-label">Fale pelo WhatsApp</span>
    <span class="whatsapp-icon">☏</span>
  </a>

  <script>
    const LOGO_OFICIAL = 'data:image/webp;base64,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';

    document.querySelectorAll('.logo-nav').forEach((logo) => {
      logo.src = LOGO_OFICIAL;
    });
    const ATENDENTES_WHATSAPP = [
      {
        nome: 'Rafael',
        telefone: '5513988215842'
      },
      {
        nome: 'Alexander',
        telefone: '5513988229261'
      }
    ];

    function gerarLinkWhatsAppIntercalado() {
      const chaveIndice = 'zero13_whatsapp_indice_atendente';
      const indiceSalvo = Number(localStorage.getItem(chaveIndice) || '0');
      const atendente = ATENDENTES_WHATSAPP[indiceSalvo % ATENDENTES_WHATSAPP.length];
      const proximoIndice = (indiceSalvo + 1) % ATENDENTES_WHATSAPP.length;

      localStorage.setItem(chaveIndice, String(proximoIndice));

      const mensagem = encodeURIComponent(`Olá, gostaria de falar com ${atendente.nome} da Zero13.`);
      return `https://wa.me/${atendente.telefone}?text=${mensagem}`;
    }

    document.querySelectorAll('[data-whatsapp-rotate="true"]').forEach((link) => {
      link.addEventListener('click', () => {
        link.href = gerarLinkWhatsAppIntercalado();
      });
    });


    const DEPOIMENTOS_ZERO13 = [
      {
        estrelas: '★★★★★',
        texto: 'A implantação do PDV deixou nosso caixa mais rápido e reduziu erros no atendimento. O suporte acompanhou a equipe nos primeiros dias e isso fez muita diferença.',
        avatar: 'ME',
        empresa: 'Mercado Estrela Azul',
        meta: 'Marcelo Ribeiro • Mercado de bairro'
      },
      {
        estrelas: '★★★★★',
        texto: 'Organizamos balcão, impressora, comandas e fechamento de caixa. A rotina da padaria ficou mais simples e os pedidos passaram a sair com mais controle.',
        avatar: 'PV',
        empresa: 'Padaria Pão da Vila',
        meta: 'Carla Pereira • Padaria e confeitaria'
      },
      {
        estrelas: '★★★★★',
        texto: 'Com as comandas e mesas automatizadas, conseguimos acompanhar melhor o movimento do salão e reduzir atrasos nos pedidos.',
        avatar: 'P13',
        empresa: 'Restaurante Porto 13',
        meta: 'Renato Silva • Bar e restaurante'
      },
      {
        estrelas: '★★★★★',
        texto: 'Antes era difícil controlar estoque, vendas e fechamento. Com a retaguarda organizada, ficou muito mais fácil tomar decisões no dia a dia.',
        avatar: 'UM',
        empresa: 'Loja Urban Mix',
        meta: 'Fernanda Lima • Loja de varejo'
      },
      {
        estrelas: '★★★★★',
        texto: 'A balança integrada e as etiquetas ajudaram a reduzir filas no balcão. O atendimento ficou mais rápido e com menos retrabalho.',
        avatar: 'BC',
        empresa: 'Açougue Bom Corte',
        meta: 'André Matos • Açougue e carnes'
      },
      {
        estrelas: '★★★★★',
        texto: 'O pós-venda foi o grande diferencial. Sempre que precisamos de orientação, tivemos retorno rápido, claro e direto.',
        avatar: 'SM',
        empresa: 'Empório Santa Marina',
        meta: 'Patrícia Alves • Empório e conveniência'
      },
      {
        estrelas: '★★★★★',
        texto: 'As comandas e os pedidos para a cozinha ficaram muito mais organizados. A equipe ganhou agilidade nos horários de maior movimento.',
        avatar: 'BR',
        empresa: 'Brasa do Canal',
        meta: 'Gustavo Nunes • Hamburgueria'
      },
      {
        estrelas: '★★★★★',
        texto: 'Com produtos bem cadastrados e caixa configurado, conseguimos controlar melhor preços, promoções e relatórios de venda.',
        avatar: 'NP',
        empresa: 'Minimercado Nova Praia',
        meta: 'Luciana Costa • Minimercado'
      },
      {
        estrelas: '★★★★★',
        texto: 'A impressora, o leitor e o controle de caixa passaram a trabalhar juntos. A rotina ficou mais simples para os operadores.',
        avatar: 'PA',
        empresa: 'Conveniência Ponto Azul',
        meta: 'Ricardo Gomes • Conveniência'
      }
    ];

    function atualizarDepoimentos(indiceGrupo) {
      const cards = Array.from(document.querySelectorAll('[data-testimonial-card]'));
      const dots = Array.from(document.querySelectorAll('[data-testimonial-dot]'));
      const totalPaginas = Math.ceil(DEPOIMENTOS_ZERO13.length / Math.max(cards.length, 1));

      if (!cards.length) return;

      cards.forEach((card) => card.classList.add('is-fading'));

      setTimeout(() => {
        cards.forEach((card, posicao) => {
          const depoimento = DEPOIMENTOS_ZERO13[(indiceGrupo + posicao) % DEPOIMENTOS_ZERO13.length];

          card.querySelector('[data-testimonial-stars]').textContent = depoimento.estrelas;
          card.querySelector('[data-testimonial-text]').textContent = depoimento.texto;
          card.querySelector('[data-testimonial-avatar]').textContent = depoimento.avatar;
          card.querySelector('[data-testimonial-business]').textContent = depoimento.empresa;
          card.querySelector('[data-testimonial-meta]').textContent = depoimento.meta;

          card.classList.remove('is-fading');
        });

        const paginaAtiva = Math.floor(indiceGrupo / cards.length) % Math.max(totalPaginas, 1);
        dots.forEach((dot, index) => dot.classList.toggle('is-active', index === paginaAtiva));
      }, 280);
    }

    const testimonialControls = document.querySelector('.testimonials-controls');
    const testimonialCards = Array.from(document.querySelectorAll('[data-testimonial-card]'));
    if (testimonialControls && testimonialCards.length) {
      const totalPaginas = Math.ceil(DEPOIMENTOS_ZERO13.length / testimonialCards.length);
      testimonialControls.innerHTML = Array.from({ length: totalPaginas }, (_, index) => `<span class="testimonial-dot ${index === 0 ? 'is-active' : ''}" data-testimonial-dot></span>`).join('');
    }

    let indiceDepoimentoAtual = 0;
    atualizarDepoimentos(indiceDepoimentoAtual);
    setInterval(() => {
      const cardsVisiveis = Math.max(document.querySelectorAll('[data-testimonial-card]').length, 1);
      indiceDepoimentoAtual = (indiceDepoimentoAtual + cardsVisiveis) % DEPOIMENTOS_ZERO13.length;
      atualizarDepoimentos(indiceDepoimentoAtual);
    }, 5000);
    document.getElementById('anoAtual').textContent = new Date().getFullYear();
  </script>
</body>
</html>
