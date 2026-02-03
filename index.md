# Lyrics Shelf

This repository stores lyrics for the **Khen PPT Generator** tool, organized by version. Each version introduces new syntax features that enhance how lyrics are formatted and displayed in PowerPoint presentations.

## 📁 Directory Structure

```
lyrics-shelf/
├── legacy-version/    # Original format (basic subsections only)
├── version-1/         # Added song sections
├── version-2/         # Added page breaks and empty slides
└── version-3/         # Added metadata and advanced settings
```

---

## Version Guide

### `legacy-version/` - Original Format

**Features:**

- Basic subsection markers (`---`) for verses, choruses, etc.
- Cover slides with main and secondary titles (`# Title ## Subtitle`)
- Simple lyric formatting without advanced controls

**Example:**

```
--- 1. 我要全心赞美 My Heart Will Praise You, Lord
# 我要全心赞美 ## My Heart Will Praise You, Lord
全心感谢 全心赞美
进入祢的院

--- 2. 我要爱慕祢 I Adore You
# 我要爱慕祢 ## I Adore You
耶稣
我要爱慕祢
```

**Limitations:**

- No separation between different songs in a medley
- No page breaks (`**`) or empty slides (`***`) for transitions
- No metadata support

---

### `version-1/` - Song Sections

**New Features:**

- **Song sections** (`----`) to separate different songs in a medley or mark major divisions

**Example:**

```
---- 1. 在祢没有难成的事 Nothing Is Impossible
# 在祢没有难成的事 ## Nothing Is Impossible
--- Verse
芥菜种的信心
可以将大山挪开

---- 2. 能不能 Let Me Stay
# 能不能 ## Let Me Stay
--- Verse
能不能让我留在祢身边
```

**Why use this version:**

- When you have multiple songs in one presentation
- When you need to organize songs into distinct sections
- When you want automatic section numbering

---

### `version-2/` - Page Breaks and Empty Slides

**New Features:**

- **Page breaks** (`**`) to start a new slide without specific content markers
- **Empty slides** (`***`) for completely blank slides (transitions, pauses, instrumental breaks)

**Example:**

```
---- 主祷文 The Lord's Prayer
# 主祷文 ## The Lord's Prayer
--- [Verse]
我们在天上的父
愿人都尊祢的名为圣
**
我们日用的饮食
今日赐给我们
**
--- [Chorus]
不叫我们遇见试探
救我们脱离凶恶
***

---- 君王就在这里 Worthy Is the King
# 君王就在这里 ## Worthy Is the King
```

**Why use this version:**

- When you need explicit control over slide breaks
- When you want empty/blank slides between songs
- When you need pauses for prayer or instrumental sections
- When lyrics need to be separated across multiple slides

---

### `version-3/` - Metadata and Advanced Settings

**New Features:**

- **Metadata** (`@key: value`) for song information (author, license, etc.)
- **Inline JSON settings overwrites** (`{...}`) for advanced per-section customization

**Example:**

```
---- 主祷文 The Lord's Prayer 赞美之泉
@author:Stream of Praise Music
@license_id:3636851
@license_provider:CCLI
# 主祷文 ## The Lord's Prayer
--- [Verse]
我们在天上的父
愿人都尊祢的名为圣
**
我们日用的饮食
今日赐给我们
```

**Why use this version:**

- When you need to track licensing information
- When you need custom settings per section (font sizes, colors, etc.)
- When you want version-controlled settings embedded with lyrics
- For advanced users who need precise control over formatting

**Note:** Inline JSON settings overwrites are an advanced feature and not yet stable. See the User Guide for details.

---

## 🔍 Which Version Should I Use?

| If you need...                          | Use this version     |
| --------------------------------------- | -------------------- |
| Basic lyrics with verses/choruses       | `legacy-version`     |
| Multiple songs separated into sections  | `version-1` or newer |
| Page breaks or empty slides             | `version-2` or newer |
| Licensing metadata or advanced settings | `version-3`          |

**Recommendation:** Use the **latest version** (`version-3`) for new lyrics, as it supports all features from previous versions while adding metadata and advanced controls.

---

## 📖 Understanding Lyric Syntax

If you're confused about the format when viewing lyrics, here's a quick reference:

| Syntax                | Meaning                                          | Introduced In |
| --------------------- | ------------------------------------------------ | ------------- |
| `# Title ## Subtitle` | Cover slide with main and secondary titles       | All versions  |
| `---`                 | Subsection (Verse, Chorus, Bridge)               | All versions  |
| `----`                | Song section (separate songs or major divisions) | version-1+    |
| `**`                  | Page break (new slide)                           | version-2+    |
| `***`                 | Empty slide (blank/transition)                   | version-2+    |
| `@key: value`         | Metadata (author, license, etc.)                 | version-3+    |
| `{...}`               | Inline JSON settings overwrite                   | version-3+    |

---

## 📚 Full Documentation

For complete details on:

- How to format lyrics
- All syntax options
- Settings and customization
- Troubleshooting tips
- Advanced features

**Please refer to the [PPT Generator User Guide](../khen/docs/PPT_GENERATOR_USER_GUIDE.md)**

---

## 💡 Tips

1. **Backwards compatible:** Lyrics from older versions work in newer versions of the PPT Generator
2. **Preview before generating:** Always use the preview feature to verify formatting
3. **Start simple:** Begin with basic syntax and add advanced features as needed
4. **Copy examples:** Use existing lyrics as templates for your own songs
5. **Metadata is optional:** You can use version-3 without adding metadata if you don't need it

---

Last updated: 2026-02-03
