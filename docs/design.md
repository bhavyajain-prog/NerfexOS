# Design Language

## Theme

Blood Moon

## Philosophy

Darkness is the default.
Color is earned.

## Visual Style

- Cinematic
- Minimal
- Atmospheric
- High contrast
- Heavy use of negative space

## Primary Colors

Background : #0F0F10

Surface : #1A1A1D

Foreground : #F2F2F2

Accent : #B31217

Muted : #666666

## Typography

UI Font:
Inter

Terminal Font:
JetBrains Mono Nerd Font

Decorative Font:
Cinzel (used sparingly — lock screen clock, splash/boot text, wordmark. Not
for body or UI text.)

## Animation

Animations should be:

- Smooth
- Slow
- Intentional

Avoid flashy effects.

## UI Rules

- No unnecessary gradients
- No rainbow color schemes
- Thin borders
- Consistent spacing
- Accent color only for interactive elements
- Wallpapers should dominate the desktop

## Spacing

4px base grid. All padding/margin values across every themed surface (Klassy,
Waybar, Rofi, mako, GTK, Qt) should be a multiple of this.

| Token | Value |
| ----- | ----- |
| xs    | 4px   |
| sm    | 8px   |
| md    | 16px  |
| lg    | 24px  |
| xl    | 32px  |
| xxl   | 48px  |

## Border

**1px hairline** everywhere by default (Klassy window borders, Rofi/mako
outlines, GTK/Qt widget borders). No thick or double borders. A 2px width is
reserved exclusively for the focus ring (see Interactive States).

## Corner Radius

Not a single flat value — scaled by surface size so small controls and large
windows don't share an identical radius:

| Token | Value | Used for                                |
| ----- | ----- | --------------------------------------- |
| sm    | 8px   | buttons, chips, tags, small controls    |
| md    | 12px  | cards, notification popups, Rofi window |
| lg    | 16px  | windows, major panels (Klassy)          |

## Interactive States

Applies to any clickable/focusable element (buttons, list items, panel
entries, etc.):

| State            | Treatment                                                               |
| ---------------- | ----------------------------------------------------------------------- |
| Default          | Surface background, Foreground text, Muted border                       |
| Hover            | Surface lightened slightly (no color introduced)                        |
| Focus            | Accent-colored 2px outline/ring — this is a genuine "earned" moment     |
| Active / Pressed | Accent fill or stronger accent border                                   |
| Disabled         | Foreground at reduced opacity (~40%) on Surface, no border color change |

## Semantic States (notifications, alerts, validation)

Rather than introducing new hues that would break the monochrome-plus-crimson
rule, urgency is expressed as _intensity of the same accent_, literalizing
"color is earned":

| Level            | Treatment                                                 |
| ---------------- | --------------------------------------------------------- |
| Info / Success   | Foreground / Muted only — quiet, no color                 |
| Warning          | Accent at reduced opacity (dimmed crimson)                |
| Error / Critical | Full-strength Accent — the only state that earns it fully |

## Inspiration

- Ghost of Tsushima
- Sekiro
- Dark Souls
- Elden Ring
- Japanese minimalism
