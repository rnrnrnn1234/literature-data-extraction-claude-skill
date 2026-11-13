# Literature Data Extraction — Claude Skill

문헌고찰을 위한 논문 데이터 추출을 Claude 안에서 바로 수행하는 스킬입니다. 추출 양식을 미리 준비할 필요 없이, 논문 PDF를 올리면 기본 양식으로 추출한 표를 보여주고 연구설계에 맞는 추가 항목을 제안하며, 확정된 표를 엑셀 파일로 받을 수 있습니다.

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Claude Skill](https://img.shields.io/badge/Claude-Skill-orange.svg)
[![DOI](https://zenodo.org/badge/1310891282.svg)](https://doi.org/10.5281/zenodo.24156717)

## 주요 기능

- **양식 준비 불필요** — 저자·국가·연구설계·대상자·표본수·중재·결과변수·주요 결과 등 기본 13개 항목이 내장되어 있어 PDF만 올리면 바로 추출
- **설계별 추가 항목 제안** — 연구설계를 판별하여 실험연구(RCT·준실험)에는 무작위배정·배정 은닉·눈가림·탈락률·효과크기를, 비실험연구(횡단적)에는 표집방법·도구 신뢰도·통계분석 결과를 제안
- **근거 위치 병기** — 모든 추출값 뒤에 원문 위치가 붙어 원문 대조 검증이 바로 가능 (`총 94명 (중재 47/대조 47) (p.3, Fig.1)`)
- **추측 금지 원칙** — 원문에서 확인되지 않은 값은 만들어내지 않고 `NR`(not reported)로 표시하며, 보고되지 않은 항목을 표 아래에 따로 요약
- **반복 조정 가능** — 원하는 항목을 직접 요청하여 열을 추가·삭제할 수 있으며, 이미 추출한 값은 유지되고 변경분만 다시 추출
- **엑셀 저장** — 추출표와 항목정의 시트로 구성된 .xlsx 파일로 저장

## 설치 및 사용 방법

1. `literature-data-extraction.skill` 다운로드
2. Claude.ai → 대화창 "+" 클릭 → 스킬 클릭 → 스킬 관리 클릭 → "추가" 클릭 → "스킬 업로드" 클릭 → 다운로드 받은 스킬 업로드
3. 대화창에 "+" 클릭 후 스킬 선택 → 논문 PDF 업로드 후 Enter
4. Claude가 연구설계를 판별하고 기본 항목을 추출하여 표로 제시
5. 제안된 설계별 추가 항목 중 필요한 항목 선택 (원하는 항목을 직접 요청해도 됨)
6. 표 확정 후 엑셀(.xlsx) 다운로드

## 사용 시 유의사항

- **한 번에 2~3편씩 추출하는 것을 권장합니다.** 논문이 많아지면 추출 정확도가 눈에 띄지 않게 떨어질 수 있습니다. 배치마다 엑셀로 저장하고 새 대화에서 이어가세요.
- **추출값은 원문 대조 검증이 필요합니다.** 특히 표본수·효과크기 등 결과에 직결되는 수치는 표기된 위치에서 확인하세요.
- 체계적 문헌고찰의 표준 절차는 2인 독립 추출 후 검토입니다. 이 도구는 그중 **1차 추출을 보조하는 용도**이며, 논문 방법 기술 시 AI 보조 추출 및 검증 절차를 명시하는 것을 권장합니다.

## 인용

Park S., Woo K. (2026). literature-data-extraction: A Claude skill for data extraction in literature reviews (Version 1.0.1) [Computer software]. ANDA Lab, Seoul National University College of Nursing. https://doi.org/10.5281/zenodo.24156717

## 라이선스

- 소스 코드: [MIT License](LICENSE) © 2026 Soyeon Park

## 제작자

**박소연 (Soyeon Park)** — 서울대학교 간호대학 박사과정

rnsy1029@snu.ac.kr

## 지도교수

**우경미 (Kyungmi Woo)** — 서울대학교 간호대학 부교수

ANDA Lab: https://andalab.snu.ac.kr/

## 감사의 말

이 도구는 AI 도구(Claude, Anthropic)를 활용하여 개발되었습니다. 모든 설계 결정, 요구사항 정의 및 검증은 제작자가 수행했습니다.

---

# Literature Data Extraction — Claude Skill (English)

A Claude skill that performs data extraction for literature reviews directly inside your conversation. No template preparation required — upload paper PDFs, review the extracted table, choose additional items suited to the study design, and download the finalized table as an Excel file.

## Features

- **No template preparation needed** — 13 built-in base items including author, country, study design, participants, sample size, intervention, outcome measures, and key results
- **Design-specific add-on packs** — identifies the study design and suggests randomization, allocation concealment, blinding, attrition, and effect sizes for experimental studies (RCT/quasi-experimental); sampling method, instrument reliability, and statistical results for non-experimental (cross-sectional) studies
- **Source locations inline** — every extracted value carries its location in the original text, enabling immediate verification (`n = 94 (47/47) (p.3, Fig.1)`)
- **No-guessing rule** — values not found in the paper are marked `NR` (not reported) rather than inferred, with unreported items summarized below the table
- **Iterative refinement** — request additional columns at any point; previously extracted values are preserved and only the changes are re-extracted
- **Excel export** — saves as .xlsx with an extraction sheet and an item-definition sheet

## Installation & Usage

1. Download `literature-data-extraction.skill`
2. In Claude.ai, click "+" in the chat box → Manage skills → Add → Upload skill → upload the downloaded file
3. Click "+" in the chat box, select the skill, upload paper PDFs, and press Enter
4. Claude identifies the study design and presents the extracted base items as a table
5. Select the suggested design-specific items you need (or request your own items directly)
6. Confirm the table and download the Excel (.xlsx) file

## Usage Notes

- **Extract 2–3 papers per batch.** Accuracy can degrade without obvious signs when too many papers are processed at once. Save each batch to Excel and continue in a new conversation.
- **All extracted values require verification against the original text**, especially sample sizes and effect sizes.
- The standard procedure for systematic reviews is independent dual extraction followed by reconciliation. This tool assists **first-pass extraction only**; disclose AI-assisted extraction and your verification procedure in your methods section.

## Citation

Park S. (2026). literature-data-extraction: A Claude skill for data extraction in literature reviews (Version 1.0.1) [Computer software]. ANDA Lab, Seoul National University College of Nursing. https://doi.org/10.5281/zenodo.24156717

## License

- Source code: [MIT License](LICENSE) © 2026 Soyeon Park

## Author

**Soyeon Park (박소연)** — Doctoral Student, College of Nursing, Seoul National University

rnsy1029@snu.ac.kr

## Advisor

**Kyungmi Woo (우경미)** — Associate Professor, College of Nursing, Seoul National University

ANDA Lab: https://andalab.snu.ac.kr/

## Acknowledgements

Developed with the assistance of AI tools (Claude, Anthropic). All design decisions, requirements, and validation were performed by the author.
