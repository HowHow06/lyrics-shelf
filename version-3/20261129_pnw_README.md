# 2026-11-29 worship service — revision and secondary-file notes

Recorded at Howard's request on 2026-11-27. **Use filename revision v3 for the latest approved decks.** Filename v2/v3 means service revision, not Khen syntax version; all these inputs use Khen version-3 syntax.

## Why there are ten TXT files

| Filename prefix | Purpose | Files |
| --- | --- | --- |
| `20261129_pnw_` (no revision) | Original four-song arrangement; historical snapshot. | onsite + live main |
| `20261129_pnw_v2_` | Six-song revision: added 我的生命献给祢 and 一生敬拜祢; Chinese-main Holy Forever and the second 我要歌颂祢圣名 use English secondary instead of pinyin. | onsite + onsite_secondary + live + live_secondary |
| `20261129_pnw_v3_` | Latest approved: retains six-song v2 and inserts full English versions after the two bilingual songs. Howard wanted both options because the leader's language choice was uncertain. | onsite + onsite_secondary + live + live_secondary |

Earlier revisions are intentional history, not missing updates. Do not overwrite them or mix revisions/variants.

## Latest approved input pairs

- Onsite: [main](20261129_pnw_v3_onsite.txt) + [secondary](20261129_pnw_v3_onsite_secondary.txt).
- Live: [main](20261129_pnw_v3_live.txt) + [secondary](20261129_pnw_v3_live_secondary.txt).

All four were published together in commit `0794ace` (Add 20261129 v3 with full English songs after bilingual versions). **Live secondary was updated too**, including the inserted English blocks; it was not left at v2. Onsite and live have different wrapping/settings; their secondary files are not interchangeable.

## Final v3 song order

| Position | Main lyrics | Secondary strategy |
| --- | --- | --- |
| 1 | 我要歌颂祢圣名 — Chinese | Pinyin |
| 2 | 在祢没有难成的事 — Chinese | Pinyin |
| 3 | 永远圣洁 / Holy Forever — Chinese | English lyrics, not pinyin |
| 4 | Holy Forever — full English | English preset; matching English text retained in aligned secondary input |
| 5 | 我要歌颂祢圣名 — Chinese, second occurrence | English lyrics, not pinyin |
| 6 | I sing praises to Your name — full English | English preset; matching English text retained in aligned secondary input |
| 7 | 我的生命献给祢 — Chinese | Pinyin |
| 8 | 一生敬拜祢 — Chinese | Pinyin |

“After the third and fourth songs” referred to v2 ordering. After insertion, bilingual songs are positions 3 and 5; English alternatives are 4 and 6. Repeated titles are intentional: do not deduplicate them.

## Regeneration and future reuse

Use `--main` with the selected main file and **`--secondary` with its matching secondary file**, not `--auto-pinyin`; auto-pinyin would lose the requested English secondary lyrics. Use the onsite pair with `Default Onsite Chinese`, and live pair with `Default Live Chinese`. Preserve full-English blocks' inline `onsiteEnglishPreset` / `liveEnglishPreset` overrides. Run normal lint, analyze, preview and rendered-PPT QA before publishing regenerated decks.

Main and secondary are coupled artifacts. Preserve matching song order, section markers, lyric-line slots, slide breaks and variant-specific wrapping; check both when revising. Future shelf reuse must retain the selected song's matching secondary block and language intent, not assume every Chinese song uses pinyin. Keep explanatory comments in this Markdown sidecar, not in lyric text that could become slide content.

## Previously delivered approved v3 links

| Variant | PPT | Final preview |
| --- | --- | --- |
| Onsite | [PPT](https://drive.google.com/file/d/1mssUmdttjVnU0kH0t5WeVVz_gvZCAsze/view) | [Preview](https://drive.google.com/file/d/1VqzfFbRdOJGeFjk0v-UVOa3emk-J4kox/view) |
| Live | [PPT](https://drive.google.com/file/d/1moua1n1ypO-EaT_6aiTm6zyyL1gH-ufV/view) | [Preview](https://drive.google.com/file/d/1cDf6Y7YoUQruBcTicIgrVapSNxdYaJ6h/view) |

This documentation-only follow-up does not regenerate or replace the approved lyrics or PPTs.
