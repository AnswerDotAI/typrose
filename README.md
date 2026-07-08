# typrose

Typography styles for Tailwind CSS v4. A CSS-native alternative to [@tailwindcss/typography](https://github.com/tailwindlabs/tailwindcss-typography).

## What is this?

The official Tailwind Typography plugin provides beautiful typographic defaults for rendering prose content (like markdown). This package started as a CSS-only port of that plugin, although it's since been further restructured for clarity and correctness.

By using plain CSS instead of a JavaScript plugin, customization becomes simpler and more direct. We've also reduced the default vertical spacing to be more in line with traditional book-style typography, which many find more visually balanced for long-form reading.

## Installation

```bash
npm install typrose
```

## Usage

Import in your main CSS file:

```css
@import "typrose";
```

Then apply the `prose` class to your content just like with the original typography plugin. The same variants (prose-sm, prose-lg, prose-xl, prose-2xl) can be added. The same themes (prose-slate, prose-zinc, prose-neutral, prose-stone) are also available. And dark mode is supported using the `prose-invert` class.

## Custom spacing

One advantage of this CSS-native approach is the ability to control spacing and font size through simple CSS variables, rather than needing to configure a plugin or override utilities.

Reduce or increase all vertical spacing:

```css
.prose-tight { --prose-scale: 0.6; }
.prose-loose { --prose-scale: 1.2; }
```

Scale font size independently from spacing:

```css
.prose-large-text {
  --prose-font-scale: 1.25;
  --prose-scale: 1; /* keep normal spacing */
}
```

## Attribution

Based on [@tailwindcss/typography](https://github.com/tailwindlabs/tailwindcss-typography) by [Tailwind Labs](https://tailwindcss.com).

## License

MIT
