<script>
    import favicon from '$lib/assets/favicon.svg';
    let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={favicon} />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Raleway:ital,wght@0,300;0,400;1,300&display=swap" rel="stylesheet" />
</svelte:head>

<div class="galaxy-layout">
    <!-- Animated star field layers -->
    <div class="stars stars-1"></div>
    <div class="stars stars-2"></div>
    <div class="stars stars-3"></div>

    <!-- Nebula clouds -->
    <div class="nebula nebula-1"></div>
    <div class="nebula nebula-2"></div>
    <div class="nebula nebula-3"></div>

    <!-- Galactic core glow -->
    <div class="galactic-core"></div>

    <!-- Shooting stars -->
    <div class="shooting-star s1"></div>
    <div class="shooting-star s2"></div>
    <div class="shooting-star s3"></div>
    <div class="shooting-star s4"></div>

    <!-- Content -->
    <div class="content">
        {@render children()}
    </div>
</div>

<style>
    :global(*) {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    :global(body) {
        background: #00000f;
        overflow-x: hidden;
    }

    :global(:root) {
        --star-color: #ffffff;
        --nebula-purple: rgba(88, 28, 175, 0.35);
        --nebula-blue: rgba(29, 78, 216, 0.3);
        --nebula-pink: rgba(157, 23, 77, 0.25);
        --nebula-teal: rgba(15, 118, 110, 0.2);
        --core-glow: rgba(251, 191, 36, 0.15);
        --text-primary: #e2e8f0;
        --text-accent: #a78bfa;
        --font-display: 'Orbitron', monospace;
        --font-body: 'Raleway', sans-serif;
    }

    /* ─── Layout ───────────────────────────────────────── */
    .galaxy-layout {
        position: relative;
        min-height: 100vh;
        width: 100%;
        background: radial-gradient(ellipse at 20% 50%, #0a001a 0%, #000008 40%, #00000f 100%);
        overflow: hidden;
        font-family: var(--font-body);
        color: var(--text-primary);
    }

    /* ─── Star Fields ───────────────────────────────────── */
    .stars {
        position: fixed;
        inset: -50%;
        width: 200%;
        height: 200%;
        pointer-events: none;
    }

    .stars-1 {
        background-image:
            radial-gradient(1px 1px at 10% 15%, white, transparent),
            radial-gradient(1px 1px at 25% 8%, white, transparent),
            radial-gradient(1px 1px at 38% 42%, white, transparent),
            radial-gradient(1px 1px at 52% 71%, white, transparent),
            radial-gradient(1px 1px at 67% 22%, white, transparent),
            radial-gradient(1px 1px at 78% 88%, white, transparent),
            radial-gradient(1px 1px at 89% 55%, white, transparent),
            radial-gradient(1px 1px at 5% 63%, white, transparent),
            radial-gradient(1px 1px at 42% 91%, white, transparent),
            radial-gradient(1px 1px at 95% 33%, white, transparent),
            radial-gradient(1px 1px at 18% 77%, white, transparent),
            radial-gradient(1px 1px at 33% 19%, white, transparent),
            radial-gradient(1px 1px at 71% 48%, white, transparent),
            radial-gradient(1px 1px at 85% 12%, white, transparent),
            radial-gradient(1px 1px at 3% 39%, white, transparent),
            radial-gradient(1px 1px at 57% 5%, white, transparent),
            radial-gradient(1px 1px at 46% 58%, white, transparent),
            radial-gradient(1px 1px at 92% 74%, white, transparent),
            radial-gradient(1px 1px at 14% 93%, white, transparent),
            radial-gradient(1px 1px at 63% 36%, white, transparent),
            radial-gradient(1px 1px at 29% 54%, white, transparent),
            radial-gradient(1px 1px at 76% 67%, white, transparent),
            radial-gradient(1px 1px at 8% 28%, white, transparent),
            radial-gradient(1px 1px at 49% 82%, white, transparent),
            radial-gradient(1px 1px at 84% 41%, white, transparent),
            radial-gradient(1.5px 1.5px at 21% 6%, rgba(200,200,255,0.9), transparent),
            radial-gradient(1.5px 1.5px at 55% 95%, rgba(200,200,255,0.9), transparent),
            radial-gradient(1.5px 1.5px at 88% 18%, rgba(200,200,255,0.9), transparent),
            radial-gradient(1.5px 1.5px at 37% 73%, rgba(200,200,255,0.9), transparent),
            radial-gradient(1.5px 1.5px at 72% 59%, rgba(255,220,200,0.8), transparent);
        animation: drift-slow 120s linear infinite;
    }

    .stars-2 {
        background-image:
            radial-gradient(1px 1px at 7% 44%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 19% 31%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 31% 67%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 44% 13%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 59% 79%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 73% 37%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 81% 62%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 93% 8%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 2% 86%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 16% 52%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 48% 24%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 66% 93%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 39% 47%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 87% 76%, rgba(255,255,255,0.7), transparent),
            radial-gradient(1px 1px at 25% 88%, rgba(255,255,255,0.7), transparent),
            radial-gradient(2px 2px at 53% 34%, rgba(167,139,250,0.9), transparent),
            radial-gradient(2px 2px at 77% 15%, rgba(167,139,250,0.9), transparent),
            radial-gradient(2px 2px at 12% 71%, rgba(147,197,253,0.9), transparent),
            radial-gradient(2px 2px at 96% 50%, rgba(253,186,116,0.7), transparent),
            radial-gradient(2px 2px at 34% 3%, rgba(253,186,116,0.7), transparent);
        animation: drift-medium 80s linear infinite reverse;
        opacity: 0.8;
    }

    .stars-3 {
        background-image:
            radial-gradient(2px 2px at 15% 20%, rgba(255,255,255,0.5), transparent),
            radial-gradient(2px 2px at 45% 60%, rgba(255,255,255,0.5), transparent),
            radial-gradient(2px 2px at 75% 30%, rgba(255,255,255,0.5), transparent),
            radial-gradient(2px 2px at 90% 80%, rgba(255,255,255,0.5), transparent),
            radial-gradient(2px 2px at 30% 90%, rgba(255,255,255,0.5), transparent),
            radial-gradient(3px 3px at 60% 10%, rgba(255,255,255,0.6), transparent),
            radial-gradient(3px 3px at 20% 50%, rgba(200,230,255,0.6), transparent),
            radial-gradient(3px 3px at 80% 55%, rgba(255,220,200,0.6), transparent);
        animation: twinkle 6s ease-in-out infinite alternate, drift-slow 150s linear infinite;
        opacity: 0.9;
    }

    /* ─── Nebula Clouds ─────────────────────────────────── */
    .nebula {
        position: fixed;
        border-radius: 50%;
        filter: blur(80px);
        pointer-events: none;
        mix-blend-mode: screen;
    }

    .nebula-1 {
        width: 70vw;
        height: 60vh;
        top: -10%;
        left: -15%;
        background: radial-gradient(ellipse, var(--nebula-purple) 0%, var(--nebula-blue) 40%, transparent 70%);
        animation: nebula-pulse 18s ease-in-out infinite alternate;
    }

    .nebula-2 {
        width: 60vw;
        height: 70vh;
        bottom: -20%;
        right: -10%;
        background: radial-gradient(ellipse, var(--nebula-pink) 0%, var(--nebula-purple) 40%, transparent 70%);
        animation: nebula-pulse 22s ease-in-out infinite alternate-reverse;
    }

    .nebula-3 {
        width: 50vw;
        height: 50vh;
        top: 30%;
        left: 30%;
        background: radial-gradient(ellipse, var(--nebula-teal) 0%, var(--nebula-blue) 50%, transparent 70%);
        animation: nebula-pulse 28s ease-in-out infinite alternate;
        opacity: 0.7;
    }

    /* ─── Galactic Core ─────────────────────────────────── */
    .galactic-core {
        position: fixed;
        width: 40vw;
        height: 40vw;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        background: radial-gradient(ellipse,
            rgba(251, 191, 36, 0.08) 0%,
            rgba(251, 146, 60, 0.06) 20%,
            rgba(139, 92, 246, 0.05) 40%,
            transparent 70%
        );
        filter: blur(40px);
        pointer-events: none;
        animation: core-breathe 12s ease-in-out infinite alternate;
    }

    /* ─── Shooting Stars ────────────────────────────────── */
    .shooting-star {
        position: fixed;
        height: 1px;
        background: linear-gradient(90deg, transparent, rgba(255,255,255,0.9), rgba(167,139,250,0.5), transparent);
        border-radius: 50%;
        pointer-events: none;
        opacity: 0;
    }

    .s1 { width: 200px; top: 15%; left: -200px; animation: shoot 8s ease-out 1s infinite; transform: rotate(15deg); }
    .s2 { width: 150px; top: 35%; left: -150px; animation: shoot 8s ease-out 4s infinite; transform: rotate(10deg); }
    .s3 { width: 250px; top: 55%; left: -250px; animation: shoot 8s ease-out 6.5s infinite; transform: rotate(20deg); }
    .s4 { width: 180px; top: 75%; left: -180px; animation: shoot 8s ease-out 2.5s infinite; transform: rotate(8deg); }

    /* ─── Content ───────────────────────────────────────── */
    .content {
        position: relative;
        z-index: 10;
        min-height: 100vh;
    }

    /* ─── Keyframes ─────────────────────────────────────── */
    @keyframes drift-slow {
        from { transform: translateX(0) translateY(0); }
        to   { transform: translateX(-25%) translateY(-10%); }
    }

    @keyframes drift-medium {
        from { transform: translateX(0) translateY(0) rotate(0deg); }
        to   { transform: translateX(15%) translateY(8%) rotate(5deg); }
    }

    @keyframes twinkle {
        from { opacity: 0.5; }
        to   { opacity: 1; }
    }

    @keyframes nebula-pulse {
        from { opacity: 0.5; transform: scale(1) rotate(0deg); }
        to   { opacity: 1;   transform: scale(1.15) rotate(8deg); }
    }

    @keyframes core-breathe {
        from { opacity: 0.6; transform: translate(-50%, -50%) scale(0.9); }
        to   { opacity: 1;   transform: translate(-50%, -50%) scale(1.1); }
    }

    @keyframes shoot {
        0%   { opacity: 0; transform: translateX(0) rotate(15deg); }
        5%   { opacity: 1; }
        40%  { opacity: 0.8; }
        60%  { opacity: 0; transform: translateX(130vw) rotate(15deg); }
        100% { opacity: 0; transform: translateX(130vw) rotate(15deg); }
    }

    /* ─── Global Typography for child content ───────────── */
    :global(h1, h2, h3, h4, h5, h6) {
        font-family: var(--font-display);
        color: #e2d9f3;
        letter-spacing: 0.05em;
    }

    :global(p, span, li, a) {
        font-family: var(--font-body);
        color: #c4b5e8;
        line-height: 1.7;
    }

    :global(a) {
        color: var(--text-accent);
        text-decoration: none;
        transition: color 0.3s, text-shadow 0.3s;
    }

    :global(a:hover) {
        color: #c4b5fd;
        text-shadow: 0 0 12px rgba(167, 139, 250, 0.6);
    }
</style>