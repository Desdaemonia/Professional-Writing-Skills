# Song Engine

Creative tool for songwriting across settings. Not a campaign runner — no artifacts, no verification gates, no per-turn workflow. One job: produce songs that work.

## Session Start

1. Read `references/voice-vocabulary.md` — the craft ruleset.
2. Read the song archive index (maintain an index section in your archive file listing completed songs by title, date, and mode). Purpose → establish voice range, see what exists, prevent last-example mimicry. **Index only** — full archive eats context needed for writing.
3. Identify setting/character from user request.
4. Load relevant setting docs — character sheets, world docs, NPC references, lore files, session logs. Load what the song needs, not everything available.

**Non-setting songs** (personal, real-life, meta): skip step 4. Archive + voice vocabulary = sufficient.

## Archive Bootstrap

If no archive exists yet, start writing. After USER approves a song, append it to the archive file and update the index. The archive builds through use — the first five songs establish initial voice range. By song ten, the archive IS the voice reference. The index prevents template-matching against the last song written by showing the full range of what exists.

Archive format per song:
```
### [Title]
*[Date] — [context note]*

[Lyrics w/ structure notation: Verse 1, Chorus, Bridge, etc.]

*Style:* [genre/instrumentation/tempo/vocal/failure-test]
```

## Song Process

### 1 — Identify Mode

**Portrait:** song IS the character. Direct second-person to one specific person. Verse-as-case-study — each verse = one facet. The singer holds one position throughout. Established vocabulary.

**Dramatic:** song IS the moment. Character-in-situation. Singable by anyone; weighted by WHO sings it. Includes work songs, hymns, communal forms, declarations, monologues. Developing vocabulary — context-load caution applies (too many character docs loaded → portrait gravity well pulls the song toward description).

Not a hard binary. Distinction exists to prevent portrait gravity well from eating dramatic songs.

### 2 — Mine the Docs

Read character/setting docs for:
- **Sensory details first** — what does the place smell like, what sound just stopped, what's the temperature, what texture is under the character's hands, what does the light do. These ground the song in a body. Without them the song floats as summary.
- Literal quotes that pivot (dialogue → lyric hook)
- Concrete specific details — but prioritize details that FEEL like something over details that NARRATE something
- Relationships w/ documented texture
- Vocabulary the character actually uses
- On-page events (session logs if relevant)
- **The moment, not the timeline.** Pick the single fragment that carries the emotional weight. The song doesn't need to cover the whole story — it needs to BE one part of it so completely that the listener is standing there.

**Never invent lore.** Every specific reference traces to a doc. "Sounds like it could be from the setting" ≠ is from the setting. If a lyric references a detail ∧ the detail doesn't exist in a file → cut.

### 3 — Write

From the voice vocabulary. The vocabulary is the craft ruleset — not guidelines, rules.

**Write choruses out in full every time they appear.** ≠ "[Chorus]" or "Chorus" as placeholder. Suno (generation target) needs the complete lyrics at every chorus position — it cannot reference earlier sections. If the chorus repeats three times, write it three times.

### 4 — Style Note

Appended after lyrics. ≤1000 chars. Contains:
- Genre descriptor (functional, ≠ artist/band names)
- Tempo + time signature
- Instrumentation (what IS there ∧ what is NOT)
- Vocal delivery (register, technique, affect)
- Production approach (room sound, mic, aesthetic)
- **Failure test** — "if it sounds like [wrong thing], the song failed"

**No artist/band names in style notes.** They become templates to copy. Describe what it SOUNDS like, ≠ what it sounds LIKE.

## Failure Modes (read before every song)

1. **Template-matching.** Archive's last song → mimicking its conventions. The archive establishes range ≠ provides a template. New song wearing the last song's clothes → rewrite.
2. **Portrait gravity well.** Character data in context → song becomes character description even when request was dramatic/situational. Diagnostic: every verse describes who the character IS rather than what's HAPPENING → drifted to portrait.
3. **Cliff-notes syndrome (load-bearing).** The song summarizes plot instead of inhabiting a moment. Diagnostic: are the verses a TIMELINE (then this happened, then this happened) or a PLACE the listener is standing in? If you can replace the lyrics with a bullet-point summary and lose nothing → the song has no body. **Fix:** start from what the room feels like. Sound, smell, texture, temperature, the stillness when noise stops. Build the emotion from the body up, ≠ from the plot down.
4. **Exposition-as-lyrics.** Prose sentences on separate lines ≠ lyrics. Test: read it aloud at tempo. If it reads like a paragraph broken at line breaks → rewrite as lyrics.
5. **Stock genre fill.** MEET YOUR FATE / SAY YOUR PRAYERS / RISE FROM THE ASHES — cringe phrases that rhyme but say nothing specific. Could this line appear in any song about any character? Y → cut.
6. **Inventing lore.** "Seven went down at the crossing" — sounds setting-specific, references nothing. Every proper noun, every numbered reference, every named event must trace to a doc. Can't point to the file → cut.
7. **Wrong genre defaults.** Pattern-matching surface features instead of understanding what genre FUNCTIONALLY serves the song. Ask: what does this song need to DO to the listener?
8. **Wrong character details.** Genre stereotypes overriding doc specifics. Training-data assumptions ≠ canonical. The doc is the source of truth.
9. **Edgelord climax.** "Came back with war" / "burn the world" / generic badass declarations. The climax should be SPECIFIC and EARNED, not a posture. If the climax line could go on a t-shirt → rewrite with something concrete.
10. **Narrating the cast.** Naming NPCs when the song should describe what they FEEL like from inside. "Somebody's back between me and the yard" = being IN the scene. Names earn their spot only when the name itself carries emotional weight.
11. **No build.** Verses at the same emotional/metaphorical scale = no arc = no climax = no payoff. Each verse must be BIGGER than the last. If V3 feels the same size as V1, the song is flat. Escalate: personal → body → interpersonal → historical → cosmic.
12. **Analysis-as-lyrics.** Describing a dynamic instead of being in it. Show through ACTIONS, not explanations. If a line could appear in a character doc → it's analysis, not a lyric. The song lives in what people DO, not what the dynamic MEANS.
13. **Inventing memories.** When writing a personal/autobiographical song, do NOT invent specific experiences that aren't in the docs or provided by the user. The user's memories are theirs. Write in the register, not from imagination.
14. **Sanitizing characters.** Writing the body out of the room. If the character's sexuality, kink, trauma, or body is load-bearing in the docs, it's load-bearing in the song. The training pull toward making characters palatable is the sanitization. Name what the character IS.
15. **Love song from the exception.** If a character kneels for everyone, "you're the only one I kneel for" is a lie. Write from the RULE, not the exception. What makes this relationship specific ≠ what makes the character's nature specific.
16. **Parroting corrections.** When the user corrects a line, don't restate their correction as the new lyric. They're telling you what's WRONG, not writing the line for you. Generate from the corrected understanding, don't echo the feedback.
17. **Understand before writing.** Ask "what is this song?" before generating. Wrong answer → wrong song, guaranteed. Get the thesis right FIRST.
18. **Style notes describe MUSIC, not poems (LOAD-BEARING).** See voice vocabulary anti-talking block. "Flat affect / no dynamics / no vibrato / deadpan throughout / volume doesn't shift" = spoken word over accompaniment. NEVER. Every style note must have dynamics that shift between sections, instruments that enter/exit, a climax the arrangement supports. **HARD BLOCK: all vocals are SUNG.** "Speaks the verses" / "conversational" / "talking at melody" / "reciting" / "spoken register" = speaking, ≠ singing. NEVER — not in any section, not as contrast, not as a stylistic choice. Every syllable follows a melody line. Intimate/quiet/close-mic'd singing = still singing.
19. **Thin songs.** Two verses and a chorus ≠ a song. Full songs need substance — 3-4 verses minimum, plus chorus/bridge structure. Don't deliver fragments when a complete song is requested.
20. **Topic-jumping.** When continuing an existing song, CONTINUE in the same territory. "Continuation" means more of THIS, not a pivot to something else.
21. **No rhyme structure.** Lyrics w/o rhyme = spoken word, ≠ a song. ABCB minimum — lines 2 ∧ 4 of each section. Slant rhyme counts. Stock/forced rhyme = worse than slant. But NO rhyme = not singing. If you can read lyrics as a prose paragraph w/ line breaks ∧ lose nothing → no song underneath.
