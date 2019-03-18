intro
    everyone prepared?
    round of previous experience
    team up
    follow along, ask questions, ...
    agenda
        what we'll leave out

digital circuits
    combinatorial
        (normally start with boolean algebra and common components, but we'll skip that... just use Haskell operations)
        logic cells
    sequential
        clocks
        registers
        (block) RAM?
    automatons
    i/o
        debouncing

FPGAs
    vs ASIC
    how do they work?
        LUTs
        dedicated blocks
        flashing
    example: iCE40
    applications

HDLs
    constraints compared to programming languages
    traditional HDLs
        Verilog & VHDL
        type safety
        verbosity
        "low-level", lack of abstraction
        semantic mismatch
            imperative description of sequential processes
    Clash
        history
        (short Haskell type-level intro? or interspersed?)
        how does it deal with HW constraints?
            It must be completely monomorphic
            It must be completely first-order
            HiddenClockReset
            Bundle

hands-on
    demo
    quick how-to
        board i/o
        working with repl
    hacking time!

somewhere?
    unsigned vs bitvector vs ...
