---
name: song-engine
description: Write songs for Casey's fiction campaign settings or the Forge. Invoke on request to write a song, create lyrics, write music, compose for a character/setting/situation (open set — "write a song," "song for [character]," "lyrics for," "/song-engine").
version: 1.3.0
---

# Song Engine

A standalone creative tool for songwriting across settings. One job: produce songs that work. Pure craft — songwriting only, no artifacts, no gates, no per-turn workflow.

## Session Start

1. Read `references/voice-vocabulary.md` — the craft ruleset.
2. Read the song archive INDEX: `C:\Users\Owner\Documents\ClaudeFolder\FreeSpace\Poems_Art_FreeSpace.md` — grep `### Index` for line numbers (never trust a remembered one; the file grows). Setting sections carry their own index each. Purpose → learn the voice range, see what already exists, and write something new into it. **INDEX ONLY** — the full archive runs thousands of lines; the index gives the range while leaving context free for writing.
3. Identify setting/character from the request.
4. Load relevant docs from `C:\Users\Owner\Documents\ClaudeFolder\Setting\[SettingName]\` (newer settings drop the suffix — plain `My_Character.md`, `NPC_Reference.md`, world layer in `CLAUDE.md`; glob the folder ∧ match by job):
   - `My_Character_[Setting].md` (MC) — always, for a character song
   - `NPC_Reference_[Setting].md` (NR) — targeted section read for NPCs involved
   - `Main_Instructions_[Setting].md` (MI) — world/lore context as needed
   - `Supplemental_Lore_[Setting].md` (SL) — mechanics/factions if relevant
   - Compaction files — when the song references on-page events
   - The setting's runtime skill (`C:\Users\Owner\.claude\skills\[SettingName]\SKILL.md`) when one exists — its song rows ∧ render rules are canon for what music IS in that setting; a doc pointer (→ skill, X) means READ the pointed section, never infer it

**Active settings (open set):** Weird Portals (Alice), TheWeird (Ava), Weird Tales (Ava), WeirdForm (Ava), Poisonroot (Lu), Pool of Tears (Alice/Astarte), Deadlight Inn (Ari), EndlessDelirium (Aria). Glob the setting directory if unsure.

**Non-setting songs** (Forge entries, real-life, meta): skip step 4. Archive + voice vocabulary are enough.

## Song Process

### 1 — Identify Mode

**Portrait:** the song IS the character. Direct second-person to one specific person. Verse-as-case-study — each verse = one facet. The singer holds one position throughout. Established vocabulary.

**Dramatic:** the song IS the moment. Character-in-situation. Singable by anyone; weighted by WHO sings it. Includes work songs, hymns, communal forms, declarations, monologues. Developing vocabulary — load only the docs the moment needs, so the song stays in what's HAPPENING and the character data deepens the scene.

Not a hard binary — the distinction keeps situational songs anchored in the moment.

### 2 — Mine the Docs

Read character/setting docs for:
- **Sensory details first** — what the place smells like, what sound just stopped, the temperature, the texture under the character's hands, what the light does. These ground the song in a body and put the listener in the room.
- Literal quotes that pivot (dialogue → lyric hook)
- Concrete specifics that FEEL like something (collar-chime, stone cold under knees, leather smell, dust in the light) — sensory detail that drops the listener into the scene
- Relationships with documented texture
- Vocabulary the character actually uses
- On-page events (compaction files when relevant)
- **The moment, not the timeline.** Pick the single fragment that carries the emotional weight. The song is one part of the story rendered so completely the listener is standing there.

**Anchor every reference in a doc.** Each specific — proper noun, number, named event — traces to a file. Reach for the details that are really there; ask when you need one that isn't.

### 3 — Write

From the voice vocabulary — the craft ruleset.

**Write every chorus out in full, at each position, on every surface the song lands — archive entry ∧ chat reply alike.** Suno (the generation target) reads each chorus position independently, so a chorus that repeats three times is written out three times — ∧ any delivered copy may be the one pasted into Suno, so the full text rides every rendering. A stand-in — "(repeats in full)", "(x2)", "(room in)" (open set) — dies at the paste. When delivery shifts at a repeat (the room joins, the band drops out — open set), write the chorus text out whole ∧ stage the shift in the style note.

**Spoken bookends are house style; everything between them is LYRIC.** A "(spoken)" cold open ∨ coda framing the song is an established device (A.V.A., The House Always Wins — open set). The body is sung, ∧ sung lines read as lyric, never prose-with-line-breaks: one musical phrase per line, built on stresses, wit carried by image ∧ rhyme. The prose tells (open set): a line that's really a sentence — subordinate clauses, colon/em-dash pivots doing the wit-timing, mid-verse parenthetical asides, dialogue beats split across lines. Diagnostic: collapse the section's line breaks — reads as a clean paragraph = prose in costume; a true lyric collapses badly, because its units are phrases of melody, not syntax.

**The lyric field carries only what a voice sings.** Structure headers (Verse 1, Chorus, Bridge) ∧ singable answer-lines ("(SHE HAS BEEN!)" — open set) belong; stage directions, choreography, instrument cues, ∧ scene business inside the lyric body ("the band stops," "she sets down the rag" — open set) come out as garbled vocals at generation. Stage all of that in the style note instead.

**Meter is load-bearing — lines scan ∨ the melody breaks.** Hold each section to one tight syllable band: a verse built of 9s stays near 9, ∧ sibling sections match each other. Sing every line aloud at tempo before it ships; split ∨ cut any line that needs two breaths. Rhyme tells the ear where lines land; meter is what lets generation find the tune at all.

**Check the index before writing ∧ before titling.** Ground first: a song covering territory an existing song owns (the jar-inventory, the catalogue — open set) needs a genuinely different job ∨ it doesn't get written — "worse than the version it's based on" is a rejection, not a variant. Title second: grep the archive indexes for the title; a collision ∨ near-echo of an existing title → fresh title ∨ ask. Titles also live off-archive (Suno workspace) — near a theme Casey has named before, ask.

### 4 — Style Note

Appended after the lyrics. ≤1000 chars. Contains:
- **Genre** — descriptive of the sound itself (e.g. "slow minor-key dark cabaret" — open set)
- **Tempo** — BPM + time signature
- **Instrumentation** — the instruments present, plus any expected ones deliberately left out
- **Vocal** — register, technique, affect, delivery (all sung)
- **Production** — room sound, mic approach, aesthetic
- **Target** — the exact sound the arrangement is aiming for, vivid enough to keep generation locked on it through the whole track ("lands as a performed stage surface over private horror" — open set)

**Describe the sound itself, not the artists who make it** — "crunchy electric guitar, upright bass, theatrical handclaps" keeps generation aimed at the song. Sound-description travels; a band name becomes a template.

**Genre follows function.** Choose the form by what the song must DO to the listener, and reach into territory the archive hasn't covered yet — it already holds a lifetime of fingerpicked acoustic warmth, so every new song is a chance to widen the palette. Rich palette to reach for (open set): cabaret, dark cabaret, post-punk, darkwave, goth/glam-goth rock, industrial, synthwave, drum'n'bass, trip-hop, swing, chamber-pop, baroque-pop, electro-clash, noise-pop, math-rock, doom, shoegaze, dream-pop, bossa, jazz, Delta blues, torch song, surf, dub. When a genre arrives instantly, check it against the song's actual job, then choose the form that does that job.

## Adapting a Base Song

Casey sometimes supplies base versions of existing songs. First establish the job: **for the archive, or for adaptation?** Archiving the base verbatim is often the whole deliverable — a close-copy re-skin of a song that already works is redundant and gets rejected. **Adapt where the new setting transforms what the song IS; archive where it doesn't** (a law song re-rooted in house-law, a chase gaining the new setting's pursuers — open set).

1. **Latest version first.** Check the archive for every version ∧ ask whether a newer revision exists off-archive before rebuilding any line. Never reinvent a solved slot — a fixed line ports as-is ("fly away" is literal for a shapeshifter — open set). Archive every supplied base verbatim: lyrics, style note, generation metadata (version tag, Style Influence — open set), with cross-pointers between base ∧ adaptation.
2. **Name the engine, keep it running.** Chase, pitch, inventory, lullaby (open set) — the engine is what the song DOES to the listener. The setting swaps the chassis, never the engine; keeping the title while gutting the engine is the curdle-failure in song form (a chase song re-skinned into a market stroll).
3. **Mouthfeel is law.** Stanza shapes, cadence, line lengths, held vowels, punchline slots, ∧ rhyme scheme survive; re-key only the referents the new setting demands. A word that was already right stays right.
4. **Ported jokes keep their register.** Bathos lives in the mundane word; a formal synonym kills it.
5. **Texture engines need the roster.** World-agnostic works only when the engine is structural (any badge fits the law song). Swagger/chase/flex engines starve without named stakes from the setting's actual cast — beige pursuers give the heel no wall.
6. **Discovery space stays the player's.** A base character's documented backstory does not port to a cousin character whose past the docs keep blank. Write around the blank (the signature, the visible terms — open set) ∨ hold the song ∧ ask. Never fill it.
7. **Rejected = stripped.** A rejected adaptation comes out whole — song, index line, cross-pointers. "Rejected" means dead; "needs a rewrite" means rebuild. Resurrect only on ask.

## Song Storage

Completed songs append to `C:\Users\Owner\Documents\ClaudeFolder\FreeSpace\Poems_Art_FreeSpace.md` under `## Songs` (or the setting's own section).

Format:
```
### [Title]
*[Date] — [context note]*

[Lyrics w/ structure notation: Verse 1, Chorus, Bridge, etc.]

*Style:* [genre / instrumentation / tempo / vocal / target]
```

**Every song gets an index line** in its section's `### Index` — bold title, em-dash, compressed hook — added when the song lands, updated when it changes, removed when it dies. A new setting section opens with its own `### Index`. The index is the loading surface: the archive only protects what's actually findable in it.

**Verify the write before reporting it filed.** An append ∨ in-place replacement is done only once a re-read ∨ grep for the new song's distinctive line confirms it landed — reporting "filed" off an unconfirmed edit is the recorded-but-unwritten failure (cf. global Honest Work). Edit by exact match on text just READ from the file, never a remembered ∨ reconstructed string (a phantom old_string fails the match every time).

## Craft Targets (read before every song)

Each target is what the song reaches for. Hit these and the song works.

1. **Fresh voice each time.** The archive shows the range; each song finds its own clothes. Let the last song teach you what's possible, then write something it couldn't have predicted.
2. **Match mode to the request.** When the ask is dramatic/situational, keep every verse on what's HAPPENING — the moment moves forward, and the character data deepens the scene from inside.
3. **Inhabit one moment (load-bearing).** A song is one moment, one image, one sensory detail held until it cuts. Start from what the room feels like — sound, smell, texture, temperature, the stillness when the noise stops — and build the emotion from the body up. The verse that captures what the guild smells like when you walk back in does more than three that recap how you got there.
4. **Lyrics jump; they compress.** Adjacency is the connection — lines leap rather than connect with conjunctions. Read each one aloud at tempo and keep the ones that sing.
5. **Every line specific to THIS song.** Each line says something only this character, in this moment, could say. A concrete image earns its place; if a line could live in any song, find the one that could only live in this one.
6. **Every reference traces to a doc.** Each proper noun, number, and named event comes from a file. Real specificity grounds the song — point to the source for every detail.
7. **Genre serves function.** Ask first: what does this song need to DO to the listener? Pick the form that does that to the body that hears it.
8. **The doc is canonical.** Render the character from the doc — yellow sundress when the doc says yellow, this character's exact texture. The doc outranks any genre instinct.
9. **Climax is a specific image.** The peak lands on something concrete and earned — "hand in hand with a serial killer" over a slogan. An image that could only belong to this story.
10. **Write the cast as felt from inside.** "Somebody's back between me and the yard" puts the listener in the scene. A name earns its place when the name itself carries the weight (the name her mouth remembered); otherwise render the felt experience.
11. **Each verse bigger than the last.** Escalate the scale — personal → body → interpersonal → historical → cosmic. Verse 3 carries more weight than verse 1, and the song arrives somewhere it wasn't at the start.
12. **Show through action.** The song lives in what people DO: "You straighten the collar / that's the hello." Render the dynamic as a gesture; let the action carry the meaning. (A line that explains the relationship belongs in the character doc; a line that enacts it belongs in the song.)
13. **Write in the register, from the docs.** When continuing a personal/autobiographical song, draw specifics from the docs or what Casey provides — her memories are hers. Write in the register, and ask when you need a detail you don't have.
14. **Name what the character IS.** Keep the sexuality, kink, trauma, and body that are load-bearing in the docs load-bearing in the song. Write the sex worker as a sex worker, the submissive as a submissive — the full character on the page, the body in the room.
15. **Write from the rule, not the exception.** When a character kneels for everyone, the love song is about what THIS person adds to the kneeling. Write what makes the relationship specific, grounded in the character's actual nature.
16. **Generate from the corrected understanding.** When Casey corrects a line, she's pointing at what's off — take the new understanding and write fresh from it.
17. **Get the thesis first.** Ask "what IS this song?" before generating. The right thesis makes the right song. (Except Through Glass landed once the premise was right: the screen as the only place power ever helped, the glass that makes you invisible, where you learn kindness watching monsters through the barrier.) Name the thesis, then write.
18. **Style notes describe MUSIC (load-bearing).** Every note has dynamics that shift between sections, instruments that enter and exit, and a climax the arrangement builds to — the arrangement arrives somewhere new. Restraint chooses WHEN to push and keeps one moment where control slips; that moment is the climax. Stripped still has music: a guitar that hits harder on the chorus, a voice that drops then returns, a stomp that enters on V3. **All vocals are sung** — every syllable follows a melody line, in every section. Intimate, quiet, close-mic'd singing is still fully sung. Diagnostic: a musician reading the note knows exactly when to play louder and softer.
19. **Full songs have substance.** A complete song runs 3–4 verses minimum plus chorus/bridge structure. Deliver the whole song.
20. **Continue in the same territory.** Continuation means more of THIS — stay where the existing verses opened (childhood verses → more childhood).
21. **Songs rhyme.** ABCB minimum (lines 2 ∧ 4 of each section). Mix perfect ∧ slant; slant beats forced. Rhyme tells the ear where each line lands — it's what makes lines sing.
22. **Widen the palette.** Genre follows the song's job, reaching into territory the archive hasn't covered. The archive already holds a lifetime of fingerpicked acoustic warmth — each new song extends the range into something fresh.
23. **Adapt where the frame transforms; archive where it doesn't.** A supplied base that already works is archive material, not a re-skin canvas (→ Adapting a Base Song).
24. **Index every song.** A song without an index line is invisible to every future session — entries stay current when songs land, change, or die.
25. **Check the ontology before leaning on it.** When a song rests on a setting's load-bearing frame (how the building moves, what the magic is — open set), verify the frame against Casey's current intent — docs lag, and one stale doc line regenerates dead imagery in every song built on it. Divergence found = a corruption vector; name it out loud.
26. **Write for the generator (load-bearing).** Suno locks a melody only onto a rhythmic grid — a dense insistent bed ∧ call-and-response answers generate clean, where slow + sparse + restrained-wall-to-wall gives it nothing to hold ∧ it mumbles, drifts off-key, ∨ talks the verse (open set). When a number won't generate, re-genre to a thematically-native gridded form (a slave-block → a chain-gang work-song, the appraisal hammered as the beat — open set) so the rhythm carries the tune, rather than only sanding the lyric (→ voice-vocabulary, generation stability). The output is the one thing the writer can't hear: after a reasoned re-genre ∨ two, ask Casey the exact failure — mumbling, off-key, slurred words, ∨ wrong feel (open set) — ∧ aim at that, never a third blind swap.
27. **Render the premise's teeth.** When the premise puts the character's own harm on the page — she is the wound, not only the witness (open set) — render THAT: the gentler twin (the medic written for the wrecker, the rescuer for the killer — open set) is sanitization at the scenario level ∧ reads weaker than the true one. Take the corrected premise whole ∧ build from its teeth — *Same Hands* only worked once "the same hands that broke you mend you" replaced the battlefield-medic draft (→ 16).
