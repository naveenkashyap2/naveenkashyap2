

<!doctype html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Naveen Kashyap | AI Full Stack Developer</title>
<meta name="description" content="Naveen Kashyap, AI Full Stack Developer. MERN, microservices, Generative AI, RAG, AI agents and MCP.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@500;700;800&family=DM+Sans:wght@400;500;700&family=JetBrains+Mono:wght@500;700&display=swap" rel="stylesheet">
<style>
/* Layout: floating pill nav over one big raised hero shell, then raised and inset neomorphic cards stacked section by section. Pink and white clay surfaces, one pink gradient as the only loud colour. */
:root{
  --bg:#f6e7f1;
  --fg:#3a1c2c;
  --muted:#7a566a;
  --pink:#c81e68;
  --violet:#7c5cf0;
  --cyan:#1aa6c9;
  --grad:linear-gradient(135deg,#d6286f 0%,#8b5cf6 58%,#22b8d8 100%);
  --grad-btn:linear-gradient(135deg,#d6286f 0%,#8b5cf6 100%);
  --on-accent:#ffffff;
  --cl:42%;
  --tl:42%;
  --sd:#dab9d1;
  --sl:#ffffff;
  --blob1:rgba(255,140,185,.36);
  --blob2:rgba(150,130,255,.22);
  --f-display:'Outfit',system-ui,-apple-system,'Segoe UI',sans-serif;
  --f-body:'DM Sans',system-ui,-apple-system,'Segoe UI',sans-serif;
  --f-mono:'JetBrains Mono',ui-monospace,Menlo,Consolas,monospace;
  --raise:10px 10px 22px var(--sd),-10px -10px 22px var(--sl);
  --raise-sm:5px 5px 11px var(--sd),-5px -5px 11px var(--sl);
  --raise-xs:3px 3px 7px var(--sd),-3px -3px 7px var(--sl);
  --inset:inset 6px 6px 12px var(--sd),inset -6px -6px 12px var(--sl);
  --inset-sm:inset 3px 3px 7px var(--sd),inset -3px -3px 7px var(--sl);
}
@media (prefers-color-scheme:dark){
  :root:not([data-theme="light"]){
    --bg:#262a3c;--fg:#eceefa;--muted:#aab0c9;--pink:#ff86b6;--violet:#a78bfa;--cyan:#67e8f9;
    --grad:linear-gradient(135deg,#ff7eb3 0%,#a78bfa 55%,#67e8f9 100%);--grad-btn:linear-gradient(135deg,#ff7eb3 0%,#a78bfa 100%);--on-accent:#1b1630;--cl:50%;--tl:70%;
    --sd:#181b29;--sl:#343954;--blob1:rgba(255,126,179,.17);--blob2:rgba(167,139,250,.16);
    color-scheme:dark;
  }
}
:root[data-theme="dark"]{
  --bg:#262a3c;--fg:#eceefa;--muted:#aab0c9;--pink:#ff86b6;--violet:#a78bfa;--cyan:#67e8f9;
  --grad:linear-gradient(135deg,#ff7eb3 0%,#a78bfa 55%,#67e8f9 100%);--grad-btn:linear-gradient(135deg,#ff7eb3 0%,#a78bfa 100%);--on-accent:#1b1630;--cl:50%;--tl:70%;
  --sd:#181b29;--sl:#343954;--blob1:rgba(255,126,179,.17);--blob2:rgba(167,139,250,.16);
  color-scheme:dark;
}
*,*::before,*::after{box-sizing:border-box}
html{scroll-behavior:smooth;-webkit-text-size-adjust:100%}
body{margin:0;background:var(--bg);color:var(--fg);font-family:var(--f-body);font-size:16px;line-height:1.65;overflow-x:hidden;-webkit-font-smoothing:antialiased}
body::before{content:"";position:fixed;inset:0 0 auto;height:env(safe-area-inset-top,0px);z-index:60;background:var(--bg)}
img{max-width:100%;display:block}
a{color:inherit;text-decoration:none}
h1,h2,h3,p,ul,ol{margin:0}
ul,ol{padding:0;list-style:none}
button{font:inherit;color:inherit;border:0;background:none;cursor:pointer}
:focus-visible{outline:3px solid var(--pink);outline-offset:3px;border-radius:12px}
.wrap{width:min(1180px,100%);margin-inline:auto;padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px))}
section{scroll-margin-top:104px}
.mono{font-family:var(--f-mono);letter-spacing:.14em;text-transform:uppercase;font-size:.74rem;font-weight:700}
.grad-text{background:var(--grad);-webkit-background-clip:text;background-clip:text;color:transparent;-webkit-text-fill-color:transparent}

/* ambient background */
.bg{position:fixed;inset:0;pointer-events:none;z-index:0;overflow:hidden}
.bg i{position:absolute;border-radius:50%;animation:drift 18s ease-in-out infinite alternate}
.bg i:nth-child(1){width:46vmax;height:46vmax;left:-14vmax;top:-10vmax;background:radial-gradient(circle,var(--blob1),transparent 68%)}
.bg i:nth-child(2){width:40vmax;height:40vmax;right:-12vmax;top:34vh;background:radial-gradient(circle,var(--blob2),transparent 66%);animation-delay:-6s}
.bg i:nth-child(3){width:34vmax;height:34vmax;left:20vw;bottom:-14vmax;background:radial-gradient(circle,var(--blob1),transparent 70%);animation-delay:-11s}
@keyframes drift{to{transform:translate3d(4vmax,3vmax,0) scale(1.08)}}
main,header,footer{position:relative;z-index:1}
#bar{position:fixed;left:0;right:0;top:env(safe-area-inset-top,0px);height:3px;z-index:70;background:var(--grad);transform:scaleX(0);transform-origin:0 50%}

/* nav */
header.nav-wrap{position:sticky;top:env(safe-area-inset-top,0px);z-index:50;padding-block:14px 6px}
nav.nav{display:flex;align-items:center;gap:12px;justify-content:space-between;background:var(--bg);border-radius:26px;padding:10px 14px 10px 22px;box-shadow:var(--raise-sm);position:relative}
.logo{font-family:var(--f-display);font-weight:800;font-size:1.45rem;letter-spacing:-.02em}
.logo b{font-weight:800}
.links{display:flex;gap:6px;align-items:center}
.links a{font-family:var(--f-mono);font-weight:700;font-size:.74rem;letter-spacing:.14em;text-transform:uppercase;color:var(--muted);padding:10px 14px;border-radius:14px;transition:box-shadow .25s,color .25s}
.links a:hover{color:var(--pink);box-shadow:var(--raise-xs)}
.links a[aria-current="true"]{color:var(--pink);box-shadow:var(--inset-sm)}
.nav-tools{display:flex;align-items:center;gap:12px}
.icon-btn{width:44px;height:44px;border-radius:50%;display:grid;place-items:center;box-shadow:var(--raise-xs);background:var(--bg);transition:box-shadow .2s,transform .2s}
.icon-btn:hover{transform:translateY(-1px)}
.icon-btn:active{box-shadow:var(--inset-sm)}
.icon-btn svg{width:20px;height:20px;stroke:currentColor;fill:none;stroke-width:2;stroke-linecap:round;stroke-linejoin:round}
.burger{display:none}
.btn{display:inline-flex;align-items:center;justify-content:center;gap:10px;font-family:var(--f-mono);font-weight:700;font-size:.78rem;letter-spacing:.12em;text-transform:uppercase;padding:16px 26px;border-radius:18px;background:var(--bg);color:var(--fg);box-shadow:var(--raise-sm);transition:transform .2s,box-shadow .2s;min-height:48px}
.btn:hover{transform:translateY(-2px)}
.btn:active{transform:none;box-shadow:var(--inset-sm)}
.btn svg{width:16px;height:16px;stroke:currentColor;fill:none;stroke-width:2.2;stroke-linecap:round;stroke-linejoin:round;flex:none}
.btn.primary{background:var(--grad-btn);color:var(--on-accent);box-shadow:6px 6px 14px var(--sd),-6px -6px 14px var(--sl)}
.btn.sm{padding:12px 20px;border-radius:16px;min-height:44px}

/* hero */
.hero{padding-block:34px 18px}
.shell{background:var(--bg);border-radius:44px;padding:clamp(24px,4.6vw,64px);box-shadow:var(--raise);display:grid;grid-template-columns:minmax(0,1.25fr) minmax(0,.75fr);gap:clamp(24px,4vw,56px);align-items:center}
.badge{display:inline-flex;align-items:center;gap:12px;box-shadow:var(--inset-sm);border-radius:999px;padding:11px 20px;color:var(--muted)}
.badge i{width:10px;height:10px;border-radius:50%;background:var(--cyan);box-shadow:0 0 0 0 rgba(26,166,201,.6);animation:ping 2s infinite;flex:none}
@keyframes ping{70%{box-shadow:0 0 0 10px rgba(26,166,201,0)}100%{box-shadow:0 0 0 0 rgba(26,166,201,0)}}
h1.name{font-family:var(--f-display);font-weight:800;font-size:clamp(2.5rem,7.6vw,5.4rem);line-height:1;letter-spacing:-.035em;margin-top:26px;text-transform:uppercase}
.role{font-family:var(--f-display);font-weight:700;font-size:clamp(1.35rem,3.2vw,2.15rem);line-height:1.2;margin-top:14px;letter-spacing:-.01em}
.typed{font-family:var(--f-mono);font-weight:700;letter-spacing:.2em;text-transform:uppercase;font-size:.9rem;color:var(--violet);margin-top:16px;min-height:1.6em}
.typed::after{content:"";display:inline-block;width:3px;height:1.05em;margin-left:6px;background:var(--violet);vertical-align:-.18em;animation:blink 1s steps(2) infinite}
@keyframes blink{50%{opacity:0}}
.lead{color:var(--muted);font-size:clamp(1rem,1.5vw,1.14rem);margin-top:20px;max-width:56ch}
.cta{display:flex;flex-wrap:wrap;gap:16px;margin-top:30px}
.stats{display:grid;grid-template-columns:repeat(3,1fr);margin-top:34px;box-shadow:var(--inset);border-radius:26px;padding:20px 8px}
.stat{text-align:center;padding-inline:8px;position:relative;min-width:0}
.stat+.stat::before{content:"";position:absolute;left:0;top:12%;bottom:12%;width:2px;border-radius:2px;box-shadow:inset 1px 0 1px var(--sd),inset -1px 0 1px var(--sl)}
.stat b{display:block;font-family:var(--f-display);font-weight:800;font-size:clamp(1.6rem,3.2vw,2.3rem);line-height:1.1;font-variant-numeric:tabular-nums}
.stat span{display:block;font-family:var(--f-mono);font-weight:700;font-size:.64rem;letter-spacing:.14em;text-transform:uppercase;color:var(--muted);margin-top:6px}
.portrait{position:relative;display:grid;justify-items:center;gap:26px}
.ring{width:min(100%,380px);aspect-ratio:1;border-radius:50%;padding:14px;box-shadow:var(--raise);background:var(--bg);position:relative}
.ring::before{content:"";position:absolute;inset:14px;border-radius:50%;box-shadow:var(--inset)}
.ring .inner{position:absolute;inset:30px;border-radius:50%;padding:7px;background:var(--grad)}
.ring img{width:100%;height:100%;border-radius:50%;object-fit:cover;background:var(--bg)}
.float{position:absolute;font-family:var(--f-mono);font-weight:700;font-size:.72rem;letter-spacing:.1em;text-transform:uppercase;background:var(--bg);color:var(--pink);padding:9px 14px;border-radius:14px;box-shadow:var(--raise-xs);animation:bob 5s ease-in-out infinite}
.float.a{top:6%;left:-2%;color:var(--pink)}
.float.b{top:30%;right:-4%;animation-delay:-1.4s;color:var(--violet)}
.float.c{bottom:14%;left:-4%;animation-delay:-2.8s;color:var(--cyan)}
.float.d{bottom:2%;right:4%;animation-delay:-4s}
@keyframes bob{50%{transform:translateY(-10px)}}
.cap{text-align:center;font-family:var(--f-mono);font-weight:700;font-size:.72rem;letter-spacing:.16em;text-transform:uppercase;line-height:1.9;color:var(--muted)}
.cap b{color:var(--pink)}

/* marquee */
.marquee{margin-top:28px;border-radius:26px;box-shadow:var(--inset);overflow:hidden;padding-block:18px;-webkit-mask-image:linear-gradient(90deg,transparent,#000 6%,#000 94%,transparent);mask-image:linear-gradient(90deg,transparent,#000 6%,#000 94%,transparent)}
.track{display:flex;width:max-content;gap:48px;animation:slide 38s linear infinite;padding-left:48px}
.marquee:hover .track{animation-play-state:paused}
.track span{--c:hsl(var(--h,330) 70% var(--tl));font-family:var(--f-mono);font-weight:700;font-size:.82rem;letter-spacing:.16em;text-transform:uppercase;color:var(--c);white-space:nowrap;transition:transform .2s}
.track span:hover{transform:scale(1.12)}
.track span::after{content:"\2726";margin-left:48px;color:var(--violet);opacity:.7;display:inline-block}
@keyframes slide{to{transform:translateX(-50%)}}

/* sections */
.sec{padding-block:clamp(44px,7vw,84px) 0}
.sec-head{margin-bottom:34px;display:grid;gap:10px}
.sec-head .mono{color:var(--pink)}
.sec-head h2{font-family:var(--f-display);font-weight:800;font-size:clamp(1.9rem,4.6vw,3rem);line-height:1.08;letter-spacing:-.025em;text-wrap:balance}
.card{background:var(--bg);border-radius:30px;box-shadow:var(--raise);padding:clamp(22px,3vw,36px);min-width:0}
.rv{transform:translateY(26px);transition:transform .8s cubic-bezier(.2,.7,.2,1) var(--d,0s)}
.rv.in{transform:none}

/* about */
.about{display:grid;grid-template-columns:minmax(0,1.3fr) minmax(0,.7fr);gap:clamp(20px,3vw,34px)}
.about p{color:var(--muted);font-size:1.06rem;max-width:62ch}
.about p+p{margin-top:16px}
.facts{display:grid;gap:14px;align-content:start}
.fact{box-shadow:var(--inset-sm);border-radius:20px;padding:14px 18px;min-width:0}
.fact small{display:block;font-family:var(--f-mono);font-weight:700;font-size:.64rem;letter-spacing:.14em;text-transform:uppercase;color:var(--muted)}
.fact b{display:block;font-family:var(--f-display);font-weight:700;font-size:1.02rem;margin-top:2px;overflow-wrap:anywhere}

/* skills */
.grid{display:grid;gap:clamp(18px,2.6vw,30px)}
.g3{grid-template-columns:repeat(3,minmax(0,1fr))}
.g2{grid-template-columns:repeat(2,minmax(0,1fr))}
.skill h3{font-family:var(--f-display);font-weight:700;font-size:1.15rem;margin-bottom:16px}
.chips{display:flex;flex-wrap:wrap;gap:10px}
.chip{--c:hsl(var(--h,330) 68% var(--cl));display:inline-flex;align-items:center;gap:8px;font-family:var(--f-mono);font-weight:700;font-size:.72rem;letter-spacing:.06em;padding:9px 14px;border-radius:12px;background:var(--bg);color:var(--fg);box-shadow:var(--raise-xs);cursor:pointer;user-select:none;-webkit-tap-highlight-color:transparent;transition:transform .2s,box-shadow .25s,background-color .25s,color .25s}
.chip::before{content:"";width:8px;height:8px;border-radius:50%;background:var(--c);flex:none;transition:background-color .25s}
.chip:hover,.chip:focus-visible,.chip.on{background:var(--c);color:#fff;box-shadow:0 10px 22px color-mix(in srgb,var(--c) 42%,transparent),inset 0 0 0 1px rgb(255 255 255 / .2)}
.chip:hover::before,.chip:focus-visible::before,.chip.on::before{background:#fff}
.chip:hover{transform:translateY(-3px)}
.chip.on{transform:scale(.97)}

/* genai roadmap */
.meter{display:flex;align-items:center;gap:16px;margin-bottom:26px}
.meter .rail{flex:1;height:16px;border-radius:999px;box-shadow:var(--inset-sm);padding:3px;min-width:0}
.meter .fill{display:block;height:100%;width:0;border-radius:999px;background:var(--grad);transition:width 1.6s cubic-bezier(.2,.7,.2,1)}
.meter .fill.go{width:100%}
.meter b{font-family:var(--f-mono);font-weight:700;font-size:.8rem;letter-spacing:.1em;white-space:nowrap;color:var(--pink)}
.road{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:clamp(16px,2.2vw,26px);counter-reset:s}
.step{background:var(--bg);border-radius:26px;box-shadow:var(--raise-sm);padding:22px 20px 22px;position:relative;min-width:0;transition:transform .25s,box-shadow .25s}
.step:hover{transform:translateY(-4px)}
.step .n{width:44px;height:44px;border-radius:50%;box-shadow:var(--inset-sm);display:grid;place-items:center;font-family:var(--f-mono);font-weight:700;font-size:.84rem;color:var(--pink);margin-bottom:14px}
.step h3{font-family:var(--f-display);font-weight:700;font-size:1.12rem;line-height:1.25}
.step p{color:var(--muted);font-size:.92rem;margin-top:8px;line-height:1.55}
.step .ok{position:absolute;top:20px;right:18px;width:24px;height:24px;border-radius:50%;background:var(--grad);display:grid;place-items:center}
.step .ok svg{width:13px;height:13px;stroke:var(--on-accent);fill:none;stroke-width:3.2;stroke-linecap:round;stroke-linejoin:round}
.step.last{background:var(--bg);outline:2px solid transparent}
.step.last .n{background:var(--grad);color:var(--on-accent);box-shadow:var(--raise-xs)}

/* projects */
.proj{display:flex;flex-direction:column;gap:16px}
.proj-top{display:flex;justify-content:space-between;gap:14px;align-items:flex-start}
.proj h3{font-family:var(--f-display);font-weight:800;font-size:clamp(1.25rem,2.2vw,1.55rem);line-height:1.2;letter-spacing:-.01em}
.proj .sub{color:var(--muted);font-size:.95rem;margin-top:2px}
.pill{flex:none;font-family:var(--f-mono);font-weight:700;font-size:.64rem;letter-spacing:.14em;text-transform:uppercase;padding:8px 13px;border-radius:999px;box-shadow:var(--inset-sm);color:var(--pink);display:inline-flex;align-items:center;gap:8px;white-space:nowrap}
.pill i{width:8px;height:8px;border-radius:50%;background:currentColor;animation:ping2 1.8s infinite}
@keyframes ping2{50%{opacity:.35}}
.proj ul{display:grid;gap:10px}
.proj li{position:relative;padding-left:22px;color:var(--muted);font-size:.96rem;line-height:1.6}
.proj li::before{content:"";position:absolute;left:0;top:.62em;width:9px;height:9px;border-radius:50%;background:var(--grad)}
.proj .chips{margin-top:auto;padding-top:4px}
.proj .actions{display:flex;flex-wrap:wrap;gap:14px;padding-top:6px}

/* experience */
.tl{display:grid;gap:clamp(18px,2.6vw,28px);position:relative;padding-left:clamp(26px,4vw,44px)}
.tl::before{content:"";position:absolute;left:8px;top:14px;bottom:14px;width:8px;border-radius:8px;box-shadow:var(--inset-sm)}
.job{position:relative}
.job::before{content:"";position:absolute;left:calc(-1 * clamp(26px,4vw,44px) + 4px);top:30px;width:16px;height:16px;border-radius:50%;background:var(--grad);box-shadow:var(--raise-xs)}
.job-top{display:flex;flex-wrap:wrap;justify-content:space-between;gap:8px 18px;align-items:baseline;margin-bottom:14px}
.job h3{font-family:var(--f-display);font-weight:800;font-size:clamp(1.15rem,2vw,1.4rem);line-height:1.25}
.job .when{font-family:var(--f-mono);font-weight:700;font-size:.74rem;letter-spacing:.1em;text-transform:uppercase;color:var(--pink)}
.job .org{color:var(--muted);font-weight:500;margin-bottom:10px}
.job ul{display:grid;gap:9px}
.job li{position:relative;padding-left:20px;color:var(--muted);font-size:.96rem}
.job li::before{content:"";position:absolute;left:0;top:.66em;width:8px;height:8px;border-radius:50%;box-shadow:var(--inset-sm)}

/* education */
.edu h3{font-family:var(--f-display);font-weight:800;font-size:1.25rem;line-height:1.3}
.edu p{color:var(--muted);margin-top:8px}
.edu .big{font-family:var(--f-display);font-weight:800;font-size:2.4rem;line-height:1;margin-top:14px}
.edu .big small{font-size:1rem;color:var(--muted);font-weight:500}

/* contact */
.contact{display:grid;grid-template-columns:minmax(0,1fr) minmax(0,1fr);gap:clamp(20px,3vw,40px);align-items:center}
.contact h2{font-family:var(--f-display);font-weight:800;font-size:clamp(1.9rem,4.4vw,3rem);line-height:1.08;letter-spacing:-.025em;text-wrap:balance}
.contact p{color:var(--muted);margin-top:14px;max-width:46ch}
.mail{display:flex;align-items:center;gap:12px;box-shadow:var(--inset);border-radius:22px;padding:10px 10px 10px 20px;min-width:0}
.mail span{font-family:var(--f-mono);font-weight:700;font-size:clamp(.78rem,1.6vw,.95rem);overflow-wrap:anywhere;flex:1;min-width:0}
.social{display:flex;flex-wrap:wrap;gap:14px;margin-top:20px}
.social .btn{flex:1 1 150px}
.toast{position:fixed;left:50%;bottom:max(24px,env(safe-area-inset-bottom,0px));transform:translate(-50%,24px);opacity:0;pointer-events:none;background:var(--bg);color:var(--pink);font-family:var(--f-mono);font-weight:700;font-size:.78rem;letter-spacing:.1em;text-transform:uppercase;padding:14px 22px;border-radius:18px;box-shadow:var(--raise);transition:opacity .25s,transform .25s;z-index:80}
.toast.show{opacity:1;transform:translate(-50%,0)}
footer{padding-block:54px max(40px,env(safe-area-inset-bottom,0px))}
footer p{text-align:center;color:var(--muted);font-size:.9rem}
footer p b{color:var(--pink)}

/* hero entrance */
.rise>*{animation:rise .8s cubic-bezier(.2,.7,.2,1) both}
.rise>*:nth-child(2){animation-delay:.08s}.rise>*:nth-child(3){animation-delay:.16s}.rise>*:nth-child(4){animation-delay:.24s}.rise>*:nth-child(5){animation-delay:.32s}.rise>*:nth-child(6){animation-delay:.4s}
@keyframes rise{from{opacity:0;transform:translateY(22px)}to{opacity:1;transform:none}}
.pop{animation:pop 1s cubic-bezier(.2,.8,.2,1) .2s both}
@keyframes pop{from{opacity:0;transform:scale(.9)}to{opacity:1;transform:none}}

@media (max-width:1020px){
  .road{grid-template-columns:repeat(3,minmax(0,1fr))}
  .g3{grid-template-columns:repeat(2,minmax(0,1fr))}
}
@media (max-width:900px){
  .shell{grid-template-columns:minmax(0,1fr)}
  .portrait{order:-1}
  .ring{width:min(78%,320px)}
  .about,.contact{grid-template-columns:minmax(0,1fr)}
  .links{display:none;position:absolute;left:0;right:0;top:calc(100% + 12px);flex-direction:column;align-items:stretch;background:var(--bg);border-radius:24px;padding:14px;box-shadow:var(--raise)}
  .nav.open .links{display:flex}
  .links a{text-align:center;padding:14px}
  .burger{display:grid}
}
@media (max-width:720px){
  .g2,.g3{grid-template-columns:minmax(0,1fr)}
  .road{grid-template-columns:repeat(2,minmax(0,1fr))}
  .shell{border-radius:32px}
  .card{border-radius:26px}
}
@media (max-width:520px){
  .road{grid-template-columns:minmax(0,1fr)}
  nav.nav{padding-left:16px;gap:8px}
  .nav-tools{gap:8px}
  .nav-tools .btn{display:none}
  .stats{padding-inline:2px}
  .stat span{font-size:.56rem;letter-spacing:.08em}
  .cta .btn{flex:1 1 100%}
  .float{font-size:.62rem;padding:7px 10px}
  .proj-top{flex-direction:column}
}
@media (prefers-reduced-motion:reduce){
  *,*::before,*::after{animation:none!important;transition:none!important}
  html{scroll-behavior:auto}
  .rv{transform:none}
}
</style>
</head>
<body>
<div class="bg" aria-hidden="true"><i></i><i></i><i></i></div>
<div id="bar" aria-hidden="true"></div>

<header class="nav-wrap">
  <div class="wrap">
    <nav class="nav" id="nav" aria-label="Main">
      <a class="logo" href="#top" aria-label="Naveen.dev home">Naveen<span class="grad-text">.dev</span></a>
      <div class="links" id="links">
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#genai">GenAI</a>
        <a href="#projects">Projects</a>
        <a href="#experience">Experience</a>
        <a href="#contact">Contact</a>
      </div>
      <div class="nav-tools">
        <button class="icon-btn" id="theme" type="button" aria-label="Switch colour theme"></button>
        <a class="btn primary sm" href="#contact">Hire me</a>
        <button class="icon-btn burger" id="burger" type="button" aria-label="Open menu" aria-expanded="false" aria-controls="links">
          <svg viewBox="0 0 24 24"><path d="M4 7h16M4 12h16M4 17h16"/></svg>
        </button>
      </div>
    </nav>
  </div>
</header>

<main id="top">
  <section class="hero">
    <div class="wrap">
      <div class="shell">
        <div>
          <div class="rise">
            <span class="badge mono"><i></i>Open to work &middot; B.Tech CSE 2026 graduate</span>
            <h1 class="name">Naveen <span class="grad-text">Kashyap</span></h1>
            <h2 class="role"><span class="grad-text">AI</span> Full Stack Developer</h2>
            <p class="typed" id="typed" aria-live="off">Generative AI</p>
            <p class="lead">I build scalable, real-time and AI-powered web applications with the MERN stack, microservices and Generative AI, from Gemini API and RAG pipelines to AI agents and MCP.</p>
            <div class="cta">
              <a class="btn primary" href="#projects">View projects
                <svg viewBox="0 0 24 24"><path d="M5 12h14M13 6l6 6-6 6"/></svg></a>
              <a class="btn" href="Naveen_Kashyap_Resume.pdf" download>
                <svg viewBox="0 0 24 24"><path d="M12 4v11M7 10l5 5 5-5M5 20h14"/></svg>Download CV</a>
              <a class="btn" href="#contact">Get in touch</a>
            </div>
          </div>
          <div class="stats pop" role="list">
            <div class="stat" role="listitem"><b data-count="1" data-suffix="+">1+</b><span>Year experience</span></div>
            <div class="stat" role="listitem"><b data-count="11" data-suffix="+">11+</b><span>Projects built</span></div>
            <div class="stat" role="listitem"><b data-count="7.5" data-dec="1">7.5</b><span>CGPA / 10</span></div>
          </div>
        </div>
        <div class="portrait pop">
          <div class="ring">
            <div class="inner"><img src="data:image/jpeg;base64,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" width="360" height="360" alt="Portrait of Naveen Kashyap" fetchpriority="high" decoding="async"></div>
            <span class="float a">RAG</span>
            <span class="float b">Gemini</span>
            <span class="float c">React</span>
            <span class="float d">MCP</span>
          </div>
          <p class="cap"><b>Full Stack</b> &middot; <b>Generative AI</b><br>MERN + Microservices</p>
        </div>
      </div>
      <div class="marquee" aria-hidden="true">
        <div class="track" id="track">
          <span>Python</span><span>FastAPI</span><span>Gemini API</span><span>LangChain</span><span>RAG</span><span>Embeddings</span><span>AI Agents</span><span>MCP</span><span>React</span><span>Next.js</span><span>Node.js</span><span>Express</span><span>MongoDB</span><span>PostgreSQL</span><span>TypeScript</span><span>Docker</span><span>Kafka</span><span>Redis</span><span>Vercel</span>
        </div>
      </div>
    </div>
  </section>

  <section class="sec" id="about">
    <div class="wrap">
      <div class="sec-head rv"><span class="mono">About</span><h2>Shipping products from UI to database to AI</h2></div>
      <div class="card about rv">
        <div>
          <p>I am a Full Stack Developer at Buildanta Private Limited, owning both the frontend and the backend of production applications. I work comfortably across the MERN stack with TypeScript, Next.js and PostgreSQL.</p>
          <p>I build REST APIs, authentication systems and real-time apps, and I add AI where it earns its place: Gemini-powered features, retrieval over private data, and agents that call real tools. I like finishing the whole loop, from the first component to deployment.</p>
        </div>
        <div class="facts">
          <div class="fact"><small>Role</small><b>AI Full Stack Developer</b></div>
          <div class="fact"><small>Now at</small><b>Buildanta Private Limited</b></div>
          <div class="fact"><small>Education</small><b>B.Tech CSE, AIT Kanpur</b></div>
          <div class="fact"><small>Certified</small><b>Microsoft Azure AZ-900</b></div>
        </div>
      </div>
    </div>
  </section>

  <section class="sec" id="skills">
    <div class="wrap">
      <div class="sec-head rv"><span class="mono">Skills</span><h2>The stack I work in every day</h2></div>
      <div class="grid g3">
        <article class="card skill rv"><h3>Languages</h3><div class="chips"><span class="chip">JavaScript</span><span class="chip">TypeScript</span><span class="chip hot">Python</span></div></article>
        <article class="card skill rv" style="--d:.06s"><h3>Frontend</h3><div class="chips"><span class="chip">React.js</span><span class="chip">Next.js</span><span class="chip">HTML</span><span class="chip">CSS</span><span class="chip">Tailwind CSS</span><span class="chip">Bootstrap</span></div></article>
        <article class="card skill rv" style="--d:.12s"><h3>Backend</h3><div class="chips"><span class="chip">Node.js</span><span class="chip">Express.js</span><span class="chip">REST APIs</span><span class="chip">JWT</span><span class="chip">OAuth 2.0</span><span class="chip">Socket.IO</span><span class="chip">WebSockets</span><span class="chip hot">FastAPI</span></div></article>
        <article class="card skill rv"><h3>Database &amp; Services</h3><div class="chips"><span class="chip">MongoDB</span><span class="chip">PostgreSQL</span><span class="chip">Prisma</span><span class="chip">Redis</span><span class="chip">Apache Kafka</span><span class="chip">Elasticsearch</span></div></article>
        <article class="card skill rv" style="--d:.06s"><h3>Cloud &amp; DevOps</h3><div class="chips"><span class="chip">Docker</span><span class="chip">Docker Compose</span><span class="chip">Vercel</span><span class="chip">Netlify</span><span class="chip">Render</span></div></article>
        <article class="card skill rv" style="--d:.12s"><h3>Generative AI</h3><div class="chips"><span class="chip hot">Gemini API</span><span class="chip hot">Claude</span><span class="chip hot">Prompt Engineering</span><span class="chip hot">Embeddings</span><span class="chip hot">RAG</span><span class="chip hot">LangChain</span><span class="chip hot">AI Agents</span><span class="chip hot">MCP</span></div></article>
      </div>
    </div>
  </section>

  <section class="sec" id="genai">
    <div class="wrap">
      <div class="sec-head rv"><span class="mono">GenAI journey</span><h2>From Python to advanced GenAI, step by step</h2></div>
      <div class="meter rv"><div class="rail"><span class="fill" id="fill"></span></div><b>11 / 11 steps</b></div>
      <ol class="road">
        <li class="step rv"><span class="n">01</span><h3>Python</h3><p>Core language, async code, packaging and clean project structure.</p><span class="ok"><svg viewBox="0 0 24 24"><path d="M5 12l5 5L20 7"/></svg></span></li>
        <li class="step rv" style="--d:.05s"><span class="n">02</span><h3>GenAI Fundamentals</h3><p>How LLMs work: tokens, context windows, transformers and model limits.</p><span class="ok"><svg viewBox="0 0 24 24"><path d="M5 12l5 5L20 7"/></svg></span></li>
        <li class="step rv" style="--d:.1s"><span class="n">03</span><h3>Prompt Engineering</h3><p>Structured prompts, few-shot examples and controlled outputs.</p><span class="ok"><svg viewBox="0 0 24 24"><path d="M5 12l5 5L20 7"/></svg></span></li>
        <li class="step rv" style="--d:.15s"><span class="n">04</span><h3>Gemini API</h3><p>Text and multimodal calls, streaming and structured responses.</p><span class="ok"><svg viewBox="0 0 24 24"><path d="M5 12l5 5L20 7"/></svg></span></li>
        <li class="step rv"><span class="n">05</span><h3>FastAPI</h3><p>Fast async backends for AI features with typed request schemas.</p><span class="ok"><svg viewBox="0 0 24 24"><path d="M5 12l5 5L20 7"/></svg></span></li>
        <li class="step rv" style="--d:.05s"><span class="n">06</span><h3>Embeddings</h3><p>Turning text into vectors and searching by meaning.</p><span class="ok"><svg viewBox="0 0 24 24"><path d="M5 12l5 5L20 7"/></svg></span></li>
        <li class="step rv" style="--d:.1s"><span class="n">07</span><h3>RAG</h3><p>Retrieval pipelines that ground answers in your own data.</p><span class="ok"><svg viewBox="0 0 24 24"><path d="M5 12l5 5L20 7"/></svg></span></li>
        <li class="step rv" style="--d:.15s"><span class="n">08</span><h3>LangChain</h3><p>Chains, loaders, memory and tool calling in one framework.</p><span class="ok"><svg viewBox="0 0 24 24"><path d="M5 12l5 5L20 7"/></svg></span></li>
        <li class="step rv"><span class="n">09</span><h3>AI Agents</h3><p>Agents that plan, call tools and complete multi-step tasks.</p><span class="ok"><svg viewBox="0 0 24 24"><path d="M5 12l5 5L20 7"/></svg></span></li>
        <li class="step rv" style="--d:.05s"><span class="n">10</span><h3>MCP</h3><p>Model Context Protocol servers and clients that connect models to tools.</p><span class="ok"><svg viewBox="0 0 24 24"><path d="M5 12l5 5L20 7"/></svg></span></li>
        <li class="step last rv" style="--d:.1s"><span class="n">11</span><h3>Advanced GenAI</h3><p>Evaluation, guardrails and shipping AI features to production.</p><span class="ok"><svg viewBox="0 0 24 24"><path d="M5 12l5 5L20 7"/></svg></span></li>
      </ol>
    </div>
  </section>

  <section class="sec" id="projects">
    <div class="wrap">
      <div class="sec-head rv"><span class="mono">Projects</span><h2>Things I have built and shipped</h2></div>
      <div class="grid g2">
        <article class="card proj rv">
          <div class="proj-top"><div><h3>Resumify AI</h3><p class="sub">AI-powered resume builder</p></div><span class="pill"><i></i>Live</span></div>
          <ul>
            <li>Turns structured input into professional, ATS-friendly one-page resumes with 20+ templates and instant switching.</li>
            <li>Real-time live preview on a reusable component architecture, where every template reads one normalized data model.</li>
            <li>One-click PDF export from the same render tree, and resume data stays in the browser.</li>
          </ul>
          <div class="chips"><span class="chip">React</span><span class="chip">Tailwind CSS</span><span class="chip">Framer Motion</span><span class="chip">Vercel</span></div>
          <div class="actions">
            <a class="btn primary sm" href="https://resume-builder-74fb.vercel.app/" target="_blank" rel="noopener">Live demo
              <svg viewBox="0 0 24 24"><path d="M7 17L17 7M8 7h9v9"/></svg></a>
            <a class="btn sm" href="https://github.com/naveenkashyap2" target="_blank" rel="noopener">Source</a>
          </div>
        </article>

        <article class="card proj rv" style="--d:.06s">
          <div class="proj-top"><div><h3>CareerAI</h3><p class="sub">AI-powered career platform</p></div><span class="pill">Gemini</span></div>
          <ul>
            <li>Full-stack platform for resume analysis, job matching, resume creation and interview preparation, powered by the Google Gemini API.</li>
            <li>AI Resume Analyzer with ATS scoring, keyword-gap detection and section-wise feedback.</li>
            <li>Google OAuth sign-in, personalized sessions and ATS-friendly PDF export.</li>
          </ul>
          <div class="chips"><span class="chip">MongoDB</span><span class="chip">Express</span><span class="chip">React</span><span class="chip">Node.js</span><span class="chip hot">Gemini API</span></div>
          <div class="actions"><a class="btn sm" href="https://github.com/naveenkashyap2" target="_blank" rel="noopener">Source</a></div>
        </article>

        <article class="card proj rv">
          <div class="proj-top"><div><h3>Railway Ticket Booking</h3><p class="sub">Microservices architecture</p></div><span class="pill"><i></i>Ongoing</span></div>
          <ul>
            <li>Independent microservices behind an API Gateway, with a database per service.</li>
            <li>Event-driven booking and payment flows on Apache Kafka, with Saga orchestration and dead-letter queues.</li>
            <li>Redis distributed seat locking to stop double reservations, plus Razorpay payments, webhooks and refunds.</li>
            <li>Elasticsearch train and station search, and JWT, OTP, Google OAuth, rate limiting and circuit breakers.</li>
          </ul>
          <div class="chips"><span class="chip">Node.js</span><span class="chip">React</span><span class="chip">PostgreSQL</span><span class="chip">Prisma</span><span class="chip">Redis</span><span class="chip">Kafka</span><span class="chip">Elasticsearch</span><span class="chip">Docker</span></div>
          <div class="actions"><a class="btn sm" href="https://github.com/naveenkashyap2" target="_blank" rel="noopener">Source</a></div>
        </article>

        <article class="card proj rv" style="--d:.06s">
          <div class="proj-top"><div><h3>Streamify</h3><p class="sub">Real-time communication platform</p></div><span class="pill">WebRTC</span></div>
          <ul>
            <li>1:1 video and audio calling with instant chat, built on WebRTC and Socket.IO.</li>
            <li>Secure authentication and call signaling, with call history and user profiles.</li>
            <li>Cloudinary for media upload, storage and sharing.</li>
          </ul>
          <div class="chips"><span class="chip">MERN</span><span class="chip">WebRTC</span><span class="chip">Socket.IO</span><span class="chip">Cloudinary</span></div>
          <div class="actions"><a class="btn sm" href="https://github.com/naveenkashyap2" target="_blank" rel="noopener">Source</a></div>
        </article>
      </div>
    </div>
  </section>

  <section class="sec" id="experience">
    <div class="wrap">
      <div class="sec-head rv"><span class="mono">Experience</span><h2>Where I have worked</h2></div>
      <div class="tl">
        <article class="card job rv">
          <div class="job-top"><h3>Full Stack Developer</h3><span class="when">Oct 2026 &ndash; Present</span></div>
          <p class="org">Buildanta Private Limited</p>
          <ul>
            <li>Own the complete lifecycle of web applications across frontend and backend: requirements, design, development, testing and deployment.</li>
            <li>Build responsive, reusable React.js and Next.js interfaces and connect them to backend services.</li>
            <li>Design scalable REST APIs with Node.js and Express.js, with JWT and role-based access control.</li>
            <li>Model schemas and write optimized queries in MongoDB and PostgreSQL.</li>
            <li>Debug production issues and improve performance, stability and maintainability, working through code reviews and release cycles on Git and GitHub.</li>
          </ul>
        </article>
        <article class="card job rv" style="--d:.06s">
          <div class="job-top"><h3>Front-End Developer Intern</h3><span class="when">May 2025 &ndash; Sep 2025</span></div>
          <p class="org">CodexIntern</p>
          <ul>
            <li>Built responsive, reusable React.js components with JavaScript, Tailwind CSS and Bootstrap.</li>
            <li>Integrated REST APIs to fetch, process and display dynamic data.</li>
            <li>Built APIs with Node.js and Express.js, and stored data in MongoDB.</li>
            <li>Debugged issues and tuned frontend functionality, responsiveness and user experience.</li>
          </ul>
        </article>
      </div>
    </div>
  </section>

  <section class="sec" id="education">
    <div class="wrap">
      <div class="sec-head rv"><span class="mono">Education</span><h2>Degree and certification</h2></div>
      <div class="grid g2">
        <article class="card edu rv"><h3>B.Tech in Computer Science &amp; Engineering</h3><p>Apollo Institute of Technology (AIT), Kanpur Nagar, Uttar Pradesh<br>2022 &ndash; 2026</p><div class="big grad-text">7.5 <small>/ 10 CGPA</small></div></article>
        <article class="card edu rv" style="--d:.06s"><h3>Microsoft Certified: Azure Fundamentals</h3><p>AZ-900 &middot; cloud concepts, core Azure services, security and governance.</p><div class="chips" style="margin-top:18px"><span class="chip hot">Microsoft</span><span class="chip">AZ-900</span></div></article>
      </div>
    </div>
  </section>

  <section class="sec" id="contact">
    <div class="wrap">
      <div class="card contact rv">
        <div>
          <span class="mono" style="color:var(--pink)">Contact</span>
          <h2 style="margin-top:10px">Let&rsquo;s build something <span class="grad-text">intelligent</span> together</h2>
          <p>Open to AI Full Stack, Full Stack, Frontend and Backend roles, remote or hybrid. Send a message and I will reply.</p>
        </div>
        <div>
          <div class="mail"><span id="mailtxt">nk1910479@gmail.com</span>
            <button class="btn primary sm" id="copymail" type="button">
              <svg viewBox="0 0 24 24"><rect x="9" y="9" width="11" height="11" rx="2"/><path d="M5 15V6a2 2 0 0 1 2-2h9"/></svg>Copy</button></div>
          <div class="social">
            <a class="btn" href="https://linkedin.com/in/naveen-kashyap08/" target="_blank" rel="noopener">LinkedIn</a>
            <a class="btn" href="https://github.com/naveenkashyap2" target="_blank" rel="noopener">GitHub</a>
            <a class="btn" href="https://leetcode.com/naveenkyp854/" target="_blank" rel="noopener">LeetCode</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="wrap"><p>Designed and built by <b>Naveen Kashyap</b> &middot; Kanpur, India</p></div>
</footer>
<div class="toast" id="toast" role="status" aria-live="polite"></div>

<script>
(function(){
  var d=document,root=d.documentElement,$=function(s){return d.querySelector(s)};
  var reduce=window.matchMedia&&window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  /* theme */
  var tbtn=$('#theme');
  var SUN='<svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="4"/><path d="M12 2v2M12 20v2M4.9 4.9l1.4 1.4M17.7 17.7l1.4 1.4M2 12h2M20 12h2M4.9 19.1l1.4-1.4M17.7 6.3l1.4-1.4"/></svg>';
  var MOON='<svg viewBox="0 0 24 24"><path d="M20 14.5A8 8 0 0 1 9.5 4 8 8 0 1 0 20 14.5z"/></svg>';
  function isDark(){var t=root.getAttribute('data-theme');if(t)return t==='dark';return window.matchMedia&&window.matchMedia('(prefers-color-scheme: dark)').matches}
  function paint(){tbtn.innerHTML=isDark()?SUN:MOON;tbtn.setAttribute('aria-label',isDark()?'Switch to light theme':'Switch to dark theme')}
  try{var saved=localStorage.getItem('nk-theme');if(saved==='dark'||saved==='light')root.setAttribute('data-theme',saved)}catch(e){}
  paint();
  tbtn.addEventListener('click',function(){var n=isDark()?'light':'dark';root.setAttribute('data-theme',n);try{localStorage.setItem('nk-theme',n)}catch(e){}paint()});

  /* mobile menu */
  var nav=$('#nav'),burger=$('#burger');
  burger.addEventListener('click',function(){var o=nav.classList.toggle('open');burger.setAttribute('aria-expanded',o?'true':'false')});
  d.querySelectorAll('#links a').forEach(function(a){a.addEventListener('click',function(){nav.classList.remove('open');burger.setAttribute('aria-expanded','false')})});

  /* one distinct colour per skill (same skill, same colour everywhere) */
  var hmap={},hn=0;
  d.querySelectorAll('.chip,.track span').forEach(function(n){
    var k=n.textContent.trim().toLowerCase().replace(/^apache\s+/,'').replace(/\.js$/,'');
    if(!(k in hmap)){hmap[k]=Math.round((hn*137.508+330)%360);hn++}
    n.style.setProperty('--h',hmap[k]);
    if(n.classList.contains('chip')){n.tabIndex=0;n.setAttribute('role','button');n.setAttribute('aria-pressed','false')}
  });
  d.addEventListener('click',function(e){var c=e.target.closest&&e.target.closest('.chip');if(!c)return;c.setAttribute('aria-pressed',c.classList.toggle('on')?'true':'false')});
  d.addEventListener('keydown',function(e){var t=e.target;if((e.key==='Enter'||e.key===' ')&&t.classList&&t.classList.contains('chip')){e.preventDefault();t.click()}});

  /* marquee: duplicate for a seamless loop */
  var track=$('#track');track.innerHTML=track.innerHTML+track.innerHTML;

  /* typed roles */
  var el=$('#typed'),words=['Generative AI','MERN Stack','RAG Pipelines','AI Agents','MCP Servers','Microservices'],wi=0,ci=0,del=false;
  function tick(){
    var w=words[wi];
    if(!del){ci++;el.firstChild.nodeValue=w.slice(0,ci);if(ci===w.length){del=true;return setTimeout(tick,1500)}}
    else{ci--;el.firstChild.nodeValue=w.slice(0,ci);if(ci===0){del=false;wi=(wi+1)%words.length;return setTimeout(tick,350)}}
    setTimeout(tick,del?38:74);
  }
  if(!reduce){el.firstChild.nodeValue='';setTimeout(tick,900)}

  /* counters */
  function count(n){
    var target=parseFloat(n.getAttribute('data-count')),dec=parseInt(n.getAttribute('data-dec')||'0',10),suf=n.getAttribute('data-suffix')||'';
    if(reduce){return}
    var t0=null,dur=1300;
    function f(ts){if(t0===null)t0=ts;var p=Math.min((ts-t0)/dur,1),e=1-Math.pow(1-p,3);n.textContent=(target*e).toFixed(dec)+(p<1?'':suf);if(p<1)requestAnimationFrame(f)}
    n.textContent=(0).toFixed(dec);requestAnimationFrame(f);
  }
  d.querySelectorAll('[data-count]').forEach(function(n){setTimeout(function(){count(n)},500)});

  /* reveal + roadmap meter */
  var fill=$('#fill');
  if('IntersectionObserver' in window){
    var io=new IntersectionObserver(function(es){es.forEach(function(e){if(e.isIntersecting){e.target.classList.add('in');io.unobserve(e.target)}})},{threshold:.12,rootMargin:'0px 0px -6% 0px'});
    d.querySelectorAll('.rv').forEach(function(n){io.observe(n)});
    var mo=new IntersectionObserver(function(es){es.forEach(function(e){if(e.isIntersecting){fill.classList.add('go');mo.disconnect()}})},{threshold:.4});
    mo.observe(fill.parentNode);
  }else{d.querySelectorAll('.rv').forEach(function(n){n.classList.add('in')});fill.classList.add('go')}

  /* active nav link */
  var links={};d.querySelectorAll('#links a').forEach(function(a){links[a.getAttribute('href').slice(1)]=a});
  if('IntersectionObserver' in window){
    var so=new IntersectionObserver(function(es){es.forEach(function(e){
      if(e.isIntersecting){Object.keys(links).forEach(function(k){links[k].removeAttribute('aria-current')});var a=links[e.target.id];if(a)a.setAttribute('aria-current','true')}
    })},{rootMargin:'-45% 0px -50% 0px'});
    ['about','skills','genai','projects','experience','contact'].forEach(function(id){var s=d.getElementById(id);if(s)so.observe(s)});
  }

  /* scroll progress */
  var bar=$('#bar'),pend=false;
  function prog(){pend=false;var h=root.scrollHeight-root.clientHeight;bar.style.transform='scaleX('+(h>0?Math.min(root.scrollTop/h,1):0)+')'}
  window.addEventListener('scroll',function(){if(!pend){pend=true;requestAnimationFrame(prog)}},{passive:true});prog();

  /* copy email */
  var toast=$('#toast'),tt;
  function say(m){toast.textContent=m;toast.classList.add('show');clearTimeout(tt);tt=setTimeout(function(){toast.classList.remove('show')},1800)}
  $('#copymail').addEventListener('click',function(){
    var txt=$('#mailtxt').textContent.trim();
    function fb(){try{var r=d.createRange();r.selectNodeContents($('#mailtxt'));var s=getSelection();s.removeAllRanges();s.addRange(r);say('Press Ctrl+C to copy')}catch(e){}}
    if(navigator.clipboard&&navigator.clipboard.writeText){navigator.clipboard.writeText(txt).then(function(){say('Email copied')}).catch(fb)}else{fb()}
  });
})();
</script>
</body>
</html>


















































































<!-- <div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0F0C29,25:302B63,50:4C1D95,75:7C3AED,100:A78BFA&height=260&section=header&text=NAVEEN%20KASHYAP&fontSize=62&fontColor=ffffff&animation=fadeIn&fontAlignY=36&desc=Full%20Stack%20Engineer%20%E2%80%A2%20MERN%20Specialist%20%E2%80%A2%20AI%20Product%20Developer&descAlignY=55&descSize=17" />

<a href="https://real-portfolio-26.vercel.app/">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=800&size=28&duration=2800&pause=800&color=A78BFA&background=00000000&center=true&vCenter=true&multiline=false&width=800&height=45&lines=%3E+Full+Stack+Developer+%7C+MERN+Specialist;%3E+Real-Time+Systems+with+WebRTC+%26+Socket.io;%3E+AI+Product+Engineering+with+OpenAI+API;%3E+React+%E2%80%A2+Next.js+%E2%80%A2+Node+%E2%80%A2+MongoDB+%E2%80%A2+TypeScript;%3E+Clean+Architecture.+Production+Mindset." alt="Typing SVG" />
</a>

<br/>

<img src="https://raw.githubusercontent.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/main/rainbow-line.gif" width="100%" height="4" />

<br/>

<img src="https://img.shields.io/badge/B.Tech-CSE-4C1D95?style=for-the-badge&labelColor=0F0C29&logo=graduation-cap" />
<img src="https://img.shields.io/badge/2022%20%E2%80%93%202026-Apollo%20Institute-5B21B6?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/CGPA-7.0%2F10-6D28D9?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/Kanpur-Uttar%20Pradesh%2C%20IN-7C3AED?style=for-the-badge&logo=googlemaps&logoColor=white&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/Status-Open%20to%20Work-00E676?style=for-the-badge&labelColor=0F0C29" />

<br/><br/>

<a href="https://real-portfolio-26.vercel.app/">
  <img src="https://img.shields.io/badge/PORTFOLIO-000000?style=for-the-badge&logo=vercel&logoColor=white" />
</a>
<a href="https://linkedin.com/in/naveen-kashyap08/">
  <img src="https://img.shields.io/badge/LINKEDIN-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
</a>
<a href="mailto:nk1910479@gmail.com">
  <img src="https://img.shields.io/badge/EMAIL-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
</a>
<a href="https://github.com/naveenkashyap2">
  <img src="https://img.shields.io/badge/GITHUB-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>
<a href="https://leetcode.com/naveenkyp854/">
  <img src="https://img.shields.io/badge/LEETCODE-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" />
</a>

<br/><br/>

<img src="https://komarev.com/ghpvc/?username=naveenkashyap2&label=PROFILE+VIEWS&color=7c3aed&style=for-the-badge" />
<img src="https://img.shields.io/github/followers/naveenkashyap2?label=FOLLOWERS&style=for-the-badge&color=A78BFA&labelColor=0F0C29&logo=github" />
<img src="https://img.shields.io/github/stars/naveenkashyap2?label=TOTAL%20STARS&style=for-the-badge&color=FFD700&labelColor=0F0C29&logo=github" />

<br/>

<img src="https://raw.githubusercontent.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/main/rainbow-line.gif" width="100%" height="4" />

</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%92%A0%20%20A%20B%20O%20U%20T%20%20%20M%20E&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<br/>

<img align="right" width="330" src="https://raw.githubusercontent.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/main/Developer.gif" />

I am a **Full Stack Developer** specializing in the **MERN stack**, focused on designing and shipping production-grade web applications with clean architecture, predictable performance, and measurable user impact.

🟣 &nbsp;My work spans the **complete delivery lifecycle** — REST API design, authentication systems, and database modeling on the backend; component-driven interfaces, state management, and responsive design systems on the frontend.

🔵 &nbsp;I build **real-time platforms** using **WebRTC** and **Socket.io**, delivering low-latency peer-to-peer audio/video and live messaging for multiple concurrent users.

🟢 &nbsp;I ship **applied AI** to production — integrating the **OpenAI API** into live products and using AI-augmented workflows to accelerate delivery without compromising engineering rigor.

🟡 &nbsp;I approach every build with a **product engineering mindset**: understand the problem, define the constraints, ship a scalable solution, then measure and refine.

<br clear="right"/>

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=2500&pause=700&color=00E676&background=00000000&center=true&vCenter=true&width=900&lines=OPEN+TO%3A++Full+Stack+Engineer+%E2%80%A2+Frontend+Engineer+%E2%80%A2+Backend+%2F+API+Engineering;OPEN+TO%3A++AI+Product+Engineering+%E2%80%A2+Remote+%26+Hybrid+Roles+%E2%80%A2+Open+Source" />

</div>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%E2%9A%A1%20%20T%20E%20C%20H%20%20%20S%20T%20A%20C%20K&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<div align="center">

<br/>

### `01` &nbsp;Languages

<img src="https://skillicons.dev/icons?i=js,ts,java,html,css&theme=dark&perline=5" />

<img src="https://img.shields.io/badge/JavaScript%20ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" />
<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" />

<br/><br/>

### `02` &nbsp;Frontend

<img src="https://skillicons.dev/icons?i=react,nextjs,tailwind,bootstrap,redux,figma&theme=dark&perline=6" />

<img src="https://img.shields.io/badge/React.js-61DAFB?style=flat-square&logo=react&logoColor=black" />
<img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
<img src="https://img.shields.io/badge/Framer%20Motion-0055FF?style=flat-square&logo=framer&logoColor=white" />
<img src="https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white" />

<br/><br/>

### `03` &nbsp;Backend & Databases

<img src="https://skillicons.dev/icons?i=nodejs,express,mongodb,postgres,mysql,firebase&theme=dark&perline=6" />

<img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white" />
<img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white" />
<img src="https://img.shields.io/badge/WebRTC-333333?style=flat-square&logo=webrtc&logoColor=white" />

<br/><br/>

### `04` &nbsp;Cloud, DevOps & Tooling

<img src="https://skillicons.dev/icons?i=azure,git,github,vercel,netlify,vscode,idea,postman&theme=dark&perline=8" />

<img src="https://img.shields.io/badge/Microsoft%20Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" />
<img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" />
<img src="https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white" />
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white" />

<br/><br/>

### `05` &nbsp;Core Concepts

<img src="https://img.shields.io/badge/REST%20API%20Design-4C1D95?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/JWT%20Authentication-5B21B6?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/SSR%20%2F%20SSG-6D28D9?style=for-the-badge&labelColor=0F0C29" />
<br/>
<img src="https://img.shields.io/badge/WebSockets-7C3AED?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/Component%20Architecture-8B5CF6?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/Responsive%20Design-A78BFA?style=for-the-badge&labelColor=0F0C29" />

</div>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%A7%A0%20%20A%20I%20%20%2F%20%20M%20L%20%20%20E%20X%20P%20E%20R%20T%20I%20S%20E&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<br/>

| 🎯 Domain | 📊 Proficiency | 🔍 Details |
| :--- | :---: | :--- |
| **LLM API Integration** | ![](https://img.shields.io/badge/ADVANCED-00E676?style=flat-square&labelColor=0F0C29) | Production integration of the **OpenAI API** — prompt pipelines, streaming responses, token/cost control, and structured output handling via Express.js routes. |
| **AI Product Engineering** | ![](https://img.shields.io/badge/ADVANCED-00E676?style=flat-square&labelColor=0F0C29) | Shipped AI-first products end to end: code generation tooling, resume intelligence, snippet history dashboards, and multi-language output rendering. |
| **Prompt Engineering** | ![](https://img.shields.io/badge/ADVANCED-00E676?style=flat-square&labelColor=0F0C29) | Deterministic, constraint-driven prompts for code generation, refactoring, and documentation with reproducible output quality. |
| **AI-Augmented Development** | ![](https://img.shields.io/badge/ADVANCED-00E676?style=flat-square&labelColor=0F0C29) | Daily use of **ChatGPT, Claude, Gemini, Cursor, Blackbox AI** for architecture reviews, debugging, test scaffolding, and delivery acceleration. |
| **Applied NLP Features** | ![](https://img.shields.io/badge/INTERMEDIATE-FFA116?style=flat-square&labelColor=0F0C29) | Text generation, summarization, and content structuring surfaced through clean React interfaces. |
| **AI UX Patterns** | ![](https://img.shields.io/badge/INTERMEDIATE-FFA116?style=flat-square&labelColor=0F0C29) | Live preview, syntax-highlighted output, incremental rendering, and graceful failure states for latency-bound AI interactions. |

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%9A%80%20%20F%20E%20A%20T%20U%20R%20E%20D%20%20%20P%20R%20O%20J%20E%20C%20T%20S&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<br/>

<details open>
<summary><h3>🎥 &nbsp;Streamify — Full Stack Video & Chat Calling Platform</h3></summary>

<br/>

<div align="center">
<img src="https://img.shields.io/badge/MERN%20Stack-4C1D95?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/WebRTC-333333?style=for-the-badge&logo=webrtc&logoColor=white" />
<img src="https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socketdotio&logoColor=white" />
<img src="https://img.shields.io/badge/Jan%202026%20%E2%80%93%20Feb%202026-7C3AED?style=for-the-badge&labelColor=0F0C29" />
</div>

<br/>

> A real-time communication platform delivering peer-to-peer video calling and instant messaging with persistent user profiles and call history.

| 🔧 Attribute | 📌 Detail |
| :--- | :--- |
| **Stack** | ![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Node](https://img.shields.io/badge/-Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) ![Express](https://img.shields.io/badge/-Express-000000?style=flat-square&logo=express&logoColor=white) ![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) ![WebRTC](https://img.shields.io/badge/-WebRTC-333333?style=flat-square&logo=webrtc&logoColor=white) ![Socket.io](https://img.shields.io/badge/-Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white) |
| **Scale** | Multiple concurrent users across independent call rooms and live chat channels |
| **Performance** | Low-latency peer-to-peer audio/video streaming via direct WebRTC connections |
| **Security** | JWT-based authentication, protected routes, server-side session validation |
| **Impact** | Complete communication suite — calling, chat, profiles, and history in one platform |
| **Repository** | [![Repo](https://img.shields.io/badge/View%20Source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/naveenkashyap2) |

**Engineering Notes** — Streamify combines a **WebRTC** signaling layer with **Socket.io** event channels so media travels peer-to-peer while presence, room state, and messaging remain server-coordinated. **MongoDB** persists user profiles and call history, **JWT** secures every authenticated route, and a responsive **Tailwind CSS** interface delivers a consistent experience across desktop and mobile.

</details>

<details open>
<summary><h3>🤖 &nbsp;AI Code Generator — MERN + OpenAI API</h3></summary>

<br/>

<div align="center">
<img src="https://img.shields.io/badge/AI%20Powered-10A37F?style=for-the-badge&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/MERN%20Stack-4C1D95?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/Developer%20Tooling-6D28D9?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/Mar%202026%20%E2%80%93%20Apr%202026-7C3AED?style=for-the-badge&labelColor=0F0C29" />
</div>

<br/>

> An AI-powered developer tool that generates, previews, and exports production-ready code across multiple programming languages.

| 🔧 Attribute | 📌 Detail |
| :--- | :--- |
| **Stack** | ![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Node](https://img.shields.io/badge/-Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) ![Express](https://img.shields.io/badge/-Express-000000?style=flat-square&logo=express&logoColor=white) ![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) ![OpenAI](https://img.shields.io/badge/-OpenAI%20API-10A37F?style=flat-square&logo=openai&logoColor=white) |
| **Scale** | Multi-language generation with per-user snippet history |
| **Performance** | Server-side prompt pipelines with optimized response handling and syntax-highlighted rendering |
| **Security** | Server-held API credentials, validated request payloads, isolated user data access |
| **Impact** | Significant reduction in boilerplate coding time for repetitive implementation work |
| **Repository** | [![Repo](https://img.shields.io/badge/View%20Source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/naveenkashyap2) |

**Engineering Notes** — The application routes user prompts through **Express.js** pipelines that shape context before reaching the **OpenAI API**, keeping credentials server-side and responses consistent. A **MongoDB**-backed history dashboard lets users revisit, manage, and reuse generated snippets, while the React client provides live preview, syntax highlighting, and one-click copy.

</details>

<details open>
<summary><h3>📄 &nbsp;Resumify AI — AI-Powered Resume Builder</h3></summary>

<br/>

<div align="center">
<a href="https://resume-builder-74fb.vercel.app/">
  <img src="https://img.shields.io/badge/%E2%96%B6%20LIVE%20DEMO-00E676?style=for-the-badge&logoColor=black&labelColor=0F0C29" />
</a>
<img src="https://img.shields.io/badge/20%2B%20Templates-6D28D9?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/ATS%20Friendly-A78BFA?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/Jan%202026%20%E2%80%93%20Apr%202026-7C3AED?style=for-the-badge&labelColor=0F0C29" />
</div>

<br/>

> A modern resume platform that turns structured user input into professional, ATS-friendly one-page resumes.

| 🔧 Attribute | 📌 Detail |
| :--- | :--- |
| **Stack** | ![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Tailwind](https://img.shields.io/badge/-Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) ![Framer](https://img.shields.io/badge/-Framer%20Motion-0055FF?style=flat-square&logo=framer&logoColor=white) ![Vercel](https://img.shields.io/badge/-Vercel-000000?style=flat-square&logo=vercel&logoColor=white) |
| **Scale** | 20+ professionally designed templates with instant switching |
| **Performance** | Real-time live preview with fast re-rendering and reusable component architecture |
| **Security** | Client-side data handling — resume content never leaves the user's browser |
| **Impact** | Complete, download-ready ATS-friendly resume in minutes |
| **Live Demo** | [![Live](https://img.shields.io/badge/resume--builder--74fb.vercel.app-000000?style=flat-square&logo=vercel&logoColor=white)](https://resume-builder-74fb.vercel.app/) [![Repo](https://img.shields.io/badge/Source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/naveenkashyap2) |

**Engineering Notes** — Built on a **reusable component architecture** where every template consumes a single normalized data model, so adding a template requires zero changes to form logic. **Framer Motion** drives interaction polish, **Tailwind CSS** enforces layout consistency, and one-click PDF export produces print-accurate output from the same render tree used for live preview.

</details>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%92%BC%20%20E%20X%20P%20E%20R%20I%20E%20N%20C%20E&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<br/>

### 🟣 &nbsp;Frontend Developer Intern &nbsp;·&nbsp; [CODEXINTERN](https://codexintern.com)

<img src="https://img.shields.io/badge/Apr%202025%20%E2%80%93%20Sep%202025-4C1D95?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/React%20Developer-6D28D9?style=for-the-badge&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/Remote%20%E2%80%94%20Delhi-7C3AED?style=for-the-badge&labelColor=0F0C29" />

<br/><br/>

Delivered production-ready frontend applications as part of a remote engineering team, owning feature development from component design through API integration and performance tuning.

**⚙️ Scope of Work**

- ▸ Developed and optimized **production-ready frontend applications** using React.js, JavaScript, Tailwind CSS, and Framer Motion with a strong focus on performance and responsiveness.
- ▸ Designed and implemented a **Resume Builder Application** featuring dynamic resume generation, multiple templates, live preview, form validation, and PDF download functionality.
- ▸ Integrated **REST APIs**, managed application state, and engineered **reusable React components** to improve scalability, maintainability, and user experience.
- ▸ Maintained consistent UI standards and responsive behavior across desktop, tablet, and mobile breakpoints.

**🏷️ Skills Applied**

<img src="https://img.shields.io/badge/React.js-61DAFB?style=flat-square&logo=react&logoColor=black" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
<img src="https://img.shields.io/badge/Framer%20Motion-0055FF?style=flat-square&logo=framer&logoColor=white" />
<img src="https://img.shields.io/badge/REST%20API-4C1D95?style=flat-square&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/State%20Management-5B21B6?style=flat-square&labelColor=0F0C29" />
<img src="https://img.shields.io/badge/Responsive%20UI-6D28D9?style=flat-square&labelColor=0F0C29" />

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%8F%86%20%20A%20C%20H%20I%20E%20V%20E%20M%20E%20N%20T%20S&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<br/>

<div align="center">

| 🏅 Recognition | 📋 Details |
| :--- | :--- |
| 🥇 **Top 5% of Class** | Ranked in the top 5% of the B.Tech Computer Science cohort at Apollo Institute of Technology. |
| ☁️ **Microsoft Azure Certified** | AZ-900 Azure Fundamentals — cloud concepts, core services, security, and governance. |
| 🚀 **Production Deployments** | Multiple full stack applications shipped live on Vercel with real users and public demos. |
| ⚡ **Real-Time Systems** | Engineered a WebRTC + Socket.io platform supporting concurrent low-latency audio/video sessions. |
| 🤖 **AI Product Delivery** | Built and deployed AI-integrated products using the OpenAI API within full stack architectures. |
| 👥 **Technical Community** | Active participant in technical clubs and inter-college coding contests. |

</div>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%93%9C%20%20C%20E%20R%20T%20I%20F%20I%20C%20A%20T%20I%20O%20N%20S&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<div align="center">

<br/>

**☁️ &nbsp;Microsoft**

<img src="https://img.shields.io/badge/AZ--900%20%E2%80%94%20Azure%20Fundamentals-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white&labelColor=0F0C29" />

<br/><br/>

**🎓 &nbsp;Professional Development**

<a href="https://www.udemy.com/certificate/UC-c0e8dc21-8e8b-4f6e-9d05-5d109a9523cd/">
  <img src="https://img.shields.io/badge/Udemy%20%E2%80%94%20Full%20Stack%20Web%20Development-A435F0?style=for-the-badge&logo=udemy&logoColor=white&labelColor=0F0C29" />
</a>

<br/><br/>

**🤖 &nbsp;AI Productivity Tooling**

<img src="https://img.shields.io/badge/ChatGPT-10A37F?style=for-the-badge&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/Claude%20AI-D97757?style=for-the-badge&logo=anthropic&logoColor=white" />
<img src="https://img.shields.io/badge/Gemini%20AI-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" />
<br/>
<img src="https://img.shields.io/badge/Cursor%20AI-000000?style=for-the-badge&logo=cursor&logoColor=white" />
<img src="https://img.shields.io/badge/Blackbox%20AI-1A1A1A?style=for-the-badge&logo=blackbox&logoColor=white" />

</div>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%92%BB%20%20C%20O%20D%20I%20N%20G%20%20%20P%20R%20O%20F%20I%20L%20E%20S&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<div align="center">

<br/>

<a href="https://leetcode.com/naveenkyp854/">
  <img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black&labelColor=0F0C29" height="42" />
</a>
&nbsp;
<a href="https://github.com/naveenkashyap2">
  <img src="https://img.shields.io/badge/GeeksforGeeks-2F8D46?style=for-the-badge&logo=geeksforgeeks&logoColor=white&labelColor=0F0C29" height="42" />
</a>

<br/><br/>

<a href="https://github.com/naveenkashyap2">
  <img src="https://img.shields.io/badge/HackerRank-00EA64?style=for-the-badge&logo=hackerrank&logoColor=black&labelColor=0F0C29" height="42" />
</a>
&nbsp;
<a href="https://github.com/naveenkashyap2">
  <img src="https://img.shields.io/badge/CodeChef-5B4638?style=for-the-badge&logo=codechef&logoColor=white&labelColor=0F0C29" height="42" />
</a>

<br/><br/>

<img src="https://leetcard.jacoblin.cool/naveenkyp854?theme=nord&font=JetBrains%20Mono&ext=heatmap&border=0&radius=16" alt="LeetCode Stats" />

</div>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%93%8A%20%20G%20I%20T%20H%20U%20B%20%20%20A%20N%20A%20L%20Y%20T%20I%20C%20S&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<div align="center">

<br/>

<img width="49%" src="https://github-readme-stats.vercel.app/api?username=naveenkashyap2&show_icons=true&count_private=true&hide_border=true&border_radius=16&title_color=A78BFA&icon_color=7C3AED&text_color=C9D1D9&bg_color=30,0F0C29,302B63,24243E&ring_color=A78BFA" />
<img width="49%" src="https://github-readme-streak-stats.herokuapp.com/?user=naveenkashyap2&hide_border=true&border_radius=16&background=30,0F0C29,302B63,24243E&stroke=7C3AED&ring=A78BFA&fire=FF6B6B&currStreakLabel=A78BFA&sideLabels=C9D1D9&currStreakNum=FFFFFF&sideNums=FFFFFF&dates=8B949E" />

<br/><br/>

<img width="42%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=naveenkashyap2&layout=compact&langs_count=10&hide_border=true&border_radius=16&title_color=A78BFA&text_color=C9D1D9&bg_color=30,0F0C29,302B63,24243E" />

<br/><br/>

<img width="49%" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=naveenkashyap2&theme=radical" />
<img width="49%" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=naveenkashyap2&theme=radical" />

<br/>

<img width="49%" src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=naveenkashyap2&theme=radical" />
<img width="49%" src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=naveenkashyap2&theme=radical&utcOffset=5" />

</div>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%8F%85%20%20G%20I%20T%20H%20U%20B%20%20%20T%20R%20O%20P%20H%20I%20E%20S&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<div align="center">

<br/>

<img width="98%" src="https://github-profile-trophy.vercel.app/?username=naveenkashyap2&theme=radical&no-frame=true&no-bg=true&column=7&margin-w=6&margin-h=6" />

</div>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%93%88%20%20C%20O%20N%20T%20R%20I%20B%20U%20T%20I%20O%20N%20%20%20A%20C%20T%20I%20V%20I%20T%20Y&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<div align="center">

<br/>

<img width="98%" src="https://github-readme-activity-graph.vercel.app/graph?username=naveenkashyap2&bg_color=0F0C29&color=A78BFA&line=7C3AED&point=00E676&area=true&area_color=4C1D95&hide_border=true&radius=16&custom_title=Contribution%20Graph" />

</div>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%90%8D%20%20C%20O%20N%20T%20R%20I%20B%20U%20T%20I%20O%20N%20%20%20S%20N%20A%20K%20E&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<div align="center">

<br/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake.svg" />
  <img alt="Contribution Snake Animation" src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake.svg" />
</picture>

</div>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%8E%AF%20%20C%20U%20R%20R%20E%20N%20T%20%20%20F%20O%20C%20U%20S&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<br/>

```yaml
name: Naveen Kashyap
role: Full Stack Developer
location: Kanpur, Uttar Pradesh, India
availability: Open to Opportunities

learning:
  - Advanced System Design & Scalable Architecture
  - TypeScript at Production Scale
  - Next.js App Router, SSR & Edge Rendering
  - Database Optimization & Query Performance

building:
  - Real-Time Communication Platforms (WebRTC + Socket.io)
  - AI-Integrated Developer Tooling (OpenAI API)
  - Production-Grade MERN Applications

exploring:
  - LLM Application Architecture & Prompt Pipelines
  - Cloud Deployment & CI/CD Automation
  - Microservices & API Gateway Patterns
  - Web Performance Engineering

open_to:
  - Full Stack Engineer Roles
  - Frontend / Backend Engineering Roles
  - AI Product Engineering
  - Remote & Hybrid Opportunities
  - Open Source Collaboration

contact:
  email: nk1910479@gmail.com
  portfolio: https://real-portfolio-26.vercel.app/
  linkedin: https://linkedin.com/in/naveen-kashyap08/
```

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12&height=3" />
</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0F0C29,50:4C1D95,100:7C3AED&height=48&section=header&text=%F0%9F%A4%9D%20%20L%20E%20T%20%E2%80%99%20S%20%20%20C%20O%20N%20N%20E%20C%20T&fontSize=22&fontColor=ffffff&fontAlignY=62&animation=fadeIn" />
</div>

<div align="center">

<br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=3000&pause=900&color=A78BFA&background=00000000&center=true&vCenter=true&width=700&lines=Always+open+to+meaningful+collaborations;Let%E2%80%99s+build+something+exceptional+together;Reach+out+%E2%80%94+I+reply+to+every+message." />

<br/><br/>

<a href="mailto:nk1910479@gmail.com">
  <img src="https://img.shields.io/badge/nk1910479%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0F0C29" height="40" />
</a>
&nbsp;
<a href="https://linkedin.com/in/naveen-kashyap08/">
  <img src="https://img.shields.io/badge/naveen--kashyap08-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0F0C29" height="40" />
</a>

<br/><br/>

<a href="https://github.com/naveenkashyap2">
  <img src="https://img.shields.io/badge/naveenkashyap2-181717?style=for-the-badge&logo=github&logoColor=white&labelColor=0F0C29" height="40" />
</a>
&nbsp;
<a href="https://real-portfolio-26.vercel.app/">
  <img src="https://img.shields.io/badge/View%20Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white&labelColor=0F0C29" height="40" />
</a>

<br/><br/>

<img src="https://raw.githubusercontent.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/main/rainbow-line.gif" width="100%" height="4" />

</div>

<br/>

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=22&duration=4000&pause=1000&color=A78BFA&background=00000000&center=true&vCenter=true&width=850&lines=%22Write+code+that+scales.+Build+products+that+matter.+Ship+with+intent.%22" />

<br/>

⭐ **If my work resonates with you, consider starring a repository — it genuinely helps.**

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:A78BFA,25:7C3AED,50:4C1D95,75:302B63,100:0F0C29&height=180&section=footer&text=Thanks%20for%20visiting!&fontSize=28&fontColor=ffffff&animation=twinkling&fontAlignY=70" />

</div>
 -->
