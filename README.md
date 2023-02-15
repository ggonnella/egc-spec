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

Differently from GFA, each line can also include a comment, i.e. a last field
in the line, introduced by '#' after the tab. Everything following this
character and until the end of the line is considered a comment. For simplicity,
comments cannot contain tabs.

## Line types

The following line types have been defined.

Groups of organisms:
- 'G': (Group) a group of organisms

Genome contents:
- 'U' (Units) element observed/predicted/computed in the genome sequence and/or
              annotation when measuring an attribute
- 'M' (Model) a model in an external database identifying a unit
- 'A' (Attribute) a quantity which can be measured for a genome

Rules of expectation:
- 'C': (Comparison): a rule of expectation comparing a genome attribute
                      in two group of organisms
- 'V': (Value) a rule of expectation comparing a genome attribute
               to a value or a set of values

Sources of rules:
- 'D' (Document): describe an external textual document
- 'S' (Snippet): reports a snippet of text from a document
- 'T' (Tables): refers to a table in a document

Metadata (these lines do not support tags):
- 'F' (tag deFinitions): describe user-specific tags usage contexts
                              format and semantics
- 'X' (eXternal resources definitions): describe external resources,
    their usage contexts, homepage, citation and item URLs

## Implementation of the specification

The specification is given as a set of TextFormats specification files.
The main specification file is "egc.tf.yaml", in which the "line"
datatype is defined. This represent a single line (i.e. a record) of a EGC file.

## Acknowledgements

This specification has been created in context of the DFG project GO 3192/1-1
“Automated characterization of microbial genomes and metagenomes by collection
and verification of association rules”. The funders had no role in study
design, data collection and analysis.

