# salon-showcase-demo

A test landing page for a nail salon showcase. One page, no build step: open `index.html`, or see it live on GitHub Pages.

It is a demo. The studio name, the numbers, the prices and the pictures are placeholders.

## What is on the page

1. **Hero.** Headline, one Book button, three numbers, and a wall of nail sets that fills the screen and drifts slowly. The sets carry on behind the text, dimmed. Tap any set to open it.
2. **Looks.** The same sets as a grid with style filters.
3. **Prices.** Three services with starting prices.
4. **How to book.** Three steps and the booking button.

There is an EN / 中文 switch at the top and a colour switch in the footer (ink green, mocha, cherry). `index.html?look=3` opens one set directly.

## Built for phones first

Most visitors will arrive on a phone, so that layout gets the attention:

- The wall fills the first screen, with the words over its dimmed upper part and the bright sets below.
- A set opens as a sheet from the bottom of the screen, where the thumb is.
- The style filters sit on one line that scrolls sideways.
- A Book bar appears at the bottom once the first Book button has scrolled away.
- Fewer, bigger pictures on the wall, and lighter effects than on desktop.
- Motion stops for visitors who have reduced motion turned on.

## Changing the content

All content is in the block at the top of the `<script>` in `index.html`, marked `CONTENT`:

- `SITE`: booking link and Instagram handle. While they are empty, the Book button says the page is a demo and the Instagram line is hidden.
- `SERVICES`: the price list.
- `STYLES`: the filter names.
- `LOOKS`: one entry per set (name in both languages, style, service, nail shape).

**Real photos:** put them in a `photos/` folder and add `photo: "photos/cherry-french.jpg"` to the look's entry. The photo then replaces the drawing everywhere. Crop them all to 4:5 (portrait) with similar lighting. Keep each under about 300 KB.

## Design choices

- **Colour:** ink green for the page, aged ivory for text, antique brass for prices. To change the default, edit `:root` at the top of the `<style>`.
- **Faded-film look:** every picture on the wall and in the grid is slightly desaturated and warmed, with fine paper grain over the page. A picture returns to true colour when opened, so the real polish colour is still visible.
- **Type:** Bricolage Grotesque for everything, heavy and condensed for headlines. It loads from Google Fonts; without a connection the page falls back to the system font.
- **Pictures:** until real photos go in, each set is drawn by the page as an SVG.

## Not done

- No real booking: the button is a link, and "Book this look" only notes the chosen set on the page.
- Checked by screenshot at desktop and phone width in Chrome. Not yet tried in Safari or on a range of real phones.
