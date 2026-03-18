<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Studio — Artist Portfolio</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            serif: ['"Playfair Display"', 'Georgia', 'serif'],
            sans: ['"Inter"', 'system-ui', 'sans-serif'],
          },
          colors: {
            ink: '#1a1a1a',
            muted: '#9a9a9a',
          },
          letterSpacing: {
            superwide: '0.22em',
          },
        },
      },
    };
  </script>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;0,600;1,400;1,500&family=Inter:wght@300;400;500&display=swap" rel="stylesheet" />
  <style>
    html { scroll-behavior: smooth; }

    /* Custom scrollbar */
    ::-webkit-scrollbar { width: 4px; }
    ::-webkit-scrollbar-track { background: transparent; }
    ::-webkit-scrollbar-thumb { background: #d4d4d4; border-radius: 2px; }

    /* Masonry columns */
    .masonry {
      columns: 2;
      column-gap: 2rem;
    }
    @media (min-width: 768px)  { .masonry { columns: 2; } }
    @media (min-width: 1100px) { .masonry { columns: 3; } }

    .masonry-item {
      break-inside: avoid;
      margin-bottom: 2rem;
    }

    .masonry-item img {
      display: block;
      width: 100%;
      transform-origin: center center;
      transition:
        transform 0.7s cubic-bezier(0.25, 0.46, 0.45, 0.94),
        opacity   0.7s cubic-bezier(0.25, 0.46, 0.45, 0.94);
      will-change: transform, opacity;
    }
    .masonry-item:hover img {
      transform: scale(1.04);
      opacity: 0.93;
    }

    /* Nav link underline animation */
    .nav-link {
      position: relative;
      font-weight: 400;
      letter-spacing: 0.18em;
    }
    .nav-link::after {
      content: '';
      position: absolute;
      left: 0; bottom: -2px;
      width: 0; height: 1px;
      background: #1a1a1a;
      transition: width 0.35s ease;
    }
    .nav-link:hover::after,
    .nav-link.active::after { width: 100%; }

    /* Artist name display */
    .artist-name {
      font-family: 'Playfair Display', Georgia, serif;
      font-size: 1.35rem;
      font-style: italic;
      font-weight: 500;
      line-height: 1.25;
      letter-spacing: 0.01em;
    }

    /* Section heading */
    .section-heading {
      font-family: 'Playfair Display', Georgia, serif;
      font-style: italic;
      font-weight: 400;
      letter-spacing: -0.01em;
      line-height: 1.1;
    }

    /* Section fade-in */
    .section { display: none; }
    .section.active { display: block; }

    /* Overlay caption */
    .caption-overlay {
      opacity: 0;
      transition: opacity 0.3s ease;
    }
    .masonry-item:hover .caption-overlay { opacity: 1; }

    /* ── Skeleton loader ── */
    .img-skeleton {
      background: linear-gradient(
        90deg,
        #f2f2f2 0%,
        #ebebeb 40%,
        #f2f2f2 100%
      );
      background-size: 200% 100%;
      animation: skeleton-shimmer 1.6s ease-in-out infinite;
    }
    .img-skeleton.img-done {
      background: #f9f9f9;
      animation: none;
    }
    @keyframes skeleton-shimmer {
      0%   { background-position:  200% 0; }
      100% { background-position: -200% 0; }
    }

    /* Image hidden until loaded — opacity controlled via JS */
    .img-loading {
      opacity: 0 !important;
    }

    /* ── Lightbox ── */
    #lightbox {
      position: fixed;
      inset: 0;
      z-index: 1000;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 2rem;
      background: rgba(255, 255, 255, 0.97);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);

      /* hidden state */
      visibility: hidden;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.32s ease, visibility 0.32s ease;
    }
    #lightbox.lb-open {
      visibility: visible;
      opacity: 1;
      pointer-events: auto;
    }

    /* Image wrapper — scales in on open */
    #lb-inner {
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      max-width: 100%;
      max-height: calc(100vh - 8rem);
      transform: scale(0.95);
      transition: transform 0.32s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    }
    #lightbox.lb-open #lb-inner { transform: scale(1); }

    #lb-img {
      display: block;
      max-width: 100%;
      max-height: calc(100vh - 8rem);
      width: auto;
      height: auto;
      object-fit: contain;
      opacity: 0;
      transition: opacity 0.25s ease;
    }
    #lb-img.lb-loaded { opacity: 1; }

    /* Spinner */
    #lb-spinner {
      position: absolute;
      inset: 0;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    #lb-spinner::after {
      content: '';
      width: 28px; height: 28px;
      border: 1.5px solid #d4d4d4;
      border-top-color: #1a1a1a;
      border-radius: 50%;
      animation: lb-spin 0.7s linear infinite;
    }
    #lb-spinner.lb-hide { display: none; }
    @keyframes lb-spin { to { transform: rotate(360deg); } }

    /* Close button */
    #lb-close {
      position: absolute;
      top: 1.75rem; right: 2rem;
      width: 2.5rem; height: 2.5rem;
      display: flex; align-items: center; justify-content: center;
      font-size: 1.6rem;
      font-weight: 300;
      color: #9a9a9a;
      background: none; border: none;
      cursor: pointer;
      line-height: 1;
      transition: color 0.2s ease, transform 0.2s ease;
    }
    #lb-close:hover { color: #1a1a1a; transform: rotate(90deg); }

    /* Prev / Next */
    .lb-nav {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      width: 2.75rem; height: 2.75rem;
      display: flex; align-items: center; justify-content: center;
      background: none; border: none;
      color: #c0c0c0;
      cursor: pointer;
      font-size: 1.25rem;
      transition: color 0.2s ease, transform 0.2s ease;
    }
    #lb-prev { left: 1.25rem; }
    #lb-next { right: 1.25rem; }
    .lb-nav:hover { color: #1a1a1a; }
    #lb-prev:hover { transform: translateY(-50%) translateX(-3px); }
    #lb-next:hover { transform: translateY(-50%) translateX(3px); }

    /* Caption */
    #lb-caption {
      position: absolute;
      bottom: 2rem;
      left: 50%; transform: translateX(-50%);
      text-align: center;
      white-space: nowrap;
      pointer-events: none;
    }
    #lb-title {
      font-family: 'Playfair Display', Georgia, serif;
      font-style: italic;
      font-size: 0.9rem;
      color: #1a1a1a;
      letter-spacing: 0.01em;
    }
    #lb-meta {
      font-family: 'Inter', sans-serif;
      font-size: 0.65rem;
      font-weight: 300;
      color: #9a9a9a;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      margin-top: 0.4rem;
    }

    /* Counter badge */
    #lb-counter {
      position: absolute;
      top: 1.9rem;
      left: 50%; transform: translateX(-50%);
      font-family: 'Inter', sans-serif;
      font-size: 0.65rem;
      font-weight: 300;
      letter-spacing: 0.16em;
      color: #b0b0b0;
      text-transform: uppercase;
    }
  </style>
</head>
<body class="bg-white text-ink font-sans antialiased">

  <!-- Mobile top bar -->
  <header class="md:hidden flex items-center justify-between px-7 py-6 border-b border-gray-100">
    <span class="artist-name">Elena Voss</span>
    <button id="mobile-menu-btn" class="text-muted hover:text-ink transition-colors" aria-label="Menu">
      <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24">
        <path stroke-linecap="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"/>
      </svg>
    </button>
  </header>

  <!-- Mobile nav drawer -->
  <div id="mobile-nav" class="md:hidden hidden bg-white border-b border-gray-100 px-7 py-6">
    <nav class="flex flex-col space-y-5 text-[11px] tracking-superwide uppercase text-muted font-sans">
      <a href="#" class="nav-link mobile-nav-link active" data-section="works">Works</a>
      <a href="#" class="nav-link mobile-nav-link" data-section="about">About</a>
      <a href="#" class="nav-link mobile-nav-link" data-section="contact">Contact</a>
    </nav>
  </div>

  <div class="flex min-h-screen">

    <!-- ─── Sidebar ─── -->
    <aside class="hidden md:flex flex-col fixed left-0 top-0 h-full w-64 px-12 py-16 border-r border-gray-100 z-10 bg-white">

      <!-- Name / Logo -->
      <div class="mb-20">
        <p class="artist-name">Elena Voss</p>
        <p class="text-[10px] tracking-superwide text-muted uppercase mt-3 font-sans">Painter</p>
      </div>

      <!-- Navigation -->
      <nav class="flex flex-col space-y-7">
        <a href="#" class="nav-link text-[11px] tracking-superwide uppercase text-muted hover:text-ink transition-colors duration-300 active font-sans" data-section="works">Works</a>
        <a href="#" class="nav-link text-[11px] tracking-superwide uppercase text-muted hover:text-ink transition-colors duration-300 font-sans" data-section="about">About</a>
        <a href="#" class="nav-link text-[11px] tracking-superwide uppercase text-muted hover:text-ink transition-colors duration-300 font-sans" data-section="contact">Contact</a>
      </nav>

      <!-- Footer info -->
      <div class="mt-auto">
        <p class="text-[11px] text-muted leading-7 font-sans font-light">
          Based in Vienna<br />
          Available for commissions
        </p>
        <div class="flex space-x-5 mt-6">
          <a href="#" class="text-[10px] tracking-widest uppercase text-muted hover:text-ink transition-colors font-sans">IG</a>
          <a href="#" class="text-[10px] tracking-widest uppercase text-muted hover:text-ink transition-colors font-sans">TW</a>
          <a href="#" class="text-[10px] tracking-widest uppercase text-muted hover:text-ink transition-colors font-sans">CV</a>
        </div>
      </div>
    </aside>

    <!-- ─── Main Content ─── -->
    <main class="w-full md:ml-64 px-8 md:px-16 lg:px-24 py-14 md:py-20">

      <!-- ── Works Section ── -->
      <section id="works" class="section active">
        <div class="flex items-baseline justify-between mb-14">
          <h2 class="section-heading text-4xl md:text-5xl">Selected Works</h2>
          <span class="text-[10px] text-muted tracking-superwide uppercase font-sans hidden sm:block">2019 — 2024</span>
        </div>

        <div class="masonry" id="gallery"></div>
      </section>

      <!-- ── About Section ── -->
      <section id="about" class="section">

        <!-- Two-column grid: image | content -->
        <div class="grid grid-cols-1 lg:grid-cols-[280px_1fr] xl:grid-cols-[320px_1fr] gap-12 lg:gap-20 xl:gap-28">

          <!-- ── Left: Portrait column (sticky on desktop) ── -->
          <div class="lg:sticky lg:top-16 lg:self-start">

            <!-- Portrait -->
            <div class="overflow-hidden">
              <img
                src="https://picsum.photos/seed/portrait/480/600"
                alt="Elena Voss portrait"
                class="w-full grayscale block"
                style="transition: filter 0.6s ease;"
                onmouseenter="this.style.filter='grayscale(0)'"
                onmouseleave="this.style.filter='grayscale(1)'"
              />
            </div>

            <!-- Caption below portrait -->
            <div class="mt-6 pl-px border-l-2 border-gray-200 space-y-1">
              <p class="font-serif italic text-base text-ink">Elena Voss</p>
              <p class="text-[10px] tracking-superwide uppercase text-muted font-sans">b. 1992, Vienna</p>
            </div>

            <!-- Pull quote -->
            <blockquote class="mt-10 relative">
              <span class="absolute -top-3 -left-1 font-serif text-5xl text-gray-200 leading-none select-none">&ldquo;</span>
              <p class="font-serif italic text-sm leading-8 text-ink/60 pl-4 pt-3">
                Painting is the act of paying attention — slowly, completely, until something becomes visible.
              </p>
            </blockquote>

          </div>

          <!-- ── Right: Content column ── -->
          <div class="min-w-0">

            <!-- Heading -->
            <h2 class="section-heading text-4xl md:text-5xl mb-12">About</h2>

            <!-- Bio -->
            <div class="space-y-7 text-sm leading-9 text-ink/70 font-light font-sans max-w-xl">
              <p>
                Elena Voss is a Vienna-based painter working primarily in oil and watercolour.
                Her practice investigates the thresholds between the observed and the remembered —
                light falling across ordinary interiors, figures caught mid-gesture, landscapes
                reduced to essential mark and tone.
              </p>
              <p>
                Her work has been exhibited across Europe and is held in private collections
                in Austria, Germany, and the United Kingdom. She graduated from the Academy
                of Fine Arts Vienna in 2017, where she studied under Professor Karin Huber.
              </p>
              <p>
                She is currently working on a new body of work exploring coastal topographies
                and the language of erasure, with a solo exhibition planned for autumn 2025
                at Galerie Meyer, Vienna.
              </p>
            </div>

            <!-- ── Selected Exhibitions ── -->
            <div class="mt-14 pt-12 border-t border-gray-100">
              <h3 class="text-[10px] tracking-superwide uppercase text-muted mb-8 font-sans">Selected Exhibitions</h3>
              <ul class="font-sans font-light text-ink/70 divide-y divide-gray-100">
                <li class="flex items-baseline justify-between py-4 gap-6">
                  <div>
                    <span class="text-sm">Group Show</span>
                    <span class="text-muted text-sm"> — Galerie Krinzinger, Vienna</span>
                  </div>
                  <span class="text-[11px] text-muted tracking-widest shrink-0">2024</span>
                </li>
                <li class="flex items-baseline justify-between py-4 gap-6">
                  <div>
                    <span class="text-sm">Solo Exhibition</span>
                    <span class="text-muted text-sm"> — The White Room, Berlin</span>
                  </div>
                  <span class="text-[11px] text-muted tracking-widest shrink-0">2023</span>
                </li>
                <li class="flex items-baseline justify-between py-4 gap-6">
                  <div>
                    <span class="text-sm">Juried Exhibition</span>
                    <span class="text-muted text-sm"> — Kunsthalle Wien</span>
                  </div>
                  <span class="text-[11px] text-muted tracking-widest shrink-0">2022</span>
                </li>
                <li class="flex items-baseline justify-between py-4 gap-6">
                  <div>
                    <span class="text-sm">Group Show</span>
                    <span class="text-muted text-sm"> — Platform Projects, London</span>
                  </div>
                  <span class="text-[11px] text-muted tracking-widest shrink-0">2021</span>
                </li>
                <li class="flex items-baseline justify-between py-4 gap-6">
                  <div>
                    <span class="text-sm">Graduate Exhibition</span>
                    <span class="text-muted text-sm"> — Academy of Fine Arts Vienna</span>
                  </div>
                  <span class="text-[11px] text-muted tracking-widest shrink-0">2017</span>
                </li>
              </ul>
            </div>

            <!-- ── Books & Publications ── -->
            <div class="mt-14 pt-12 border-t border-gray-100">
              <h3 class="text-[10px] tracking-superwide uppercase text-muted mb-8 font-sans">Books &amp; Publications</h3>

              <ul class="space-y-0 divide-y divide-gray-100">

                <li class="py-6 flex gap-5">
                  <div class="shrink-0 w-8 text-[10px] text-muted font-sans tracking-widest pt-1">2023</div>
                  <div>
                    <p class="font-serif italic text-base text-ink leading-snug">Light and Threshold</p>
                    <p class="text-[11px] text-muted font-sans mt-1 tracking-wide">Hatje Cantz Verlag — Monograph, 128 pp.</p>
                    <p class="text-xs text-ink/60 font-sans font-light mt-2 leading-7 max-w-sm">
                      A comprehensive survey of works from 2018–2023, with an essay by curator Mia Sander and a foreword by the artist.
                    </p>
                  </div>
                </li>

                <li class="py-6 flex gap-5">
                  <div class="shrink-0 w-8 text-[10px] text-muted font-sans tracking-widest pt-1">2022</div>
                  <div>
                    <p class="font-serif italic text-base text-ink leading-snug">Painters of Now, Vol. IV</p>
                    <p class="text-[11px] text-muted font-sans mt-1 tracking-wide">Phaidon Press — Group Publication, 320 pp.</p>
                    <p class="text-xs text-ink/60 font-sans font-light mt-2 leading-7 max-w-sm">
                      Featured alongside twelve contemporary painters selected for their contribution to representational painting.
                    </p>
                  </div>
                </li>

                <li class="py-6 flex gap-5">
                  <div class="shrink-0 w-8 text-[10px] text-muted font-sans tracking-widest pt-1">2021</div>
                  <div>
                    <p class="font-serif italic text-base text-ink leading-snug">Vienna Contemporary</p>
                    <p class="text-[11px] text-muted font-sans mt-1 tracking-wide">Kehrer Verlag — Exhibition Catalogue, 96 pp.</p>
                    <p class="text-xs text-ink/60 font-sans font-light mt-2 leading-7 max-w-sm">
                      Official catalogue for the Kunsthalle Wien juried exhibition. Text by Franziska Hofer.
                    </p>
                  </div>
                </li>

                <li class="py-6 flex gap-5">
                  <div class="shrink-0 w-8 text-[10px] text-muted font-sans tracking-widest pt-1">2019</div>
                  <div>
                    <p class="font-serif italic text-base text-ink leading-snug">Interior Studies</p>
                    <p class="text-[11px] text-muted font-sans mt-1 tracking-wide">Self-published — Artist Book, limited ed. 200</p>
                    <p class="text-xs text-ink/60 font-sans font-light mt-2 leading-7 max-w-sm">
                      Hand-bound artist book of drawings and notes produced during a three-month residency in Lisbon.
                    </p>
                  </div>
                </li>

              </ul>
            </div>

          </div><!-- /right column -->
        </div><!-- /grid -->
      </section>

      <!-- ── Contact Section ── -->
      <section id="contact" class="section max-w-md">
        <h2 class="section-heading text-4xl md:text-5xl mb-14">Contact</h2>

        <div class="mb-14 text-sm font-light font-sans text-ink/70 leading-9">
          <p>
            For studio visits, commission inquiries, or exhibition proposals,
            please reach out by email. Response within three to five working days.
          </p>
        </div>

        <div class="space-y-0 text-sm mb-16 font-sans">
          <div class="flex items-start gap-8 border-b border-gray-100 py-5">
            <span class="text-[10px] text-muted uppercase tracking-superwide w-20 pt-0.5 shrink-0">Email</span>
            <a href="mailto:studio@elenavoss.com" class="font-light hover:text-muted transition-colors">studio@elenavoss.com</a>
          </div>
          <div class="flex items-start gap-8 border-b border-gray-100 py-5">
            <span class="text-[10px] text-muted uppercase tracking-superwide w-20 pt-0.5 shrink-0">Studio</span>
            <span class="font-light">Praterstraße 14, 1020 Vienna</span>
          </div>
          <div class="flex items-start gap-8 border-b border-gray-100 py-5">
            <span class="text-[10px] text-muted uppercase tracking-superwide w-20 pt-0.5 shrink-0">Instagram</span>
            <a href="#" class="font-light hover:text-muted transition-colors">@elenavoss.studio</a>
          </div>
        </div>

        <!-- Minimal contact form -->
        <form class="space-y-10 font-sans" onsubmit="return false;">
          <div>
            <label class="block text-[10px] tracking-superwide uppercase text-muted mb-3">Name</label>
            <input type="text" placeholder="Your name"
              class="w-full border-b border-gray-200 py-3 text-sm font-light placeholder-gray-300
                     focus:outline-none focus:border-ink transition-colors bg-transparent" />
          </div>
          <div>
            <label class="block text-[10px] tracking-superwide uppercase text-muted mb-3">Email</label>
            <input type="email" placeholder="your@email.com"
              class="w-full border-b border-gray-200 py-3 text-sm font-light placeholder-gray-300
                     focus:outline-none focus:border-ink transition-colors bg-transparent" />
          </div>
          <div>
            <label class="block text-[10px] tracking-superwide uppercase text-muted mb-3">Message</label>
            <textarea rows="5" placeholder="Write your message…"
              class="w-full border-b border-gray-200 py-3 text-sm font-light placeholder-gray-300
                     focus:outline-none focus:border-ink transition-colors bg-transparent resize-none"></textarea>
          </div>
          <button type="submit"
            class="text-[10px] tracking-superwide uppercase border border-ink px-8 py-4
                   hover:bg-ink hover:text-white transition-colors duration-300">
            Send message
          </button>
        </form>
      </section>

    </main>
  </div>

  <!-- ─── Lightbox ─── -->
  <div id="lightbox" role="dialog" aria-modal="true" aria-label="Image viewer">

    <!-- Close -->
    <button id="lb-close" aria-label="Close">&times;</button>

    <!-- Counter -->
    <span id="lb-counter"></span>

    <!-- Prev / Next -->
    <button id="lb-prev" class="lb-nav" aria-label="Previous">
      <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.25" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="15 18 9 12 15 6"/>
      </svg>
    </button>
    <button id="lb-next" class="lb-nav" aria-label="Next">
      <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.25" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="9 18 15 12 9 6"/>
      </svg>
    </button>

    <!-- Image -->
    <div id="lb-inner">
      <div id="lb-spinner"></div>
      <img id="lb-img" src="" alt="" />
    </div>

    <!-- Caption -->
    <div id="lb-caption">
      <p id="lb-title"></p>
      <p id="lb-meta"></p>
    </div>

  </div>

<script>
  // ─────────────────────────────────────────
  // Resim veritabanı — buraya yeni eser ekle
  // ─────────────────────────────────────────
  const paintings = [
    {
      seed   : 'paint1',
      width  : 600,
      height : 780,
      title  : 'Untitled No. 1',
      medium : 'Oil on canvas',
      year   : 2023,
    },
    {
      seed   : 'paint2',
      width  : 600,
      height : 420,
      title  : 'Study in Blue',
      medium : 'Acrylic',
      year   : 2022,
    },
    {
      seed   : 'paint3',
      width  : 600,
      height : 700,
      title  : 'Garden Hour',
      medium : 'Watercolour',
      year   : 2022,
    },
    {
      seed   : 'paint4',
      width  : 600,
      height : 500,
      title  : 'Interior Light',
      medium : 'Oil on linen',
      year   : 2021,
    },
    {
      seed   : 'paint5',
      width  : 600,
      height : 880,
      title  : 'Dusk Figures',
      medium : 'Oil on canvas',
      year   : 2021,
    },
    {
      seed   : 'paint6',
      width  : 600,
      height : 460,
      title  : 'Fragment III',
      medium : 'Mixed media',
      year   : 2020,
    },
    {
      seed   : 'paint7',
      width  : 600,
      height : 600,
      title  : 'Still Morning',
      medium : 'Watercolour',
      year   : 2020,
    },
    {
      seed   : 'paint8',
      width  : 600,
      height : 740,
      title  : 'Periphery',
      medium : 'Acrylic on paper',
      year   : 2019,
    },
    {
      seed   : 'paint9',
      width  : 600,
      height : 520,
      title  : 'Overcast',
      medium : 'Oil on canvas',
      year   : 2019,
    },
  ];

  // ── Galeriyi diziden otomatik oluştur ──
  function renderGallery() {
    const grid = document.getElementById('gallery');
    grid.innerHTML = '';

    paintings.forEach((p, index) => {
      const src     = `https://picsum.photos/seed/${p.seed}/${p.width}/${p.height}`;
      const caption = `${p.medium}, ${p.year}`;

      const item = document.createElement('div');
      item.className = 'masonry-item group cursor-pointer';
      item.innerHTML = `
        <div
          class="img-skeleton relative overflow-hidden"
          style="aspect-ratio: ${p.width} / ${p.height};"
        >
          <img
            src="${src}"
            alt="${p.title}"
            loading="lazy"
            class="img-loading absolute inset-0 w-full h-full object-cover"
          />
          <div class="caption-overlay absolute inset-0 flex flex-col justify-end p-5 bg-gradient-to-t from-black/35 to-transparent">
            <p class="text-white font-serif italic text-base leading-snug">${p.title}</p>
            <p class="text-white/65 text-[10px] tracking-widest uppercase font-sans mt-1">${caption}</p>
          </div>
        </div>`;

      // Reveal image and stop shimmer once loaded
      const imgEl     = item.querySelector('img');
      const wrapperEl = item.querySelector('.img-skeleton');

      function onImageReady() {
        imgEl.classList.remove('img-loading');
        wrapperEl.classList.add('img-done');
      }

      if (imgEl.complete && imgEl.naturalHeight !== 0) {
        // Already cached by the browser
        onImageReady();
      } else {
        imgEl.addEventListener('load',  onImageReady);
        imgEl.addEventListener('error', onImageReady); // fail gracefully
      }

      item.addEventListener('click', () => openLightbox(index));
      grid.appendChild(item);
    });
  }

  // ── Section navigation ──
  const allLinks = document.querySelectorAll('[data-section]');
  const allSecs  = document.querySelectorAll('.section');

  function showSection(id) {
    allSecs.forEach(s => s.classList.remove('active'));
    allLinks.forEach(l => l.classList.remove('active', 'text-ink'));

    const target = document.getElementById(id);
    if (target) target.classList.add('active');

    allLinks.forEach(l => {
      if (l.dataset.section === id) l.classList.add('active', 'text-ink');
    });
  }

  allLinks.forEach(link => {
    link.addEventListener('click', e => {
      e.preventDefault();
      showSection(link.dataset.section);
      document.getElementById('mobile-nav').classList.add('hidden');
    });
  });

  // ── Mobile menu toggle ──
  document.getElementById('mobile-menu-btn').addEventListener('click', () => {
    document.getElementById('mobile-nav').classList.toggle('hidden');
  });

  // ════════════════════════════════════════
  //  Lightbox — sıfırdan, kütüphanesiz
  // ════════════════════════════════════════
  const lb         = document.getElementById('lightbox');
  const lbImg      = document.getElementById('lb-img');
  const lbSpinner  = document.getElementById('lb-spinner');
  const lbTitle    = document.getElementById('lb-title');
  const lbMeta     = document.getElementById('lb-meta');
  const lbCounter  = document.getElementById('lb-counter');

  let currentIndex = 0;

  function openLightbox(index) {
    currentIndex = index;
    loadImage(index);
    lb.classList.add('lb-open');
    document.body.style.overflow = 'hidden';
    document.getElementById('lb-close').focus();
  }

  function closeLightbox() {
    lb.classList.remove('lb-open');
    document.body.style.overflow = '';
    // reset image so spinner shows fresh on next open
    lbImg.classList.remove('lb-loaded');
    lbImg.src = '';
  }

  function navigate(dir) {
    currentIndex = (currentIndex + dir + paintings.length) % paintings.length;
    loadImage(currentIndex);
  }

  function loadImage(index) {
    const p       = paintings[index];
    const src     = `https://picsum.photos/seed/${p.seed}/${p.width}/${p.height}`;
    const caption = `${p.medium}, ${p.year}`;

    // Show spinner, hide image
    lbImg.classList.remove('lb-loaded');
    lbSpinner.classList.remove('lb-hide');

    lbTitle.textContent   = p.title;
    lbMeta.textContent    = caption;
    lbCounter.textContent = `${index + 1} / ${paintings.length}`;

    // Load into a temp element to detect completion
    const tmp = new Image();
    tmp.onload = () => {
      lbImg.src = src;
      lbImg.alt = p.title;
      lbSpinner.classList.add('lb-hide');
      lbImg.classList.add('lb-loaded');
    };
    tmp.onerror = () => {
      lbSpinner.classList.add('lb-hide');
    };
    tmp.src = src;
  }

  // Controls
  document.getElementById('lb-close').addEventListener('click', closeLightbox);
  document.getElementById('lb-prev').addEventListener('click', () => navigate(-1));
  document.getElementById('lb-next').addEventListener('click', () => navigate(1));

  // Click backdrop (not inner image) to close
  lb.addEventListener('click', e => {
    if (e.target === lb) closeLightbox();
  });

  // Keyboard: Esc closes, arrows navigate
  document.addEventListener('keydown', e => {
    if (!lb.classList.contains('lb-open')) return;
    if (e.key === 'Escape')     closeLightbox();
    if (e.key === 'ArrowLeft')  navigate(-1);
    if (e.key === 'ArrowRight') navigate(1);
  });

  // ── Başlat ──
  renderGallery();
</script>
</body>
</html>
