# PowerPlay Visual Design Brief

Use this document as the design reference for generating PowerPlay screens in Gemini, Stitch, or any layout/design AI.

## Product Identity

PowerPlay is a turn-based cricket card roguelike.

The visual identity is:

**Nostalgic Cricket Arcade + Comic-Book Cricket Cards + Sticker Album Energy**

The player should feel like they are playing a modern, colorful cricket card game with the emotional nostalgia of classic early-2000s cricket games. It should feel joyful, sporty, readable, and collectible.

This is not a gully-noir game. This is not a tactical dossier interface. This is not a dark cyber dashboard. The final direction is bright, cricket-forward, comic-styled, and nostalgic.

## Core Gameplay Constraints

These gameplay facts must be respected in every screen:

- A match has 2 overs total.
- The player bats one 6-ball over and bowls one 6-ball over.
- The active match squad is exactly 12 cards.
- One selected card is consumed per ball.
- Cards have BAT and BOWL stats.
- Cards have roles: Batter, Bowler, All-rounder.
- Cards can have rarity and traits.
- The opponent has visible cards during the match.
- Before locking squad, the player sees a vague opponent scout/archetype, not an exact perfect answer.
- The toss is an actual event: call heads/tails, coin lands, winner chooses bat/bowl.
- Ball outcomes are probability-based.
- Probability should be shown through a normal-curve style outcome graph, not a straight bar.
- Outcomes are W, 0, 1, 2, 4, 6.
- Avoid fake systems that do not exist yet, especially squad synergy.

## Visual Style

### Mood

- Colorful cricket arcade.
- Comic-book cricket heroes.
- Sticker album / trading-card collection.
- Bright cricket pitch.
- Stadium energy.
- Chunky sports UI.
- Playful and nostalgic.
- Modern polish, but not sterile.

### Must Avoid

- Tactical dashboard.
- Military/contact-sheet styling.
- Noir dossier styling.
- Intelligence brief as the main identity.
- Cyberpunk neon UI.
- SaaS admin panels.
- Black/grey empty dashboards.
- Generic dark strategy game layout.
- Fake systems such as synergy, total cost, pitch bonus, league rank, or market tabs unless they are actual mechanics.

## Color Direction

Use bright cricket colors. Do not make the interface black-heavy or neon-green dominant.

### Base Colors

- Grass green: `#39B54A`
- Deep pitch green: `#176B3A`
- Outfield light green: `#7BC96F`
- Scoreboard navy: `#173B63`
- Night stadium blue: `#1C3E70`
- Pitch tan: `#D7B56D`
- Umpire white: `#FFF7E5`

### Action Colors

- Cricket ball red: `#D9342B`
- Boundary yellow: `#FFD23F`
- Sky cyan: `#4FC3F7`
- Fresh lime accent: `#A7F432`

### Role Colors

- Batters: bright blue / cyan frames.
- Bowlers: red / orange frames.
- All-rounders: purple / green hybrid frames.
- Coaches: gold / cream.
- Bench cards: greyscale sticker-paper look, still readable.

### Rarity Colors

- Common: white / silver.
- Uncommon: green.
- Rare: blue.
- Epic: purple.
- Legendary: gold foil.

## Typography Direction

- Use bold, condensed sports lettering for titles.
- Use playful comic/sports lettering for card names.
- Use chunky readable numerals for BAT, BOWL, runs, wickets, ball count, and probability values.
- UI labels should feel like scoreboard strips, stickers, or broadcast graphics.
- Avoid tiny stat text.

## Card Design System

Cards are the soul of the game.

The card style should be a colorful comic cricket trading card:

- Fictional cartoon cricket player.
- Thick black outlines.
- Expressive pose.
- Bright stadium or pitch background.
- Halftone comic shading.
- Speed lines and impact bursts.
- Sticker-like active/bench labels.
- Clear role and rarity badges.
- BAT and BOWL stats visible at a glance.

Do not use real cricketer likenesses, real team kits, real league logos, or recognizable player silhouettes.

### Hero Card

Used for:

- Match duel.
- Shop featured offers.
- Rewards.
- Card inspection.

Hero card traits:

- Larger full-body art.
- Plastic sleeve / sticker album energy.
- Big rarity badge.
- Big BAT/BOWL callouts.
- More expressive pose.

### Compact Card

Used for:

- Squad prep.
- Player hand.
- Opponent row.
- Squad management lanes.

Compact card traits:

- Smaller art crop.
- Role chip.
- Rarity ribbon or compact badge.
- Name.
- BAT stat with bat icon.
- BOWL stat with ball icon.
- Active sticker or bench stamp.
- Still clearly cricket.
- Stats must remain readable.

### Role Art Rules

- Batter cards must show a bat, batting stance, pads, gloves, or shot follow-through.
- Bowler cards must show ball grip, run-up, delivery action, seam trail, or spin motion.
- All-rounder cards must show both bat and ball cues.
- Coach cards should show cap, clipboard, whistle, strategy board, or training equipment.

## Global Layout Rules

- Use screen real estate efficiently.
- Prefer dense, readable sports UI over empty panels.
- No giant blank spaces.
- No vertical scroll in main gameplay screens.
- Horizontal scroll is allowed inside role/category lanes.
- Cards must be readable on a 1280x720 desktop frame.
- Use clear hierarchy: scoreboard, cards, action, outcome.
- Do not create marketing landing pages.
- Do not add navigation tabs unless the game flow needs them.

## Screen Flow

The product flow is:

1. Title / Run Start
2. Opponent Scout + Squad Prep
3. Toss
4. Match
5. Ball Resolution State
6. Shop / Upgrade
7. Squad Management
8. Run Over / Victory

## Screen 1: Title / Run Start

### Purpose

Start the run and establish the game mood.

### Must Include

- PowerPlay logo.
- Start Run button.
- Small stats:
  - Best run.
  - Cups won.
- Cricket stadium / pitch / card pack atmosphere.

### Visual Direction

- Bright cricket arcade title screen.
- Stadium lights.
- Scattered comic cricket cards.
- Sticker album or card pack details.
- Chunky playful Start Run button.

### Avoid

- Long marketing copy.
- App dashboard layout.
- Dark empty menu.

## Screen 2: Opponent Scout + Squad Prep

### Purpose

Let the player choose exactly 12 active cards after seeing useful opponent context.

### Gameplay Requirements

- Player roster starts at 15 cards, but can grow later.
- Player chooses exactly 12 active cards.
- 12 cards are Active.
- Remaining cards are Bench.
- Show role grouping:
  - Batters.
  - Bowlers.
  - All-rounders.
- No vertical scroll.
- Horizontal scroll is allowed inside each role container.
- Eventually each category can have more cards, so each role lane must support horizontal scrolling.

### Layout

1280x720 frame.

Top header, max 64px:

- PowerPlay logo.
- Round number.
- Opponent name.
- `12 Active / 3 Bench` or equivalent active/bench count.
- Auto Select button.
- Lock Squad button.

Main area:

- Left panel, about 20-25 percent width: Match Preview.
- Right area, about 75-80 percent width: three horizontal role lanes.

Role lanes:

- Batters lane.
- Bowlers lane.
- All-rounders lane.
- Each lane has:
  - role heading.
  - count.
  - horizontal scroll affordance if cards overflow.
  - compact cricket cards.

### Match Preview Panel

Should feel like a colorful cricket match preview poster, not an intelligence brief.

Include:

- Rival team name.
- Rival archetype: Bowling Heavy / Batting Heavy / Balanced / All-rounder Heavy.
- 3 compact tendency bars.
- Short scout note.
- Small cartoon rival badge, mascot, or captain icon.

### Card States

- Active cards: colorful, clear active sticker.
- Bench cards: greyscale/desaturated, clear BENCH stamp, still readable.
- Bench cards must not also show an ACTIVE label.

### Avoid

- Empty placeholder cards.
- Bottom navigation.
- Left app navigation.
- Tactical dossier styling.
- Dark contact sheet styling.
- Fake synergy score.
- Total cost.
- Pitch bonus.

## Screen 3: Toss

### Purpose

Create a short, exciting cricket toss moment after squad lock.

### Layout

Top header:

- PowerPlay logo.
- Round.
- Opponent.
- Active/bench count.

Center:

- Large colorful arcade coin/token.
- HEADS button.
- TAILS button.

After result:

- Coin landed result.
- If player wins: BAT FIRST and BOWL FIRST buttons.
- If rival wins: rival decision and START MATCH button.

Side or bottom compact context:

- Rival archetype.
- Your role split.
- Opponent tendency split.

### Visual Direction

- Comic speed lines around the coin.
- Scoreboard result banner.
- Sticker labels.
- Cricket ball red, boundary yellow, sky blue.

### Avoid

- Huge comparison dashboard.
- Long text.
- Management-screen feel.

## Screen 4: Match Screen

### Purpose

Main playable screen where the player chooses one card per ball.

### Must Include

- Compact scoreboard.
- You score/wickets.
- Rival score/wickets.
- Innings state: Batting or Bowling.
- Ball count, e.g. Ball 3/6.
- Target or runs needed.
- Opponent 12 cards visible across top.
- Player 12 cards visible across bottom.
- Center duel arena.
- Probability graph.
- Last 6 balls.
- Confirm action after selection.

### Layout

Top:

- Compact scoreboard strip.

Top side of table:

- Opponent cards, all 12 visible.
- Can be fanned or overlapped.
- Current rival card highlighted.

Center:

- Duel arena.
- Player selected card on one side.
- Current rival card opposite.
- Cricket pitch / comic panel visual.
- Confirm BAT/BOWL button appears after card selection.

Bottom:

- Player active hand, all 12 visible.
- Cards can fan/overlap.
- Hover/focus pops selected card out for readability.

Side or compact panel:

- Normal-curve probability graph.
- Outcomes: W, 0, 1, 2, 4, 6.
- Last 6 balls as cricket-ball chips.

### Visual Direction

- Bright cricket field.
- Comic panel dividers.
- Scoreboard strips.
- Sticker labels.
- Colorful cards.
- Stadium energy.

### Avoid

- Blank center space.
- Duplicate outcome text areas.
- Hidden opponent cards.
- Random-spawn opponent card.
- Dark tactical UI.

## Screen 5: Ball Resolution State

This is a state of the Match Screen, not a separate page.

### Interaction Beat

1. Player confirms selected card.
2. Player card and rival card lock into center.
3. Probability curve moves to center focus.
4. Marker flashes across W, 0, 1, 2, 4, 6.
5. Marker slows near likely outcome neighborhood.
6. Marker lands on final outcome.
7. The probability curve transforms into a giant payoff:
   - W
   - 0
   - 1
   - 2
   - 4
   - 6
8. Cards clear out.
9. Next Ball button appears.

### Visual Direction

- One focal area.
- Comic impact burst.
- Ball impact lines.
- Scoreboard flash.
- Sticker explosion.
- Crowd burst.

### Celebration Rules

Use confetti/burst only for:

- Bowling: Wicket or Dot.
- Batting: Four or Six.

### Avoid

- Tiny outcome text.
- Separate graph and outcome competing for attention.
- Hard cut from graph to text.

## Screen 6: Shop / Upgrade

### Purpose

Let the player improve the run between matches.

### Core Rules

- Player must always own at least 12 cards.
- Selling only applies to surplus bench cards.
- Do not mention deck thinning.
- Do not add fake mechanics.

### Layout

Top header:

- PowerPlay logo.
- Current round.
- Coins.
- Scout Next Rival / Next Opponent button.

Main sections:

1. Player Signings.
2. Coaches.
3. Consumables / Match Boosts.
4. Training.
5. Bench / Sell Surplus.

### Visual Direction

- Arcade cricket clubhouse.
- Cricket card packs.
- Sticker sheets.
- Comic sports shop.
- Scoreboard price tags.
- Ticket-stub labels.
- Colorful offer cards.
- Cartoon coach cards.

### Avoid

- Empty shop panels.
- Black SaaS cards.
- Fake synergy.
- Total cost.
- Market tab layout.
- Tactical marketplace.

## Screen 7: Squad Management / Training

### Purpose

Inspect roster, train cards, and sell surplus bench cards.

### Gameplay Requirements

- Roster can grow beyond 15.
- There are three horizontal scroll containers:
  - Batters.
  - Bowlers.
  - All-rounders.
- No vertical page scroll.
- Each role lane scrolls horizontally.
- Show active and bench cards.
- Player must always keep at least 12 cards.
- Sell is disabled if roster has only 12 cards.
- Training actions:
  - Train BAT.
  - Train BOWL.

### Layout

Top header:

- PowerPlay logo.
- Roster count.
- Active squad count.
- Coins.
- Back / Continue button.

Left compact action panel:

- Train BAT.
- Train BOWL.
- Sell Surplus.
- Current selected action.

Right main area:

- Three horizontal card lanes.
- Each lane has title, count, horizontal scroll affordance.
- Cards use same compact cricket sticker-card style.

### Visual Direction

- Cricket sticker album binder.
- Colorful role rows.
- Arcade clubhouse.
- Bright cricket palette.
- Comic labels.

### Avoid

- Tactical dossier.
- Dark management dashboard.
- Vertical scrolling.

## Screen 8: Run Over / Victory

### Purpose

Clear, satisfying end state after losing or winning.

### Must Include

- Big headline:
  - RUN OVER
  - or CHAMPIONS
- Final score summary:
  - You: runs/wickets.
  - Rival: runs/wickets.
- Match/cup progress.
- Rewards earned if any.
- Buttons:
  - Start New Run.
  - Back to Title.

### Visual Direction

- Colorful cricket scoreboard result.
- Comic-book sports headline.
- Stadium crowd background.
- Cricket ball / bat celebration elements.
- Sticker/trophy graphics.
- Bright nostalgic arcade mood.

### Avoid

- Dark failure modal.
- Tiny score text.
- Generic popup.
- Tactical report styling.

## Recommended Gemini Workflow

Use the Squad Prep reference image as the visual anchor.

Generate screens in this order:

1. Match Screen.
2. Ball Resolution State.
3. Shop / Upgrade.
4. Toss.
5. Squad Management.
6. Run Over / Victory.
7. Title.

For each prompt, tell Gemini:

> Use `design.md` as the design bible. Use the attached Squad Prep image as the visual style reference. Generate only the requested screen. Do not redesign the game identity.

## Short Prompt Template

Use this when asking for a specific screen:

```text
Use design.md as the design bible and use the attached PowerPlay Squad Prep image as the visual style reference.

Generate ONLY the [SCREEN NAME] screen.

Keep the identity: colorful nostalgic cricket arcade + comic-book cricket trading cards + sticker album energy.

Do not use tactical dashboard, noir dossier, cyberpunk neon, SaaS admin panels, fake synergy, total cost, rank systems, or dark empty UI.

Respect all gameplay requirements from design.md.
```
