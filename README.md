# tw-capsize

[Capsize](https://seek-oss.github.io/capsize/) for Tailwind CSS v4. It is implemented using [custom utilities](https://tailwindcss.com/docs/adding-custom-styles#adding-custom-utilities).

## Getting started

1. Install the package:

   ```sh
   npm install -D tw-capsize
   ```

1. Add the following line to your CSS file:

   ```css
   @import "@tw-capsize";
   ```

1. Add font metrics for each font family utility (`font-*`) in your CSS file:

   ```css
   @utility font-sans {
     --cap-height: 740;
     --ascent: 1010;
     --descent: -240;
     --line-gap: 100;
     --units-per-em: 1000;
   }

   /* Repeat for each font family. */
   ```

   To get your font metrics, go to the [Capsize](https://seek-oss.github.io/capsize/), select your font under "1. Choose a font," and select the "JSON" tab. The following metrics are needed:
   - `--cap-height`
   - `--ascent`
   - `--descent`
   - `--line-gap`
   - `--units-per-em`

1. Add the `capsize` class on text elements:

   ```html
   <span class="capsize">...</span>
   ```

   `capsize` will automatically adjust for font size (`text-*`) and line height (`leading-*`) classes. They can be set on the same element as `capsize` or on a parent.

> [!NOTE]
> It's possible not all font size and line height classes are supported. Please feel free to open a pull request with fixes.
