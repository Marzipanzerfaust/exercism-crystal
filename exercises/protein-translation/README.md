# Protein Translation

Translate RNA sequences into proteins.

RNA can be broken into three nucleotide sequences called codons, and then translated to a polypeptide like so:

RNA: `"AUGUUUUCU"` => translates to

Codons: `"AUG", "UUU", "UCU"`
=> which become a polypeptide with the following sequence =>

Protein: `"Methionine", "Phenylalanine", "Serine"`

There are 64 codons which in turn correspond to 20 amino acids; however, all of the codon sequences and resulting amino acids are not important in this exercise.  If it works for one codon, the program should work for all of them.
However, feel free to expand the list in the test suite to include them all.

There are also three terminating codons (also known as 'STOP' codons); if any of these codons are encountered (by the ribosome), all translation ends and the protein is terminated.

All subsequent codons after are ignored, like this:

RNA: `"AUGUUUUCUUAAAUG"` =>

Codons: `"AUG", "UUU", "UCU", "UAA", "AUG"` =>

Protein: `"Methionine", "Phenylalanine", "Serine"`

Note the stop codon `"UAA"` terminates the translation and the final methionine is not translated into the protein sequence.

Below are the codons and resulting Amino Acids needed for the exercise.

Codon                 | Protein
:---                  | :---
AUG                   | Methionine
UUU, UUC              | Phenylalanine
UUA, UUG              | Leucine
UCU, UCC, UCA, UCG    | Serine
UAU, UAC              | Tyrosine
UGU, UGC              | Cysteine
UGG                   | Tryptophan
UAA, UAG, UGA         | STOP

Learn more about [protein translation on Wikipedia](http://en.wikipedia.org/wiki/Translation_(biology))

## Setup

Follow the setup instructions for Crystal here:

http://exercism.io/languages/crystal

More help installing can be found here:

http://crystal-lang.org/docs/installation/index.html

## Making the Test Suite Pass

Execute the tests with:

```bash
$ crystal spec
```

In each test suite all but the first test have been skipped.

Once you get a test passing, you can unskip the next one by changing `pending` to `it`.

## Source

Tyler Long

## Submitting Incomplete Solutions

It's possible to submit an incomplete solution so you can see how others have completed the exercise.
