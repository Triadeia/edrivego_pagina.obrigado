# e-Drive Go — Design System (site de pagamento dos motoristas)

Extraído de https://pr-reserva-edrive-go-f03e613a.vercel.app (jul/2026).
Este é o visual **oficial do funil de pagamento** — a página de obrigado deve seguir esta identidade.

## Tipografia
- **Display (h1/h2):** `"Archivo Black", Archivo, sans-serif` — peso 700–900, tracking negativo (`letter-spacing: -0.02em`), line-height apertado (~0.98–1.02)
- **Títulos menores (h3):** `Archivo` peso 700
- **Corpo/UI:** `Archivo` (pesos 400/500/600/800/900)
- Google Fonts: `Archivo:wght@400;500;600;700;800;900` + `Archivo Black` (a "Archivo Black" é o Archivo weight 900; pode usar `Archivo 900` como equivalente)

| Elemento | Fonte | Tamanho | Peso | Extra |
|---|---|---|---|---|
| h1 | Archivo Black | 36px | 800–900 | letter-spacing -0.36px, lh 0.98 |
| h2 | Archivo Black | 30px | 800 | lh 1.02 |
| h3 | Archivo | 24px | 700 | — |
| p  | Archivo | 16px | 400 | lh 1.55, cor ink-muted |

## Cores
```
/* Base */
--bg:            #0A0812;   /* rgb(10,8,18) fundo principal (roxo-preto) */
--bg-alt:        #09071 2;  /* #090712 */
--bg-elev:       #110C1E;   /* rgb(17,12,30) superfície elevada */

/* Texto */
--ink:           #F6F4FA;   /* rgb(246,244,250) texto principal */
--ink-muted:     #D5D0E2;   /* rgb(213,208,226) parágrafo */
--ink-dim:       #B9A8D6;   /* rgb(185,168,214) secundário lilás */
--ink-chip:      #DED8EA;   /* rgb(222,216,234) texto de chips */

/* Acento primário (mint) */
--mint:          #2EE6A8;   /* rgb(46,230,168) CTA / destaque */
--mint-light:    #8DFFF0;   /* rgb(141,255,240) gradiente claro */
--mint-2:        #7FF0C8;   /* rgb(127,240,200) */
--on-mint:       #05110C;   /* rgb(5,17,12) texto sobre mint */

/* Marca (roxo) */
--purple:        #4B0081;   /* rgb(75,0,129) */
--lilac:         #C9A8F0;   /* rgb(201,168,240) bordas/realces roxos */

/* Estado */
--error:         #B00020;   /* rgb(176,0,32) */
```

## Fundo da página (assinatura visual)
```css
background:
  radial-gradient(1200px 600px at 80% -10%, rgba(75, 0, 129, 0.55), transparent 60%),
  radial-gradient(900px 500px at 0% 30%, rgba(46, 230, 168, 0.08), transparent 55%),
  #0A0812;
```
Brilhos extras (spots): `radial-gradient(circle at 50% 20%, rgba(46,230,168,0.16), transparent 34%)` + `radial-gradient(circle at 80% 80%, rgba(75,0,129,0.45), transparent 38%)`.

## Botões / CTA
**Primário (pílula):**
```css
background: #2EE6A8;
color: #05110C;
font: 900 16px Archivo;
border-radius: 999px;        /* variante secundária usa 12px */
padding: 0 26px; height ~52px;
box-shadow: 0 16px 44px rgba(46, 230, 168, 0.30);  /* glow mint */
```
Gradiente opcional no CTA: `linear-gradient(90deg, #2EE6A8, #8DFFF0)`.

**Chips / toggles:**
- Inativo: `bg rgba(255,255,255,0.05)`, texto `#DED8EA`, borda `rgba(255,255,255,0.16)`, radius 8–10px, peso 800
- Ativo: `bg rgba(46,230,168,0.14)`, texto `#2EE6A8`, borda `#2EE6A8`

## Cards
- **Padrão (glass):** `bg rgba(10,8,18,0.7)` **ou** `rgba(255,255,255,0.04)`, borda `rgba(255,255,255,0.10–0.12)`, radius **14–16px**
- **Destaque roxo:** `linear-gradient(160deg, rgba(75,0,129,0.22), rgba(20,16,31,0.9))`, borda `rgba(255,255,255,0.10)`, radius **20px**, padding 28px 20px
- **Destaque mint:** `bg rgba(46,230,168,0.07)`, borda `rgba(46,230,168,0.30)`, radius 14px
- **Destaque lilás:** `bg rgba(75,0,129,0.18)`, borda `rgba(201,168,240,0.35)`, radius 14px

## Raios (escala)
`8px` (chips) · `10–12px` (botões/inputs) · `14–16px` (cards) · `20px` (card hero) · `999px` (pílula CTA)

## Tom de voz (copy do site)
Direto, provocativo, foco em dor do motorista de app:
- "Pare de trabalhar para pagar o posto de gasolina."
- "Todo dia você faz uma corrida que não aparece no aplicativo."
- "A Virada Elétrica é a mudança de lógica."
CTAs em 1ª pessoa: "Quero entrar na pré-reserva", "Quero saber se me qualifico", "Reservar minha posição".

## Diferença vs. página de obrigado atual
A página de obrigado usa hoje: verde `#00E676`, fundo `#0C0C0C`, fontes Montserrat/Inter.
Para casar com o funil de pagamento, migrar para: mint `#2EE6A8`, fundo `#0A0812` (roxo-preto) + blobs roxo/mint, fontes **Archivo/Archivo Black**.
