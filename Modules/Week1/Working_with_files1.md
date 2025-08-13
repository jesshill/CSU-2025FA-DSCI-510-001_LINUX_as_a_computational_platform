# Working With Files 1

### Peeking inside files with more and less

There are four main commands for printing file contents to the screen …

- **more** – scroll down through files
- **less** – scroll up or down through files
- **head** – show the top n lines. The default is n = 10
- **tail** – show the bottom n lines. The default is n = 10

**!!! Exercise**: 

- Navigate to your directory titled `chromsizes2`
- Try the following ways of peeking into files in that directory …

```
$ more ce11_chrom_sizes.txt # OR
$ more hs1_chrom_sizes.txt
```

Use **spacebar** or **down arrow** or **return** to scroll down

Type **q** to quit

```
$ less hs1_chrom_sizes.txt
```

Use **spacebar** or **down arrow** or **return** to scroll down

Use **b** or **up arrow** to scroll up

Type **q** to quit

```
$ head hs1_chrom_sizes.txt #show first 10 lines
$ head -n 5 hs1_chrom_sizes.txt #show first 5 lines
$ tail hs1_chrom_sizes.txt #show last 10 lines
$ tail -n 5 hs1_chrom_sizes.txt #show last 5 lines
```

**!!! Quick tip**: Sometimes it looks like head or tail are showing way more lines than you expect. If your lines are very, very long (typical in bioinformatics), this may be due to forced word wrapping in the terminal. Try re-sizing your browser bigger or smaller to see if this is the case.

**!!! Exercises**: S


