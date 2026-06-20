# Findings & Decisions: feiman-translation

## Requirements
- Translate Feynman's "The Character of Physical Law" (1965, 2017 MIT Press) to Chinese
- Output as GitHub Pages-compatible Markdown with MathJax 3
- Preserve Feynman's conversational lecture style
- All math in $$...$$ delimiters per kramdown requirements

## Research Findings
- PDF: ClearScan OCR version (185 pages, 7045 lines text, 8.6MB), text extraction successful via pdftotext
- Book 7 Messenger Lectures (1964) + new foreword by Frank Wilczek (2017)
- Wilczek's foreword provides critical scientific updates: QCD, asymptotic freedom, gravitational entropy, Noether's theorem appreciation
- Feynman's style: conversational, witty, philosophical but grounded in specific examples
- Key translation challenges: "imagination in a terrible straitjacket", "QED on steroids", chess analogy for conservation laws

## Technical Decisions
| Decision | Rationale |
|----------|-----------|
| Adapted output format for physics lectures (no code/paper sections) | Book is pure physics exposition, not CS course with code |
| $$...$$ for ALL math | kramdown compatibility requirement |
| 中文 (English) on first term use | Standard academic translation practice in China |
| 8 parallel Paper Agents | One agent per chapter maximizes parallelism |
| Mythos depth=2 per chapter | Sufficient for terminology research without excessive time |

## Quality Observations (Completed Chapters)
| Chapter | Quality | Notes |
|---------|---------|-------|
| ch00 Foreword | Excellent | "terrible straitjacket" → "可怕的紧身衣", "QED on steroids" → "打了兴奋剂的 QED" |
| ch01 Gravitation | Excellent | Bongo drums opening preserved, $$F=Gm_1m_2/r^2$$ formatted correctly |
| ch02 Math & Physics | Complete | Babylonian vs Greek traditions well translated |
| ch03 Conservation | Excellent | Chess analogy (红象) brilliantly rendered, charge conservation clear |
| ch05 Past & Future | Excellent | Irreversibility paradox, ratchet-pawl machine, entropy discussion all solid |
| ch07 Seeking New Laws | Complete | Scientific method, "guessing" translated well |

## Issues Encountered
| Issue | Resolution |
|-------|------------|
| First PDF was scanned images (PdfCompressor) | Re-downloaded ClearScan OCR version |
| pdftotext on scanned PDF returned empty | ClearScan version has embedded text layer |
| CodeAct readFile returned empty object for large text file | Used Bash sed for chapter splitting instead |

## Resources
- Source: The Character of Physical Law, Richard Feynman, MIT Press 2017
- Translation reference: 《物理定律的本性》(台湾译本) terminology conventions
- Math reference: kramdown MathJax pipeline docs
