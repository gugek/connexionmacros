# Connexion Macros

Some macros for OCLC Connexion. Use the mbk file in your Connexion\Macros
directory. The .BAS files are for browsing or for using Copy and Paste
directly into your own local macrobook.

## Install to OCLC Connexion 2.51 or 2.50

To install copy the macrobook (.mbk file) you want to install to the
`C:\Program Files (x86)\OCLC\Connexion\Program\Macros`

Use the Tools > Macros > Manage (CTRL-ALT-SHIFT-G) to copy the macro to the
whatever macrobook you are using. Map the macro to a key or to a user tool
using the Keymaps menu item.

## Macros

### ConvertToRDA

Converts an existing record into a PCC RDA record using the following steps:

  1. Update `040` with `$b eng` and `$e rda`.
  2. Set the `042` to `pcc`
  3. Transform the `260` into a `264`
     * Convert a copyright date to a `264 #4` and bracket `264 #1 $c`
     * Set fixed fields for copyright date if necessary
  4. Convert abbreviations in `300`
     * Update fixed fields for illustrations
  5. Convert abbreviations in `504`
     * Updated fixed fields for bibliographic references and indexes.
     * Remove brackets in pages
  6. Insert `336`, `337`, `338` for textual materials.
     * Appropriate content, media, carrier types for online textual material
     * Other materials get an `{UNABLE_TO_EXTRACT}` stub.
  7. Update fixed fields to reflect:
     * Elvl: blankc
     * Srce: 

#### TODO

* Relator terms for access points.
* Additional content carrier media type identification.

### ConvertToRDACore
Converts an existing record into a Core RDA record using the following steps:

  1. Update `040` with `$b eng` and `$e rda`.
  2. Transform the `260` into a `264`
     * Convert a copyright date to a `264 #4` and bracket `264 #1 $c`
     * Set fixed fields for copyright date if necessary
  3. Convert abbreviations in `300`
     * Update fixed fields for illustrations
  4. Convert abbreviations in `504`
     * Updated fixed fields for bibliographic references and indexes.
     * Remove brackets in pages
  5. Insert `336`, `337`, `338` for textual materials.
     * Appropriate content, media, carrier types for online textual material
     * Other materials get an `{UNABLE_TO_EXTRACT}` stub.
  6. Update fixed fields to reflect:
     * Elvl: 4
     * Srce: d
     * Desc: i

#### TODO

* Relator terms for access points.
* Additional content carrier media type identification.

### Add RDA Encoding
  * Adds 040 $b, $e LDR/18 (Descriptive Cataloging Form) to a Bibliographic
  + Record. 040 $b, $e LDR/18

### Add Database Notes
Add local database notes to a record (NDL specific)

  * 006/007
  * Campus Wide
  * Law School Community
  * Password Access
  * Free Database
  * Database Format
  * Website Format
  * Ebooks
  * EJournals


### Add Cataloging Notes

Add bibliographic record notes from a menu:

  * 504 Includes bibliographical references.
  * 504 Includes bibliographical references (pages <page-span>).
  * 504 Includes bibliographical references and index.
  * 504 Includes bibliographical references (pages <page-span>) and index.
  * 500 Include index.
  * 502 Dissertation (RDA 7.9.1.3)
  * 500 Originally presented as the author's (RDA 7.9.1.3)
  * 588 Title from cover (RDA 2.17.2)
  * 500 Revision of the author's <Title of original work> (Unstructured)
  * 775 $i revision of: $a <Title of original work> 
  * 588 DBO online resource; title from PDF title page (<Provider>, viewed <Today>)'
  * 588 DBO print version record.
