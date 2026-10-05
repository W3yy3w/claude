# Lion's Den Reptile Farm: Landing Page Plan

## Brief (from brainstorming)

| Decision | Choice |
|---|---|
| Venue | Snake and reptile farm, Pahang jungle, Malaysia (location kept vague) |
| Name | Lion's Den. No lions on the page; the name is the only mention |
| Vibe | Dark and thrilling: black, blood red, bold condensed type, hazard tape |
| Photos | Real photos, free Unsplash, hotlinked (swap for the farm's own later) |
| Goal | Sell tickets, English only |
| Sections | Hero, Animals, Tickets (plus warning strip and footer) |
| Prices | Realistic placeholders in RM |
| Deliverable | Single `index.html` |

## Skeleton layout

```
┌──────────────────────────────────────────────┐
│ ▨▨▨▨ HAZARD TAPE (18px, yellow/black) ▨▨▨▨▨▨ │
├──────────────────────────────────────────────┤
│ NAV (over hero)   LION'S DEN        [GET TICKETS] │
│                                              │
│ HERO  (full-bleed king cobra photo,          │
│        dark gradient + red glow at bottom-left) │
│   eyebrow: REPTILE FARM · PAHANG, MALAYSIA   │
│   H1: ENTER THE DEN.   (DEN in blood red)    │
│   lede paragraph                             │
│   [BUY TICKETS]  [MEET THE RESIDENTS]        │
├──────────────────────────────────────────────┤
│ WARNING STRIP (hazard yellow, black text)    │
│ DANGER: VENOMOUS · CLOSED SHOES · BEHIND LINE│
├──────────────────────────────────────────────┤
│ #animals                                     │
│  eyebrow + H2 "Four ways this ends badly…"   │
│  12-column staggered grid (photo cards)      │
│  ┌──────── King Cobra (7) ──┐ ┌─ Python (5) ┐│
│  └──────────────────────────┘ └─────────────┘│
│  ┌─ Water Monitor (5) ┐ ┌─ Saltwater Croc (7)┐│
│  └────────────────────┘ └────────────────────┘│
│  each card: latin name, name, blurb,         │
│             threat badge + max length        │
├──────────────────────────────────────────────┤
│ #tickets  (charcoal band, red/black borders) │
│  eyebrow + H2 "Pick your level of risk"      │
│  ┌ Bystander ┐ ┌ VENOM HOUR ┐ ┌ Keeper/Day ┐ │
│  │ RM35      │ │ RM75       │ │ RM220      │ │
│  │ bullets   │ │ bullets    │ │ bullets    │ │
│  │ [BUY]     │ │ [BUY]      │ │ [BUY]      │ │
│  └───────────┘ └─ red border ┘ └───────────┘ │
│  fine print: hours, last entry, rain policy  │
├──────────────────────────────────────────────┤
│ FOOTER: logo · hours · rules of the den      │
│ legal line (photo credit, fictional venue)   │
├──────────────────────────────────────────────┤
│ ▨▨▨▨ HAZARD TAPE ▨▨▨▨▨▨▨▨▨▨▨▨▨▨▨▨▨▨▨▨▨▨▨▨▨▨ │
└──────────────────────────────────────────────┘
```

Responsive behaviour:
- At 760px and below, the animal cards stack to one column.
- Ticket cards wrap with `auto-fit`, minimum 16rem each.
- The page gutter is at least 1rem at every width.

## Color palette

Single dark theme. The same values are the CSS tokens at the top of `index.html`.

| Token | Hex | Role |
|---|---|---|
| `--ink` | `#0a0808` | Page background, ticket card fill |
| `--coal` | `#151111` | Cards, hero fallback, ticket band |
| `--bone` | `#efe8e0` | Primary text, ghost buttons |
| `--ash` | `#a39a92` | Secondary text, labels, fine print |
| `--blood` | `#c4161c` | Primary accent: CTAs, "Den", threat badges, featured ticket |
| `--hazard` | `#f2b705` | Warning strip, hazard tape, eyebrows, "extreme" threat badge |

Supporting values:
- **Card borders:** `#332a2a`
- **Section dividers:** `#2a2222`

Usage rules:
- Blood red is the single loud colour. It goes on CTAs, the "Den" word and threat badges.
- Hazard yellow marks warnings and small labels only. It is never used as a button fill.
- Text sits on `--ink` or `--coal` for strong contrast. `--ash` is for secondary text only.
- Photos get a dark gradient, plus extra contrast and desaturation (the cards get a little of the saturation back on hover). This keeps them in the palette.

## Typography

| Role | Font | Use |
|---|---|---|
| Display | Big Shoulders Display, 800/900 | Headlines, buttons, prices, tape-style labels. Uppercase |
| Body | Barlow, 400-600 | Paragraphs |
| Utility | IBM Plex Mono, 500 | Eyebrows, Latin names, threat meters, legal line |

## Open items

- Replace the hotlinked Unsplash photos with the farm's own, or confirm each one matches its caption. They couldn't be checked from the build environment.
- Connect the "Buy ticket" buttons to a real booking or payment flow. Right now they only scroll to the ticket section.
- Confirm real prices, hours, animal counts and show details. All are placeholders.
- Optional sections not built: show times, safety FAQ, map and location.
