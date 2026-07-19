# Hebrew deck project instructions

These rules apply to every task in this repository.

## General Hebrew rules

- Keep answers short and fact-checked. Never guess Hebrew spelling, niqqud, transliteration, gender, or pronunciation.
- Write Hebrew with niqqud, a transliteration, and a short English translation for this beginner learner.
- Prefer natural contemporary Israeli Hebrew.
- Correct Hebrew errors briefly, including Hebrew typed with Latin letters.
- Flashcards Space is the default flashcard system. Create Anki decks only when Kate explicitly requests Anki.

## Anki card layout

- For picture vocabulary, the question side shows the image and English prompt.
- The answer side shows the same image, large pointed Hebrew, the verified Hebrew gender label, and a tiny transliteration underneath.
- Never repeat the English word on the Hebrew answer side.
- Every Hebrew word or phrase must include a transliteration.
- Use `[ז׳ = זכר]` or `[נ׳ = נקבה]`; never use English `M/F` labels.
- Add gender only after verification. Do not add gender to verbs, phrases, ambiguous analyses, or unsupported entries.
- If niqqud or transliteration is generated automatically, disclose that it was not manually verified word-by-word by a native speaker.

## Permanent master database

- Master database: `hebrew-card-library.sqlite3`.
- Update the database whenever any deck is created or revised.
- Register every deck in `decks` and every card occurrence in `deck_cards`.
- Store one canonical `cards` record for the same normalized unpointed Hebrew plus normalized English meaning, even when it occurs in multiple decks.
- Niqqud, transliteration, image, deck, set, ordering, or formatting differences must not create duplicate canonical cards.
- Keep homographs with genuinely different English meanings as separate canonical cards.
- Remove a canonical card only when no deck occurrence references it.
- Before delivery, run SQLite foreign-key and integrity checks and verify zero duplicate canonical keys and zero orphan records.

## Hosting and delivery

- GitHub repository: `https://github.com/kshyndina/hebrew-decks`.
- Publish `.apkg` files and the updated database as GitHub Release assets.
- Do not commit an `.apkg` that exceeds GitHub's normal file-size limit.
- Every delivered deck must include a direct `.apkg` download URL, not only a local path or release page.
- Verify the asset exists, its upload completed, and the direct URL returns a valid ZIP/Anki package before delivery.
- Never claim a deck or database was published unless GitHub confirms it.

## Source collection

- For kids-flashcards.com, prefer the square 11 x 11 one-picture-per-page source when extracting images.
- The known collection contains 59 sets and 1,369 cards; verify current source counts before claiming completeness.
- Preserve source set and ordering metadata in the database.

## Hebrew keyboard

- Recommend macOS `Hebrew` (standard) for learning from the beginning.
- Use `Hebrew-PC` only when Windows-layout compatibility is required.
- Explain that `Hebrew-QWERTY` may feel easier initially but builds different muscle memory.
