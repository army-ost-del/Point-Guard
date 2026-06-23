# Point Guard — Ironside Basketball

A choose-your-own-adventure basketball game. You run the offense as the
point guard for the **Ironside**, facing off against the **Voltage**, in
a game with original team branding and arena atmosphere built entirely
from CSS and SVG — no real team names, logos, or player likenesses are
used anywhere. Every possession, you pick the play — and the game teaches
real basketball IQ through what happens next, not through a lecture up
front.

### The matchup
- **Ironside** (Foundry City) — your team. Orange and charcoal, a
  shield-and-bolt mark, "Hits Hard. Every Possession."
- **Voltage** (Circuit Heights) — the visiting team. Electric blue, a
  bolt-through-circle mark, "Fast. Bright. Electric."

The game opens with a tip-off screen introducing both teams before
handing you the ball, and a simple animated crowd strip behind the
scoreboard cheers (visibly bounces faster) every time either team scores.

## How to install on an Android phone

Same as any installable web app — you need it the URL, then add it
to your home screen from Chrome.

## How the game works

You play 4 quarters, 5 of your possessions each. On your possession, pick
one of:

- **Drive** — attack the rim. Your highest-ceiling shot, but it carries
  real turnover risk if you force it into a crowd.
- **Pass** — swing the ball, make the defense move. Safe, and it improves
  your shot the more the defense has to react — but every pass still has a
  small chance of getting picked off.
- **Post Up** — a steady, reliable look inside. Doesn't swing much based on
  how rushed you are, which makes it a good fallback late in a possession.
- **Shoot** — pull up right now. Fastest option, but usually your
  lowest-percentage shot unless the defense is genuinely caught off guard.
- **Call Timeout** — reset a possession that's going sideways. Costs one of
  your 3 timeouts for the game.

After your possession, the CPU gets a turn automatically — you'll see a
quick result, then it's back to you.

### Where you are on the court
Every decision and every result shows an overhead court diagram — like a
coach's whiteboard — with a glowing marker showing exactly where the ball
is. On result screens, a dashed trail shows where the ball moved during
that action: a drive shows a line from the perimeter to the rim, a pass
shows the ball swinging to a different spot on the perimeter, and a
pull-up shot shows the marker staying put. Red markers are your team,
navy markers are the opponent.

### Watching the action happen
Every result screen also shows a small animated graphic of the actual
motion — a hand releasing the ball along an arc into the hoop for a shot,
the ball sliding between two hands for a pass, or getting knocked loose
for a turnover or steal. It's a quick, looping animation, not a video —
all built from simple shapes, so it loads instantly and works offline.

### Playing defense
When Away has the ball, you're no longer just watching — you pick the
defensive scheme before they make their move:

- **Man-to-Man** — balanced, no real weakness, never the standout either
- **Press** — pressures the ball-handler hard, drawing more turnovers, but
  if they beat it off the dribble the lane is wide open behind you
- **Pack the Paint** — collapses everyone toward the rim, shutting down
  drives almost completely, but leaves outside shooters open
- **Double the Post** — sends a second defender at the post the instant
  they get the ball there, shutting it down, but somebody else on the
  floor is left unguarded

The CPU's tendencies actually shift based on what you pick — a press
sees more drives and more turnovers, packing the paint sees far more
jump shots, doubling the post sees almost no post-ups at all. When a
scheme's real weakness gets exploited, a coach's tip explains exactly
what happened and why, the same way the offense tips do.

### Seeing the whole floor
The court view is now a full-court, angled broadcast-style diagram — both
baskets visible, all 10 players plotted as simple dots, with the
ball-handler highlighted by a gold ring and a small ball icon. Defensive
positioning visibly shifts with the scheme in play — Pack the Paint
visibly clusters defenders near the rim, Press visibly steps a defender
up tight on the ball-handler, and so on.

### Awareness ratings
Two live meters help guide your choices instead of leaving the math
hidden:
- **Offense Awareness**, shown on your decision card, reflects how good
  your current shot-selection situation is — low when you're rushed,
  highest when the defense is scrambling after good ball movement
- **Defense Awareness**, shown next to each scheme on the defensive card,
  reflects how well that scheme fits the situation — for example, a press
  rates better when you badly need the ball back, but worse against a
  team that's currently on fire from outside

### Players you can actually see
Every player on the court now shows a jersey number instead of a plain
dot — a consistent roster (1, 4, 23, 32, 55 for Ironside; 3, 7, 11, 21,
44 for Voltage) so the same person reads as the same person from frame
to frame, not a re-colored circle.

### Sound
The game now has sound effects — synthesized in-browser, no audio files
to load. Makes, three-pointers, misses, turnovers, blocked shots, foul
whistles, the quarter buzzer, timeouts, and catching fire all have their
own distinct cue, including a different feel for a basket scored against
you versus one you make yourself. A speaker icon in the bottom corner of
the scoreboard mutes everything — your preference is remembered next
time you open the app.

### Real player movement
All 10 players now occupy genuine frontcourt positions — corners, wings,
post, dunker spot — and visibly relocate based on what just happened.
Drive or post up and a teammate drifts to the open corner for a kick-out
look; swing a pass and the floor redistributes. Nobody stands around at
midcourt anymore, on either end of the floor.

### Defense posture, named and shown
Every decision card now tells you plainly how Away is currently
guarding you — **pressuring** (tight, daring a blow-by), **set and
balanced** (neutral), or **sagging off** (packed in, conceding the
arc). Your own actions push this around: drive or post up enough and
they collapse inward; one good pass against tight pressure relaxes
them back to neutral. It's not flavor text — it directly changes the
real odds of your next shot.

### 3PT Shot
A new action with its own real tradeoff: lower base percentage than a
two, but worth the extra point — and it specifically punishes a
sagging defense. When Away packs the paint to stop your drives, the
three becomes the correct counter-punch, with odds that jump
accordingly. Pull one up against a tight, alert defense and it's a
genuinely tough shot, same as it should be.

### Smarter meters with real deltas
Offense Awareness and the defensive scheme ratings are now both on a
real 0-5 scale that actually moves possession to possession — built
from an accumulating "good process" score, not a flat 3-state lookup.
Pass the ball and the meter visibly climbs; drive or settle for a
contested shot and it drops back down. The number on screen now means
something concrete: a higher Offense Awareness genuinely correlates
with better odds on whatever you do next.

### Desktop mode
On a wide screen (roughly laptop-width or larger), the court moves into
its own permanent panel on the left — always visible, never scrolling
away with the cards. It's a real broadcast-size view of all 10 players
and the ball, sitting beside the decision/result cards rather than
stacked above them. Mobile is untouched — same single-column layout as
before, court diagram inline above each card.

### Momentum
A small green arrow sits between the two scores in the scoreboard. It
points toward whichever team currently has momentum — left for
Ironside, right for Voltage — and the number of arrows (1 to 3) shows
how strong it is. It moves on real events: makes, threes (a bigger
push), and turnovers either way. No arrows means things are even.
There's no hidden math here to chase — it's just a fast visual read on
who's controlling the run of play right now.

### Coach's Advice
Stuck on a read? Tap "Coach's Advice" on either the offense or defense
screen — it's free, no timeout cost, since this is just your coach
yelling from the sideline like a real coach would. It tells you the
actual best option for the current situation, computed from the same
odds the game itself uses (not a guess), and it's aware of your
assigned role for the game — a Shooter and a Big Man get genuinely
different advice in the exact same situation, because the right answer
for them really is different.

### Player Roles (15U Upgrade)
Each game randomly assigns you one of four roles, shown at tip-off and
reflected with a badge on every decision card:

- **⚡ Slasher** — strong driving, weaker as a shooter from range
- **🎯 Shooter** — dangerous beyond the arc and on pull-ups, a less
  reliable rim threat
- **🧠 Floor General** — every pass builds your read on the defense
  twice as fast, and turnovers are rarer across the board
- **🏗️ Big Man** — dominant in the post, including a real chance to draw
  shooting fouls down low, but no real threat from the perimeter

The role isn't flavor text — it changes the actual odds behind every
action, and Coach's Advice, the strategy guide math, and the post-game
decision report are all aware of it.

### 35-Second Shot Clock (15U Upgrade)
Every possession now has a real, visible shot clock, ticking down from
35 as you make decisions. Passing the ball is still valuable, but it's
no longer free — work the ball too many times without getting a shot up
and you'll run the clock out, which is a turnover (and a real momentum
swing toward Away) just like any other live-ball mistake. The clock
resets to 35 at the start of every new possession.

### Draw Up a Play (15U Upgrade)
Calling a timeout is no longer just a possession reset — after the
huddle, you pick a named play (Iso for your driver, a Pick and Pop
Three, a Post Feed, or a Quick Hitter), and it runs automatically with a
real success boost, since the whole team is on the same page coming out
of a timeout. It still costs the timeout, and the play executes through
the same engine as a normal possession — same court diagram, same sound,
same coach's tip afterward — just with better odds. Drawn-up plays don't
count against your shot-selection grade in the post-game decision
report, since they're a scripted call, not a free read of the defense.

### Coach's Playbook
Not sure if you're actually playing well, or just repeating a favorite
button? Tap "Read the Strategy Guide First" on the tip-off screen before
you start, or "Coach's Playbook" any time mid-game from your offense or
defense screen. It lays out the real logic in plain language — why no
single action or defensive scheme wins by itself, when to switch things
up, and what to do late in a close game. Checking it never costs a
possession or changes anything — it just shows you the guide and drops
you right back where you were.

### Catching fire
Score 3 possessions in a row — by any method (drive, post-up, pull-up
shot, or free throws) — and your team catches fire, NBA-Jam style. While
you're on fire:
- Your shot odds get a real boost across every shot type
- The scoreboard shows your score glowing and your flame meter lit up
- A bold banner announces it on every screen until it fades

Staying on fire means scoring again on your very next possession — miss
or turn it over once and the heat resets to zero. The CPU can catch fire
under the exact same rule, so a hot streak from the other team is a real
threat worth playing around (calling timeout to cool them off is often
the right move here).

### What it's teaching
The lessons show up as "Coach's tips" tied to what just happened, not as
a wall of text up front:
- Why driving into a packed lane is risky, but driving into space is great
- Why a quick shot is fine when the defense is caught off guard, but
  low-percentage against a set defense
- Why getting to the free-throw line is one of the most efficient ways to
  score
- When calling timeout is worth it (stopping an opponent's run, resetting
  a bad possession) — and why you should save at least one for the end
- When fouling on purpose late in a close game actually makes sense, and
  when it doesn't

### Scoring & state
Score, team fouls, and your 3 timeouts are all tracked live in the
scoreboard at the top and persist for the whole game. At the final buzzer,
you'll see the final score and a short recap of the game's biggest plays.
Nothing is saved between sessions — closing or reloading the app starts a
brand new game, the same way turning off a console would.
