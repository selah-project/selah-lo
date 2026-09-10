# The Selah Lao Rendering — NOTES

*lo.v1 · chair 67 · seated 2026-09-10. The first chair whose script
writes no spaces between words, and the first Kra-Dai chair.*

## The seal

| Count | Value |
|---|---|
| Verses | 23,213 / 23,213 |
| Token spine ≡ en floor | 23,213 / 23,213, zero mismatches |
| ຢາເວ (glosses) | 6,986 — יהוה 6,819/6,819 at the Name seat, 100% |
| ເອໂລຮິມ (glosses) | 2,363 |
| ⟨את⟩ | 11,866 in the token row ≡ 11,866 in the flow ≡ the en floor |
| Erasure (ພຣະຜູ້ເປັນເຈົ້າ / ພະຜູ້ເປັນເຈົ້າ / ເຢໂຮວາ, both ຣ/ລ) | **0** |
| Aleph-tav audit | `[]` |
| ໆ ຯ U+200B, Thai block, Khmer, Latin runs, non-Lao scripts | **0** |

## Cruxes of the chair

- **Scriptio continua.** Lao writes no spaces between words: token
  counts come from the token row and OSHB only, never the flow; no
  `\b` exists for a Lao string anywhere in the tooling; ⟨את⟩ sits
  flush against its neighbours in 10,251 places (spacing posture is
  flag 6, open).
- **The ໆ ruling.** The Lao repeat mark is banned; every reduplication
  is written in full (ຕ່າງໆ → ຕ່າງຕ່າງ) — 190 occurrences over 24
  enumerated units repaired at seating (`dev/scripts/lo_fix_repeat_marks.py`).
- **The Thai hazard, realized backwards.** The feared leak was Thai
  glyphs inside Lao (4 single-codepoint lookalikes found and cured).
  The real event was **Hebrew leaking into Lao by arithmetic**: 94
  token surfaces carried the Hebrew codepoint **+0x8C0**, landing
  inside the Lao block (ນהוה for יהוה at 1 Sam 28:6; ສ́ת for את at
  Judg 3:24). 653 surfaces restored against the en floor
  (lookalikes, plene/defective drift back to the kethib, stray
  spaces, and ~20 slots that held Lao text or a Strong's number —
  Ps 137:1 had five Lao words standing where its Hebrew belongs).
- **Dan 3:12, the fourteenth chair.** יתהון is the Aramaic pronoun
  object, not the marker: bare ພວກເຂົາ, no ⟨את⟩, per every sibling.
- **The Buddhist floor held.** ນະລົກ ນິບພານ ອະນິຈຈັງ ເທວະດາ ພະສົງ:
  zero. ຄວາມວ່າງເປົ່າ never at הבל (הבל → ອາຍ, the vapor image).
  שאול forks perfectly: ເຊໂອນ 53 at the place, ຊາອູນ 397 at the king.
  The leaks that did occur were cured at seating: ວັດ (the wat) at
  בית יהוה (2 Chr 29:17–18 → ວິຫານ), ຂໍ້ກຳມະ (*kamma*) at דברי
  (→ ເລື່ອງລາວ/ຖ້ອຍຄຳ/ສິ່ງ), ແຖນ (the Lao-Tai sky-god) added in
  Jer 50:31's flow (deleted).
- **Register.** Plain register throughout — royal anatomy zero
  (ມືຂອງຢາເວ, not ພຣະຫັດ); ຊົງ dropped at the two divine seats;
  ເດີ້ (attitude particle) → ເຖີດ at נא (Ps 118:25 ×4). "Hello,
  Yahwe" (ຈົ່ງສະຫວັດດີ at ברוך) → ຈົ່ງສັນລະເສີນ; the breastplate
  החשן itself was hiding under a non-word (ສະຫວັດນິລະມາດ → ໂຄເຊນ).
- **Jeshua guarded.** ເຢຊູອາ (Ezra/Nehemiah) and ເຢຊູຣູນ (Jeshurun)
  are lawful; the one bare ເຢຊູ (1 Chr 24:11 — the string that reads
  as *Jesus*) normalized to ເຢຊູອາ per the chair's own convention.
  ພຣະຄຣິດ/ເມຊີອາ NT forms: zero; מָשִׁיחַ → ມາຊີອາ.
- **ໂກເຮນ 767/767** after the one dropped gloss (Ezek 18:14);
  (ປະໂລຫິດ) paren-shadow posture filed (flag: first-use-only vs 33×).

## The burn signature

~34 hours, glm-5.2 lean-prompt lane. Two relay stalls relit; the tail
pressed one-verse-per-call. **Every :json-error was the ceiling, never
the model** — cured by max-tokens 24–32k, twice with temperature 0.55,
twice by glm-5.3 (Lev 6:2, Jer 52:31). Isa 64:1–4 and Num 36:13 burned
in English and were re-rendered. Spine-diff at quiescence: 30
mismatches of 23,213 (0.13% — the cleanest spine on the ladder at that
stage). Tekoa (read-only, 11 lanes): ~486 class-A edits applied at
seating — `dev/scripts/lo_tekoa_class_a.py` and
`data/experiments/lo-seating/` in the Selah repo hold the full trail.

## PENDING SCOTT — class B (never auto-fixed)

Filed in the Tekoa report
(`data/experiments/lo-seating/lo-tekoa-report.md`, lane 14), 11 classes:
flag 4 (ພຣະອົງ, 58 — incl. human referents), flag 6 (⟨את⟩ spacing
10,251 flush / 1,624 spaced), paren-shadow posture (301/203 distinct;
multi-spelled shadows), pointed-vs-unpointed surfaces (~5,800 after the
seating restore), empty glosses 67, ellipsis glosses 396, ຮັບສັ່ງ ×3
homograph, ຂ້າພະເຈົ້າ register, the general precision lane (8/25
sample verses carry one soft garble), Josh 18:7 ການເປັນປະໂລຫິດ,
Job 11:13 כף palm/arm.
