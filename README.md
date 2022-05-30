# Python Image Scraper

## :computer: Commands

- To scrape images using `FastClass`, run
  ```console
  fcd -c BING -s 0 -o raw_images config/fastclass.csv
  ```
- To scrape images using `google-images-download`, run
  ```console
  googleimagesdownload -cf ../config/google_images_download.json
  ```
- To rename image files to zero-padded sequential numbers, run
  ```console
  ls | cat -n | while read n f; do mv "$f" `printf "%03d.extension" $n`; done
  ```

## :bangbang: Things to Note
- Refer to [google-images-download](https://github.com/hardikvasa/google-images-download) and [FastClass](https://github.com/cwerner/fastclass) for documentation of usage.
- Google crawler from `FastClass` won't work.
- If you face issues when using `google-images-download`, see [#360](https://github.com/hardikvasa/google-images-download/issues/360#issuecomment-1048313028) and [#298](https://github.com/hardikvasa/google-images-download/pull/298) to learn how to download the forked version that has the bug fix. It seems like `google-images-download` is not maintained by the current repo owner anymore.
- You can use [TinyPNG](https://tinypng.com) and its [VS Code extension](https://marketplace.visualstudio.com/items?itemName=Pierrick.tinypngminimifyandcrop) to resize and compress your scraped images. Get your API key [here](https://tinypng.com/developers).
- By default, this repo comes with a `devcontainer.json` configuration. If you have Docker installed, you can start the container to get packages and extensions installed at one go.
