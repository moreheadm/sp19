# 130-web


Public course materials for [UCSD CSE 130](https://ucsd-progsys.github.io/130-sp19/)

## Install

You too, can build this webpage locally, like so:

```bash
$ git clone git@github.com:ucsd-cse130/sp19.git
$ cd sp19
$ make
```

To then update the webpage after editing stuff, do:

```bash
$ make upload
```

The website will live in `_site/`.

## Customize

By editing the parameters in `siteCtx` in `Site.hs`

## View

You can view it by running

```bash
make server
```

## Update

Either do

```bash
make upload
```

or, if you prefer

```bash
make
cp -r _site/* docs/
git commit -a -m "update webpage"
git push origin master
```

## To build Lecture Versions 

To build the "lecture" version of all the htmls i.e. *without* 
the answers to quizzes and other questions, you can replace 

    crunchWithCtxCustom "final" postCtx 
    
with 

    crunchWithCtxCustom "lecture" postCtx 
    
in `Site.hs` (edited) 

Then, as you go through the lectures, replace `match "lectures/*"` with

```
match "lectures/00-*"    $ crunchWithCtxCustom "final" postCtx
match "lectures/*"       $ crunchWithCtxCustom "lecture" postCtx
```

(and gradually add more and more lectures to `final` as I go through them)



## Credits

This theme is a fork of [CleanMagicMedium-Jekyll](https://github.com/SpaceG/CleanMagicMedium-Jekyll)
originally published by Lucas Gatsas.




## New Class Checklist

- [x] Site.hs
- [x] index.md
- [x] assignments.md
- [x] contact.md
- [x] grades.md
- [x] links.md
- [x] calendar.md
- [x] clicker groups
- [x] clicker chart
- [ ] lectures.md

## SP 19

- [Roster](https://docs.google.com/spreadsheets/d/1DqB98XNyDpqsL1FWyReTOecj8GFD6KXVnkjM6iI2Lrs/edit?usp=sharing)



