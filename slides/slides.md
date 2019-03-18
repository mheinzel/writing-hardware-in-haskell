% Writing Hardware in Haskell
% Matthias Heinzel
% March 22nd, 2019

## First Things First

tools set up?

previous experience?

ask questions

## Agenda (v2)

Motivation

* Hardware
* FPGAs
* HDLs
* Clash

Digital Circuits

* combinatorial
* sequential
* automata
* I/O

# Motivation

## Hardware

full control over circuit layout

parallelism 8)

## FPGAs

Field-Programmable Gate Array

rapid prototyping

affordable in low quantities

## HDLs

Hardware Description Languages

e.g. VHDL, Verilog

similar to programming languages, BUT...

## Clash

clash-lang.org

developed at University of Twente, Enschede

publications since ~2009

## Clash

functional HDL

compiles to Verilog or VHDL

fork of the Haskell compiler

this gives us incredible potential of abstraction and convenience

. . .

~TemplateHaskell!~


# Digital Circuits

## combinatorial

~~boolean algebra~~

~~logic cells~~

all the power of Haskell!

. . .

really?

## IO, FFI, Exceptions

no

. . .

but we don't like that anyways

## algebraic data types

with caveats:

* size?

```haskell
Vec (n :: Nat) (a :: Type)
```

## recursive functions

umh...

## top level signatures (to be synthesized)

monomorphic

first-order


## sequential

aka synchronised

```haskell
register :: a -> Signal a -> Signal a
```

Signal is Applicative

FRP anyone?

## clocks

potentially multiple domains

```haskell
register
    :: HiddenClockReset
    => a
    -> Signal domain a
    -> Signal domain a
```

## simulation

```haskell
sampleN :: (Foldable f, NFData a) => Int -> f a -> [a]
```

```haskell
simulate :: (NFData a, NFData b) => (Signal domain1 a -> Signal domain2 b) -> [a] -> [b]
```

## recursion


## automata


## I/O

pinmap

primitives, Verilog/VHDL interaction

```haskell
button
    :: HasCallStack
    => Clock domain source
    -> Bit
    -> Signal domain Bit
```


# Hacking!
