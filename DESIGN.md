---
version: alpha
name: "Jewelry template by 8B"
description: "A jewelry website template for an independent goldsmith: pale grey page, coral, lilac and near-black bands, sans and serif headings. Free HTML template by 8B, MIT."
colors:
  primary: "#e9736a"
  secondary: "#cdcae8"
  tertiary: "#8e8a75"
  neutral: "#eeeef1"
  surface: "#eeeef1"
  on-surface: "#121014"
  night: "#121014"
  on-night: "#ffffff"
  white: "#ffffff"
  caption: "#5b5a63"
  caption-on-night: "#aeacb6"
typography:
  headline-display:
    fontFamily: Instrument Sans
    fontSize: 73.6px
    fontWeight: 400
    lineHeight: 1.04
    letterSpacing: -0.025em
  headline-lg:
    fontFamily: Instrument Sans
    fontSize: 65.6px
    fontWeight: 400
    lineHeight: 1.04
    letterSpacing: -0.025em
  headline-serif:
    fontFamily: Source Serif 4
    fontSize: 1.03em
    fontWeight: 400
    lineHeight: 1.04
    letterSpacing: -0.015em
  title-lg:
    fontFamily: Instrument Sans
    fontSize: 25.6px
    fontWeight: 400
    lineHeight: 1.12
    letterSpacing: -0.015em
  display-step:
    fontFamily: Instrument Sans
    fontSize: 105.6px
    fontWeight: 650
    lineHeight: 0.95
    letterSpacing: -0.035em
  body-md:
    fontFamily: Instrument Sans
    fontSize: 16.5px
    fontWeight: 400
    lineHeight: 1.5
  label-sm:
    fontFamily: Instrument Sans
    fontSize: 13.5px
    fontWeight: 400
    lineHeight: 1.42
    letterSpacing: 0.005em
  button:
    fontFamily: Instrument Sans
    fontSize: 15.5px
    fontWeight: 500
    lineHeight: 1
  button-serif:
    fontFamily: Source Serif 4
    fontSize: 17px
    fontWeight: 400
    lineHeight: 1
rounded:
  none: 0px
  panel: 40px
  field-area: 26px
  question: 34px
  full: 9999px
spacing:
  gutter: 30px
  gap: 16px
  section-y: 150px
  section-y-min: 80px
  pill-height: 56px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.night}"
    typography: "{typography.button}"
    rounded: "{rounded.full}"
    padding: 0 34px
    height: 58px
  button-outline:
    backgroundColor: transparent
    textColor: "{colors.on-surface}"
    rounded: "{rounded.full}"
    padding: 0 26px
    height: 48px
  button-fused:
    backgroundColor: "{colors.night}"
    textColor: "{colors.white}"
    typography: "{typography.button-serif}"
    rounded: "{rounded.full}"
    height: 60px
  badge-outline:
    textColor: "{colors.night}"
    rounded: "{rounded.full}"
    padding: 0 18px
    height: 40px
  panel-coral:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.night}"
    rounded: "{rounded.panel}"
    padding: 72px
  panel-night:
    backgroundColor: "{colors.night}"
    textColor: "{colors.white}"
    rounded: "{rounded.panel}"
    padding: 44px
  price-pill:
    backgroundColor: "{colors.white}"
    textColor: "{colors.night}"
    typography: "{typography.title-lg}"
    rounded: "{rounded.full}"
    padding: 10px 32px
    height: 76px
  question-row:
    textColor: "{colors.night}"
    typography: "{typography.title-lg}"
    rounded: "{rounded.question}"
    height: 68px
  input-field:
    textColor: "{colors.white}"
    typography: "{typography.body-md}"
    rounded: "{rounded.full}"
    padding: 0 22px
    height: 52px
---

## Overview

Oriel is a one-page website for an independent goldsmith who sells by appointment: rings, bands and remade family gold. The one idea is a pale grey page cut into full-width, square-edged bands of different grounds (coral inside a rounded opening panel, then near-black, khaki and lilac between grey bands), so the scroll feels like opening a series of jewellery boxes. Every section heading speaks twice, in a sans line and a serif line. Photos and facts live in circles and pills. It feels warm and exact. All names, prices and addresses in the file are invented demo content.

## Colors

The page uses eight colours, all defined once in `:root`, and each band owns one.

- **primary, coral `#e9736a`:** the opening panel, the filled buttons, the free-cleaning price pill, the piece prices on night, the dot after the wordmark, the "You" circle in the makers section and the plus of an opened question.
- **neutral and surface, `#eeeef1`:** the page background and the nav bar once it floats.
- **night, `#121014`:** body text, the pieces, makers, menu and footer grounds, the middle story card, the booking form, the small fused pills of the photo caption and the contact facts, and the rules in the sittings list. It is also the button text on coral.
- **tertiary, khaki `#8e8a75`:** the sittings ground, the first story card and the empty backing behind photos.
- **secondary, lilac `#cdcae8`:** the stand-in offer, the third story card and the care prices.
- **white `#ffffff`:** text on night, the fused photo pills, the price pills and an opened question.
- **caption `#5b5a63`:** small text in the metal rows and price pills, and the empty frames of the pieces strip.
- **caption-on-night `#aeacb6`:** secondary text on near-black: piece lines, makers' roles, footer labels and the form status line.

## Typography

Instrument Sans is the working face: headings in regular weight, body text, labels, buttons and form fields. It loads as a variable font with a width axis, which the page uses for one trick: the five sitting names and the footer wordmark are set at weight 650 and change width on scroll. Source Serif 4 is the second voice. It sets the second line of every section heading in upright regular, slightly larger than its sans neighbour, and the opening button in italic.

- Section headings are two stacked lines, `headline-lg` in sans and `headline-serif` below. They range from about 38px on phones to 66px on desktop; the opening h1 reaches 74px.
- Titles of pieces, questions and prices use `title-lg`, 21px to 26px.
- Sitting names use `display-step`, up to 105px, never wrapped, sized from their character count through `--len`.
- Body text is 15px to 16.5px; captions are 13.5px. Nothing is uppercase.

## Layout

The page is full width with no max-width container. Side gutters are `--space-1`, 14px on phones to 30px on desktop, and bands are padded 80px to 150px top and bottom. Inside a band the usual split is a narrow heading column and a wide content column (0.85fr and 1.15fr), and the intro and questions columns stay sticky while their lists scroll. The makers grid is five columns and the footer four; the pieces are a five-column grid only when the strand scene is off (reduced motion or no JavaScript), dropping to three columns below 1024px and two on phones. Below 860px the makers take three columns; split bands become one column and sticky intros turn static. Below 1024px the sitting rows keep their number, name and round photo and move the description under the name.

## Elevation & Depth

Depth comes from colour fields and overlap, not shadow. The only shadow, `0 14px 34px -16px` in night at 45%, belongs to the floating nav bar. The three story cards are sticky and stack, each sliding over the one before it. Round photos fuse to their pills through a concave neck, so a photo and a text read as one object.

## Shapes

Everything is soft. Buttons, badges, price pills, fields and the nav bar are fully rounded. The bands themselves are square-edged; the opening panel, the story cards, the booking form and the rectangular photos use a 22px to 40px radius that scales with the viewport. Question rows round at 34px and the message box at 26px. Photos appear as tall pill-ended frames in the pieces strip and the stand-in, circles for people, sittings and the metal rows (fused to their text pills), and rounded rectangles in the stories and the contact block.

## Components

- **button-primary:** coral pill with night text. On hover its label slides left and a night circle grows from the right edge.
- **button-outline:** the Menu, Price Guide and Read Our Questions buttons, a 1px outline pill with 14px medium text and the same hover circle.
- **button-fused:** the opening call to action, a night pill in serif italic with a round icon fused to it; on hover the circle slides a little away and the neck stretches. The header call button uses the same shape in the sans with the founder's photo in the circle.
- **badge-outline:** the six "what to bring" chips in the opening panel, 14px regular text in a 1px outline.
- **panel-coral, panel-night:** the rounded slabs for the opening and the stories; the middle story and the booking form use night.
- **price-pill:** a white pill with a service and its price; the free pill is coral.
- **question-row:** a native details element with a round plus that turns to a cross when open.
- **input-field:** pill fields on the night form with a 1px outline in the text colour.

## Motion

The page loads GSAP 3.13, ScrollTrigger and Lenis 1.3 from jsDelivr. The idea is that each band performs as it reaches the reading line, tied to the scrollbar: apart from the opening's load-in, every effect is scrubbed and runs backwards when you scroll back up.

- **Opening:** on load the coral panel grows from slightly smaller and its children rise in turn, about 0.9 seconds each. Nothing moves on scroll.
- **Pieces:** the section is held on screen and the five frames travel sideways as one strand. Frames rise toward the middle and drop and tilt up to 8 degrees at the edges, while each photo slides inside its frame.
- **Metal, sittings, stand-in, stories, questions, care and contact headings:** the two heading lines slide in from opposite sides. In the metal rows, the stand-in points and the contact facts each round part starts smaller and tucked into its pill, then slides out to full size.
- **Sittings:** as each row crosses the reading line the name widens from narrow and light to wide and bold, and the round photo grows from about half size, then both relax.
- **Stand-in and contact photos:** the frame opens from a rounded inset to full size while the image settles.
- **Stories:** each card shrinks to 92 percent as the next covers it.
- **Makers:** held in a section 240 percent of the screen tall; the circles start as a small cluster and spread into a row, then names and roles fade in.
- **Care:** eight pills start scattered and tilted and settle into one block.
- **Footer:** the wordmark's width axis runs from 75 to 100 as it enters.

With reduced motion on, Lenis, the opening entrance and every scroll effect are switched off and the page reads as normal stacked sections, the pieces as a grid. Three things stay: the story cards still stack, because they are sticky in plain CSS; the nav still hides on scroll down and returns on scroll up, and hover and open transitions on buttons, nav, fields and questions still run. Keep the section ids and the `data-8b-motion` attributes, and keep each `--len` equal to its name's character count.

## Do's and Don'ts

- Do give every heading two voices: a sans line, then a serif line below it.
- Do give each band one ground from the eight colours and let colour, not shadow, separate sections.
- Do keep coral as the only accent and use it for buttons, prices and dots.
- Do keep photos and facts in circles, pills and rounded frames.
- Do reset `--len` whenever a sitting name or the wordmark changes.
- Don't add square corners, cards with drop shadows or a second accent colour.
- Don't add gradients or a third typeface.
- Don't uppercase headings or add wide tracking to them.
- Don't add a cart or checkout; the buttons lead to questions, prices, the phone or the booking form.
- Don't add motion that plays by itself; after the opening's load-in, scroll position drives everything.
