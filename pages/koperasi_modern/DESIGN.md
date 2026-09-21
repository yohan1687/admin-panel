---
name: Koperasi Modern
colors:
  surface: '#f6faff'
  surface-dim: '#d3dbe3'
  surface-bright: '#f6faff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#ecf5fd'
  surface-container: '#e7eff7'
  surface-container-high: '#e1e9f1'
  surface-container-highest: '#dbe3ec'
  on-surface: '#151d22'
  on-surface-variant: '#404942'
  inverse-surface: '#293138'
  inverse-on-surface: '#eaf2fa'
  outline: '#707971'
  outline-variant: '#bfc9c0'
  surface-tint: '#226b47'
  primary: '#004328'
  on-primary: '#ffffff'
  primary-container: '#0d5c3a'
  on-primary-container: '#8ad2a7'
  inverse-primary: '#8ed6aa'
  secondary: '#7f5700'
  on-secondary: '#ffffff'
  secondary-container: '#fdba45'
  on-secondary-container: '#6f4b00'
  tertiary: '#233f34'
  on-tertiary: '#ffffff'
  tertiary-container: '#3a564a'
  on-tertiary-container: '#abcabb'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#a9f3c5'
  primary-fixed-dim: '#8ed6aa'
  on-primary-fixed: '#002111'
  on-primary-fixed-variant: '#005232'
  secondary-fixed: '#ffdeae'
  secondary-fixed-dim: '#fdba45'
  on-secondary-fixed: '#281900'
  on-secondary-fixed-variant: '#604100'
  tertiary-fixed: '#caeada'
  tertiary-fixed-dim: '#aecebe'
  on-tertiary-fixed: '#032017'
  on-tertiary-fixed-variant: '#304c41'
  background: '#f6faff'
  on-background: '#151d22'
  surface-variant: '#dbe3ec'
typography:
  display-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 32px
    fontWeight: '800'
    lineHeight: 40px
    letterSpacing: -0.02em
  display-lg-mobile:
    fontFamily: Plus Jakarta Sans
    fontSize: 26px
    fontWeight: '800'
    lineHeight: 34px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 32px
    letterSpacing: -0.015em
  headline-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 20px
    fontWeight: '700'
    lineHeight: 28px
    letterSpacing: -0.01em
  headline-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
  title-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '600'
    lineHeight: 22px
  body-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
  label-numeric-lg:
    fontFamily: JetBrains Mono
    fontSize: 20px
    fontWeight: '600'
    lineHeight: 26px
    letterSpacing: -0.02em
  label-numeric-md:
    fontFamily: JetBrains Mono
    fontSize: 14px
    fontWeight: '500'
    lineHeight: 18px
    letterSpacing: -0.01em
  label-caps:
    fontFamily: Plus Jakarta Sans
    fontSize: 11px
    fontWeight: '700'
    lineHeight: 14px
    letterSpacing: 0.06em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  gutter: 1rem
  gutter-mobile: 0.75rem
  margin: 1rem
  margin-desktop: 2rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 1rem
  space-lg: 1.5rem
  space-xl: 2rem
---

## Brand & Style

This design system embodies community wealth, institutional trust, and grassroots financial empowerment for an Indonesian savings and loan cooperative (*Koperasi Simpan Pinjam*). Drawing from a modern corporate financial aesthetic infused with organic community vitality, it balances formal stability with approachable warmth. 

The visual personality combines:
- **Trust & Security:** Deep, rich greens that evoke growth, solvency, and ethical Islamic/Indonesian communal savings (*gotong royong*).
- **Prestige & Value:** Measured touches of warm gold and amber for yields, dividends (*Sisa Hasil Usaha* / SHU), and milestone achievements.
- **Utilitarian Clarity:** High-legibility typography, unambiguous transaction states, and hyper-legible numerical figures designed to resist ambiguity under direct equatorial sunlight.

The overall style fuses clean modern card architecture with subtle tonal layering and soft borders to establish clear touch ergonomics on mobile devices.

## Colors

The palette establishes an immediate sense of financial health, calm authority, and accessibility.

- **Primary (`#0D5C3A` - Emerald Heritage):** Anchors main actions, app bars, key callouts, and primary active states. Represents stability, ethical stewardship, and financial renewal.
- **Secondary (`#D99B26` - Warm Kencana Gold):** Dedicated to high-value moments: SHU disbursement badges, interest returns, loan progress markers, and alert highlights.
- **Tertiary (`#1E3A2F` - Forest Canopy):** Provides deep, low-luminance backgrounds for high-tier balance cards, headers, and modal surfaces.
- **Neutral (`#1A2228` - Slate Charcoal):** Governs high-contrast text hierarchies, subtle division borders (`#E2E8F0`), and soft slate canvas tones (`#F8FAFC`).

### Functional Colors
- **Deposit/Inflow (Success):** `#0E7444` on `#ECFDF3`
- **Withdrawal/Outflow (Neutral Alert):** `#334155` on `#F1F5F9`
- **Late Payment/Alert (Destructive):** `#B91C1C` on `#FEF2F2`
- **Under Review/Pending:** `#D97706` on `#FFFBEB`

## Typography

Typography pairs **Plus Jakarta Sans**—a typeface originating from Indonesian design culture offering contemporary geometry and friendly legibility—with **JetBrains Mono** for monetary figures, account IDs, and timestamps.

- Indonesian Rupiah figures (`Rp 12.450.000,00`) rely on `label-numeric-*` tokens to guarantee clean vertical tabular alignment across transaction feeds and financial ledgers.
- Headlines leverage strong weights (`700` and `800`) with tight letter spacing for authoritative, modern presence.
- Body text prioritizes comfortable x-heights and open apertures to maintain effortless readability on lower-tier mobile screens.

## Layout & Spacing

The layout is engineered mobile-first around a fluid 4-column structure with an explicit max content width of `480px` for mobile app views, centering cleanly on wider desktop viewports.

- **Vertical Rhythm:** Rooted in an 8px base grid system, with 4px intervals (`space-xs`) reserved for compact data labels and tight metric grouping.
- **Canvas Margins:** Fixed at `1rem` (16px) on mobile viewports, providing edge-to-edge breathing space while maximizing tap area for single-handed thumb operation.
- **Touch Ergonomics:** All actionable elements respect a minimum hit footprint of `48px × 48px`, even when rendered visually smaller using internal component padding.

## Elevation & Depth

Visual hierarchy leverages crisp tonal surfaces with ambient tinted drop-shadows rather than stark black shadows, evoking warm daylight depth.

- **Level 0 (Base Canvas):** `#F8FAFC` Slate background with no shadow.
- **Level 1 (Cards, List Elements):** `#FFFFFF` background bordered by a 1px crisp outline of `#E2E8F0`, paired with an ambient shadow: `box-shadow: 0 1px 3px rgba(13, 92, 58, 0.04), 0 1px 2px rgba(15, 23, 42, 0.06)`.
- **Level 2 (Featured Savings / Hero Balance Card):** `#1E3A2F` or `#0D5C3A` deep fill with `box-shadow: 0 8px 20px -4px rgba(13, 92, 58, 0.25)`.
- **Level 3 (Bottom Navigation & Modals):** `#FFFFFF` with `box-shadow: 0 -4px 16px rgba(15, 23, 42, 0.08)`.
- **Level 4 (Toasts / Floating Action Buttons):** `box-shadow: 0 12px 28px -6px rgba(13, 92, 58, 0.35)`.

## Shapes

The interface embraces a balanced modern radius:
- Standard buttons, input surfaces, and transaction items adopt a `0.5rem` (8px) radius.
- Interactive cards, balance modules, and bottom sheet containers use `1rem` (16px) or `1.5rem` (24px) for prominent visual anchors.
- Badges, status chips, and avatar rings take full `9999px` circular pill treatments to contrast against structured rectangular data tables.

## Components

### Buttons
- **Primary Action:** Solid `#0D5C3A` with high-contrast `#FFFFFF` text. Height `48px`, radius `0.5rem`. Subtle active depression effect (`scale(0.98)`).
- **Secondary / Accent Action:** Solid `#D99B26` with `#1A2228` text for loan drawdowns or SHU claiming.
- **Ghost / Outline:** Transparent background, 1.5px border `#0D5C3A`, text `#0D5C3A`.

### Balance & Metric Cards
- **Simpanan Wajib / Pokok (Savings) Card:** Deep `#1E3A2F` surface, text in `#FFFFFF`, with gold `#D99B26` label chips showing annual interest or SHU distribution. Numbers formatted in tabular monospaced font.
- **Pinjaman (Loan) Card:** `#FFFFFF` surface with emerald-tinted progress bar illustrating installment repayment counts (`e.g., Angsuran 4/12`).

### Transaction Feeds & Badges
- **Transaction Item:** Minimal padding (`space-md`), 1px divider border (`#F1F5F9`). Left: circular 40px icon badge (`#ECFDF3` for savings credit, `#F8FAFC` for repayments). Middle: transaction title and date. Right: JetBrains Mono monetary amount colored green (`+`) or neutral dark (`-`).
- **Status Badges:** Pill-shaped, font `label-caps`. 
  - *Lunas* (Paid): `#ECFDF3` background, `#0E7444` text.
  - *Jatuh Tempo* (Due): `#FEF2F2` background, `#B91C1C` text.
  - *Diproses* (Pending): `#FFFBEB` background, `#B45309` text.

### Input Fields
- **Monetary Inputs:** Currency symbol fixed prefix (`Rp`) in muted slate, trailing numbers set in `label-numeric-lg`.
- **States:** Default border `#CBD5E1`, focus border `#0D5C3A` with a 3px ring of `rgba(13, 92, 58, 0.12)`. Error state uses `#B91C1C`.
- Min height `48px` to guarantee zero-friction touch input on mobile.

### Selection Controls
- **Checkboxes & Radios:** `#0D5C3A` active fill with crisp white internal checks. Target container padded to at least `44px` across row items for agreement to cooperative bylaws (*Anggaran Dasar/Anggaran Rumah Tangga*).