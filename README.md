# Flanders: legislation in git

Part of [lexifina/global-law](https://github.com/lexifina/global-law), one git history for every country's law: this is the law of Flanders, Belgium, which global-law reads at `belgium/flanders/acts/`.

Dutch legislation from the Vlaamse Codex, the Flemish Government's consolidated legal collection. This corpus is incomplete and is not an official publication. The binding publication is the Belgisch Staatsblad.

## Coverage

The acts actually included, their source parts and version dates are recorded in [data/parts.json](data/parts.json) and [data/versions.json](data/versions.json). Those inventories describe the published record. The Codex lists decrees, government and ministerial orders, and other Flemish instruments; an instrument is included here only when it appears in the inventories.

| Record form | Text and dates |
| --- | --- |
| Article history | Article files with the dated source versions available for that act. |
| Current-text baseline, where present | One `text.md` file containing a current consolidated version, labelled oldest version available and credited to the publisher. |

Current-text files retain the source order. Official lists retain their numbering controls and nesting; textual tables retain their row and cell structure; hyperlinks retain their published targets. An external link or publisher notice that a normative annex is unavailable does not stand in for the annex itself: such acts are excluded until the complete annex can be included. Unreconciled judicial changes and uncertain commencement dates are also excluded from current-text additions.

## Source and dates

Source: Vlaamse Codex, Flemish Government, https://codex.vlaanderen.be/, through its official Open Data API at https://codex.opendata.api.vlaanderen.be/.

The Codex retains version history from 1 June 2006. For earlier documents it supplies the surviving consolidated provisions. A current-text baseline uses a source-dated change applicable to that text; a source date takes precedence over the date of retrieval. Missing making or publication metadata remains unknown. Judicial effects require separate reconciliation where the source's structured dates do not reflect them.

Versions with a future commencement belong to the `toekomst` branch. The author of an historical change identifies the act credited by the source; an oldest-version baseline is credited to the publisher. This repository is an unofficial record and the published inventories are not a claim of complete jurisdiction coverage.

## Reuse

Official acts of the authorities are excluded from copyright under Code of Economic Law XI.172 §2. Source: Vlaamse Codex, Flemish Government. Lexifina's own arrangement and contributions are dedicated to the public domain under CC0 1.0, as described in LICENSE.

## Nederlands

Deze verzameling bevat Vlaamse regelgeving uit de Vlaamse Codex. De dekking is nog onvolledig. De opgenomen teksten en versies staan in de gegevensinventarissen. De Vlaamse Codex is geen officiële bekendmaking; de publicatie in het Belgisch Staatsblad is bindend.
