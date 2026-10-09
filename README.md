[王佳妮的主页 · 个人介绍.html](https://github.com/user-attachments/files/33251364/default.html)
<!DOCTYPE html>
<!-- saved from url=(0027)http://192.168.43.204:9999/ -->
<html lang="zh-CN"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <script type="module">
import RefreshRuntime from "/@react-refresh"
RefreshRuntime.injectIntoGlobalHook(window)
window.$RefreshReg$ = () => {}
window.$RefreshSig$ = () => (type) => type
window.__vite_plugin_react_preamble_installed__ = true
</script>

    <script type="module" src="./王佳妮的主页 · 个人介绍_files/client"></script>

    
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="王佳妮的个人主页：个人介绍、项目作品与爱好展示。">
    <title>王佳妮的主页 · 个人介绍</title>
  <script>
(function () {
  if (window.__ACCIO_BOOTSTRAP__) return;
  window.__ACCIO_BOOTSTRAP__ = true;

  var SKIP = { SCRIPT: 1, STYLE: 1, NOSCRIPT: 1, TEMPLATE: 1, SVG: 1 };

  function annotateEl(el, segs) {
    if (SKIP[el.tagName]) return;
    el.setAttribute('data-edit-path', segs.join('-'));
    var ci = 0;
    for (var i = 0; i < el.children.length; i++) {
      var ch = el.children[i];
      if (SKIP[ch.tagName]) continue;
      annotateEl(ch, segs.concat(String(ci)));
      ci++;
    }
  }

  function annotateDom() {
    var body = document.body;
    if (!body) return;
    var ci = 0;
    for (var i = 0; i < body.children.length; i++) {
      var ch = body.children[i];
      if (SKIP[ch.tagName]) continue;
      annotateEl(ch, [String(ci)]);
      ci++;
    }
  }

  function buildOverlayHtml(loc) {
    return [
      '<canvas id="hlCanvas" aria-hidden="true"></canvas>',
      '<div class="etb-wrap hidden" id="etbWrap">',
      '  <div class="etb" onmousedown="event.stopPropagation()">',
      '    <div style="display:flex;align-items:center;gap:12px">',
      '      <button class="badge" id="badgeBtn" onclick="toggleCards()">',
      '        <svg width="18" height="18" viewBox="0 0 16 16" fill="currentColor"><path d="M7.529 7.529c.188-.189.471-.248.719-.148l6.666 2.666a.667.667 0 01.02 1.239l-2.599 1.027-1.027 2.599a.667.667 0 01-1.238-.02L7.404 8.225a.667.667 0 01.125-.696zM1.333 12.667a.667.667 0 011.334 0c0 .177.07.346.195.472.126.125.295.195.472.195a.667.667 0 010 1.333 2 2 0 01-2-2zM7.333 13.333a.667.667 0 010 1.334H6a.667.667 0 010-1.334h1.333zM10.663 12.863l.518-1.308.028-.063a.667.667 0 01.347-.312l1.308-.518-3.666-1.466 1.466 3.666zM1.333 10V9.333a.667.667 0 011.334 0V10a.667.667 0 01-1.334 0zM13.333 7.333V6a.667.667 0 011.334 0v1.333a.667.667 0 01-1.334 0zM1.333 6.667V6a.667.667 0 011.334 0v.667a.667.667 0 01-1.334 0zM1.333 3.333c0-.53.211-1.039.586-1.414A2 2 0 013.333 1.333a.667.667 0 010 1.334c-.177 0-.346.07-.471.195a.667.667 0 00-.196.471.667.667 0 01-1.333 0zM13.333 3.333c0-.177-.07-.346-.195-.471a.667.667 0 00-.472-.196.667.667 0 010-1.333 2 2 0 012 2 .667.667 0 01-1.333 0zM6.667 1.333a.667.667 0 010 1.334H6a.667.667 0 010-1.334h.667zM10 1.333a.667.667 0 010 1.334h-.667a.667.667 0 010-1.334H10z"/></svg>',
      '        <span class="badge-n" id="badgeN">0</span>',
      '      </button>',
      '    </div>',
      '    <div class="ab">',
      '      <button class="b-dis" id="disBtn" disabled onclick="doDiscard()">' + loc.discardBtn + '</button>',
      '      <button class="b-app" id="appBtn" disabled onclick="doApply()">' + loc.applyBtn + '</button>',
      '    </div>',
      '    <div class="ecards hidden" id="ecards"></div>',
      '  </div>',
      '</div>',
      '<div class="si-overlay" id="siOverlay">',
      '  <div class="si-panel hidden" id="siPanel" onmousedown="event.stopPropagation()">',
      '    <div class="si-header-wrap"><div class="si-comment-row"><div class="si-comment-wrap">',
      '      <textarea class="si-comment" id="siComment" rows="1" placeholder="' + loc.describeChangePlaceholder + '"></textarea>',
      '    </div><div class="si-panel-actions">',
      '      <button class="si-confirm-btn" id="siConfirmBtn" onclick="confirmSI()">' + loc.editorConfirm + '</button>',
      '      <button class="si-close-btn" id="siCloseBtn" title="' + loc.closeTitle + '">',
      '        <svg viewBox="0 0 12 12" width="10" height="10" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><line x1="1" y1="1" x2="11" y2="11"/><line x1="11" y1="1" x2="1" y2="11"/></svg>',
      '      </button></div></div></div>',
      '    <div class="si-content-area hidden" id="siContentArea"></div>',
      '    <div class="si-tabs">',
      '      <button class="si-tab active" id="siTabStyle" onclick="setSITab(\'styles\')">' + loc.styleTab + '</button>',
      '      <button class="si-tab" id="siTabLayout" onclick="setSITab(\'spacing\')">' + loc.layoutTab + '</button>',
      '    </div>',
      '    <div class="si-body-wrap"><div class="si-body-pane" id="siPaneStyle"></div><div class="si-body-pane" id="siPaneLayout"></div></div>',
      '  </div>',
      '</div>',
      '<svg id="cmSvg" style="position:fixed;top:0;left:0;width:100%;height:100%;pointer-events:none;z-index:2147483643"></svg>',
      '<div id="cmBox" style="position:fixed;top:0;left:0;width:100%;height:100%;pointer-events:none;z-index:2147483644"></div>',
    ].join('');
  }

  function doInject(msg) {
    if (window.__ACCIO_EDITOR_INJECTED__) {
      annotateDom();
      window.parent.postMessage({ type: 'ACCIO_EDITOR_READY' }, '*');
      return;
    }
    window.__ACCIO_EDITOR_INJECTED__ = true;
    var styleEl = document.createElement('style');
    styleEl.textContent = msg.css;
    document.head.appendChild(styleEl);
    var wrap = document.createElement('div');
    wrap.id = '__ba_editor_overlay__';
    wrap.innerHTML = buildOverlayHtml(msg.loc);
    document.body.appendChild(wrap);
    annotateDom();
    window.__BA_debounce__ = (function() {
      return function debounce(fn, wait) {
        var timer = null;
        return function() { var a = arguments; if (timer) clearTimeout(timer); timer = setTimeout(function() { fn.apply(this, a); }, wait); };
      };
    })();
    window.__BA_EDITOR_LOC__ = msg.loc;
    try { (0, eval)(msg.bundle); } catch(e) { console.error('[accio] bundle eval error', e); }
    try { (0, eval)(msg.init); }   catch(e) { console.error('[accio] init eval error', e); }
    window.parent.postMessage({ type: 'ACCIO_EDITOR_READY' }, '*');
  }

  function doReinit() {
    annotateDom();
    window.parent.postMessage({ type: 'ACCIO_EDITOR_READY' }, '*');
  }

  window.addEventListener('message', function(e) {
    var d = e.data;
    if (!d || !d.type) return;
    if (d.type === 'ACCIO_INJECT_EDITOR') { doInject(d); return; }
    if (d.type === 'ACCIO_REINIT_EDITOR') { doReinit(); return; }
  });

  // vite 编译错误红屏探测并上报(在 iframe 内部跑,对自己 document 同源,绕开父窗口跨域读不到的限制)。
  // vite client 编译失败时往 body 注入 vite-error-overlay 自定义元素;这里监听其增删,
  // 通过 postMessage 把 hasError 状态告诉父窗口,由父窗口结合流式状态决定是否亮提示。
  // 不禁用 vite 原生 overlay:本脚本万一没跑,原生红屏仍会暴露错误,绝不静默吞掉最终错误。
  (function () {
    var last = null;
    function report() {
      var has = false;
      try { has = !!document.querySelector('vite-error-overlay'); } catch (err) {}
      if (has === last) return;
      last = has;
      window.parent.postMessage({ type: 'ACCIO_VITE_OVERLAY', data: { hasError: has } }, '*');
    }
    try {
      new MutationObserver(report).observe(document.documentElement, { childList: true, subtree: true });
    } catch (err) {}
    report();
  })();

  // 路由跟随：iframe 内导航（点链接 / SPA 路由跳转）后，把当前路径上报父窗口，
  // 让工具栏的路由输入框跟随变化。覆盖三种导航来源：
  //   - popstate / hashchange：浏览器前进后退、hash 路由
  //   - history.pushState / replaceState：SPA（react-router 等）编程式导航
  (function () {
    var last = null;
    function currentPath() {
      try {
        // 同时带上 hash（hash 路由站点用 #/instructor 这种形式）
        return location.pathname + location.search + location.hash;
      } catch (err) { return '/'; }
    }
    function report() {
      var p = currentPath();
      if (p === last) return;
      last = p;
      window.parent.postMessage({ type: 'ACCIO_ROUTE_CHANGE', data: { path: p } }, '*');
    }
    try {
      window.addEventListener('popstate', report);
      window.addEventListener('hashchange', report);
      // 包裹 pushState / replaceState：原生不触发 popstate，需手动钩。
      var _push = history.pushState;
      var _replace = history.replaceState;
      history.pushState = function () { var r = _push.apply(this, arguments); report(); return r; };
      history.replaceState = function () { var r = _replace.apply(this, arguments); report(); return r; };
    } catch (err) {}
    report();
  })();

  // 外链外开：拦截预览 iframe 内的外部 http(s) 链接，统一 postMessage 交给宿主
  // 用系统浏览器打开。覆盖面：<a> 点击（含 target=_blank）与 window.open 两条路径；
  // location.href= / location.assign() 等编程式框内导航**暂不覆盖**（AI 生成站点
  // 中极少用，若成为真实场景需在 Electron 主进程 will-frame-navigate 层兜底）。
  // 不拦截同源链接（站内路由跳转）与非 http(s) 协议（mailto/tel 等维持默认行为）。
  // 背景：iframe 框内导航到 X-Frame-Options:deny 的站点（github 等）会直接白屏，
  // 且即使能加载，用户也会被困在预览里无法返回。
  (function () {
    function externalUrl(href) {
      try {
        var u = new URL(href, location.href);
        if (u.protocol !== 'http:' && u.protocol !== 'https:') return null;
        return u.origin === location.origin ? null : u.href;
      } catch (err) { return null; }
    }
    function openExternal(url) {
      window.parent.postMessage({ type: 'ACCIO_OPEN_EXTERNAL', data: { url: url } }, '*');
    }
    // capture 阶段拦截，保证站点自身 stopPropagation 的 handler 拦不住外开；
    // 只 preventDefault 不 stopPropagation，站点自己的点击副作用（埋点等）照常执行。
    document.addEventListener('click', function (e) {
      var el = e.target;
      while (el && el !== document.documentElement) {
        if (el.tagName === 'A' && el.getAttribute && el.getAttribute('href')) break;
        el = el.parentElement;
      }
      if (!el || el === document.documentElement || el.tagName !== 'A') return;
      var url = externalUrl(el.getAttribute('href'));
      if (!url) return;
      e.preventDefault();
      openExternal(url);
    }, true);
    // SPA 代码里的 window.open(外链) 同样外开。
    try {
      var _open = window.open;
      window.open = function (url) {
        var ext = url ? externalUrl(String(url)) : null;
        if (ext) { openExternal(ext); return null; }
        return _open.apply(window, arguments);
      };
    } catch (err) {}
  })();

  window.parent.postMessage({ type: 'ACCIO_BOOTSTRAP_READY' }, '*');
})();</script><style type="text/css" data-vite-dev-id="C:/Users/I/AccioWork/2026-10-09-14-49-12-722-5527ece6/cute-personal-site/src/components/hero/hero.css">/* Hero scene — 整页封面插图（入场页与首屏共用同一张、同一层水洗） */

.scene--hero {
  position: relative;
  min-height: 100svh;
  overflow: hidden;
}

/* 插图层：铺满整屏，保持比例裁切，不拉伸、不重复，居中 */
.cover-media {
  position: absolute;
  inset: 0;
  z-index: 0;
  background-color: var(--color-surface);
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}

/* 水洗层：让深棕文字在最浅的金色花纹上也足够清楚 */
.cover-wash {
  position: absolute;
  inset: 0;
  z-index: 1;
  background-image: linear-gradient(
      to bottom,
      rgba(255, 251, 239, 0.18) 0%,
      rgba(255, 251, 239, 0.34) 46%,
      rgba(255, 251, 239, 0.68) 100%
    ),
    radial-gradient(
      circle at 50% 50%,
      rgba(255, 251, 239, 0) 42%,
      rgba(255, 251, 239, 0.42) 100%
    );
  pointer-events: none;
}

/* 封面上的两处小星星，避开文字区 */
.cover-sparkle {
  z-index: var(--z-deco);
  opacity: 0.45;
}

.cover-sparkle--tl {
  top: 14%;
  left: 5%;
}

.cover-sparkle--br {
  bottom: 12%;
  right: 6%;
}

.hero-title {
  font-family: var(--font-display);
  font-size: var(--text-hero);
  font-weight: 700;
  line-height: 1.12;
  letter-spacing: -0.01em;
}

.hero-support {
  max-width: 32ch;
  margin-top: var(--space-sm);
  font-size: var(--text-lead);
  line-height: 1.75;
  color: var(--color-on-surface-soft);
}

.scroll-cue {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: var(--space-sm);
  margin-top: var(--space-md);
}

.scroll-cue__rule {
  width: 48px;
  border-top: 2px dotted var(--color-border-strong);
}

.profile-panel {
  position: relative;
  max-width: 560px;
  margin-left: auto;
  padding: var(--space-xl);
  border-radius: var(--rounded-blob) var(--rounded-blob) var(--rounded-blob)
    var(--rounded-md);
}

.profile-panel__ribbon {
  top: -18px;
  right: 24px;
}

.profile-panel__name {
  margin-top: var(--space-sm);
  font-family: var(--font-display);
  font-size: var(--text-panel);
  font-weight: 700;
  line-height: 1.3;
}

.profile-panel__tagline {
  margin-top: 6px;
  font-size: var(--text-small);
  color: var(--color-on-surface-soft);
}

.profile-facts {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: var(--space-md);
  margin-top: var(--space-lg);
  padding-bottom: var(--space-md);
}

.profile-fact__label {
  display: block;
  color: var(--color-tertiary-strong);
}

.profile-fact__value {
  margin: 6px 0 0;
  font-size: var(--text-small);
  font-weight: 500;
  overflow-wrap: break-word;
}

/* 封面上不用 on-surface-mute（对最浅的花纹对比偏低），统一用 on-surface-soft */
.scene--hero .micro-label {
  color: var(--color-on-surface-soft);
}

@media (max-width: 767px) {
  .scene--hero {
    min-height: 100svh;
  }

  .profile-panel {
    max-width: none;
    margin-left: 0;
    padding: var(--space-lg);
  }

  .profile-panel__ribbon {
    top: -14px;
    right: 18px;
  }

  .profile-facts {
    grid-template-columns: 1fr;
    gap: var(--space-sm);
  }

  .cover-sparkle--tl {
    top: 8%;
    left: 4%;
  }

  .cover-sparkle--br {
    bottom: 6%;
    right: 5%;
  }
}
</style><style type="text/css" data-vite-dev-id="C:/Users/I/AccioWork/2026-10-09-14-49-12-722-5527ece6/cute-personal-site/src/components/projects/projects.css">/* Projects scene */

.project-list {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: var(--card-gap);
}

.project-list__item {
  display: flex;
  min-width: 0;
}

.project-card {
  display: flex;
  flex-direction: column;
  gap: var(--space-md);
  width: 100%;
  min-height: 320px;
  padding: 20px;
  border-radius: var(--rounded-xl);
  border: 2px solid var(--color-border);
  background-color: var(--color-surface-card);
  box-shadow: var(--shadow-2);
  text-align: left;
  transition: transform var(--dur-expressive) var(--ease-spring),
    box-shadow var(--dur-standard) var(--ease-soft),
    border-color var(--dur-micro) linear;
}

.project-card:hover {
  transform: translateY(-8px) scale(1.02);
  box-shadow: var(--shadow-3);
  border-color: var(--color-primary-soft);
}

.project-card:active {
  transform: translateY(-2px);
}

.project-card--active {
  border-color: var(--color-secondary);
}

.project-card__cover {
  position: relative;
  display: block;
  aspect-ratio: 16 / 10;
  overflow: hidden;
  border-radius: var(--rounded-lg);
  border: 2px solid var(--color-surface-card);
  background-image: linear-gradient(
    135deg,
    var(--color-primary-tint),
    var(--color-tertiary-tint)
  );
}

.project-card__cover img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.project-card__tape {
  position: absolute;
  top: -8px;
  left: 18px;
}

.project-card__body {
  display: flex;
  flex-direction: column;
  gap: var(--space-xs);
  min-width: 0;
}

.project-card__title {
  font-family: var(--font-display);
  font-size: var(--text-card);
  font-weight: 700;
  line-height: 1.35;
  overflow-wrap: break-word;
}

.project-card__desc {
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
  font-size: var(--text-small);
  color: var(--color-on-surface-soft);
}

.project-card__tags,
.tag-row {
  display: flex;
  flex-wrap: wrap;
  gap: var(--space-xs);
  margin-top: var(--space-2xs);
}

.project-blush {
  position: static;
  margin-top: var(--space-sm);
  justify-content: flex-end;
}

/* ---- Detail overlay ---- */

.project-detail {
  display: grid;
  grid-template-columns: 44fr 56fr;
  gap: var(--space-2xl);
  margin-top: var(--space-lg);
}

.project-detail__media {
  position: relative;
  align-self: start;
  overflow: hidden;
  border-radius: var(--rounded-lg);
  border: 2px solid var(--color-border);
  background-image: linear-gradient(
    135deg,
    var(--color-primary-tint),
    var(--color-tertiary-tint)
  );
}

.project-detail__media img {
  width: 100%;
  height: auto;
  object-fit: cover;
}

.project-detail__body {
  display: flex;
  flex-direction: column;
  gap: var(--space-sm);
  min-width: 0;
}

.detail-title {
  font-family: var(--font-display);
  font-size: var(--text-detail);
  font-weight: 700;
  line-height: 1.16;
  letter-spacing: -0.01em;
  overflow-wrap: break-word;
}

.project-detail__summary {
  color: var(--color-on-surface-soft);
}

.project-detail__grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: var(--space-md);
  margin-top: var(--space-xs);
}

.info-card__text {
  margin-top: var(--space-xs);
  font-size: var(--text-small);
}

.bullet-list {
  display: flex;
  flex-direction: column;
  gap: 6px;
  margin-top: var(--space-xs);
  font-size: var(--text-small);
}

.bullet-list li {
  display: flex;
  align-items: flex-start;
  gap: var(--space-xs);
}

.bullet-list li svg {
  margin-top: 5px;
}

.action-row {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  gap: var(--space-md);
  margin-top: var(--space-md);
  padding-top: var(--space-md);
  border-top: 2px dotted var(--color-border-strong);
}

.action-row__buttons {
  display: flex;
  flex-wrap: wrap;
  gap: var(--space-sm);
}

@media (max-width: 1199px) {
  .project-card {
    min-height: 0;
  }
}

@media (max-width: 767px) {
  .project-list {
    grid-template-columns: 1fr;
    gap: var(--card-gap-mobile);
  }

  .project-card {
    padding: 16px;
  }

  .project-detail {
    grid-template-columns: 1fr;
    gap: var(--space-lg);
  }

  .project-detail__grid {
    grid-template-columns: 1fr;
  }

  .action-row {
    flex-direction: column;
    align-items: stretch;
  }

  .action-row__buttons {
    flex-direction: column;
  }

  .action-row__buttons .btn {
    width: 100%;
  }
}
</style><style type="text/css" data-vite-dev-id="C:/Users/I/AccioWork/2026-10-09-14-49-12-722-5527ece6/cute-personal-site/src/components/animated-list/AnimatedList.css">/* AnimatedList — 滑动展示目录（配色来自 DESIGN.md 的四色 pastel token） */

.scroll-list-container {
  position: relative;
  width: 100%;
  padding: var(--space-sm);
  border-radius: var(--rounded-lg);
  border: 2px solid var(--color-border);
  background-color: var(--color-surface-card);
  box-shadow: var(--shadow-2);
}

.scroll-list {
  max-height: 400px;
  overflow-y: auto;
  overscroll-behavior: contain;
  scrollbar-width: thin;
  scrollbar-color: var(--color-primary-soft) var(--color-surface-sunken);
}

.scroll-list::-webkit-scrollbar {
  width: 8px;
}

.scroll-list::-webkit-scrollbar-track {
  background: var(--color-surface-sunken);
  border-radius: var(--rounded-full);
}

.scroll-list::-webkit-scrollbar-thumb {
  background: var(--color-primary-soft);
  border-radius: var(--rounded-full);
}

.no-scrollbar {
  scrollbar-width: none;
  -ms-overflow-style: none;
}

.no-scrollbar::-webkit-scrollbar {
  display: none;
}

.animated-item {
  margin-bottom: 6px;
}

.animated-item:last-child {
  margin-bottom: 0;
}

.item {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: var(--space-sm);
  width: 100%;
  min-height: 52px;
  padding: 12px 14px;
  border-radius: var(--rounded-md);
  background-color: transparent;
  text-align: left;
  transition: background-color var(--dur-micro) linear,
    transform var(--dur-standard) var(--ease-spring);
}

.item:hover {
  background-color: var(--color-surface-sunken);
}

.item:active {
  transform: translateY(2px);
}

.item.selected {
  background-color: var(--color-primary-tint);
}

.item__notch {
  position: absolute;
  left: 10px;
  top: 50%;
  width: 4px;
  height: 20px;
  margin-top: -10px;
  border-radius: var(--rounded-full);
  background-color: var(--color-primary-strong);
}

.item__text {
  display: flex;
  flex-direction: column;
  gap: 2px;
  min-width: 0;
  padding-left: 14px;
}

.item__micro {
  color: var(--color-on-surface-mute);
}

.item__label {
  font-size: var(--text-body);
  font-weight: 500;
  line-height: 1.5;
  color: var(--color-on-surface);
  overflow-wrap: break-word;
}

.item.selected .item__label {
  font-weight: 700;
}

.item__badge {
  display: inline-flex;
  align-items: center;
  flex: 0 0 auto;
  height: 20px;
  padding: 4px 10px;
  border-radius: var(--rounded-full);
  font-family: var(--font-micro);
  font-size: var(--text-label);
  font-weight: 600;
  letter-spacing: 0.12em;
  white-space: nowrap;
}

.item__badge--scene {
  background-color: var(--color-primary-tint);
  color: var(--color-primary-strong);
}

.item__badge--project {
  background-color: var(--color-secondary-tint);
  color: var(--color-secondary-strong);
}

.item__badge--gallery {
  background-color: var(--color-tertiary-tint);
  color: var(--color-tertiary-strong);
}

/* 渐隐遮罩：向所在场景的底色淡出，永远不是黑色 */
.top-gradient {
  position: absolute;
  top: 2px;
  left: 2px;
  right: 2px;
  height: 32px;
  border-radius: var(--rounded-lg) var(--rounded-lg) 0 0;
  background: linear-gradient(to bottom, #eafbf1 0%, rgba(234, 251, 241, 0) 100%);
  pointer-events: none;
  transition: opacity var(--dur-micro) ease;
}

.bottom-gradient {
  position: absolute;
  bottom: 2px;
  left: 2px;
  right: 2px;
  height: 32px;
  border-radius: 0 0 var(--rounded-lg) var(--rounded-lg);
  background: linear-gradient(to top, #eafbf1 0%, rgba(234, 251, 241, 0) 100%);
  pointer-events: none;
  transition: opacity var(--dur-micro) ease;
}

@media (max-width: 1199px) {
  .scroll-list {
    max-height: 380px;
  }
}

@media (max-width: 767px) {
  .scroll-list-container {
    padding: 10px;
  }

  .scroll-list {
    max-height: 320px;
  }

  .item {
    min-height: 48px;
    padding: 10px 12px;
  }
}
</style><style type="text/css" data-vite-dev-id="C:/Users/I/AccioWork/2026-10-09-14-49-12-722-5527ece6/cute-personal-site/src/components/gallery/gallery.css">/* Gallery scene — one full slide plus a peek of the neighbours */

.carousel {
  position: relative;
  width: 100%;
  min-width: 0;
}

.carousel__viewport {
  overflow-x: auto;
  overflow-y: hidden;
  scroll-snap-type: x mandatory;
  scroll-padding-inline: 12%;
  scrollbar-width: none;
  -ms-overflow-style: none;
  overscroll-behavior-x: contain;
  touch-action: pan-y;
  cursor: grab;
  padding-bottom: var(--space-xs);
}

.carousel__viewport::-webkit-scrollbar {
  display: none;
}

.carousel__viewport.is-dragging {
  scroll-snap-type: none;
  cursor: grabbing;
}

.carousel__track {
  display: flex;
  flex-wrap: nowrap;
  align-items: stretch;
  gap: var(--card-gap);
}

.slide {
  position: relative;
  flex: 0 0 auto;
  width: calc(76% - var(--card-gap));
  scroll-snap-align: start;
  min-width: 0;
}

.slide__button {
  position: relative;
  display: block;
  width: 100%;
  border-radius: var(--rounded-lg);
  transition: transform var(--dur-expressive) var(--ease-spring),
    opacity var(--dur-expressive) var(--ease-soft);
}

.slide:not(.slide--active) .slide__button {
  opacity: 0.78;
  transform: scale(0.96);
}

.slide--active .slide__button:hover {
  transform: scale(1.01);
}

.slide__frame {
  display: block;
  aspect-ratio: 4 / 3;
  overflow: hidden;
  border-radius: var(--rounded-lg);
  border: 2px solid var(--color-surface-card);
  box-shadow: var(--shadow-2);
  background-image: linear-gradient(
    135deg,
    var(--color-primary-tint),
    var(--color-tertiary-tint)
  );
}

.slide__frame img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  pointer-events: none;
}

.slide__tape {
  position: absolute;
  top: -10px;
  left: 50%;
  margin-left: -32px;
  z-index: var(--z-deco);
}

.slide-caption {
  position: absolute;
  left: 16px;
  right: 16px;
  bottom: 16px;
  display: flex;
  flex-direction: column;
  gap: 2px;
  padding: 12px 18px;
  border-radius: var(--rounded-md);
  background-color: var(--color-surface-overlay);
  border: 2px solid var(--color-surface-card);
  backdrop-filter: blur(20px) saturate(1.1);
  -webkit-backdrop-filter: blur(20px) saturate(1.1);
  box-shadow: var(--shadow-1);
  text-align: left;
}

.slide-caption__title {
  font-family: var(--font-display);
  font-size: var(--text-card);
  font-weight: 700;
  line-height: 1.3;
  overflow-wrap: break-word;
}

.slide-caption__text {
  font-size: var(--text-caption);
  line-height: 1.6;
  color: var(--color-on-surface-soft);
  overflow-wrap: break-word;
}

.slide-caption__date,
.gallery-detail__date {
  display: flex;
  align-items: center;
  gap: 6px;
  font-size: var(--text-caption);
  font-variant-numeric: tabular-nums;
  color: var(--color-on-surface-mute);
}

.carousel__controls {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: var(--space-md);
  margin-top: var(--space-lg);
}

.carousel__counter {
  padding: 9px 16px;
  border-radius: var(--rounded-full);
  background-color: var(--color-surface-card);
  border: 2px solid var(--color-border);
}

.carousel__buttons {
  display: flex;
  gap: var(--space-sm);
}

.carousel__btn[disabled] {
  opacity: 0.45;
  cursor: not-allowed;
  transform: none;
}

/* ---- Detail overlay ---- */

.gallery-detail {
  display: grid;
  grid-template-columns: 60fr 40fr;
  gap: var(--space-2xl);
  align-items: center;
  margin-top: var(--space-lg);
}

.gallery-detail__image {
  width: 100%;
  max-height: 70vh;
  object-fit: contain;
  border-radius: var(--rounded-lg);
  border: 2px solid var(--color-border);
  background-color: var(--color-surface-alt);
}

.gallery-detail__body {
  display: flex;
  flex-direction: column;
  gap: var(--space-sm);
  min-width: 0;
}

.gallery-detail__caption {
  color: var(--color-on-surface-soft);
}

.gallery-detail__nav {
  display: flex;
  flex-wrap: wrap;
  gap: var(--space-sm);
  margin-top: var(--space-md);
}

.gallery-detail__nav .btn[disabled] {
  opacity: 0.45;
  cursor: not-allowed;
  transform: none;
}

@media (max-width: 1199px) {
  .carousel__viewport {
    scroll-padding-inline: 10%;
  }

  .slide {
    width: calc(86% - var(--card-gap));
  }
}

@media (max-width: 767px) {
  .carousel__viewport {
    scroll-padding-inline: 6%;
  }

  .slide {
    width: calc(92% - var(--card-gap-mobile));
  }

  .carousel__track {
    gap: var(--card-gap-mobile);
  }

  .slide-caption {
    left: 12px;
    right: 12px;
    bottom: 12px;
    padding: 10px 14px;
  }

  .gallery-detail {
    grid-template-columns: 1fr;
    gap: var(--space-lg);
  }

  .gallery-detail__image {
    max-height: 45vh;
  }

  .gallery-detail__nav .btn {
    flex: 1 1 auto;
  }
}
</style><style type="text/css" data-vite-dev-id="C:/Users/I/AccioWork/2026-10-09-14-49-12-722-5527ece6/cute-personal-site/src/components/contact/contact.css">/* Contact scene + feedback form */

.contact-heading {
  font-family: var(--font-display);
  font-size: var(--text-contact);
  font-weight: 700;
  line-height: 1.08;
  letter-spacing: -0.02em;
}

.contact-heading__en {
  color: var(--color-primary-strong);
}

.contact-invitation {
  max-width: 30ch;
  margin-top: var(--space-sm);
  color: var(--color-on-surface-soft);
}

.contact-rows {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: var(--space-md);
  margin-top: var(--space-lg);
}

.contact-rows__item {
  display: flex;
  min-width: 0;
}

.contact-rows__item:first-child {
  grid-column: span 2;
}

.contact-row {
  display: flex;
  align-items: center;
  gap: var(--space-md);
  width: 100%;
  padding: 22px 26px;
  border-radius: var(--rounded-xl);
  border: 2px solid var(--color-border);
  background-color: var(--color-surface-card);
  box-shadow: var(--shadow-1);
  text-align: left;
  transition: transform var(--dur-standard) var(--ease-spring),
    border-color var(--dur-micro) linear, box-shadow var(--dur-standard) var(--ease-soft);
}

a.contact-row:hover {
  transform: translateY(-4px);
  border-color: var(--color-border-strong);
  box-shadow: var(--shadow-2);
}

.contact-row__badge {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  flex: 0 0 auto;
  width: 44px;
  height: 44px;
  border-radius: var(--rounded-full);
}

.contact-row__badge--mint {
  background-color: var(--color-secondary-tint);
  color: var(--color-secondary-strong);
}

.contact-row__badge--sky {
  background-color: var(--color-primary-tint);
  color: var(--color-primary-strong);
}

.contact-row__badge--lilac {
  background-color: var(--color-tertiary-tint);
  color: var(--color-tertiary-strong);
}

.contact-row__text {
  display: flex;
  flex-direction: column;
  gap: 2px;
  min-width: 0;
}

.contact-row__label {
  display: flex;
  align-items: center;
  gap: var(--space-xs);
}

.contact-row__name {
  font-size: var(--text-caption);
  color: var(--color-on-surface-soft);
}

.contact-row__value {
  font-family: var(--font-display);
  font-size: var(--text-value);
  font-weight: 800;
  line-height: 1.25;
  letter-spacing: -0.01em;
  overflow-wrap: break-word;
  word-break: break-word;
}

.contact-row__role {
  font-size: var(--text-caption);
  color: var(--color-on-surface-mute);
}

/* ---- Feedback form ---- */

.feedback-panel {
  position: relative;
  display: flex;
  flex-direction: column;
  gap: var(--space-md);
  padding: var(--space-xl);
  border-radius: var(--rounded-blob) var(--rounded-blob) var(--rounded-md)
    var(--rounded-blob);
  background-color: var(--color-surface-overlay);
  border: 2px solid var(--color-surface-card);
  backdrop-filter: blur(20px) saturate(1.1);
  -webkit-backdrop-filter: blur(20px) saturate(1.1);
  box-shadow: var(--shadow-4);
}

.panel-title {
  font-family: var(--font-display);
  font-size: var(--text-panel);
  font-weight: 700;
  line-height: 1.3;
}

.feedback-panel__help {
  font-size: var(--text-small);
  color: var(--color-on-surface-soft);
}

.field {
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.field__label {
  color: var(--color-tertiary-strong);
}

.field__input {
  width: 100%;
  min-height: 50px;
  padding: 14px 18px;
  border-radius: var(--rounded-md);
  border: 2px solid var(--color-border);
  background-color: var(--color-surface-card);
  color: var(--color-on-surface);
  font-family: var(--font-body);
  font-size: var(--text-small);
  transition: border-color var(--dur-micro) linear, box-shadow var(--dur-micro) linear;
}

.field__input::placeholder {
  color: var(--color-on-surface-mute);
}

.field__input:focus-visible {
  outline: none;
  border-color: var(--color-primary-strong);
  box-shadow: 0 0 0 4px rgba(122, 75, 15, 0.22);
}

.field__input--textarea {
  min-height: 120px;
  resize: vertical;
}

.field__input--error {
  border-color: var(--color-error);
}

.field__error {
  display: flex;
  align-items: center;
  gap: 6px;
  font-size: var(--text-caption);
  color: var(--color-error);
}

.feedback-panel__submit {
  width: 100%;
  margin-top: var(--space-xs);
}

.feedback-panel__submit[disabled] {
  opacity: 0.6;
  cursor: not-allowed;
  transform: none;
}

.feedback-panel__spinner {
  animation: spin 900ms linear infinite;
}

@keyframes spin {
  to {
    transform: rotate(360deg);
  }
}

/* ---- Success state ---- */

.feedback-panel--success {
  border-radius: var(--rounded-blob) var(--rounded-blob) var(--rounded-md) var(--rounded-blob);
  background-color: var(--color-secondary-tint);
  border-color: var(--color-secondary-soft);
  box-shadow: var(--shadow-2);
  align-items: flex-start;
}

.feedback-panel--success .panel-title {
  color: var(--color-secondary-strong);
}

.feedback-panel__success-body {
  color: var(--color-on-surface-soft);
}

.feedback-panel--success .btn {
  align-self: flex-start;
  background-color: var(--color-surface-card);
}

@media (max-width: 767px) {
  .contact-rows {
    grid-template-columns: 1fr;
  }

  .contact-rows__item:first-child {
    grid-column: span 1;
  }

  .contact-row {
    padding: 18px;
  }

  .feedback-panel {
    padding: var(--space-lg);
  }

  .feedback-panel__submit {
    min-height: 48px;
  }
}
</style><style type="text/css" data-vite-dev-id="C:/Users/I/AccioWork/2026-10-09-14-49-12-722-5527ece6/cute-personal-site/src/styles.css">/* =========================================================================
   styles.css — design tokens (from DESIGN.md "Sakura Loop Pastel") + base
   ========================================================================= */

:root {
  /* ---- Colors（金黄灿烂：单一暖色系，文字一律深棕/深琥珀墨色） ---- */
  --color-surface: #fffbef;
  --color-surface-alt: #f9f2e0;
  --color-surface-mint: #f8e9c4;
  --color-surface-sky: #f0dca8;
  --color-surface-card: #ffffff;
  --color-surface-sunken: #f7edd6;
  --color-surface-overlay: rgba(255, 251, 240, 0.82);
  --color-scrim: rgba(74, 53, 20, 0.45);
  --color-on-surface: #3b2a15;
  --color-on-surface-soft: #6b4e24;
  --color-on-surface-mute: #755a2f;
  --color-on-primary: #ffffff;
  --color-border: #eddfc0;
  --color-border-strong: #dcc58f;
  --color-primary: #e8a62b;
  --color-primary-strong: #7a4b0f;
  --color-primary-hover: #623a08;
  --color-primary-soft: #f3d98b;
  --color-primary-tint: #fcefce;
  --color-secondary: #d98a2b;
  --color-secondary-strong: #8a4a12;
  --color-secondary-soft: #f0c37a;
  --color-secondary-tint: #fceedb;
  --color-tertiary: #c79a4e;
  --color-tertiary-strong: #5f430f;
  --color-tertiary-soft: #e6ce96;
  --color-tertiary-tint: #f5ebd4;
  --color-accent-star: #ffce4a;
  --color-accent-ribbon: #c08a45;
  --color-accent-peach: #f7be86;
  --color-accent-lavender-tint: #fbf0d8;
  --color-success: #4e6b12;
  --color-error: #b3261e;
  --color-focus-ring: #7a4b0f;

  /* ---- Typography ---- */
  --font-display: 'PingFang SC', 'Hiragino Sans GB', 'Microsoft YaHei',
    'Noto Sans SC', system-ui, -apple-system, sans-serif;
  --font-body: 'PingFang SC', 'Hiragino Sans GB', 'Microsoft YaHei',
    'Noto Sans SC', system-ui, -apple-system, sans-serif;
  --font-micro: system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue',
    Arial, sans-serif;

  --text-hero: 64px;
  --text-scene: 56px;
  --text-contact: 60px;
  --text-detail: 44px;
  --text-panel: 28px;
  --text-card: 22px;
  --text-value: 30px;
  --text-lead: 18px;
  --text-body: 16px;
  --text-small: 15px;
  --text-caption: 13px;
  --text-label: 11px;
  --text-counter: 14px;

  /* ---- Rounded ---- */
  --rounded-xs: 10px;
  --rounded-sm: 14px;
  --rounded-md: 20px;
  --rounded-lg: 28px;
  --rounded-xl: 36px;
  --rounded-blob: 48px;
  --rounded-full: 999px;

  /* ---- Spacing ---- */
  --space-2xs: 4px;
  --space-xs: 8px;
  --space-sm: 12px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;
  --space-4xl: 96px;
  --container-max: 1200px;
  --gutter: 72px;
  --gutter-tablet: 40px;
  --gutter-mobile: 20px;
  --scene-pad-top: 108px;
  --scene-pad-bottom: 96px;
  --card-gap: 24px;
  --card-gap-mobile: 16px;

  /* ---- Elevation & motion ---- */
  --shadow-1: 0 2px 8px rgba(176, 118, 18, 0.16);
  --shadow-2: 0 8px 24px rgba(176, 118, 18, 0.2);
  --shadow-3: 0 18px 44px rgba(158, 102, 12, 0.22);
  --shadow-4: 0 28px 72px rgba(134, 84, 8, 0.24);
  --shadow-sticker: 0 4px 0 rgba(176, 118, 18, 0.35);
  --ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);
  --ease-soft: cubic-bezier(0.22, 0.9, 0.3, 1);
  --dur-micro: 140ms;
  --dur-standard: 240ms;
  --dur-expressive: 420ms;
  --dur-scene: 620ms;
  --z-deco: 1;
  --z-content: 2;
  --z-fixed: 40;
  --z-scrim: 60;
  --z-overlay: 61;
}

/* =========================================================================
   Base
   ========================================================================= */

*,
*::before,
*::after {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  background-color: var(--color-surface);
  color: var(--color-on-surface);
  font-family: var(--font-body);
  font-size: var(--text-body);
  line-height: 1.7;
  -webkit-font-smoothing: antialiased;
}

h1,
h2,
h3,
p,
ul,
ol,
figure {
  margin: 0;
}

ul,
ol {
  padding: 0;
  list-style: none;
}

img {
  display: block;
  max-width: 100%;
}

button {
  font: inherit;
  color: inherit;
  border: none;
  background: none;
  cursor: pointer;
}

a {
  color: inherit;
  text-decoration: none;
}

:focus-visible {
  outline: 3px solid var(--color-focus-ring);
  outline-offset: 2px;
  box-shadow: 0 0 0 2px var(--color-surface-card);
  border-radius: var(--rounded-sm);
}

.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0 0 0 0);
  white-space: nowrap;
  border: 0;
}

.skip-link {
  position: absolute;
  top: var(--space-sm);
  left: var(--space-sm);
  z-index: 80;
  padding: 12px 20px;
  border-radius: var(--rounded-full);
  background: var(--color-surface-card);
  border: 2px solid var(--color-border-strong);
  font-family: var(--font-micro);
  font-size: var(--text-caption);
  font-weight: 600;
  letter-spacing: 0.06em;
  transform: translateY(-200%);
  transition: transform var(--dur-standard) var(--ease-soft);
}

.skip-link:focus-visible {
  transform: translateY(0);
}

/* =========================================================================
   Text primitives
   ========================================================================= */

.micro-label {
  font-family: var(--font-micro);
  font-size: var(--text-label);
  font-weight: 600;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  line-height: 1;
  color: var(--color-on-surface-mute);
}

.eyebrow {
  display: inline-block;
  font-family: var(--font-micro);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  line-height: 1;
  color: var(--color-primary-strong);
}

.dotted-rule {
  display: block;
  width: 100%;
  border-top: 2px dotted var(--color-border-strong);
}

.counter {
  font-family: var(--font-micro);
  font-size: var(--text-counter);
  font-weight: 700;
  letter-spacing: 0.08em;
  font-variant-numeric: tabular-nums;
  color: var(--color-on-surface-mute);
}

/* =========================================================================
   Buttons, tags and surfaces
   ========================================================================= */

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: var(--space-xs);
  min-height: 48px;
  padding: 13px 26px;
  border-radius: var(--rounded-full);
  border: 2px solid transparent;
  font-family: var(--font-body);
  font-size: var(--text-small);
  font-weight: 600;
  transition: transform var(--dur-standard) var(--ease-spring),
    background-color var(--dur-micro) linear,
    border-color var(--dur-micro) linear, box-shadow var(--dur-standard) var(--ease-soft);
}

.btn--primary {
  background-color: var(--color-primary-strong);
  color: var(--color-on-primary);
  box-shadow: var(--shadow-2);
}

.btn--primary:hover {
  background-color: var(--color-primary-hover);
  transform: translateY(-4px) rotate(-1deg);
}

.btn--secondary {
  background-color: var(--color-primary-tint);
  color: var(--color-primary-strong);
  border-color: var(--color-border);
}

.btn--secondary:hover {
  background-color: var(--color-primary-soft);
  transform: translateY(-4px);
}

.btn--glass {
  background-color: var(--color-surface-overlay);
  color: var(--color-on-surface);
  border-color: var(--color-surface-card);
  backdrop-filter: blur(20px) saturate(1.1);
  -webkit-backdrop-filter: blur(20px) saturate(1.1);
}

.btn--glass:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-2);
}

.btn--ghost {
  background-color: transparent;
  color: var(--color-on-surface-soft);
  border-color: var(--color-border-strong);
}

.btn--ghost:hover {
  background-color: var(--color-surface-sunken);
  transform: translateY(-2px);
}

.btn:active {
  transform: translateY(2px);
}

.btn--icon {
  width: 44px;
  height: 44px;
  min-height: 44px;
  padding: 0;
  border-radius: var(--rounded-full);
  background-color: var(--color-surface-card);
  border-color: var(--color-border);
  box-shadow: var(--shadow-1);
  color: var(--color-on-surface);
}

.btn--icon:hover {
  transform: translateY(-2px) scale(1.04);
  border-color: var(--color-border-strong);
}

.tag-pill {
  display: inline-flex;
  align-items: center;
  min-height: 26px;
  padding: 7px 14px;
  border-radius: var(--rounded-full);
  background-color: var(--color-primary-tint);
  color: var(--color-primary-strong);
  font-family: var(--font-micro);
  font-size: var(--text-label);
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  white-space: nowrap;
}

.tag-pill--mint {
  background-color: var(--color-secondary-tint);
  color: var(--color-secondary-strong);
}

.tag-pill--sky {
  background-color: var(--color-tertiary-tint);
  color: var(--color-tertiary-strong);
}

.glass-panel {
  background-color: var(--color-surface-overlay);
  border: 2px solid var(--color-surface-card);
  border-radius: var(--rounded-xl);
  box-shadow: var(--shadow-4);
  backdrop-filter: blur(20px) saturate(1.1);
  -webkit-backdrop-filter: blur(20px) saturate(1.1);
}

.info-card {
  background-color: var(--color-surface-alt);
  border: 2px solid var(--color-border);
  border-radius: var(--rounded-lg);
  padding: var(--space-lg);
}

.sticker-badge {
  position: absolute;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 6px 14px;
  border-radius: var(--rounded-full);
  background-color: var(--color-surface-card);
  border: 4px solid var(--color-surface-card);
  box-shadow: var(--shadow-sticker);
  font-family: var(--font-micro);
  font-size: var(--text-label);
  font-weight: 700;
  letter-spacing: 0.12em;
  color: var(--color-primary-strong);
}

/* =========================================================================
   Decoration (all aria-hidden, never carries meaning)
   ========================================================================= */

.deco {
  position: absolute;
  pointer-events: none;
  z-index: var(--z-deco);
}

.deco--float {
  animation: float 4s ease-in-out infinite alternate;
}

.deco--twinkle {
  animation: twinkle 1.8s ease-in-out infinite alternate;
}

.deco--wiggle {
  animation: wiggle 420ms var(--ease-spring) 1;
}

@keyframes float {
  from {
    transform: translateY(0);
  }
  to {
    transform: translateY(-8px);
  }
}

@keyframes twinkle {
  from {
    opacity: 0.4;
  }
  to {
    opacity: 1;
  }
}

@keyframes wiggle {
  0% {
    transform: rotate(0deg);
  }
  35% {
    transform: rotate(-2deg);
  }
  70% {
    transform: rotate(2deg);
  }
  100% {
    transform: rotate(0deg);
  }
}

.blush-dots {
  position: absolute;
  bottom: 18px;
  left: 22px;
  display: flex;
  gap: 6px;
}

.blush-dots span {
  width: 8px;
  height: 8px;
  border-radius: var(--rounded-full);
  background-color: var(--color-primary-soft);
}

.scallop-edge {
  position: absolute;
  left: 0;
  right: 0;
  height: 24px;
  background-repeat: repeat-x;
  background-size: 48px 24px;
  background-image: radial-gradient(
    circle at 24px 24px,
    currentColor 24px,
    transparent 25px
  );
  pointer-events: none;
}

/* =========================================================================
   Layout — scene model
   ========================================================================= */

.scene {
  position: relative;
  padding: var(--scene-pad-top) var(--gutter) var(--scene-pad-bottom);
  scroll-margin-top: 0;
}

.scene__inner {
  position: relative;
  z-index: var(--z-content);
  display: grid;
  grid-template-columns: 38fr 62fr;
  align-items: center;
  gap: var(--space-2xl);
  width: 100%;
  max-width: var(--container-max);
  margin: 0 auto;
  min-height: calc(100vh - var(--scene-pad-top) - var(--scene-pad-bottom));
}

.scene__narrative {
  display: flex;
  flex-direction: column;
  gap: var(--space-md);
  align-self: end;
  padding-bottom: var(--space-xl);
}

.scene__content {
  display: flex;
  flex-direction: column;
  gap: var(--space-lg);
  min-width: 0;
}

.scene--hero {
  background-color: var(--color-surface);
}

.scene--projects {
  background-color: var(--color-surface-sky);
}

.scene--index {
  background-color: var(--color-surface-mint);
}

.scene--gallery {
  background-color: var(--color-surface-alt);
}

.scene--contact {
  background-color: var(--color-surface);
}

/* =========================================================================
   Header
   ========================================================================= */

.site-header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: var(--z-fixed);
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: var(--space-md);
  padding: var(--space-md) var(--gutter);
  pointer-events: none;
}

.site-header > * {
  pointer-events: auto;
}

.wordmark {
  display: inline-flex;
  align-items: center;
  gap: var(--space-xs);
  min-height: 44px;
  font-family: var(--font-micro);
  font-size: var(--text-caption);
  font-weight: 700;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--color-on-surface);
}

.wordmark__dot {
  width: 10px;
  height: 10px;
  border-radius: var(--rounded-full);
  background-color: var(--color-primary);
  box-shadow: var(--shadow-1);
}

.header-controls {
  display: flex;
  align-items: center;
  gap: var(--space-sm);
}

.progress-pill {
  display: inline-flex;
  align-items: center;
  gap: var(--space-2xs);
  padding: 4px;
  border-radius: var(--rounded-full);
  background-color: var(--color-surface-overlay);
  border: 2px solid var(--color-surface-card);
  backdrop-filter: blur(20px) saturate(1.1);
  -webkit-backdrop-filter: blur(20px) saturate(1.1);
  box-shadow: var(--shadow-1);
}

.progress-dot {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 44px;
  height: 44px;
  border-radius: var(--rounded-full);
  transition: background-color var(--dur-micro) linear,
    transform var(--dur-standard) var(--ease-spring);
}

.progress-dot:hover {
  background-color: var(--color-primary-soft);
  transform: translateY(-2px);
}

.progress-dot__mark {
  display: block;
  width: 8px;
  height: 8px;
  border-radius: var(--rounded-full);
  background-color: var(--color-border-strong);
  transition: width var(--dur-standard) var(--ease-spring),
    background-color var(--dur-micro) linear;
}

.progress-dot--active {
  background-color: var(--color-primary-tint);
}

.progress-dot--active .progress-dot__mark {
  width: 22px;
  background-color: var(--color-primary-strong);
}

/* Mobile scene navigation — replaces the desktop progress dots */
.mobile-nav {
  display: none;
  position: fixed;
  right: var(--gutter-mobile);
  bottom: var(--gutter-mobile);
  z-index: var(--z-fixed);
  border-radius: var(--rounded-full);
  background-color: var(--color-surface-overlay);
  border: 2px solid var(--color-surface-card);
  backdrop-filter: blur(20px) saturate(1.1);
  -webkit-backdrop-filter: blur(20px) saturate(1.1);
  box-shadow: var(--shadow-2);
}

.mobile-nav__btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 6px;
  min-width: 76px;
  min-height: 44px;
  padding: 0 16px;
  border-radius: var(--rounded-full);
  font-family: var(--font-micro);
  font-size: var(--text-label);
  font-weight: 700;
  letter-spacing: 0.14em;
  color: var(--color-on-surface);
  transition: background-color var(--dur-micro) linear;
}

.mobile-nav__btn + .mobile-nav__btn {
  border-left: 2px solid var(--color-border);
}

.mobile-nav__btn:hover {
  background-color: var(--color-primary-tint);
}

.mobile-nav__btn:active {
  transform: translateY(2px);
}

.mobile-nav__btn[disabled] {
  opacity: 0.45;
  cursor: not-allowed;
}

/* =========================================================================
   Scene indicator
   ========================================================================= */

.scene-indicator {
  position: fixed;
  left: var(--gutter);
  bottom: var(--space-lg);
  z-index: var(--z-fixed);
  display: flex;
  flex-direction: column;
  gap: var(--space-xs);
  width: min(420px, 40vw);
  pointer-events: none;
}

.scene-indicator__rule {
  border-top: 2px dotted var(--color-border-strong);
}

.scene-indicator__label {
  font-family: var(--font-micro);
  font-size: var(--text-label);
  font-weight: 600;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--color-on-surface-mute);
}

/* =========================================================================
   Entry gate
   ========================================================================= */

.entry-gate {
  position: fixed;
  inset: 0;
  z-index: var(--z-overlay);
  display: grid;
  place-items: center;
  overflow: hidden;
  background-color: var(--color-surface);
  background-image: radial-gradient(
      circle at 50% 38%,
      rgba(244, 114, 160, 0.14),
      rgba(255, 247, 243, 0) 46%
    ),
    radial-gradient(circle at 82% 78%, rgba(143, 199, 255, 0.22), rgba(255, 247, 243, 0) 42%),
    radial-gradient(circle at 14% 82%, rgba(111, 211, 180, 0.2), rgba(255, 247, 243, 0) 40%);
  transition: opacity var(--dur-scene) var(--ease-soft),
    transform var(--dur-scene) var(--ease-soft);
}

.entry-gate--leaving {
  opacity: 0;
  transform: scale(1.03);
  pointer-events: none;
}

.entry-gate__brand {
  position: absolute;
  top: var(--space-xl);
  left: var(--gutter);
  display: inline-flex;
  align-items: center;
  gap: var(--space-xs);
  font-family: var(--font-micro);
  font-size: var(--text-caption);
  font-weight: 700;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--color-on-surface-soft);
}

.entry-capsule {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 4px;
  width: 220px;
  min-height: 92px;
  padding: 18px 44px;
  border-radius: var(--rounded-full);
  background-color: var(--color-surface-overlay);
  border: 2px solid var(--color-surface-card);
  box-shadow: var(--shadow-4);
  backdrop-filter: blur(20px) saturate(1.1);
  -webkit-backdrop-filter: blur(20px) saturate(1.1);
  transition: transform var(--dur-standard) var(--ease-spring),
    box-shadow var(--dur-standard) var(--ease-soft);
}

.entry-capsule:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-3);
}

.entry-capsule:active {
  transform: translateY(2px);
}

.entry-capsule__zh {
  font-family: var(--font-display);
  font-size: var(--text-panel);
  font-weight: 700;
  line-height: 1.3;
  color: var(--color-on-surface);
}

.entry-capsule__en {
  font-family: var(--font-micro);
  font-size: var(--text-label);
  font-weight: 600;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--color-on-surface-mute);
}

.entry-capsule__sparkle {
  position: absolute;
  top: -10px;
  right: -6px;
  opacity: 0;
  transition: opacity var(--dur-standard) var(--ease-soft);
}

.entry-capsule:hover .entry-capsule__sparkle {
  opacity: 1;
}

/* =========================================================================
   Shared overlay shell
   ========================================================================= */

.overlay {
  position: fixed;
  inset: 0;
  z-index: var(--z-scrim);
  display: grid;
  place-items: center;
  padding: var(--space-lg);
  background-color: var(--color-scrim);
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  animation: overlay-in var(--dur-standard) var(--ease-soft);
}

@keyframes overlay-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.overlay__panel {
  position: relative;
  z-index: var(--z-overlay);
  width: min(1080px, 100%);
  max-height: calc(100vh - 2 * var(--space-lg));
  overflow-y: auto;
  padding: 40px;
  border-radius: var(--rounded-xl);
  background-color: var(--color-surface-card);
  border: 2px solid var(--color-border);
  box-shadow: var(--shadow-4);
}

.overlay__close {
  position: sticky;
  top: 0;
  float: right;
  margin: -8px -8px 0 0;
}

/* =========================================================================
   Section heading block (shared by list scenes)
   ========================================================================= */

.scene-heading-block {
  position: relative;
  display: flex;
  flex-direction: column;
  gap: var(--space-sm);
}

.scene-heading {
  font-family: var(--font-display);
  font-size: var(--text-scene);
  font-weight: 700;
  line-height: 1.14;
  letter-spacing: -0.02em;
}

.scene-subtitle {
  font-size: var(--text-lead);
  line-height: 1.75;
  color: var(--color-on-surface-soft);
  max-width: 30ch;
}

/* =========================================================================
   Simple page (404)
   ========================================================================= */

.simple-page {
  display: grid;
  place-items: center;
  min-height: 100vh;
  padding: var(--space-4xl) var(--gutter);
  background-color: var(--color-surface);
}

.simple-page__card {
  position: relative;
  max-width: 560px;
  padding: var(--space-2xl);
  border-radius: var(--rounded-blob) var(--rounded-blob) var(--rounded-blob) var(--rounded-md);
  background-color: var(--color-surface-card);
  border: 2px solid var(--color-border);
  box-shadow: var(--shadow-3);
  text-align: center;
}

.simple-page__title {
  margin: var(--space-sm) 0;
  font-family: var(--font-display);
  font-size: var(--text-detail);
  font-weight: 700;
  line-height: 1.2;
}

.simple-page__body {
  margin-bottom: var(--space-xl);
  color: var(--color-on-surface-soft);
}

/* =========================================================================
   Reduced motion
   ========================================================================= */

@media (prefers-reduced-motion: reduce) {
  html {
    scroll-behavior: auto;
  }

  *,
  *::before,
  *::after {
    animation-duration: 0.18s !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.18s !important;
    transition-property: opacity, background-color, border-color, color !important;
  }

  .deco--float,
  .deco--twinkle,
  .deco--wiggle {
    animation: none !important;
  }

  .btn:hover,
  .entry-capsule:hover {
    transform: none;
  }
}

/* =========================================================================
   Responsive — tablet
   ========================================================================= */

@media (max-width: 1199px) {
  :root {
    --gutter: var(--gutter-tablet);
    --text-scene: 40px;
    --text-contact: 46px;
  }

  .scene__inner {
    grid-template-columns: 34fr 66fr;
    gap: var(--space-xl);
  }

  .scene-indicator {
    width: min(320px, 46vw);
  }
}

/* =========================================================================
   Responsive — mobile
   ========================================================================= */

@media (max-width: 767px) {
  :root {
    --gutter: var(--gutter-mobile);
    --scene-pad-top: 72px;
    --scene-pad-bottom: 88px;
    --text-hero: 34px;
    --text-scene: 34px;
    --text-contact: 42px;
    --text-detail: 28px;
    --text-panel: 24px;
    --text-card: 20px;
    --text-value: 24px;
    --text-lead: 16px;
  }

  .scene__inner {
    grid-template-columns: 1fr;
    gap: var(--space-xl);
    min-height: 0;
  }

  .scene__narrative {
    align-self: stretch;
    padding-bottom: 0;
  }

  .site-header {
    padding: var(--space-sm) var(--gutter-mobile);
  }

  .progress-pill {
    display: none;
  }

  .mobile-nav {
    display: flex;
  }

  .scene-indicator {
    left: var(--gutter-mobile);
    right: 110px;
    bottom: calc(var(--gutter-mobile) + 52px);
    width: auto;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    gap: var(--space-xs);
    padding: 9px 16px;
    border-radius: var(--rounded-full);
    background-color: var(--color-surface-overlay);
    border: 2px solid var(--color-surface-card);
    backdrop-filter: blur(20px) saturate(1.1);
    -webkit-backdrop-filter: blur(20px) saturate(1.1);
    box-shadow: var(--shadow-1);
  }

  .scene-indicator__rule {
    display: none;
  }

  .wordmark {
    font-size: 11px;
    letter-spacing: 0.16em;
  }

  .overlay {
    padding: 0;
    align-items: end;
  }

  .overlay__panel {
    width: 100%;
    max-height: 100vh;
    padding: 24px 20px 32px;
    border-radius: var(--rounded-xl) var(--rounded-xl) 0 0;
  }
}

/* =========================================================================
   Reduced decorative motion on mobile
   ========================================================================= */

@media (max-width: 767px) and (prefers-reduced-motion: no-preference) {
  .deco--float,
  .deco--twinkle {
    animation: none;
  }
}

/* =========================================================================
   Decoration details (petals, sparkle cluster, washi tape)
   ========================================================================= */

.petal {
  border-radius: 60% 40% 55% 45%;
  background-color: var(--color-tertiary-soft);
  opacity: 0.5;
}

.deco-cluster {
  position: absolute;
  display: inline-flex;
  align-items: center;
  gap: 6px;
}

.deco-cluster--heading {
  top: -14px;
  right: -4px;
}

.washi-tape {
  display: block;
  width: 64px;
  height: 22px;
  border-radius: 3px;
  background-color: var(--color-primary-tint);
  background-image: repeating-linear-gradient(
    90deg,
    rgba(111, 168, 255, 0.45) 0 2px,
    transparent 2px 7px
  );
  opacity: 0.9;
  box-shadow: var(--shadow-1);
}

/* 标题块下的一行小字提示（目录场景用） */
.scene-help {
  font-size: var(--text-caption);
  line-height: 1.6;
  color: var(--color-on-surface-mute);
}

/* =========================================================================
   Small shared text class
   ========================================================================= */

.caption {
  font-size: var(--text-caption);
  line-height: 1.6;
  color: var(--color-on-surface-soft);
}
</style></head>
  <body style="overflow: hidden;">
    <div id="root"><a class="skip-link" href="http://192.168.43.204:9999/#main" data-loc="src/pages/HomePage.jsx:113:6">跳到主要内容</a><div class="entry-gate" data-component="entry-gate" data-loc="src/components/entry-gate/EntryGate.jsx:16:4"><div class="cover-media" aria-hidden="true" data-loc="src/components/entry-gate/EntryGate.jsx:21:6"></div><div class="cover-wash" aria-hidden="true" data-loc="src/components/entry-gate/EntryGate.jsx:26:6"></div><span class="entry-gate__brand" data-loc="src/components/entry-gate/EntryGate.jsx:28:6"><span class="wordmark__dot" aria-hidden="true" data-loc="src/components/entry-gate/EntryGate.jsx:29:8"></span>JIANI</span><button type="button" class="entry-capsule" data-loc="src/components/entry-gate/EntryGate.jsx:33:6"><span class="entry-capsule__zh" data-loc="src/components/entry-gate/EntryGate.jsx:34:8">进入网站</span><span class="entry-capsule__en" data-loc="src/components/entry-gate/EntryGate.jsx:35:8">ENTER SITE</span><svg class="deco deco--twinkle entry-capsule__sparkle" width="16" height="16" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:19:4" style="color: var(--color-accent-star);"><path d="M12 0.5 L14.4 9.6 L23.5 12 L14.4 14.4 L12 23.5 L9.6 14.4 L0.5 12 L9.6 9.6 Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:28:6"></path></svg></button></div><header class="site-header" data-component="site-header" data-loc="src/components/header/Header.jsx:12:4"><button type="button" class="wordmark" data-loc="src/components/header/Header.jsx:13:6"><span class="wordmark__dot" aria-hidden="true" data-loc="src/components/header/Header.jsx:14:8"></span>JIANI</button><div class="header-controls" data-loc="src/components/header/Header.jsx:18:6"><nav class="progress-pill" aria-label="场景导航" data-loc="src/components/header/Header.jsx:19:8"><button type="button" class="progress-dot progress-dot--active" aria-current="true" data-loc="src/components/header/Header.jsx:21:12"><span class="progress-dot__mark" aria-hidden="true" data-loc="src/components/header/Header.jsx:28:14"></span><span class="visually-hidden" data-loc="src/components/header/Header.jsx:29:14">跳到欢迎</span></button><button type="button" class="progress-dot" data-loc="src/components/header/Header.jsx:21:12"><span class="progress-dot__mark" aria-hidden="true" data-loc="src/components/header/Header.jsx:28:14"></span><span class="visually-hidden" data-loc="src/components/header/Header.jsx:29:14">跳到作品</span></button><button type="button" class="progress-dot" data-loc="src/components/header/Header.jsx:21:12"><span class="progress-dot__mark" aria-hidden="true" data-loc="src/components/header/Header.jsx:28:14"></span><span class="visually-hidden" data-loc="src/components/header/Header.jsx:29:14">跳到目录</span></button><button type="button" class="progress-dot" data-loc="src/components/header/Header.jsx:21:12"><span class="progress-dot__mark" aria-hidden="true" data-loc="src/components/header/Header.jsx:28:14"></span><span class="visually-hidden" data-loc="src/components/header/Header.jsx:29:14">跳到爱好</span></button><button type="button" class="progress-dot" data-loc="src/components/header/Header.jsx:21:12"><span class="progress-dot__mark" aria-hidden="true" data-loc="src/components/header/Header.jsx:28:14"></span><span class="visually-hidden" data-loc="src/components/header/Header.jsx:29:14">跳到联系我</span></button></nav></div></header><main id="main" data-loc="src/pages/HomePage.jsx:134:6"><section id="hero" class="scene scene--hero" data-component="hero-scene" aria-labelledby="hero-title" data-loc="src/components/hero/Hero.jsx:16:4"><div class="cover-media" aria-hidden="true" data-loc="src/components/hero/Hero.jsx:22:6"></div><div class="cover-wash" aria-hidden="true" data-loc="src/components/hero/Hero.jsx:27:6"></div><svg class="deco deco--twinkle cover-sparkle cover-sparkle--tl" width="18" height="18" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:19:4" style="color: var(--color-accent-star);"><path d="M12 0.5 L14.4 9.6 L23.5 12 L14.4 14.4 L12 23.5 L9.6 14.4 L0.5 12 L9.6 9.6 Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:28:6"></path></svg><svg class="deco deco--twinkle cover-sparkle cover-sparkle--br" width="13" height="13" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:19:4" style="color: var(--color-accent-star);"><path d="M12 0.5 L14.4 9.6 L23.5 12 L14.4 14.4 L12 23.5 L9.6 14.4 L0.5 12 L9.6 9.6 Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:28:6"></path></svg><div class="scene__inner" data-loc="src/components/hero/Hero.jsx:31:6"><div class="scene__narrative" data-loc="src/components/hero/Hero.jsx:32:8"><h1 class="hero-title" id="hero-title" data-loc="src/components/hero/Hero.jsx:33:10">欢迎来到，<br data-loc="src/components/hero/Hero.jsx:35:12">王佳妮的主页</h1><p class="hero-support" data-loc="src/components/hero/Hero.jsx:39:10">在读大学生，平时喜欢做点网页，也喜欢带着相机到处走走。</p><div class="scroll-cue" data-loc="src/components/hero/Hero.jsx:41:10"><button type="button" class="btn btn--secondary" data-loc="src/components/hero/Hero.jsx:42:12">向下滚动进入</button><span class="scroll-cue__rule" aria-hidden="true" data-loc="src/components/hero/Hero.jsx:49:12"></span><span class="micro-label" data-loc="src/components/hero/Hero.jsx:50:12">SCROLL DOWN</span></div></div><div class="scene__content" data-loc="src/components/hero/Hero.jsx:54:8"><div class="glass-panel profile-panel" data-component="profile-panel" data-loc="src/components/hero/Hero.jsx:55:10"><svg class="deco profile-panel__ribbon" width="30" height="21.599999999999998" viewBox="0 0 40 29" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:74:4" style="color: var(--color-accent-ribbon); transform: rotate(-8deg);"><path d="M17 14.5 2 4.5v20z" fill="currentColor" data-loc="src/components/common/Decor.jsx:83:6"></path><path d="M23 14.5 38 4.5v20z" fill="currentColor" data-loc="src/components/common/Decor.jsx:84:6"></path><circle cx="20" cy="14.5" r="4.4" fill="var(--color-primary-soft)" data-loc="src/components/common/Decor.jsx:85:6"></circle></svg><span class="eyebrow" data-loc="src/components/hero/Hero.jsx:57:12">PROFILE</span><h2 class="profile-panel__name" data-loc="src/components/hero/Hero.jsx:58:12">王佳妮</h2><p class="profile-panel__tagline" data-loc="src/components/hero/Hero.jsx:59:12">大学学生</p><dl class="profile-facts" data-loc="src/components/hero/Hero.jsx:61:12"><div class="profile-fact" data-loc="src/components/hero/Hero.jsx:63:16"><dt class="profile-fact__label micro-label" data-loc="src/components/hero/Hero.jsx:64:18">LOCATION</dt><dd class="profile-fact__value" data-loc="src/components/hero/Hero.jsx:65:18">现居 · 山东</dd></div><div class="profile-fact" data-loc="src/components/hero/Hero.jsx:63:16"><dt class="profile-fact__label micro-label" data-loc="src/components/hero/Hero.jsx:64:18">FOCUS</dt><dd class="profile-fact__value" data-loc="src/components/hero/Hero.jsx:65:18">网页 · 摄影</dd></div></dl><span class="blush-dots " aria-hidden="true" data-loc="src/components/common/Decor.jsx:155:4"><span data-loc="src/components/common/Decor.jsx:156:6"></span><span data-loc="src/components/common/Decor.jsx:157:6"></span></span></div></div></div></section><section id="projects" class="scene scene--projects" data-component="projects-scene" aria-labelledby="projects-title" data-loc="src/components/projects/ProjectsScene.jsx:29:4"><div class="scene__inner" data-loc="src/components/projects/ProjectsScene.jsx:35:6"><div class="scene__narrative" data-loc="src/components/projects/ProjectsScene.jsx:36:8"><div class="scene-heading-block" data-component="scene-heading" data-loc="src/components/common/SceneHeading.jsx:16:4"><span class="deco-cluster deco-cluster--heading" aria-hidden="true" data-loc="src/components/common/Decor.jsx:39:4"><svg class="deco deco--twinkle " width="16" height="16" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:19:4" style="color: var(--color-accent-star); position: static;"><path d="M12 0.5 L14.4 9.6 L23.5 12 L14.4 14.4 L12 23.5 L9.6 14.4 L0.5 12 L9.6 9.6 Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:28:6"></path></svg><svg class="deco deco--twinkle " width="10" height="10" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:19:4" style="color: var(--color-accent-peach); position: static;"><path d="M12 0.5 L14.4 9.6 L23.5 12 L14.4 14.4 L12 23.5 L9.6 14.4 L0.5 12 L9.6 9.6 Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:28:6"></path></svg><svg class="deco deco--twinkle " width="7" height="7" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:19:4" style="color: var(--color-secondary); position: static;"><path d="M12 0.5 L14.4 9.6 L23.5 12 L14.4 14.4 L12 23.5 L9.6 14.4 L0.5 12 L9.6 9.6 Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:28:6"></path></svg></span><span class="eyebrow" data-loc="src/components/common/SceneHeading.jsx:18:6">PROJECTS</span><h2 class="scene-heading" id="projects-title" data-loc="src/components/common/SceneHeading.jsx:19:6">项目作品</h2><p class="scene-subtitle" data-loc="src/components/common/SceneHeading.jsx:22:18">一些自己动手做的小工具和网页。</p></div></div><div class="scene__content" data-loc="src/components/projects/ProjectsScene.jsx:45:8"><ul class="project-list" data-component="project-list" data-loc="src/components/projects/ProjectsScene.jsx:46:10"><li class="project-list__item" data-loc="src/components/projects/ProjectsScene.jsx:48:14"><button type="button" class="project-card" data-component="project-card" data-loc="src/components/projects/ProjectCard.jsx:15:4"><span class="project-card__cover" data-loc="src/components/projects/ProjectCard.jsx:21:6"><img src="./王佳妮的主页 · 个人介绍_files/project-journal-cover-v2.jpg" alt="插画：桌上的笔记本电脑打开着一份手账地图界面，旁边有一盆多肉和纸胶带" width="1536" height="1024" loading="lazy" decoding="async" data-loc="src/components/projects/ProjectCard.jsx:22:8"><span class="washi-tape project-card__tape" aria-hidden="true" data-loc="src/components/common/Decor.jsx:93:4" style="transform: rotate(-5deg);"></span></span><span class="project-card__body" data-loc="src/components/projects/ProjectCard.jsx:33:6"><span class="project-card__title" data-loc="src/components/projects/ProjectCard.jsx:34:8">手账地图</span><span class="project-card__desc" data-loc="src/components/projects/ProjectCard.jsx:35:8">把旅行照片和地点钉在一张地图上，随手写下当时的心情。</span><span class="project-card__tags" data-loc="src/components/projects/ProjectCard.jsx:36:8"><span class="tag-pill" data-loc="src/components/projects/ProjectCard.jsx:38:12">React</span><span class="tag-pill tag-pill--mint" data-loc="src/components/projects/ProjectCard.jsx:38:12">地图</span><span class="tag-pill tag-pill--sky" data-loc="src/components/projects/ProjectCard.jsx:38:12">手账</span></span></span></button></li><li class="project-list__item" data-loc="src/components/projects/ProjectsScene.jsx:48:14"><button type="button" class="project-card" data-component="project-card" data-loc="src/components/projects/ProjectCard.jsx:15:4"><span class="project-card__cover" data-loc="src/components/projects/ProjectCard.jsx:21:6"><img src="./王佳妮的主页 · 个人介绍_files/project-player-cover-v2.jpg" alt="插画：手机立在木支架上显示音乐播放器，前面放着一副耳机" width="1536" height="1024" loading="lazy" decoding="async" data-loc="src/components/projects/ProjectCard.jsx:22:8"><span class="washi-tape project-card__tape" aria-hidden="true" data-loc="src/components/common/Decor.jsx:93:4" style="transform: rotate(-5deg);"></span></span><span class="project-card__body" data-loc="src/components/projects/ProjectCard.jsx:33:6"><span class="project-card__title" data-loc="src/components/projects/ProjectCard.jsx:34:8">心情电台</span><span class="project-card__desc" data-loc="src/components/projects/ProjectCard.jsx:35:8">按心情选一张歌单，播放界面会跟着情绪换颜色。</span><span class="project-card__tags" data-loc="src/components/projects/ProjectCard.jsx:36:8"><span class="tag-pill" data-loc="src/components/projects/ProjectCard.jsx:38:12">动效</span><span class="tag-pill tag-pill--mint" data-loc="src/components/projects/ProjectCard.jsx:38:12">音乐</span><span class="tag-pill tag-pill--sky" data-loc="src/components/projects/ProjectCard.jsx:38:12">交互</span></span></span></button></li><li class="project-list__item" data-loc="src/components/projects/ProjectsScene.jsx:48:14"><button type="button" class="project-card" data-component="project-card" data-loc="src/components/projects/ProjectCard.jsx:15:4"><span class="project-card__cover" data-loc="src/components/projects/ProjectCard.jsx:21:6"><img src="./王佳妮的主页 · 个人介绍_files/project-plant-cover-v2.jpg" alt="插画：窗台上三盆绿植，上方浮着一块植物养护提醒面板" width="1536" height="1024" loading="lazy" decoding="async" data-loc="src/components/projects/ProjectCard.jsx:22:8"><span class="washi-tape project-card__tape" aria-hidden="true" data-loc="src/components/common/Decor.jsx:93:4" style="transform: rotate(-5deg);"></span></span><span class="project-card__body" data-loc="src/components/projects/ProjectCard.jsx:33:6"><span class="project-card__title" data-loc="src/components/projects/ProjectCard.jsx:34:8">植物提醒</span><span class="project-card__desc" data-loc="src/components/projects/ProjectCard.jsx:35:8">给家里的绿植排个浇水表，到点轻轻提醒一次。</span><span class="project-card__tags" data-loc="src/components/projects/ProjectCard.jsx:36:8"><span class="tag-pill" data-loc="src/components/projects/ProjectCard.jsx:38:12">仪表盘</span><span class="tag-pill tag-pill--mint" data-loc="src/components/projects/ProjectCard.jsx:38:12">提醒</span><span class="tag-pill tag-pill--sky" data-loc="src/components/projects/ProjectCard.jsx:38:12">插画</span></span></span></button></li><li class="project-list__item" data-loc="src/components/projects/ProjectsScene.jsx:48:14"><button type="button" class="project-card" data-component="project-card" data-loc="src/components/projects/ProjectCard.jsx:15:4"><span class="project-card__cover" data-loc="src/components/projects/ProjectCard.jsx:21:6"><img src="./王佳妮的主页 · 个人介绍_files/project-scrapbook-cover-v2.jpg" alt="插画：平板电脑上是一面拼贴相册，周围放着纸胶带、剪刀和贴纸" width="1536" height="1024" loading="lazy" decoding="async" data-loc="src/components/projects/ProjectCard.jsx:22:8"><span class="washi-tape project-card__tape" aria-hidden="true" data-loc="src/components/common/Decor.jsx:93:4" style="transform: rotate(-5deg);"></span></span><span class="project-card__body" data-loc="src/components/projects/ProjectCard.jsx:33:6"><span class="project-card__title" data-loc="src/components/projects/ProjectCard.jsx:34:8">拼贴相册</span><span class="project-card__desc" data-loc="src/components/projects/ProjectCard.jsx:35:8">像剪贴本一样排照片，随手贴纸胶带，排好就能导出。</span><span class="project-card__tags" data-loc="src/components/projects/ProjectCard.jsx:36:8"><span class="tag-pill" data-loc="src/components/projects/ProjectCard.jsx:38:12">相册</span><span class="tag-pill tag-pill--mint" data-loc="src/components/projects/ProjectCard.jsx:38:12">排版</span><span class="tag-pill tag-pill--sky" data-loc="src/components/projects/ProjectCard.jsx:38:12">拼贴</span></span></span></button></li></ul><span class="blush-dots project-blush" aria-hidden="true" data-loc="src/components/common/Decor.jsx:155:4"><span data-loc="src/components/common/Decor.jsx:156:6"></span><span data-loc="src/components/common/Decor.jsx:157:6"></span></span></div></div></section><section id="index" class="scene scene--index" data-component="index-scene" aria-labelledby="index-title" data-loc="src/components/index/IndexScene.jsx:60:4"><div class="scene__inner" data-loc="src/components/index/IndexScene.jsx:66:6"><div class="scene__narrative" data-loc="src/components/index/IndexScene.jsx:67:8"><div class="scene-heading-block" data-component="scene-heading" data-loc="src/components/common/SceneHeading.jsx:16:4"><span class="deco-cluster deco-cluster--heading" aria-hidden="true" data-loc="src/components/common/Decor.jsx:39:4"><svg class="deco deco--twinkle " width="16" height="16" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:19:4" style="color: var(--color-accent-star); position: static;"><path d="M12 0.5 L14.4 9.6 L23.5 12 L14.4 14.4 L12 23.5 L9.6 14.4 L0.5 12 L9.6 9.6 Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:28:6"></path></svg><svg class="deco deco--twinkle " width="10" height="10" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:19:4" style="color: var(--color-accent-peach); position: static;"><path d="M12 0.5 L14.4 9.6 L23.5 12 L14.4 14.4 L12 23.5 L9.6 14.4 L0.5 12 L9.6 9.6 Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:28:6"></path></svg><svg class="deco deco--twinkle " width="7" height="7" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:19:4" style="color: var(--color-secondary); position: static;"><path d="M12 0.5 L14.4 9.6 L23.5 12 L14.4 14.4 L12 23.5 L9.6 14.4 L0.5 12 L9.6 9.6 Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:28:6"></path></svg></span><span class="eyebrow" data-loc="src/components/common/SceneHeading.jsx:18:6">INDEX</span><h2 class="scene-heading" id="index-title" data-loc="src/components/common/SceneHeading.jsx:19:6">目录</h2><p class="scene-subtitle" data-loc="src/components/common/SceneHeading.jsx:22:18">想先看哪一段，从这里点进去。</p><p class="scene-help" data-loc="src/components/common/SceneHeading.jsx:23:14">上下滚动查看，也可以用方向键上下移动、回车跳转。</p></div></div><div class="scene__content" data-loc="src/components/index/IndexScene.jsx:77:8"><div class="scroll-list-container" data-component="index-list" data-loc="src/components/animated-list/AnimatedList.jsx:140:4"><div class="scroll-list" role="list" aria-label="页面目录" data-loc="src/components/animated-list/AnimatedList.jsx:141:6"><div data-index="0" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item selected" data-kind="scene" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__notch" aria-hidden="true" data-loc="src/components/animated-list/AnimatedList.jsx:166:30"></span><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">SCENE 01</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">欢迎</span></span><span class="item__badge item__badge--scene" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">场景</span></button></div><div data-index="1" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="scene" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">SCENE 02</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">作品</span></span><span class="item__badge item__badge--scene" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">场景</span></button></div><div data-index="2" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="scene" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">SCENE 03</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">目录</span></span><span class="item__badge item__badge--scene" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">场景</span></button></div><div data-index="3" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="scene" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">SCENE 04</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">爱好</span></span><span class="item__badge item__badge--scene" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">场景</span></button></div><div data-index="4" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="scene" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">SCENE 05</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">联系我</span></span><span class="item__badge item__badge--scene" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">场景</span></button></div><div data-index="5" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="project" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">PROJECT 01</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">手账地图</span></span><span class="item__badge item__badge--project" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">作品</span></button></div><div data-index="6" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="project" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">PROJECT 02</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">心情电台</span></span><span class="item__badge item__badge--project" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">作品</span></button></div><div data-index="7" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="project" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">PROJECT 03</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">植物提醒</span></span><span class="item__badge item__badge--project" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">作品</span></button></div><div data-index="8" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="project" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">PROJECT 04</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">拼贴相册</span></span><span class="item__badge item__badge--project" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">作品</span></button></div><div data-index="9" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="gallery" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">PHOTO 01</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">林间小路</span></span><span class="item__badge item__badge--gallery" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">爱好</span></button></div><div data-index="10" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="gallery" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">PHOTO 02</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">海边日落</span></span><span class="item__badge item__badge--gallery" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">爱好</span></button></div><div data-index="11" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="gallery" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">PHOTO 03</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">窗边咖啡</span></span><span class="item__badge item__badge--gallery" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">爱好</span></button></div><div data-index="12" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="gallery" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">PHOTO 04</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">星空湖边</span></span><span class="item__badge item__badge--gallery" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">爱好</span></button></div><div data-index="13" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="gallery" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">PHOTO 05</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">慢慢走</span></span><span class="item__badge item__badge--gallery" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">爱好</span></button></div><div data-index="14" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="gallery" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">PHOTO 06</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">去看海</span></span><span class="item__badge item__badge--gallery" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">爱好</span></button></div><div data-index="15" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="gallery" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">PHOTO 07</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">安静的下午</span></span><span class="item__badge item__badge--gallery" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">爱好</span></button></div><div data-index="16" class="animated-item" data-loc="src/components/animated-list/AnimatedList.jsx:26:4" style="opacity: 0; transform: scale(0.7);"><button type="button" class="item" data-kind="gallery" data-loc="src/components/animated-list/AnimatedList.jsx:159:14"><span class="item__text" data-loc="src/components/animated-list/AnimatedList.jsx:167:16"><span class="item__micro micro-label" data-loc="src/components/animated-list/AnimatedList.jsx:169:20">PHOTO 08</span><span class="item__label" data-loc="src/components/animated-list/AnimatedList.jsx:171:18">夜里散步</span></span><span class="item__badge item__badge--gallery" data-loc="src/components/animated-list/AnimatedList.jsx:174:18">爱好</span></button></div></div><div class="top-gradient" aria-hidden="true" data-loc="src/components/animated-list/AnimatedList.jsx:186:10" style="opacity: 0;"></div><div class="bottom-gradient" aria-hidden="true" data-loc="src/components/animated-list/AnimatedList.jsx:187:10" style="opacity: 1;"></div></div></div></div></section><section id="gallery" class="scene scene--gallery" data-component="gallery-scene" aria-labelledby="gallery-title" data-loc="src/components/gallery/GalleryScene.jsx:153:4"><div class="scene__inner" data-loc="src/components/gallery/GalleryScene.jsx:159:6"><div class="scene__narrative" data-loc="src/components/gallery/GalleryScene.jsx:160:8"><div class="scene-heading-block" data-component="scene-heading" data-loc="src/components/common/SceneHeading.jsx:16:4"><span class="deco-cluster deco-cluster--heading" aria-hidden="true" data-loc="src/components/common/Decor.jsx:39:4"><svg class="deco deco--twinkle " width="16" height="16" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:19:4" style="color: var(--color-accent-star); position: static;"><path d="M12 0.5 L14.4 9.6 L23.5 12 L14.4 14.4 L12 23.5 L9.6 14.4 L0.5 12 L9.6 9.6 Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:28:6"></path></svg><svg class="deco deco--twinkle " width="10" height="10" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:19:4" style="color: var(--color-accent-peach); position: static;"><path d="M12 0.5 L14.4 9.6 L23.5 12 L14.4 14.4 L12 23.5 L9.6 14.4 L0.5 12 L9.6 9.6 Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:28:6"></path></svg><svg class="deco deco--twinkle " width="7" height="7" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:19:4" style="color: var(--color-secondary); position: static;"><path d="M12 0.5 L14.4 9.6 L23.5 12 L14.4 14.4 L12 23.5 L9.6 14.4 L0.5 12 L9.6 9.6 Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:28:6"></path></svg></span><span class="eyebrow" data-loc="src/components/common/SceneHeading.jsx:18:6">GALLERY</span><h2 class="scene-heading" id="gallery-title" data-loc="src/components/common/SceneHeading.jsx:19:6">爱好展示</h2><p class="scene-subtitle" data-loc="src/components/common/SceneHeading.jsx:22:18">把路过的风景，收进一格一格的时间里。</p></div></div><div class="scene__content" data-loc="src/components/gallery/GalleryScene.jsx:169:8"><div class="carousel" data-component="gallery-carousel" data-loc="src/components/gallery/GalleryScene.jsx:170:10"><div class="carousel__viewport" data-loc="src/components/gallery/GalleryScene.jsx:171:12"><ul class="carousel__track" data-loc="src/components/gallery/GalleryScene.jsx:182:14"><li class="slide slide--active" data-loc="src/components/gallery/GalleryScene.jsx:184:18"><span class="washi-tape slide__tape" aria-hidden="true" data-loc="src/components/common/Decor.jsx:93:4" style="transform: rotate(-4deg);"></span><button type="button" class="slide__button" data-loc="src/components/gallery/GalleryScene.jsx:194:20"><span class="slide__frame" data-loc="src/components/gallery/GalleryScene.jsx:205:22"><img src="./王佳妮的主页 · 个人介绍_files/gallery-green-path-v2.jpg" alt="插画：两侧都是绿叶的小路向前延伸，一位戴草帽的女孩背对着镜头走远，右侧有一张木长椅" width="1280" height="853" loading="lazy" decoding="async" data-loc="src/components/gallery/GalleryScene.jsx:206:24"></span><span class="slide-caption" data-loc="src/components/gallery/GalleryScene.jsx:216:22"><span class="slide-caption__title" data-loc="src/components/gallery/GalleryScene.jsx:217:24">林间小路</span><span class="slide-caption__text" data-loc="src/components/gallery/GalleryScene.jsx:218:24">风穿过树叶，把光斑洒在石阶上。</span><span class="slide-caption__date" data-loc="src/components/gallery/GalleryScene.jsx:219:24"><svg class="" width="12" height="12" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:50:4" style="color: var(--color-primary); flex: 0 0 auto;"><path d="M12 21.2C9.6 19.3 3 14.4 3 9.4 3 6.4 5.2 4.4 7.7 4.4c1.7 0 3.2.9 4.3 2.6 1.1-1.7 2.6-2.6 4.3-2.6C18.8 4.4 21 6.4 21 9.4c0 5-6.6 9.9-9 11.8Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:63:6"></path></svg><span data-loc="src/components/gallery/GalleryScene.jsx:221:26">2026.04</span></span></span></button></li><li class="slide" data-loc="src/components/gallery/GalleryScene.jsx:184:18"><button type="button" class="slide__button" data-loc="src/components/gallery/GalleryScene.jsx:194:20"><span class="slide__frame" data-loc="src/components/gallery/GalleryScene.jsx:205:22"><img src="./王佳妮的主页 · 个人介绍_files/gallery-seaside-sunset-v2.jpg" alt="插画：黄昏的海边，木栈道伸向海面，太阳贴近地平线" width="1280" height="853" loading="lazy" decoding="async" data-loc="src/components/gallery/GalleryScene.jsx:206:24"></span><span class="slide-caption" data-loc="src/components/gallery/GalleryScene.jsx:216:22"><span class="slide-caption__title" data-loc="src/components/gallery/GalleryScene.jsx:217:24">海边日落</span><span class="slide-caption__text" data-loc="src/components/gallery/GalleryScene.jsx:218:24">浪声慢慢靠岸，把一天交给黄昏。</span><span class="slide-caption__date" data-loc="src/components/gallery/GalleryScene.jsx:219:24"><svg class="" width="12" height="12" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:50:4" style="color: var(--color-primary); flex: 0 0 auto;"><path d="M12 21.2C9.6 19.3 3 14.4 3 9.4 3 6.4 5.2 4.4 7.7 4.4c1.7 0 3.2.9 4.3 2.6 1.1-1.7 2.6-2.6 4.3-2.6C18.8 4.4 21 6.4 21 9.4c0 5-6.6 9.9-9 11.8Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:63:6"></path></svg><span data-loc="src/components/gallery/GalleryScene.jsx:221:26">2026.03</span></span></span></button></li><li class="slide" data-loc="src/components/gallery/GalleryScene.jsx:184:18"><button type="button" class="slide__button" data-loc="src/components/gallery/GalleryScene.jsx:194:20"><span class="slide__frame" data-loc="src/components/gallery/GalleryScene.jsx:205:22"><img src="./王佳妮的主页 · 个人介绍_files/gallery-cafe-corner-v2.jpg" alt="插画：窗边木桌上一杯拉花咖啡和一本打开的笔记本，窗台有一盆垂落的绿植" width="1280" height="853" loading="lazy" decoding="async" data-loc="src/components/gallery/GalleryScene.jsx:206:24"></span><span class="slide-caption" data-loc="src/components/gallery/GalleryScene.jsx:216:22"><span class="slide-caption__title" data-loc="src/components/gallery/GalleryScene.jsx:217:24">窗边咖啡</span><span class="slide-caption__text" data-loc="src/components/gallery/GalleryScene.jsx:218:24">一杯热拿铁，一本还没写完的笔记。</span><span class="slide-caption__date" data-loc="src/components/gallery/GalleryScene.jsx:219:24"><svg class="" width="12" height="12" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:50:4" style="color: var(--color-primary); flex: 0 0 auto;"><path d="M12 21.2C9.6 19.3 3 14.4 3 9.4 3 6.4 5.2 4.4 7.7 4.4c1.7 0 3.2.9 4.3 2.6 1.1-1.7 2.6-2.6 4.3-2.6C18.8 4.4 21 6.4 21 9.4c0 5-6.6 9.9-9 11.8Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:63:6"></path></svg><span data-loc="src/components/gallery/GalleryScene.jsx:221:26">2026.02</span></span></span></button></li><li class="slide" data-loc="src/components/gallery/GalleryScene.jsx:184:18"><button type="button" class="slide__button" data-loc="src/components/gallery/GalleryScene.jsx:194:20"><span class="slide__frame" data-loc="src/components/gallery/GalleryScene.jsx:205:22"><img src="./王佳妮的主页 · 个人介绍_files/gallery-starry-lake-v2.jpg" alt="插画：夜晚的湖边，天空是渐变的紫色，远处山影安静地立着" width="1280" height="853" loading="lazy" decoding="async" data-loc="src/components/gallery/GalleryScene.jsx:206:24"></span><span class="slide-caption" data-loc="src/components/gallery/GalleryScene.jsx:216:22"><span class="slide-caption__title" data-loc="src/components/gallery/GalleryScene.jsx:217:24">星空湖边</span><span class="slide-caption__text" data-loc="src/components/gallery/GalleryScene.jsx:218:24">星星落在水面上，风也跟着安静了。</span><span class="slide-caption__date" data-loc="src/components/gallery/GalleryScene.jsx:219:24"><svg class="" width="12" height="12" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:50:4" style="color: var(--color-primary); flex: 0 0 auto;"><path d="M12 21.2C9.6 19.3 3 14.4 3 9.4 3 6.4 5.2 4.4 7.7 4.4c1.7 0 3.2.9 4.3 2.6 1.1-1.7 2.6-2.6 4.3-2.6C18.8 4.4 21 6.4 21 9.4c0 5-6.6 9.9-9 11.8Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:63:6"></path></svg><span data-loc="src/components/gallery/GalleryScene.jsx:221:26">2026.01</span></span></span></button></li><li class="slide" data-loc="src/components/gallery/GalleryScene.jsx:184:18"><button type="button" class="slide__button" data-loc="src/components/gallery/GalleryScene.jsx:194:20"><span class="slide__frame" data-loc="src/components/gallery/GalleryScene.jsx:205:22"><img src="./王佳妮的主页 · 个人介绍_files/gallery-green-path-v2.jpg" alt="插画：林间小路的另一段，石板路与草地，阳光从树叶间洒下来" width="1280" height="853" loading="lazy" decoding="async" data-loc="src/components/gallery/GalleryScene.jsx:206:24"></span><span class="slide-caption" data-loc="src/components/gallery/GalleryScene.jsx:216:22"><span class="slide-caption__title" data-loc="src/components/gallery/GalleryScene.jsx:217:24">慢慢走</span><span class="slide-caption__text" data-loc="src/components/gallery/GalleryScene.jsx:218:24">沿着小路往前走，夏天就在前面。</span><span class="slide-caption__date" data-loc="src/components/gallery/GalleryScene.jsx:219:24"><svg class="" width="12" height="12" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:50:4" style="color: var(--color-primary); flex: 0 0 auto;"><path d="M12 21.2C9.6 19.3 3 14.4 3 9.4 3 6.4 5.2 4.4 7.7 4.4c1.7 0 3.2.9 4.3 2.6 1.1-1.7 2.6-2.6 4.3-2.6C18.8 4.4 21 6.4 21 9.4c0 5-6.6 9.9-9 11.8Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:63:6"></path></svg><span data-loc="src/components/gallery/GalleryScene.jsx:221:26">2025.12</span></span></span></button></li><li class="slide" data-loc="src/components/gallery/GalleryScene.jsx:184:18"><button type="button" class="slide__button" data-loc="src/components/gallery/GalleryScene.jsx:194:20"><span class="slide__frame" data-loc="src/components/gallery/GalleryScene.jsx:205:22"><img src="./王佳妮的主页 · 个人介绍_files/gallery-seaside-sunset-v2.jpg" alt="插画：海边木栈道与渐变的天空，两只海鸟飞过" width="1280" height="853" loading="lazy" decoding="async" data-loc="src/components/gallery/GalleryScene.jsx:206:24"></span><span class="slide-caption" data-loc="src/components/gallery/GalleryScene.jsx:216:22"><span class="slide-caption__title" data-loc="src/components/gallery/GalleryScene.jsx:217:24">去看海</span><span class="slide-caption__text" data-loc="src/components/gallery/GalleryScene.jsx:218:24">木栈道伸进海里，风从很远的地方来。</span><span class="slide-caption__date" data-loc="src/components/gallery/GalleryScene.jsx:219:24"><svg class="" width="12" height="12" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:50:4" style="color: var(--color-primary); flex: 0 0 auto;"><path d="M12 21.2C9.6 19.3 3 14.4 3 9.4 3 6.4 5.2 4.4 7.7 4.4c1.7 0 3.2.9 4.3 2.6 1.1-1.7 2.6-2.6 4.3-2.6C18.8 4.4 21 6.4 21 9.4c0 5-6.6 9.9-9 11.8Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:63:6"></path></svg><span data-loc="src/components/gallery/GalleryScene.jsx:221:26">2025.11</span></span></span></button></li><li class="slide" data-loc="src/components/gallery/GalleryScene.jsx:184:18"><button type="button" class="slide__button" data-loc="src/components/gallery/GalleryScene.jsx:194:20"><span class="slide__frame" data-loc="src/components/gallery/GalleryScene.jsx:205:22"><img src="./王佳妮的主页 · 个人介绍_files/gallery-cafe-corner-v2.jpg" alt="插画：午后的窗边角落，咖啡、笔记本与垂落的绿植" width="1280" height="853" loading="lazy" decoding="async" data-loc="src/components/gallery/GalleryScene.jsx:206:24"></span><span class="slide-caption" data-loc="src/components/gallery/GalleryScene.jsx:216:22"><span class="slide-caption__title" data-loc="src/components/gallery/GalleryScene.jsx:217:24">安静的下午</span><span class="slide-caption__text" data-loc="src/components/gallery/GalleryScene.jsx:218:24">窗外有花，桌上有光，时间慢下来。</span><span class="slide-caption__date" data-loc="src/components/gallery/GalleryScene.jsx:219:24"><svg class="" width="12" height="12" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:50:4" style="color: var(--color-primary); flex: 0 0 auto;"><path d="M12 21.2C9.6 19.3 3 14.4 3 9.4 3 6.4 5.2 4.4 7.7 4.4c1.7 0 3.2.9 4.3 2.6 1.1-1.7 2.6-2.6 4.3-2.6C18.8 4.4 21 6.4 21 9.4c0 5-6.6 9.9-9 11.8Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:63:6"></path></svg><span data-loc="src/components/gallery/GalleryScene.jsx:221:26">2025.10</span></span></span></button></li><li class="slide" data-loc="src/components/gallery/GalleryScene.jsx:184:18"><button type="button" class="slide__button" data-loc="src/components/gallery/GalleryScene.jsx:194:20"><span class="slide__frame" data-loc="src/components/gallery/GalleryScene.jsx:205:22"><img src="./王佳妮的主页 · 个人介绍_files/gallery-starry-lake-v2.jpg" alt="插画：紫色夜空下的湖岸与山影，湖面有细碎的星光倒影" width="1280" height="853" loading="lazy" decoding="async" data-loc="src/components/gallery/GalleryScene.jsx:206:24"></span><span class="slide-caption" data-loc="src/components/gallery/GalleryScene.jsx:216:22"><span class="slide-caption__title" data-loc="src/components/gallery/GalleryScene.jsx:217:24">夜里散步</span><span class="slide-caption__text" data-loc="src/components/gallery/GalleryScene.jsx:218:24">山影安静地站着，像在等我拍完这张。</span><span class="slide-caption__date" data-loc="src/components/gallery/GalleryScene.jsx:219:24"><svg class="" width="12" height="12" viewBox="0 0 24 24" aria-hidden="true" focusable="false" data-loc="src/components/common/Decor.jsx:50:4" style="color: var(--color-primary); flex: 0 0 auto;"><path d="M12 21.2C9.6 19.3 3 14.4 3 9.4 3 6.4 5.2 4.4 7.7 4.4c1.7 0 3.2.9 4.3 2.6 1.1-1.7 2.6-2.6 4.3-2.6C18.8 4.4 21 6.4 21 9.4c0 5-6.6 9.9-9 11.8Z" fill="currentColor" data-loc="src/components/common/Decor.jsx:63:6"></path></svg><span data-loc="src/components/gallery/GalleryScene.jsx:221:26">2025.09</span></span></span></button></li></ul></div><div class="carousel__controls" data-loc="src/components/gallery/GalleryScene.jsx:230:12"><span class="counter carousel__counter" aria-live="polite" data-loc="src/components/gallery/GalleryScene.jsx:231:14">01 / 08</span><div class="carousel__buttons" data-loc="src/components/gallery/GalleryScene.jsx:235:14"><button type="button" class="btn btn--icon carousel__btn" disabled="" aria-label="上一张" data-loc="src/components/gallery/GalleryScene.jsx:236:16"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-left" aria-hidden="true" data-loc="src/components/gallery/GalleryScene.jsx:243:18"><path d="m15 18-6-6 6-6"></path></svg></button><button type="button" class="btn btn--icon carousel__btn" aria-label="下一张" data-loc="src/components/gallery/GalleryScene.jsx:245:16"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-right" aria-hidden="true" data-loc="src/components/gallery/GalleryScene.jsx:252:18"><path d="m9 18 6-6-6-6"></path></svg></button></div></div></div></div></div></section><section id="contact" class="scene scene--contact" data-component="contact-scene" aria-labelledby="contact-title" data-loc="src/components/contact/ContactScene.jsx:21:4"><span aria-hidden="true" data-loc="src/components/common/Decor.jsx:113:4"><span class="deco deco--float petal" data-loc="src/components/common/Decor.jsx:115:8" style="top: 12%; left: 6%; width: 12px; height: 18px; animation-delay: 0s;"></span><span class="deco deco--float petal" data-loc="src/components/common/Decor.jsx:115:8" style="top: 24%; left: 88%; width: 9px; height: 13.5px; animation-delay: 0.6s;"></span><span class="deco deco--float petal" data-loc="src/components/common/Decor.jsx:115:8" style="top: 58%; left: 3%; width: 10px; height: 15px; animation-delay: 1.2s;"></span><span class="deco deco--float petal" data-loc="src/components/common/Decor.jsx:115:8" style="top: 72%; left: 92%; width: 13px; height: 19.5px; animation-delay: 0.3s;"></span><span class="deco deco--float petal" data-loc="src/components/common/Decor.jsx:115:8" style="top: 38%; left: 94%; width: 8px; height: 12px; animation-delay: 1.8s;"></span><span class="deco deco--float petal" data-loc="src/components/common/Decor.jsx:115:8" style="top: 86%; left: 10%; width: 11px; height: 16.5px; animation-delay: 2.4s;"></span></span><div class="scene__inner" data-loc="src/components/contact/ContactScene.jsx:29:6"><div class="scene__narrative" data-loc="src/components/contact/ContactScene.jsx:30:8"><span class="eyebrow" data-loc="src/components/contact/ContactScene.jsx:31:10">SCENE 05 / CONTACT</span><h2 class="contact-heading" id="contact-title" data-loc="src/components/contact/ContactScene.jsx:32:10">联系我<span class="contact-heading__en" data-loc="src/components/contact/ContactScene.jsx:34:12"> / Contact</span></h2><p class="contact-invitation" data-loc="src/components/contact/ContactScene.jsx:36:10">如果对我的作品或合作感兴趣，可以从下面任意一种方式找到我。</p><ul class="contact-rows" data-component="contact-rows" data-loc="src/components/contact/ContactScene.jsx:38:10"><li class="contact-rows__item" data-loc="src/components/contact/ContactScene.jsx:61:16"><div class="contact-row" data-loc="src/components/contact/ContactScene.jsx:67:20"><span class="contact-row__badge contact-row__badge--mint" aria-hidden="true" data-loc="src/components/contact/ContactScene.jsx:43:18"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-mail" data-loc="src/components/contact/ContactScene.jsx:47:20"><rect width="20" height="16" x="2" y="4" rx="2"></rect><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"></path></svg></span><span class="contact-row__text" data-loc="src/components/contact/ContactScene.jsx:49:18"><span class="contact-row__label" data-loc="src/components/contact/ContactScene.jsx:50:20"><span class="micro-label" data-loc="src/components/contact/ContactScene.jsx:51:22">EMAIL</span><span class="contact-row__name" data-loc="src/components/contact/ContactScene.jsx:52:22">邮箱</span></span><span class="contact-row__value" data-loc="src/components/contact/ContactScene.jsx:54:20">hello@example.com</span><span class="contact-row__role" data-loc="src/components/contact/ContactScene.jsx:55:20">合作 · 项目咨询</span></span></div></li><li class="contact-rows__item" data-loc="src/components/contact/ContactScene.jsx:61:16"><div class="contact-row" data-loc="src/components/contact/ContactScene.jsx:67:20"><span class="contact-row__badge contact-row__badge--sky" aria-hidden="true" data-loc="src/components/contact/ContactScene.jsx:43:18"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-github" data-loc="src/components/contact/ContactScene.jsx:47:20"><path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"></path><path d="M9 18c-4.51 2-5-2-7-2"></path></svg></span><span class="contact-row__text" data-loc="src/components/contact/ContactScene.jsx:49:18"><span class="contact-row__label" data-loc="src/components/contact/ContactScene.jsx:50:20"><span class="micro-label" data-loc="src/components/contact/ContactScene.jsx:51:22">GITHUB</span><span class="contact-row__name" data-loc="src/components/contact/ContactScene.jsx:52:22">GitHub</span></span><span class="contact-row__value" data-loc="src/components/contact/ContactScene.jsx:54:20">your-github</span><span class="contact-row__role" data-loc="src/components/contact/ContactScene.jsx:55:20">代码 · 作品集</span></span></div></li><li class="contact-rows__item" data-loc="src/components/contact/ContactScene.jsx:61:16"><div class="contact-row" data-loc="src/components/contact/ContactScene.jsx:67:20"><span class="contact-row__badge contact-row__badge--lilac" aria-hidden="true" data-loc="src/components/contact/ContactScene.jsx:43:18"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-video" data-loc="src/components/contact/ContactScene.jsx:47:20"><path d="m16 13 5.223 3.482a.5.5 0 0 0 .777-.416V7.87a.5.5 0 0 0-.752-.432L16 10.5"></path><rect x="2" y="6" width="14" height="12" rx="2"></rect></svg></span><span class="contact-row__text" data-loc="src/components/contact/ContactScene.jsx:49:18"><span class="contact-row__label" data-loc="src/components/contact/ContactScene.jsx:50:20"><span class="micro-label" data-loc="src/components/contact/ContactScene.jsx:51:22">DOUYIN</span><span class="contact-row__name" data-loc="src/components/contact/ContactScene.jsx:52:22">抖音</span></span><span class="contact-row__value" data-loc="src/components/contact/ContactScene.jsx:54:20">your-douyin</span><span class="contact-row__role" data-loc="src/components/contact/ContactScene.jsx:55:20">日常 · 短视频</span></span></div></li></ul></div><div class="scene__content" data-loc="src/components/contact/ContactScene.jsx:75:8"><form class="feedback-panel" data-component="feedback-form" novalidate="" data-loc="src/components/contact/FeedbackPanel.jsx:76:4"><span class="eyebrow" data-loc="src/components/contact/FeedbackPanel.jsx:82:6">FEEDBACK</span><h3 class="panel-title" data-loc="src/components/contact/FeedbackPanel.jsx:83:6">用户反馈</h3><p class="feedback-panel__help" data-loc="src/components/contact/FeedbackPanel.jsx:84:6">写点什么都可以，这条留言只会在本页显示，不会发送到服务器。</p><div class="field" data-loc="src/components/contact/FeedbackPanel.jsx:86:6"><label class="field__label micro-label" for="feedback-name" data-loc="src/components/contact/FeedbackPanel.jsx:87:8">NAME / 姓名</label><input id="feedback-name" class="field__input" name="name" type="text" placeholder="怎么称呼你" data-loc="src/components/contact/FeedbackPanel.jsx:90:8" value=""></div><div class="field" data-loc="src/components/contact/FeedbackPanel.jsx:112:6"><label class="field__label micro-label" for="feedback-email" data-loc="src/components/contact/FeedbackPanel.jsx:113:8">EMAIL / 邮箱</label><input id="feedback-email" class="field__input" name="email" type="email" placeholder="方便回复的邮箱" data-loc="src/components/contact/FeedbackPanel.jsx:116:8" value=""></div><div class="field" data-loc="src/components/contact/FeedbackPanel.jsx:138:6"><label class="field__label micro-label" for="feedback-message" data-loc="src/components/contact/FeedbackPanel.jsx:139:8">MESSAGE / 留言内容</label><textarea id="feedback-message" class="field__input field__input--textarea" name="message" rows="4" placeholder="想说的话" data-loc="src/components/contact/FeedbackPanel.jsx:142:8"></textarea></div><button type="submit" class="btn btn--primary feedback-panel__submit" data-loc="src/components/contact/FeedbackPanel.jsx:166:6">提交 / Submit</button></form></div></div></section></main><div class="scene-indicator" data-component="scene-indicator" role="status" aria-live="polite" data-loc="src/components/header/SceneIndicator.jsx:9:4"><span class="scene-indicator__rule" aria-hidden="true" data-loc="src/components/header/SceneIndicator.jsx:15:6"></span><span class="scene-indicator__label" data-loc="src/components/header/SceneIndicator.jsx:16:6">SCENE 01 · 欢迎</span></div><nav class="mobile-nav" aria-label="场景切换" data-loc="src/pages/HomePage.jsx:144:6"><button type="button" class="mobile-nav__btn" disabled="" data-loc="src/pages/HomePage.jsx:145:8"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-left" aria-hidden="true" data-loc="src/pages/HomePage.jsx:151:10"><path d="m15 18-6-6 6-6"></path></svg><span aria-hidden="true" data-loc="src/pages/HomePage.jsx:152:10">PREV</span><span class="visually-hidden" data-loc="src/pages/HomePage.jsx:153:10">上一个场景</span></button><button type="button" class="mobile-nav__btn" data-loc="src/pages/HomePage.jsx:155:8"><span aria-hidden="true" data-loc="src/pages/HomePage.jsx:161:10">NEXT</span><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-right" aria-hidden="true" data-loc="src/pages/HomePage.jsx:162:10"><path d="m9 18 6-6-6-6"></path></svg><span class="visually-hidden" data-loc="src/pages/HomePage.jsx:163:10">下一个场景</span></button></nav></div>
    <script type="module" src="./王佳妮的主页 · 个人介绍_files/main.jsx"></script>
  

</body></html>
