# GILES - Growing Intertribal Lisp Expression (Symbolic)

(Feel free to substitute other expansions of the acronym.)

**Giles** is an S-expression. Its purpose is to document all aspects
of Lisp culture.

It's appropriate that the programmable programming language (which
brought recursion and reflection into the canon of computing) should
be chronicled in its own syntax.

## Status

Presently Giles is like a newborn baby. The aim is to grow it into the
biggest S-expression in the world. A 20-year-old Giles is expected to
be in the ballpark of 100 gigabytes to a terabyte.

## Structure and release process

Giles is one S-expression.

The top level of Giles is a list of the form:

```Lisp
((2022 . entry)
 (2023 . entry)
 (2024 . entry))
```

A new version of Giles is released annually. Each new version adds
that year's entry to the top level of Giles. Prior years' entries stay
intact, preserving a stable interface for historians.

Pre-release versions of Giles have an extra `unstable` entry:

``` Lisp
((2022 . entry)
 (2023 . entry)
 (2024 . entry)
 (unstable . entry))
```

Upon release, the `unstable` entry is promoted to that year's
release. A new `unstable` entry then starts tracking the next year's
changes. At the beginning of each year, `unstable` picks up exactly
where the last year's entry left off. If no one works on Giles during
a given year, that year's entry will be identical to the previous
year's entry.

## Shared structure

The early years of Giles are likely to be haphazard and full of
experimentation as it struggles to orient itself to its vast
surroundings. Eventually Giles will settle into a stable pattern and
there will be less variation from year to year.

We will leverage _shared structure_ to "copy" unchanged parts of
earlier years' versions of Giles into later years' versions. This will
help reduce the complexity and storage requirements of Giles.

Shared structure can also be used within a given year's version of
Giles to present different views of the same data without duplicate
storage.

## Subsections

A grown up Giles is expected to be more than 100 gigabytes. Few who
take an interest in it will want to download this much data. Most
people will only want to know a part of Giles.

By constitution, Giles involves Lisp culture only. A similar
S-expression encompassing (for example) all of computing would be a
useful object, but is beyond the energies of Giles' volunteer
authors. All or part of Giles could be incorporated into such a
project using shared structure.

## Identity

Lispers know that it's the structure of code and data that makes a
long term difference, not the surface syntax. Consequently, Giles is
defined in terms of the identity of its constituent values. All or
part of Giles can be encoded in any S-expression surface syntax which
can express the data types required for that part.

## Content addressing

Giles is expected to live and grow for many decades. That makes it
unwise to rely on particular storage and transfer methods. Many times
we will download a file from a URL to be incorporated into Giles. But
the URL will surely go out of date, and in all likelihood the network
protocol will too.

The only future-proof way to preserve data one cannot write out is to
use a cryptographic hash of that data. We will use hashes extensively
to refer to parts of Giles that would be cumbersome to write out in
full.

The process of hashing bytevectors is self-evident. It's less clear
how to hash other data types. Work on Giles will necessitate the
development of ways to derive a hashable normal form out of a complex
S-expression.

## User interface

Giles will be shipped in a usable form as one or more Lisp programs
that can retrieve parts of the S-expression (either by downloading
them or by computing them).

Nevertheless, these interfaces will not serve as a definition of
Giles. Giles shall always be considered an immutable value defined by
the identity of its data. Later versions of Giles can be thought of as
persistent data structures that refer to earlier versions as
substructures.
