# 3DView
A clunky re-implementation of the aborted Firefox 3D view


----- 


<a href="javascript:(function (){ let style = document.createElement('style'); style.innerHTML = '[debug=true] { outline: 1px solid lime; outline-offset: -1px; -webkit-transform-style: preserve-3d; transform-style: preserve-3d; -webkit-perspective: 600px; perspective: 600px; } [debug=true] * { outline: 1px solid lime; outline-offset: -1px; box-shadow: 0 0 100px rgba(0, 0, 0, 0.4); -webkit-transition: all 0.5s ease; transition: all 0.5s ease; } [debug=true] *:before, [debug=true] *:after { outline: 1px solid red; outline-offset: -1px; box-shadow: 0 0 100px rgba(0, 0, 0, 0.4); left: 40px; } [debug=true] section, [debug=true] div.hero { -webkit-transform: rotateY(16deg) scale(0.8) translateX(15%) skewY(-6deg); transform: rotateY(16deg) scale(0.8) translateX(15%) skewY(-6deg); } @media (min-width: 1600px) { [debug=true] section, [debug=true] div.hero { -webkit-transform: rotateY(16deg) scale(0.6) translateX(15%) skewY(-6deg); transform: rotateY(16deg) scale(0.6) translateX(15%) skewY(-6deg); } } [debug=true] section p { left: 80px; } [debug=true] section:hover article:after { -webkit-transform: none !important; transform: none !important; }'; document.head.appendChild(style); document.body.setAttribute('debug','true'); })();">Drag'N'Drop this bookmarklet</a>
