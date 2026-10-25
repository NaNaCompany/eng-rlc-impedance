# 직렬 RLC 임피던스 계산기

이상 직렬 RLC 회로의 정현파 임피던스 크기 계산

- Plan ID: E083
- App: https://nanalab.kr/eng-rlc-impedance/
- Repository: https://github.com/NaNaCompany/eng-rlc-impedance
- Formula: `|Z| = √(R²+(2πfL−1/(2πfC))²)`
- Output: 임피던스 크기 |Z|

## Model

R≥0, L,C,f>0. 이상 소자의 직렬·정현파 정상상태 모델이다. 출력은 복소수 위상이 아닌 크기 하나다. 기생성분·포화·비선형은 제외한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `30.3822553610568`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
