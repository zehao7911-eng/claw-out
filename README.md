# CLAW OUT!

An original mobile-friendly 3D arcade crane game. Drag to aim, then press GRAB. Pick the requested robot and watch the three-finger claw close, lift, carry it to the aperture and release. All six robot figures, cabinet hardware, UI glyphs, icon and synthesized audio are authored in code. English UI, no animal cast, no real-money transactions, entry costs, random grip strength, lives or time limit.

## Play and progression

Tap a robot to aim at it, drag within the machine, or use the four large direction controls. GRAB commits one complete crane cycle. Space/Enter also grabs; arrow keys adjust aim. The gold dot marks your chosen aim; the larger ring follows the actual claw. The current requested bot is highlighted in the order row. Grabbing the wrong robot returns it without losing earned prizes. Empty grabs are freely retryable. A useful aim cue confirms the selected toy.

Cabinets 1–3 use stationary arrangements; 4–6 use rotating prize beds. Aim near the centre, allowing for the slow movement during descent. Capture uses the actual nearest live prize within a fixed range at closure, not chance. One star for finishing; another for at most one miss; another for keeping every successful catch within 0.35 world units of centre. FIND IT is an optional aiming guide and caps this visit at two stars. Stars and scores are best-only; result reload/replay cannot repeatedly award progress.

Six authored cabinets, three cabinet/environment palettes, three or four requested toys each. Overtime cycles these six configurations with shifted requests, layouts and bounded carousel-speed changes; it is not an unlimited hand-authored campaign. The six collected figures are BOLT, ORBIT, BASS, ROCKET, PIXEL and TOAST. Chrome cabinet colour unlocks at six stars; a visible lucky claw medallion attaches at twelve. Both have optional confirmed GameWave interaction alternatives.

## Reference scope

Reference: Combos **Claw CAPTCHA** by Vexxxxx, https://combos.game/zh-CN/play/68e2184e783f9c7af9f835345378eadb . Its public description specifies mobile-first 3D claw positioning, grabbing a requested plush and delivering it to a slot. Its public 720×408 cover was visually inspected for the framed/glazed cabinet, metal prongs, joystick, large action button and bright arcade presentation. The runtime showed a human-verification entry; it was not completed. No actual reference playthrough or exact parity is claimed. This independent game opens straight into normal play. No reference source, images, character models, logo or music were copied, and no image generator was used.

Generic original mesh/audio helpers and optional SDK adapter patterns are reused from our earlier projects. Controller, cabinet, robot meshes, crane assembly, progression and game-specific integration are newly authored. Three.js r147 is bundled locally with its MIT notice. `cover.jpg` is a genuine game-rendered title screenshot. This is a deterministic arcade grasp/animation model, not a general-purpose rigid-body or cloth simulation.

## Run, build and save

Open `index.html` or `standalone.html`: identical, self-contained entries containing renderer, game and CSS. No server, SDK, account, CDN, fonts or network is required; favicon/cover are optional. Serve `index-source.html` over static HTTP for modular source. `node build.cjs` rebuilds both compiled aliases. Run `node tests.mjs` and `node model-check.mjs` for controller/SDK and actual mesh tests.

Only `claw-out-v1` is read locally. The active mechanism's phase, progress, motor position, target, height, finger opening, captured prize, order, misses, score and carousel clock save, together with best results, collection, cosmetics and settings. Restoring stops at a safe menu. Between-grab idle progress stays valid even after a long wait. Reload during an active cycle preserves its physical phase. Pausing, tab interruption and page exit save safely. Nothing enumerates, uploads or clears other games' localStorage.

Vertices are colour-batched and cached, effects bounded, contact shadows inexpensive, DPR capped at 1.5 (Light: 1), with no real-time shadow maps. Input hit regions are projected after the actual render/update and initialized synchronously, including rotation/resize, to avoid stale or unpositioned first-tap targets. Controller integration uses small substeps and is checked at 1/30/60/120Hz; that is not physical-handset FPS certification.

## GameWave compatibility

Official documentation rechecked November 8, 2026, displaying October 30: https://rg975ojk5z.feishu.cn/wiki/MQg7wMknzieOkukxyWVc4UB0nDh . Ordinary browser startup never waits for `window.neonlib`. Optional methods are guarded individually, with absent/partial/late injection and asynchronous failure/timeouts contained.

The first committed GRAB starts a visit once; actual final delivery ends it once. Resuming an already committed moving cycle starts its continued visit when simulation actually advances. Restoring a between-grab idle checkpoint, looking at menus, aiming or pressing the visual guide does not invent starts. The next accepted grab starts the resumed idle visit. Abandoning an active unfinished cabinet before selecting another ends the old visit.

Only a recognized `{game:'claw-out',v:1,profile}` is merged. Best stars/scores use maxima, collection/cosmetic flags use unions. Current in-memory progress takes precedence; a fresh untouched first screen can restore a real remote checkpoint. Unknown or rejected cloud loads are not overwritten. Cloud/interface updates preserve the Resume button and update counters, collection and unlocks in place.

Confirmed positive `onLike` unlocks Chrome; a successful direct `onComment`, including empty text for an image-only comment, attaches the medallion. Actual async `code:0` registrations retain SDK-returned unsubscribe callbacks, including late completion after exit. Direct callback fields are used; project IDs stay strings, count snapshots are not identifiers, and unlike/malformed events grant nothing. Explicit durable claim flags prevent repeat cosmetic grants in the recognized browser/cloud save scope; no server-verified cross-device exactly-once claim. Unsupported social prompts remain absent; core play is never gated.

Static/controller checks, mocks, native local-browser checks and published-browser checks are separate evidence. Actual GameWave App import/account/live cloud/social callbacks and physical handsets remain unverified. Do not infer platform grading or host certification from mocks.

## License

Original code and procedural assets/audio: MIT, copyright 2026. Permission is granted free of charge to use, copy, modify, merge, publish, distribute, sublicense and sell copies, provided this notice is retained. Provided AS IS without warranty. Three.js retains its separate notice in `vendor/THREE-LICENSE.txt`.
