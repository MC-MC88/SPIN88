<div align="center">

🎡 SPIN88

Une roue qui décide, pour que vous n'ayez plus à le faire.

</div>

---

👋 Welcome

Some decisions don't deserve a pros-and-cons list. Where should we eat tonight. Which movie. Who goes first. What do I actually want to do with my afternoon. You could stand in the kitchen weighing pizza against sushi for another fifteen minutes, or you could spin a wheel and get on with your life.

SPIN88 is that wheel.

It's a single HTML file with a canvas, a textarea, and a button. You write down your options — one per line — and press Update Wheel. The wheel redraws itself, colour by colour, and waits. Then you press SPIN, the wheel turns for five seconds, decelerates, and lands on something. A modal tells you what you got. You nod, or you spin again, or you close the tab.

That's the whole app. No sign-in, no saved wheels, no sharing, no ads asking if you'd like to upgrade to Premium Wheel. Just you, your options, and physics that don't care what you wanted.

The design is quiet and earthy. Olive green, mustard yellow, cream backgrounds — the palette of a kitchen from 1975, or a good notebook cover. Eleven color-coded slices, a chunky SPIN button in the middle, a triangular pointer at the top. A single theme toggle flips the whole thing to a dark version — same wheel, same colors, deeper tones — for use at night or on a dark screen.

And it respects Arabic. RTL text gets the Amiri font and renders correctly on the slices. Because a decision is a decision in any language.

---

<!--
## 📸 Look Inside

<br />

<div align="center">
  <img src="https://github.com/mohamed005cheikh-rgb/spin88/raw/main/images/preview-1.png" alt="The wheel with default options" width="100%" />
  <br />
  <sub><b>① The wheel</b></sub>
</div>

<br />
<br />

<div align="center">
  <img src="https://github.com/mohamed005cheikh-rgb/spin88/raw/main/images/preview-2.png" alt="Editing options in the textarea" width="100%" />
  <br />
  <sub><b>② Editing the options</b></sub>
</div>

<br />
<br />

<div align="center">
  <img src="https://github.com/mohamed005cheikh-rgb/spin88/raw/main/images/preview-3.png" alt="The winner modal" width="100%" />
  <br />
  <sub><b>③ The winner</b></sub>
</div>
-->

---

✨ What you'll find

A wheel you draw yourself.
At the bottom there's a textarea. Every line is an option. Default is a small menu — Pizza, Burger, Sushi, Tacos, Salad, Pasta — so you can try it immediately. Replace those with whatever you're actually deciding between. One per line, no commas, no quotes, no format. Press Update Wheel and the canvas redraws itself, one slice per line, cycling through the olive-and-mustard palette.

Colours that stay in their lane.
The wheel uses six predefined tones — olive green, mustard, muted sage, pale cream, deep forest, warm ochre — and it cycles through them as it draws. Add seven options and the seventh reuses the first color; add twelve and they wrap around again. The result always looks intentional, never random, never a harsh clash.

A five-second spin with easing.
The wheel doesn't jump to its result. It launches at high speed, decelerates smoothly over five seconds on a cubic-bezier curve, and settles. The pointer at the top stays still — it's the wheel underneath that rotates. The final resting position is genuinely random, calculated on the first frame of the spin.

The winner is announced, plainly.
A modal appears with the winning option's text in large bold type, the title "THE WINNER IS" above it in small caps, and a single Awesome! button to dismiss. Nothing else. No confetti, no sound, no invitation to share it on social media. You asked, the wheel answered.

Reads RTL, quietly.
If an option contains Arabic (or any RTL script in the range \u0600-\u06FF), the wheel detects it and renders that slice's text with the Amiri font, right-aligned. Mixed wheels work fine — pizza, burger, كبسة, tacos — the wheel figures out each slice independently.

Truncates long options gracefully.
Long labels get shortened with a ... before they overflow their wedge — fifteen characters for Latin text, twelve for Arabic. The full string is still the answer; only the display is trimmed. If you need to know what the slice actually said, the modal shows it in full.

Two themes.
A single round button in the header flips between light and dark. The light theme is cream and olive — the default. The dark theme keeps the same colors but deepens them, swaps the background to near-black, and inverts the text. Your choice is saved, so next time you open the file it's where you left it.

A three-fold safety net for bad input.
If you save fewer than two options, an alert tells you "Please enter at least 2 options!" and refuses to redraw. If you leave lines blank, they're filtered out. If you put spaces around everything, they're trimmed. The wheel only ever gets real, non-empty options.

Responsive down to a phone.
The wheel scales with the viewport, up to a maximum of 400 pixels. On a small screen it fills most of the width; on a desktop it sits at a comfortable size. The spin button and pointer scale along with it, so nothing looks out of proportion.

---

🧭 How it works

1. Open the file.
One HTML file, no build step, no server. The wheel draws itself immediately with the default options and the theme you chose last time — or the light theme if it's your first visit.

2. Write down your options.
Scroll to the panel at the bottom. Clear the textarea. Type one option per line. As many as you want, as long or short as you want. Then press Update Wheel.

3. Watch the wheel rebuild.
The canvas redraws in a fraction of a second. Each option gets its own wedge, its own color, its own label. The wheel is now waiting for you.

4. Spin it.
Press the round SPIN button in the centre. The wheel accelerates, decelerates, and — five seconds later — stops on a slice. A modal appears with the winner. Press Awesome! to dismiss it, or click anywhere outside the modal to do the same.

5. Spin again, or change the options.
If the answer isn't what you wanted, spin again — randomness is randomness, and the wheel doesn't hold grudges. If the options themselves need to change, edit the textarea and press Update Wheel.

6. Flip the lights if you want.
The round button in the header switches themes. Your choice is remembered next time you open the file.

---

🛠️ A few small helps

"Can I save my wheels?"
No. Nothing is persisted except your theme. When you close the file, the options reset to the defaults next time you open it. If you keep a set of options you like, keep them in a note somewhere — or just open the file in a text editor and edit the default list in the textarea's HTML.

"The wheel didn't land where I expected."
It landed where it landed. The final position is calculated from a genuinely random angle, and the winner is whichever wedge sits under the pointer when the spin stops. There's a small discrepancy possible if you look extremely closely — the physics is designed to feel right, not to be a perfect simulation. That's the intent.

"Can I add more than six options?"
Yes, as many as you can fit. Beyond six, the colors start repeating, and beyond about ten the wedges get thin and the labels get truncated. Twelve is comfortable. Twenty is chaos but functional. If you need thirty options, the wheel is not the tool — a spreadsheet is.

"What does the 'Update Wheel' button actually do?"
It reads the textarea, splits it by newline, trims whitespace, drops empty lines, checks that you still have at least two options, and redraws the canvas. If you haven't changed anything, pressing it again does nothing visible — but it also doesn't break anything.

"Does the spin work on a phone?"
Yes. The SPIN button responds to touch with a slight scale-down for feedback, and the modal closes on tap. There's no special gesture to learn — everything is a button.

"How do I close the winner modal?"
Two ways: press the Awesome! button, or click anywhere outside the modal card (on the dark overlay). Either dismisses it and returns you to the wheel.

"Why is there a 💀 styled ASCII art at the bottom of the page?"
Actually, look again — it's not a skull. It's the letters M C 8 8 spelled out in blocky ASCII characters beneath the email line. It's a small signature, drawn by hand, and it renders in any monospace font. It'll look right in any browser that renders <pre> tags.

"Can I use Arabic options?"
Yes, and they'll render properly with the Amiri font. RTL text gets right-aligned on the slice, and the font is switched automatically. If you mix Arabic and English, each slice chooses its own font.

"Does the theme choice survive a refresh?"
Yes — the theme is stored in localStorage under the key spin88-theme. Your options, however, are not saved. Every session starts with the default menu.

"Can I spin it programmatically or with a keyboard?"
Not as written. There's no keyboard shortcut to trigger the spin. The button is a <button>, so if you're on a keyboard you can tab to it and press Enter, which works in practice — but there's no dedicated key binding.

"The pointer looks off-centre on my screen."
The pointer is positioned with CSS at top: -15px, slightly above the wheel's bounding box, so it sits exactly at the top edge of the drawn wheel. If you've zoomed the page or changed the browser's minimum font size, the wheel may render at a slightly different effective size and the pointer can look misaligned. Reset zoom to 100% and it corrects itself.

"Why does the wheel take five seconds?"
Because a wheel that stops instantly feels fake, and a wheel that takes fifteen seconds feels like a waste of your life. Five seconds is the sweet spot — long enough to feel the drama, short enough that you don't get bored. If you want to change it, look for 5000 in the spinWheel function and adjust both the setTimeout duration and the transition timing in the CSS to match.

"Can I share a custom wheel with someone?"
Not through the app. There's no export button and no URL parameter that loads options. If you want to send someone a wheel, send them the HTML file and tell them which lines to paste into the textarea — or edit the default options in the file itself before sending.

---

<div align="center">

📞 A question, an idea, a bug?

https://img.shields.io/badge/Email-mohamed005cheikh@gmail.com-d14836?style=flat-square&logo=gmail&logoColor=white
https://img.shields.io/badge/WhatsApp-+222_30_73_64_75-25D366?style=flat-square&logo=whatsapp&logoColor=white
https://img.shields.io/badge/GitHub-mohamed005cheikh--rgb-181717?style=flat-square&logo=github

<br />

Let the wheel decide.

<sub>© 2026 Mohamed Cheikh — MC88</sub>

<br />
<br />

</div>
