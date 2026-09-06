# McGill University LaTeX Templates

Unofficial McGill University versions of the NYU Beamer presentation and academic-poster templates. This project was adapted from [`js8544/nyu-latex-templates`](https://github.com/js8544/nyu-latex-templates); it is not an official McGill University template and is not endorsed by McGill University.

## Origin and licence

- Upstream repository: [`https://github.com/js8544/nyu-latex-templates`](https://github.com/js8544/nyu-latex-templates)
- Upstream purpose: Beamer presentation and poster templates for NYU, NYU Abu Dhabi and NYU Shanghai
- This derivative replaces the NYU names, violet palette and logo assets with a McGill-oriented visual treatment.
- The upstream GPLv3 licence is retained in [`LICENSE.md`](LICENSE.md).
- The poster and presentation also retain the acknowledgements and licence notices inherited by the upstream project.

## Official McGill visual-identity sources

The authoritative standards are maintained by McGill University's Office of Communications and Institutional Relations:

- [McGill Visual Identity portal](https://www.mcgill.ca/visual-identity/)
- [McGill Visual Identity Guide](https://www.mcgill.ca/visual-identity/visual-identity-guide)
- [Official logo and branded-asset access](https://www.mcgill.ca/visual-identity/download-mcgill-logo)

The guide specifies McGill Red as `#ED1B2F`, RGB `(237, 27, 47)`, CMYK `(0, 100, 90, 0)` and Pantone Solid 185. Dark McGill Red (`#9E0918`) is used in this template where a darker tone improves contrast; black, white and neutral grey complete the palette.

The included `mcgill-logo.png` files were prepared from the transparent PNG supplied with this project. Its original `#CF4037` artwork was colour-corrected to `#ED1B2F` while preserving the white details, transparency and anti-aliased edges. The asset now embeds 241 transparent pixels on every side, equal to one half of its detected 481-pixel shield width. This built-in `0.5x` safety zone scales with the logo and must not be cropped, trimmed or overprinted.

## Compliance review

Reviewed against the online McGill Visual Identity Guide on 7 September 2026.

| Requirement | Current status | Notes |
| --- | --- | --- |
| McGill Red | Pass | The active theme and dominant logo red use `#ED1B2F`; dark red uses the guide's `#9E0918`. |
| Core palette | Pass | The layouts primarily use McGill red, black, white and neutral grey. |
| Horizontal, undistorted full logo | Pass visually | The shield and wordmark remain horizontal and retain the supplied artwork's proportions. |
| Minimum logo size | Pass | The poster shield is approximately 1.24 inches wide and the presentation-title shield approximately 0.45 inch wide, both above the 0.25-inch minimum; both wordmarks exceed 1 inch. |
| Correct logo/background pairing | Pass for bundled layouts | The red logo appears only on a white background. Frame-header logos were removed rather than placing a red logo on McGill red. If a logo is later placed on red or dark material, use McGill's official reverse asset. |
| Logo on the front of each document | Pass | The poster and presentation title slide both display the full horizontal logo. |
| Required clear space | Enforced for bundled asset | Each `mcgill-logo.png` includes transparent padding of `0.5x` on all four sides. The LaTeX files do not crop or trim it. Replacing the PNG requires preserving or rebuilding this safety zone. |
| Official logo master artwork | Not verified | The bundled PNG came from a user-supplied file and was colour-corrected. McGill states that the shield, wordmark and logo must not be modified; strict compliance requires replacing it with an official red/reverse asset downloaded through McGill. |
| Official typography | Best available fallback | The templates use Times/Helvetica-compatible LaTeX fonts. McGill explicitly lists Times and Helvetica as macOS substitutes when its official fonts cannot be installed. McGill staff should use licensed official fonts when practical. |
| Trademark permission | Outside template scope | McGill treats its logo and related elements as registered trademarks. Students and other third parties require written approval or an applicable agreement; see the official Visual Identity portal and logo-download page. |

### Compliance conclusion

The bundled layouts now implement the publicly testable requirements for colour, orientation, light-background use, minimum size, front-page presence and `0.5x` clear space. The project nevertheless **cannot be described as fully McGill-compliant or officially approved**, because the supplied/recoloured logo is not verified as an official master file and trademark authorization cannot be established by a LaTeX template. For strict institutional use:

1. Replace both bundled PNG files with official McGill logo artwork from the brand-assets portal; do not recolour or redraw the official files.
2. When replacing the files, preserve the embedded `0.5x` transparent safety zone or implement an equivalent non-cropping LaTeX wrapper.
3. Use an official reverse logo whenever the logo is placed on McGill red or another dark background.
4. Use licensed McGill typefaces when available; otherwise retain the documented Helvetica/Times substitutes.
5. Confirm trademark permission when the template is used by a student, student organization or other third party.

This review is a technical visual check, not authorization or an official McGill brand approval. Questions and special-use requests should be directed to `logo.communications@mcgill.ca`.

## Trademark, permissions and takedown

McGill University names, logos, shields, martlets, wordmarks and related brand elements may be protected trademarks or copyrighted material. This repository does not grant permission to use them. McGill states that students, student organizations and other third parties require written authorization unless an applicable written agreement already permits the use.

The repository owner and every downstream user are responsible for checking authorization before publishing, distributing or presenting branded output. If McGill University or another rights holder identifies an infringement or requests removal, the affected logo assets, generated PDFs, screenshots and public repository content should be removed promptly. A promise to remove material after a complaint does not itself authorize otherwise unauthorized use and is not a substitute for obtaining permission in advance.

## Contents

- `presentation/`: a 16:9 Beamer slide deck using the Madrid theme
- `poster/`: a 48-by-36-inch landscape Beamer poster
- `main.pdf` in each directory: a compiled preview, when generated

## Usage

Edit the corresponding `main.tex` file, then compile from its directory so LaTeX can find the local images and style files.

```sh
cd presentation
latexmk -pdf main.tex
```

For the poster:

```sh
cd poster
latexmk -pdf main.tex
```

Running `pdflatex` twice (and `bibtex` when citations are used) also works.

## Additional acknowledgements

The poster template is based on the [Jacobs Landscape Poster](https://www.overleaf.com/latex/templates/landscape-beamer-poster-template/vjpmsxxdvtqk), and the presentation template is based on the [Unofficial NEO UEA Template](https://www.overleaf.com/latex/templates/unofficial-neo-uea-template/qvhndvzjqmqj).
