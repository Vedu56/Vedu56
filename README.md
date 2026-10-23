<svg xmlns="http://www.w3.org/2000/svg" width="480" height="280" viewBox="0 0 480 280" role="img" aria-label="VT developer ID card">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0" stop-color="#1b2140"/>
      <stop offset=".55" stop-color="#0e1124"/>
      <stop offset="1" stop-color="#1a1030"/>
    </linearGradient>
    <linearGradient id="ring" x1="0" y1="0" x2="1" y2="1" gradientTransform="rotate(0 .5 .5)">
      <stop offset="0" stop-color="#5b8cff"/>
      <stop offset=".5" stop-color="#b46bff"/>
      <stop offset="1" stop-color="#ff6bb0"/>
      <animateTransform attributeName="gradientTransform" type="rotate" from="0 .5 .5" to="360 .5 .5" dur="6s" repeatCount="indefinite"/>
    </linearGradient>
    <linearGradient id="sheen" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0" stop-color="#fff" stop-opacity="0"/>
      <stop offset=".5" stop-color="#9fe8ff" stop-opacity=".22"/>
      <stop offset="1" stop-color="#fff" stop-opacity="0"/>
    </linearGradient>
    <linearGradient id="gold" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0" stop-color="#e8c97a"/>
      <stop offset="1" stop-color="#b88a2e"/>
    </linearGradient>
    <clipPath id="card"><rect width="480" height="280" rx="20"/></clipPath>
  </defs>

  <g clip-path="url(#card)" font-family="system-ui, -apple-system, 'Segoe UI', sans-serif">
    <rect width="480" height="280" fill="url(#bg)"/>
    <rect x=".5" y=".5" width="479" height="279" rx="20" fill="none" stroke="#ffffff" stroke-opacity=".12"/>

    <text x="170" y="48" font-size="10" letter-spacing="3" fill="#9aa3c7">DEVELOPER ID</text>
    <rect x="418" y="30" width="34" height="26" rx="6" fill="url(#gold)"/>


    <circle cx="90" cy="140" r="52" fill="url(#ring)"/>
    <circle cx="90" cy="140" r="47" fill="#12162b"/>
    <text x="90" y="153" font-size="38" font-weight="700" fill="#f2f4fb" text-anchor="middle">VT</text>


    <text x="170" y="108" font-size="40" font-weight="700" fill="#f2f4fb">VT</text>
    <text x="170" y="134" font-size="14" fill="#aab3d6">BSc Mathematics &amp; Statistics</text>


    <g font-size="10.5" fill="#f2f4fb" text-anchor="middle">
      <rect x="170" y="152" width="100" height="24" rx="12" fill="#ffffff" fill-opacity=".09" stroke="#ffffff" stroke-opacity=".14"/>
      <text x="220" y="168">Machine Learning</text>
      <rect x="278" y="152" width="76" height="24" rx="12" fill="#ffffff" fill-opacity=".09" stroke="#ffffff" stroke-opacity=".14"/>
      <text x="316" y="168">Data Science</text>
      <rect x="362" y="152" width="88" height="24" rx="12" fill="#ffffff" fill-opacity=".09" stroke="#ffffff" stroke-opacity=".14"/>
      <text x="406" y="168">Quant Finance</text>
    </g>

    <g font-size="10" letter-spacing="1" fill="#8d96bb">
      <text x="170" y="228">INST  <tspan fill="#e3e7f8" font-weight="600">QMUL</tspan></text>
      <text x="170" y="244">CLASS <tspan fill="#e3e7f8" font-weight="600">2030</tspan></text>
      <text x="170" y="260">ID    <tspan fill="#e3e7f8" font-weight="600">VT-2026</tspan></text>
    </g>


    <g fill="#e8ebf8" opacity=".85">
      <rect x="360" y="222" width="2" height="38"/><rect x="365" y="222" width="3" height="38"/>
      <rect x="371" y="222" width="1" height="38"/><rect x="375" y="222" width="3" height="38"/>
      <rect x="381" y="222" width="2" height="38"/><rect x="386" y="222" width="1" height="38"/>
      <rect x="390" y="222" width="3" height="38"/><rect x="396" y="222" width="2" height="38"/>
      <rect x="401" y="222" width="1" height="38"/><rect x="405" y="222" width="3" height="38"/>
      <rect x="411" y="222" width="2" height="38"/><rect x="416" y="222" width="3" height="38"/>
      <rect x="422" y="222" width="1" height="38"/><rect x="426" y="222" width="2" height="38"/>
      <rect x="431" y="222" width="3" height="38"/><rect x="437" y="222" width="1" height="38"/>
      <rect x="441" y="222" width="2" height="38"/>
    </g>


    <rect x="-200" y="-20" width="160" height="320" fill="url(#sheen)" transform="skewX(-20)">
      <animate attributeName="x" from="-260" to="620" dur="4.5s" repeatCount="indefinite"/>
    </rect>
  </g>
  </svg>
