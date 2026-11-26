# Viral References & Growth Playbook (2025–2026)

> **Machine-Readable Spec:** [data/viral_references_20.json](file:///c:/Users/loren/OneDrive/Desktop/KDP_Automated_Agency/data/viral_references_20.json)  
> **Scope:** Actionable transformation blueprint for **LB Editorial** (`IT` & `EN`) connecting 2025–2026 platform algorithms, 32 live-observed puzzle/book references, and our local performance audit directly to templates, captions, scheduling, and storefront conversion.

---

## 1. Executive Diagnosis: Why Views Collapsed (-92%)

Local telemetry ([social_performance_report.json](file:///c:/Users/loren/OneDrive/Desktop/KDP_Automated_Agency/data/social_performance_report.json), [social_accounts.json](file:///c:/Users/loren/OneDrive/Desktop/KDP_Automated_Agency/data/social_accounts.json), and live account checks) isolates five exact causes behind the stall:

| Channel | Historical Baseline | Recent Collapse / Blocker | Root Cause Diagnosed |
| :--- | :--- | :--- | :--- |
| **IG IT** (`@lb.mente.e.logica`) | 4 followers, 132 posts; old quiz Reels **112–197 views**, **3.5–6.4s** watch time | Nov 23+ Cinema Promo Templates collapsed **-92%** to **0–13 views**, **0.9–2.5s** watch time, **0 shares, 0 saves** | Zero Frame-0 playable hook; dark/strobing AI-promo intros cause >70% immediate swipe-away before 1.5s |
| **IG EN** (`@lb.satisfyinglogic`) | 8 followers, 167 posts; last quiz got **21 likes** | Recent Cinema promos get **0–1 likes** | Missing voiceover + no pause/solve payoff + raw URLs & 16+ tags in caption |
| **YT IT** (`@lb.menteelogica`) | Avg **516 views/Short** (peak **1,155** on `XdDtSEJbiqA` & `BWJak4gKyZs` `dare_challenge` quiz) | Froze **Nov 2** (`invalid_grant` OAuth token expiry) | OAuth consent screen / refresh token drift in `.env` vs `social_accounts.json` |
| **YT EN** (`@lb.satisfynglogic`) | `dare_challenge` averaged **339.9 views** globally vs **18.8–86.5** on passive angles | Froze **Oct 29** (`invalid_grant`); handle contains typo (`satisfyng`) | Expired token + broken handle branding + passive `adhd_focus`/`screen_detox` intros |
| **FB IT / EN** | 0 fans | **0 API views**, **0 likes** | Raw `https://www.amazon...` URLs inside Reel captions triggered Meta outbound-link reach suppression |
| **TikTok** | Disabled | Not publishing | No active OAuth token in `social_accounts.json` |

### Five Fatal Anti-Patterns Eliminated by This Playbook
1. **No Frame-0 Hook (`0.0–1.5s`):** Starting with floating 3D covers, white flashes, or unreadable 133ms strobing frames guarantees 0.9–2.5s watch time and fails both IG 3s Hold (`>=45%`) and YT VVSA (`>=70%`).
2. **Caption & Hashtag Penalties:** Using `#kdp`, 15–17 hashtags (exceeding Instagram's **3–5** hashtag cap), and raw Amazon URLs inside IG/FB captions destroys non-follower recommendation eligibility.
3. **Overposting Cannibalization (`SLEEP_HOURS = 4.5`):** Posting 5–6 times/day every 4.5h suppresses per-post reach by **-31% to -35%** (Metricool 2025–2026 study) and trips YouTube's **July 15, 2025 Inauthentic Content** filter.
4. **Audience & Book Contamination:** Unpublished/ASIN-less books, deactivated `B0HNLWQ5CK`, and adult `"Tired of doomscrolling?"` copy applied to kids books (`B0GV339NJW`, `B0GVF8HGMC`, `B0HP8VR7N6`) repel both parents and adult buyers.
5. **Pricing & Visual Credibility Leaks:** `.99`/`.98` endings read as low-effort AI spam, while pure EN books (`B0HPBYGHHH`) carried stray Italian badges (`"Adulti • Logica"`) in the storefront.

---

## 2. 2025–2026 Algorithmic Lawbook

### Instagram (Adam Mosseri Ranking Signals)
- **Primary Ranking Trinity:** `Watch Time` + `Sends per Reach` (DM shares) + `Likes per Reach`.
- **Sends-per-Reach Multiplier:** `1–2%` baseline, `3–4%` strong distribution, **`>= 5%` viral non-follower explosion**. Sends outrank public comments for Explore & Reels discovery.
- **Watch Time & 3s Skip Reality:** `60–66%` of viewers drop within 3s across IG (`~65.5%` on accounts <5k). Target **`>= 45%` 3-second hold** and **`>= 8.5s` average watch time** (optimal loopable challenge runtime: **18–26s**).
- **Trial Reels (`SS_PERFORMANCE`):** Publish cold-first (`95–100%` non-follower sandbox for 24–72h). Benchmark: **`>30%` completion on 15–30s**, **`5–10` follows per 1,000 Trial views**. Graduate winners automatically via `graduation_strategy: "SS_PERFORMANCE"`.
- **4:5 Carousels (`1080x1350`):** Median ER by reach **6.9%** (~2.09x Reels' ~3.3%) and up to **9x more saves** than single images. Mix **65–75% Reels + 25–35% 4:5 Carousels**.
- **Caption & Link Rule:** Max **3–5** niche hashtags; front-load SEO keywords inside the first **125 characters**; **ZERO raw URLs** in IG captions (non-clickable & anti-discovery).

### YouTube Shorts (VVSA, AVD & July 2025 Originality Policy)
- **VVSA (Viewed vs. Swiped Away):** `<30%` stalls immediately; `50%` is average; **`>= 70%` Viewed** triggers viral Shorts feed expansion.
- **AVD (Average View Duration):** Target **`>= 100%` APV** via seamless loop endings and "pause-to-solve" / "rewatch-to-verify" puzzles.
- **July 15, 2025 "Inauthentic Content" Policy:** Repetitive, mass-templated slideshows without original human/voice value-add lose reach & monetization eligibility. **Every Short MUST carry distinct `edge-tts` narration + varied algorithmic grids from our deterministic math engine.**
- **Non-Clickable Links Policy:** Links in Shorts descriptions & pinned comments are **not clickable**. Route Shorts viewers via **Related Video** (linked to a long-form showcase/catalog video with clickable description links), **Channel Profile links**, and **YouTube Shopping product tags**.

### Facebook Reels
- **Caption Outbound-Link Penalty:** External URLs in FB Reel captions severely throttle unconnected reach.
- **Compliant Pattern:** Put **0 raw URLs** in `fb_caption`; state *"Link in first comment"* / *"Link nel primo commento"* and immediately auto-post `fb_first_comment` containing the Amazon URL via Graph API `v22.0/{video_id}/comments`.

### Cadence & Comment-to-DM Funnels
- **Metricool & Sprout Social:** Sustainable IG rhythm is **3–5 feed pieces/week** per account (e.g., 3 Reels + 1–2 Carousels) and **5–7 YouTube Shorts/week** (`SLEEP_HOURS = 24.0` default).
- **Peak Windows (UTC):**
  - **IT (`CET`):** `17:30 UTC` (`18:30 CET` evening unwind peak; secondary lunch window `11:30 UTC`) `± 18 min` jitter.
  - **EN (`EST`):** `23:00 UTC` (`18:00 EST` afternoon/evening US commute & unwind peak) `± 18 min` jitter.
- **ManyChat Comment-to-DM Funnel:** **95–99%** delivery, **80–90%** DM open rate, **25–45%** DM CTR, **15–35%** cold-to-lead conversion (**12x higher than Link-in-Bio**), plus **+30–40%** organic impression boost from comment velocity (watch Meta's **750–1,000 DM/hr** rate cap).

---

## 3. Synthesis of the 32 Live Viral References

All 32 references are stored with full URLs and structured telemetry in [data/viral_references_20.json](file:///c:/Users/loren/OneDrive/Desktop/KDP_Automated_Agency/data/viral_references_20.json).

### Bucket 1 — Viral Puzzle & Riddle Shorts (13 References)
| Creator / Ref | Observed Scale | Winning 0–2s Hook & Loop Mechanism | Direct Application to LB Editorial |
| :--- | :--- | :--- | :--- |
| **Puzzle guy** (`@Puzzleguy`) | **84.9M** views, 3.17M likes (0:51) | Overhead tactile physical puzzle + immediate *"impossible"* premise; Amazon link in description | Tactile hand/paper realism + clear physical product CTA |
| **Luke Davidson** (`@lukedavidson81`) | **81.5M** views (0:20) | Zero-intro spoken riddle on Frame 0; tight 20s runtime pushes AVD >100% | **Target 18–26s runtime**, Frame-0 spoken `edge-tts` hook |
| **Sara's logic** (`@Saraslogic`) | **31.05M** views (0:10), **38 Shopping tags** | Crisp white paper hand-lettered path visible at 0.0s; works 100% muted | **Editorial Ivory Paper (`#FBF8F1`)**, zero-mute comprehension |
| **Hope Atiba** | **27M** views | *"Can You Spot the Mistake? Challenge in 5 Seconds"* + comment race CTA | **Template 6 (`spot_the_mistake`)** core mechanic |
| **The Ezz Show** (`@TheEzzShow`) | **18.7M** views (IT/Multi, 1:00) | *"3 divertenti rompicapo"* — 3-round escalating retention arc | **Template 5 (`editorial_3tier_challenge`)** IT & EN structure |
| **Andy Math** (`@AndyMath`) | **18.2M** views (1:00) | Clear deduction breakdown + direct product link in description line 1 | **Template 7 (`micro_tutorial_save`)** + YT desc line 1 URL |
| **The Flom Family** (`@Flomfamily`) | **11.48M** & **5.2M** views (IT/EN) | Ego filter + clock (*"Un genio può risolvere in 10 secondi!"*) | Localized IT ego + countdown pressure bar |
| **MindYourLogic Shorts** (`@MindYourLogic.Shorts`) | **10.58M** & **9.37M** views (0:31) | Single-rule constraint `<2s` (*"Move 1..."*) + comment answer debate | Ambiguity/speed debate prompts that keep Shorts looping |
| **BRIGHT SIDE** (`@BRIGHTSIDEOFFICIAL`) | **10M** views (328K likes) | Participatory optical/detective alibi clues forcing watch-to-end | Multi-clue escalation before answer reveal |
| **Icycol** (`@icycol`) | **8.27M** views (IT, 0:54) | *"L'ENIGMA PIÙ DIFFICILE DEL MONDO!!"* | Validates massive IT Short demand for `enigmistica` & `enigmi` |
| **Cracking The Cryptic** (`@CrackingTheCryptic`) | **2.40M** views (40.1K likes, 0:59) | Clean Sudoku grid + *"The X-Wing"* technique -> 2–4x rewatches + Shopping tag | **Template 7** Sudoku/Nonogram/Cryptogram deduction tricks |
| **MindYourDecisions** (`@MindYourDecisions`) | 3.28M subs, 716M views | Instant high-contrast math trap sparking comment debates | Red-ink error breakdown & comment verification loop |
| **IL LATO POSITIVO** (`@IL_LATO_POSITIVO`) | 3.03M subs, 1.1B views | Timed Italian logic riddles (*"Solo l'1%..."*) | IT voiceover pacing & timed countdown structure |

### Bucket 2 — Physical Puzzle Book Organic Promos (9 References)
- **Tutorial = Viral Saves (`chloe @chlolineberg`):** Murdle cover + grid tutorial hit **14K likes, 5,636 saves (40.3% save-to-like!), 1,130 shares**, converting via *"linked in my storefront!"* -> Blueprint for **Template 7** & **4:5 Carousels**.
- **Onboarding Co-Solve (`@julianaschuyler`, `@awleariwle`):** Serialized *"Level 1/2/3"* & *"Welcome to Murdle 101"* walkthroughs remove buyer fear of difficult grids.
- **Anti-Screen Identity (`@ancsibiro11`, `@colorful.wendy`, Offline Hobbies / `#analogbag` EN & IT):** *"30 min evening brainstacking"*, *"The Puzzle Book That's Replacing My Phone"*, *"Facciamo un Murdle insieme!"* convert adult wellness audiences **only** when kept strictly on adult SKUs (`B0HPBYGHHH`, `B0HNPC6XF2`).
- **Tactile Proof & Kids Separation (`@INDIANMANGO-m4h` 2.49M, `@SunnyBunnies` 431K, Jess Lui 7.8M EN / 6.8M IT):** Crisp physical page spreads + ASMR paper/pencil SFX prove real print quality, while kids promos use joyful, parent-trusted framing—never adult doomscrolling tropes.

### Bucket 3 — Amazon Bestsellers & KDP Storefront Credibility (10 References)
- **Murdle Vol 1 (`1250892317`, BSR #11, 8,092 reviews) & `murdle.com`:** Clean **€10.85** paperback sweet spot, 8-book series identity, daily free playable puzzle funnel.
- **FUNAFTER BOOKS (`B096TW9C82`, BSR #4,403) & DLC PRESS (`B0FH7F9W1N`, BSR #4,555, 9-book series):** Show **real interior puzzle thumbnails**, explicit **`8.5x11 LARGE BOOK - SOLUTIONS INCLUDED!`**, and cohesive author storefront cross-linking.
- **J.D. Kinnest (`1988923182`, BSR #1,743) & Donovan Ellis (`B0B9QM23D3`, BSR #3,153):** Explicit Large Print & cognitive longevity trust markers.
- **Highlights Press (`1684372615`, 4.8★ 6,228) & Lulu Sparkle (`B0G1HJ89V3`, BSR #53,392, 4.8★ 262):** *"Screen Free Activities for CLEVER KIDS 8-12"*, *"Created By Teachers"*, *"Perfect Gift Under $15"*.
- **Amazon.it Leaders (`1474955428` Simon Tudhope & `B0BKMR4PK2` Unicorn Books *"da Facili a Diabolici"*):** Validates Italian appetite for clear progressive difficulty ladders (`Facile -> Medio -> Esperto`) matching `B0HP8VR7N6` (`Età 8–12`).

---

## 4. Mapping to Video Templates (`src/social_engine/promo_templates/`)

### Universal Visual, Audio & Safe-Zone Laws (All Templates `1..7`)
1. **Universal Safe Zone (`1080x1920`, 9:16):** All hooks, grids, badges, prices, and CTAs MUST stay inside **`x: 110..970`, `y: 225..1370`** (`860x1145` px). Keep right-aligned floating elements inside `x <= 930` to avoid YT Shorts/IG Reels icon bars.
2. **Frame-0 Hook (`0.0–1.5s`):** ZERO intro logo, ZERO white-card flash, ZERO fade-in from black. Frame 0 opens directly on crisp typography + playable visual puzzle + immediate `edge-tts` voiceover (`<= 0.08s` trim).
3. **Editorial Paper Palette (Templates 5, 6, 7 & Carousel):**
   - Paper Primary: `#FBF8F1` (Warm Ivory) | Secondary: `#F3ECE0` (Cream Folio) | Shadow: `#E6DCCB`
   - Ink Primary: `#1C1917` (Charcoal Print, `>14:1` contrast) | Secondary: `#44403C` | Muted: `#78716C`
   - Functional Ink Accents: Amber Highlighter `#D97706`, Terracotta `#B45309`, Red Grading Ink `#B91C1C`, Editorial Sage `#2F5D50`, Broadsheet Navy `#1E3A5F`, Foil `#B8860B`.
4. **Broadcast Audio (`audio_synth.py`):** `build_editorial_voice_and_bed(...)` uses `edge-tts` narration with trimmed leading silence, **`-14 dB` bed ducking under voice**, tactile paper/pencil SFX, normalized broadcast loudness (`-14 LUFS`), and graceful offline fallback.
5. **Rule 9 Pricing Hygiene:** Never render `.99` or `.98`. Always display clean sweet-spot pricing (**`$10.80`** / **`€10.80`**) matching `AGENTS.md` Rule 9 (60% KDP royalty tier).

### Template-by-Template Spec
- **Template 5 — `editorial_3tier_challenge` (`21.0s`, Core Viral Engine):**
  - `0.0–1.8s` **Frame-0 Hook:** Safe-zone banner (*"Can you clear all 3 levels?"* / *"Riesci a superare tutti e 3 i livelli?"*) + VO + instant Level 1 preview.
  - `1.8–6.2s` **Level 1 (Easy — 95%+ Win):** Warm highlighter sweep confirms fast dopamine win.
  - `6.2–12.4s` **Level 2 (Medium — Book Proof):** Deterministic puzzle pulled from the real book pool + subtle tension progress bar + reveal.
  - `12.4–18.4s` **Level 3 (Hard — Sends & Debate Trigger):** Hard puzzle/brain-bender + overlay: *"Comment your level & send to a smart friend"* (IT: *"Commenta il tuo livello e sfida un amico!"*).
  - `18.4–21.0s` **Micro-Proof & Seamless Loop (`<=2.6s`):** Real cover + 2 interior pages + `"Comment LOGIC / LOGICA"` + spoken bridge looping cleanly back to Frame 0.
  - *Kids Adaptation (`is_kids=True`):* Strictly uses parent/family framing (*"Try this 3-level screen-free mission with your kids tonight!"*).
- **Template 6 — `spot_the_mistake` (`16.5s`, High-Comment Engine):**
  - `0.0–1.5s`: Algorithmically verified Sudoku/Math/Word grid on `#FBF8F1` paper with **1 deliberate rule-break** + *"Spot the mistake in 8 seconds"*.
  - `1.5–10.5s`: Smooth pencil/loupe scan inviting viewers to pause and comment their row/column pick.
  - `10.5–14.0s`: Crisp **red-ink circle (`#B91C1C`)** + rule verification.
  - `14.0–16.5s`: Real book cover/interior proof + `LOGIC`/`LOGICA` CTA + loop.
- **Template 7 — `micro_tutorial_save` (`22.0s`, 40% Save-to-Like Engine):**
  - Teaches 1 genuine 15s solving trick (Nonogram edge-overlap, Cryptogram letter-frequency, or Logic Grid elimination) using animated graphite pencil marks -> *"Save this trick"* -> `2.5s` real book preview + CTA.
- **Upgraded Templates 1–4 (`20%` Showcase Tier) & `book_loader.py`:**
  - Add immediate Frame-0 safe-zone hook overlay + `edge-tts` VO across ALL four.
  - **T1 (`~16.0s`):** Cut outro to `2.2s` showing real cover + interior proof.
  - **T2 (`~13.0s`):** Remove `0.00s` white-card flash completely; open directly on illuminated 3D cover/page fan; sanitize `.99` prices to `$10.80`.
  - **T3 (`8.0s`) & `book_loader.py`:** Fix audience alignment—NEVER render `"Quit Night Scrolling"` on Kids or Senior books; sanitize price fallback to `10.80`.
  - **T4 (`~14.5s`):** Replace unreadable 4-frame strobe with `1.4s` cover hook -> **`1.8s` pause on each of 2 ultra-legible hero spreads (`"Pause to solve this!"`)** -> crisp kinetic flips -> `2.0s` back/front CTA.
- **IG 4:5 Editorial Carousel (`carousel_generator.py` -> `1080x1350`, 5 PNGs):**
  - **Slide 1 (Hook):** High-contrast warm ivory cover + *"3 Puzzles You Can Solve Off-Screen Tonight"* (or kid/parent equivalent).
  - **Slide 2 (Playable Easy):** Real clean interior puzzle grid (viewers solve on-screen).
  - **Slide 3 (Trick / Deep Proof):** Step-by-step pencil annotation or Level 2 challenge.
  - **Slide 4 (Answer Key & Craft):** Verified solution + 300 DPI / 8.5×11" interior stack proof.
  - **Slide 5 (Storefront & DM CTA):** Cover + 2 interior thumbs + `"Comment LOGIC / LOGICA for sample + Amazon link"`.

---

## 5. Mapping to Captions, Cadence, OAuth & Analytics

### `caption_generator.py` (Zero `#kdp`, Platform-Native Formats)
- **Global Ban:** Permanently purge `#kdp`, `#kdppublishing`, `#lowcontentbooks`, `#selfpublishing`, `#amazonkdp`.
- **Instagram (`ig_caption`):**
  - Line 1 (`<=125` chars): Debate/challenge SEO hook (localized EN/IT & audience-safe).
  - Body: 2-line tactile book benefit + Comment-to-DM trigger (**`LOGIC`** / **`LOGICA`** / **`TRICK`** / **`TRUCCO`**).
  - **ZERO raw `http/https` URLs.**
  - **3–5** (target **4**) niche tags (e.g. `#logicpuzzles #braintraining #puzzlebook #analogbag` or `#rompicapi #enigmistica #giocareconlalogica #libriperragazzi`).
- **Facebook (`fb_caption` + `fb_first_comment`):**
  - `fb_caption`: **ZERO raw URLs**, closes with *"Direct Amazon link in the first comment!"* / *"Link diretto Amazon nel primo commento!"* + **3** tags.
  - `fb_first_comment`: Auto-posted right after Reel upload with direct Amazon ASIN URL + engagement question.
- **YouTube Shorts (`yt_title` + `yt_description`):**
  - `yt_title`: `<= 75` chars, non-repetitive, ends with `#Shorts`.
  - `yt_description`: Direct Amazon URL in **lines 1–3** + concise book summary + **3–4** tags. Bridge traffic via **Related Video** & **Channel Profile links**.
- **TikTok (`tiktok_caption`):** BookTok `#brainstacking` / challenge hook + comment trigger + **3–4** tags, zero URLs.

### `audience_router.py` & `railway_video_worker.py`
- **Strict `get_online_books()` Filter:** Regex `^B0[A-Z0-9]{8}$`, deduplicated slugs/ASINs, hard-excludes ASIN-less folders, deactivated `B0HNLWQ5CK`, and sets `EN_CHANNEL_AUDIENCE=adults` default (`B0HPBYGHHH`, `B0HNPC6XF2`), isolating kids books (`B0GV339NJW`, `B0GVF8HGMC`, `B0HP8VR7N6`) with strict parent/youth framing.
- **80/20 Viral Content Mix (`VIRAL_CONTENT_MIX_ROTATION`):** **80%** interactive viral templates (`5, 6, 7, 5`) + **20%** upgraded showcase (`1, 2, 3, 4`) + weekly IG `4:5` Carousel.
- **Cadence (`SLEEP_HOURS = 24.0`):** Max 1 cycle/day per language aligned to UTC peak windows (`IT ~17:30 UTC`, `EN ~23:00 UTC` `± 18m` jitter).

### `social_publisher.py`, `auth_youtube_channel.py` & `performance_tracker.py`
- **YouTube OAuth Resilience:** Read `data/social_accounts.json` FIRST; never overwrite `.env` (`--no-env` default True); keep Google Cloud OAuth Consent Screen in **Production** to prevent 7-day `invalid_grant` expiry; fix `@lb.satisfynglogic` channel handle typo in YouTube Studio when re-authorizing EN.
- **Instagram Trial Reels:** Optional `IG_TRIAL_REELS=true` using `trial_params={"graduation_strategy": "SS_PERFORMANCE"}` with graceful fallback.
- **Graph API `v22.0` Telemetry (`performance_tracker.py`):** Track `views`, `reach`, `saved`, `shares`, `ig_reels_avg_watch_time`, compute `sends_per_reach_pct`, and surface `channel_health` alerts (including YT OAuth expiry) in `data/social_performance_report.json`.

---

## 6. Mapping to Storefront & Credibility (`catalog_generator.py` & Control Center)

1. **Strict 5-Book Catalog:** Exclude `B0HNLWQ5CK` completely from [catalog.json](file:///c:/Users/loren/OneDrive/Desktop/KDP_Automated_Agency/docs/catalog.json) and [index.html](file:///c:/Users/loren/OneDrive/Desktop/KDP_Automated_Agency/docs/index.html) (`total_books: 5`: `B0HPBYGHHH`, `B0HNPC6XF2`, `B0HP8VR7N6`, `B0GV339NJW`, `B0GVF8HGMC`).
2. **Pure Localization & Audience Separation:** Fix `B0HPBYGHHH` category/badge to pure English (`Adults • Logic` / `For Adults • Mindful Edition`); offer instant audience filter pills (`All Books`, `Adults & Mindful Logic`, `Kids & Parents Screen-Free`, `Italiano`).
3. **Bestseller Trust Signals (Bucket 3 Proven):** Prominently display `300 DPI Vector Print`, `Verified Single-Solution Grids`, `Complete Answer Keys`, `8.5 × 11 in Full-Page Layout`, `Fast Amazon Prime`, plus interactive **"Look Inside" 3-page interior previews** (directly applying `FUNAFTER BOOKS` & `DLC PRESS` cover/interior transparency).
4. **Pricing Discipline:** Zero `.99`/`.98` fallbacks anywhere; anchor paperback offers cleanly around **`$10.80 USD` / `€10.80 EUR`** (or current live Amazon price without fake discount spam).
5. **Control Center Visibility:** Surface `channel_health` OAuth alerts + 2026 retention metrics (`avg_watch_time_sec`, `shares`, `saves`, `sends_per_reach_pct`) alongside template `1–7` + `IG Carousel` triggers.

---

## 7. Verification Gate & 30-Day Growth KPIs

| Metric | Old Baseline (Stalled) | 30-Day Target | Verification Owner |
| :--- | :--- | :--- | :--- |
| **IG 3s Hold Rate** | `< 25%` (0.9–2.5s avg watch) | **`>= 45%`** (`>= 8.5s` avg watch time) | `@performance_tracker` / Insights |
| **IG Sends per Reach** | `0%` (0 shares) | **`>= 3.0%`** (viral threshold `>= 5.0%`) | `@performance_tracker` (`v22.0`) |
| **IG Carousel Save-to-Like** | `0%` | **`>= 25%`** (benchmark: `40.3%` Chloe) | `@carousel_generator` + Insights |
| **YT Shorts VVSA (Viewed %)** | Frozen / `< 45%` on promos | **`>= 70%`** Viewed (`< 30%` Swiped Away) | YouTube Studio + `@auth_youtube_channel` |
| **YT Shorts AVD %** | `< 40%` | **`>= 100%`** (loopable 18–26s runtime) | YouTube Studio |
| **Comment-to-DM Funnel** | Raw dead links | **`>= 80%`** DM open, **`>= 25%`** CTR | ManyChat (`LOGIC` / `LOGICA`) |
| **Pre-Publish Creative Rubric** | Unaudited AI promos | **`>= 9/10`** across all 5 Loop-2 axes | `@verifier` (`tests/test_viral_growth_engine.py`) |
