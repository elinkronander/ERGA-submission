# Need for additions
* `PACBIO_SMRT` as platform for HiFi, not only `ILLUMINA` - when tried with the PacBio Revio input, which is the means of SciLifeLab HiFi sequencing, the xml put out an ILLUMINA capture
* `library_construction_protocol` (or possibly `design_description`) - currently no text explanation of how the samples were prepared for sequencing is included, which is something we as data stewards stress is important for future reuse
* documentation - not that easy to find out how to contribute without the code additions being ugly hacks instead of real, valuable solutions. At least comments in the code explaining functions, would be helpful.

## Additions made
I've made additions that works for our purpose (BGE *Pinna rudis* HiFi sequencing initiated the need for additions in code), all rows affected/updated has a comment, but I don't know Python or this program so it is likely not good enough for production (I would check all resulting xml files and check that nothing looks weird).

### PacBio
Add an `elif` in `get_experiments` function (ugly hack, which might destroy things for others):
```
    if read_type == "ONT":
        layout = 'SINGLE'
        model = 'OXFORD_NANOPORE'
    elif read_type == "Hifi":
        layout = 'SINGLE'
        model = 'PACBIO_SMRT'
```

### library_construction_protocol
Using `exp_attr` variable to be put as library construction protocol, all places where updates have been made has a comment (#add...).
