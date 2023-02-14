# Expected Genome Content (EGC) Format Specification

Expected Genome Content (EGC) is a format for expressing rules describing
expectations about the content of genomes. In its current version, it is
dedicated to prokaryotic genomes, although it is possible to use it, and
eventually adapt it, to eukaryotic genomes.

## Structure of the format

The format is very similar in structure to GFA. Ie. it is a multi-record
tabular format (with tabs as separators), where each record is introduced by
a record-type (1 letter-code) in the first field.

Each record has a predetermined number of mandatory positional fields.
The number, format and semantics of these fields depend on the
record type.

After the positional fields, additional information can be given in the form
of tags.

Differently from GFA, each line can also include a comment, i.e. a last
field in the line, introduced by '#'. Everything following this character
and until the end of the line is considered a comment. For clarity sake,
comments cannot contain tabs.

## Implementation of the specification

The specification is given as a set of TextFormats specification files.

## Acknowledgements

This specification has been created in context of the DFG project GO 3192/1-1
“Automated characterization of microbial genomes and metagenomes by collection
and verification of association rules”. The funders had no role in study
design, data collection and analysis.

