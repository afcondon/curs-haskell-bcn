# curs-haskell-bcn
Ideas i materials cap a montar un curs o taller de Haskell a BCN

### Some initial thoughts

(i'm putting these in English because otherwise i'll take too long to write them and will never get around to it - disculpa'm, sisplau)

## Course as a product

Meaning, think of it carefully in terms of customers and, especially, from the point of view of customers/attendees.

In practice this means:
* a clear offer: 
    * time commitment
    * what you can learn
    * what the prerequisites are
    * what the benefits are
* benefits: (non-exhaustive but possibly mutually exclusive in some cases)
   * learn to do x, y & z
   * learn some aspects of FP in a language that has no "escape valve"
   * stuff your resume
   * learn something that's too hard to learn on your own
* address obvious doubts:
    * "oh, this course will be full of über-mathematical people, i'll be lost"
    * "there's no practical use to this language"
    
## Boot camp approach

At least in part, because this automatically identifies it as not being ivory tower / academic.

Guarantee that attendees will be able afterwards to count on using Haskell as a tool for whatever aspects have been covered in the course. (corollary: no guarantee that they will be able to use it for general purpose programming)

## Strong focus on the tool chain

Teach the installation and use of:

* stack
* atom / vim / emacs / intero / sublime / haskell for mac  (choose)
* interpreting GHC error messages - why they're complicated, how to deal, defuse the fear factor
* REPL, `:t`, incremental development
* tests (quickcheck and/or hspec, see note below on opinionated, tho')

## How before Why

It's a fair bet that people who "get it" (ie understand the "why") are more self-motivated to learn Haskell, but most people are not like that. A lot of people like to try something and then generalize from their experiences with it to judge whether they like it or not, and judge whether it is worth investing more time in it.

## near and far goals

This is a corollary of previous goal: what has to be managed carefully is balancing near and far goals.

Given that some of the greatest strengths of Haskell are in refactoring, working in teams, correctness, working with large codebases it is very hard to show those benefits in small "bootcamp" exercises. So some care needs to be taken to balance "neat tricks" that might get people interested without giving the impression that the language is just a couple of neat tricks.

Here's an example of a "taster" for the benefits of strong typing in a [tweet](https://twitter.com/chris__martin/status/932876020272726021) by Chris Martin

Another example might be the productivity of the Purescript and GHC teams themselves, esp the number of contributors etc

## Dry run to reduce snags

Given that the language introduces lots of strange concepts for ordinary C-family programmers it's probably a really good idea to beta test the materials with a critical eye, ideally volunteers who are not familiar with Haskell but who have good will towards testing the course materials.

What needs testing:

* installation and getting up and running, no steps skipped over
* exercises / examples, should all be available on GitHub, working on all platforms etc
* missing comments
* ambiguity on slides etc (emphasis should be on live coding, however, not powerpoint, but if there are slides they should be right)

## Domains - consider using Gabriel Gonzalez list?

In picking examples to show, we could consider showing the greatest strengths of the language based on Gabriel Gonzalez [State of the Union](https://github.com/Gabriel439/post-rfc/blob/master/sotu.md):

    Best in class
      use Haskell instead of shell (turtle)
      maintenance - _see note about near and far goals_
      single machine concurrency

    Mature:
      DSL
      Testing
      Data Structures & Algorithms
      Benchmarking
      Stream programming
      Serialization / file formats

## CoC from the beginning

Haskell coding community (even more than programming in general) seems to lack diversity. Course should make a real effort to be inclusive to women, minorities etc. Advertizing and holding to a Code of Conduct communicates to potential such attendees that the course aims to be available to all.

## Opinionated

Choose and commit to a particular approach for solving particular problems. It's fine to reference other approaches but it's confusing and off-putting for beginners to be shown a menu of options before they have decided if the language offers any value for them anyway.

An example of one approach to one problem might be for example, [ReaderT](https://www.fpcomplete.com/blog/2017/06/readert-design-pattern) 

