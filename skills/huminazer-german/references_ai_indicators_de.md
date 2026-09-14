# Quelle: Wikipedia:Künstliche Intelligenz — Anzeichen für KI-generierten Text

(Originaldokument, vom Nutzer bereitgestellt, als Referenz für die Muster im SKILL.md)

## Eindeutige Anzeichen

**Falsche Belege** — LLMs halluzinieren Aussagen und Zusammenhänge. Prüfen: Existiert die Quelle? Enthält sie die behauptete Aussage?

**Formulierungsreste aus dem Dialog mit dem Bot** — Reste des Chatbot-Dialogs im Text.

**Briefartiges Schreiben** — "Betreff:", "Liebe Wikipedia-Editoren", "Ich hoffe, diese Nachricht erreicht Sie wohlauf", "Ich schreibe, um...", Höflichkeitsformeln, die in Wikipedia-Diskussionen unüblich sind.

**Kollaborative Kommunikation** — "Ich hoffe, das hilft", "Natürlich!", "Sicherlich!", "Möchten Sie...", "lassen Sie mich wissen", "detailliertere Aufschlüsselung", "hier ist ein..." — direkte Übersetzungen englischer KI-Phrasen.

**Hinweise auf Wissenslücken** — "Stand [Datum]", "Bis zu meinem letzten Update", "Obwohl spezifische Details begrenzt/rar sind...", "nicht allgemein verfügbar/dokumentiert", "in den bereitgestellten/verfügbaren Quellen...", "basierend auf verfügbaren Informationen".

**Platzhaltertext** — Lückentextvorlagen, bei denen der Nutzer vergessen hat, Platzhalter zu ersetzen.

**Einbindung nicht existierender Vorlagen/Kategorien** — fehlerhafte oder erfundene Wiki-Vorlagen/Kategorien.

## Weichere, uneindeutige Anzeichen

**Sprache und Tonfall** — Übermäßige Betonung von Symbolik/Bedeutung: "spielt eine wichtige/bedeutende Rolle", "unterstreicht seine Bedeutung", "fasziniert weiterhin", "hinterlässt bleibenden Eindruck", "Wendepunkt", "Schlüsselmoment", "tief verwurzelt", "tiefes Erbe", "unerschütterliche Hingabe", "steht als", "festigt".

**Werbesprache** — "reiches kulturelles Erbe", "reiche Geschichte", "atemberaubend", "unbedingt besuchen/sehen", "beeindruckende natürliche Schönheit", "bleibendes Vermächtnis", "reicher kultureller Teppich", "eingebettet", "im Herzen von".

**Redaktionelle Kommentare** — "es ist wichtig zu bemerken/bedenken/beachten", "es ist bemerkenswert", "keine Diskussion wäre vollständig ohne", "dieser Artikel würde nicht ohne existieren".

**Bestimmte Konjunktionen (übermäßig/mechanisch)** — "andererseits", "darüber hinaus", "zusätzlich", "außerdem", "ferner".

**Abschnitts-Zusammenfassungen** — "zusammenfassend", "abschließend", "insgesamt" — in Wikipedia-Artikeln unüblich außer in der Einleitung.

**Fazit-Abschnitte** — typisch für KI, unpassend für Wikipedia (eher passend für medizinische/naturwissenschaftliche Fachaufsätze).

**Schlussfolgerungs-Boilerplate** — "Trotz seiner/dieser Erfolge...", "...steht vor mehreren Herausforderungen...", Vermächtnis/Zukunftsaussichten-Muster.

**Negative Parallelismen** — "nicht nur..., sondern auch...", "es geht nicht nur um..., sondern..." — grammatisch korrekt, aber unpassend argumentativer Ton.

**Trikolon (Dreierregel)** — "sowohl...als auch...und", drei koordinierte Begriffe/Adjektive/Phrasen als rhetorisches Stilmittel.

**Oberflächliche Analysen (Partizip-I-Konstruktionen)** — "...gewährleistend", "...hervorhebend", "...betonend", "...widerspiegelnd".

**Vage Autoritäten (Weasel Wording)** — "Branchenberichte", "Beobachter haben zitiert", "einige Kritiker argumentieren" — Meinungen vagen Autoritäten zugeschrieben, oft basierend auf nur ein oder zwei Quellen.

**Falsche Erweiterung** — "von...bis..." zur Aufzählung von Set-Elementen, erzeugt unenzyklopädischen Ton.

## Typische Formatierungen

- **Übermäßige Fettschrift** — aus FAQs/Foliensätzen/Verkaufsgesprächen übernommen.
- **Listen** — Aufzählungspunkte (•, -, –) statt Wikitext-Formatierung.
- **Emojis** — in deutscher Wikipedia grundsätzlich unüblich.
- **Gedankenstriche (–)** statt Viertelgeviertstrichen (-) — nur zusammen mit weiteren Hinweisen aussagekräftig; LLMs nutzen Gedankenstriche generell häufiger als Menschen.

## Auszeichnungstext

**Markdown statt Wikitext** — Sternchen (*)/Unterstriche (_) statt einfacher Anführungszeichen ('), Rauten (#) statt Gleichheitszeichen (=), runde Klammern statt eckiger für URLs, drei Zeichen (---, ***, ___) statt vier Bindestrichen.

**Fehlerhafter Wikitext** — "Gehe zu Suche Nr." als Linkplatzhalter-Reste; inkorrekt formatierte Referenzen (englische Zitierstile in deutschem Kontext); nicht existierende Kategorien.

## Userbezogene Kriterien

- **Wechsel im Schreibstil** — plötzlich fehlerfreie Grammatik bei einem sonst fehlerhaften Schreiber, Wechsel zwischen Sprachregistern, englisch-typische Konstruktionen.
- **Produktivitätsschub** — auffällig hohe Schlagzahl bei Artikelerstellung/Edits.
- **Text jünger als ChatGPT-Start** (30. November 2022) als Ausschlusskriterium für ältere Texte.
- **Ausführliche Bearbeitungszusammenfassungen** — ungewöhnlich lang, erste Person, gegen deutsche Wikipedia-Konventionen.

---

*Hinweis: Diese Liste stammt aus einer Wikipedia-internen Übersicht zur Erkennung von LLM-generiertem Text. Nicht jedes Merkmal beweist KI-Nutzung — sie sind Indikatoren, keine Beweise. Für den Zweck des huminazer-german-Skills dienen sie als Checkliste dessen, was beim Umschreiben vermieden/entfernt werden soll.*
