# Benchmarks Game using TinyGo

See https://benchmarksgame-team.pages.debian.net/benchmarksgame/measurements/go.html

## binarytrees

### Go 1.21.1
```
$ time ./build/binarytrees-go-1.21.1 21
stretch tree of depth 22         check: 8388607
2097152  trees of depth 4        check: 65011712
524288   trees of depth 6        check: 66584576
131072   trees of depth 8        check: 66977792
32768    trees of depth 10       check: 67076096
8192     trees of depth 12       check: 67100672
2048     trees of depth 14       check: 67106816
512      trees of depth 16       check: 67108352
128      trees of depth 18       check: 67108736
32       trees of depth 20       check: 67108832
long lived tree of depth 21      check: 4194303

real    0m42,670s
user    1m45,532s
sys     0m0,699s
```

### TinyGo 0.30.0
```
$ time ./build/binarytrees-tinygo-0.30.0 21
stretch tree of depth 22         check: 8388607
2097152  trees of depth 4        check: 65011712
524288   trees of depth 6        check: 66584576
131072   trees of depth 8        check: 66977792
32768    trees of depth 10       check: 67076096
8192     trees of depth 12       check: 67100672
2048     trees of depth 14       check: 67106816
512      trees of depth 16       check: 67108352
128      trees of depth 18       check: 67108736
32       trees of depth 20       check: 67108832
long lived tree of depth 21      check: 4194303

real    1m17,389s
user    1m17,235s
sys     0m0,144s
```

## fasta

### Go 1.21.1

```
$ time ./build/fasta-go-1.21.1 25000000

...
caatgaggatgtaccgacaaaagctcgatttaaaagcctcgaaacgagatgtacgaatcg
tttactgccttttatgaggagtcgagtactgttggttcatatttgctacatgattgtatg
taataacgatcccgccctttatcggttcgatcctttatggcgataagttatgaatcgtca
gtatctttagatcaaaaactcaactagtacccagttccccggaggaacggtcatgattaa
tgcgttttacggtctcccgtccctcttcttgtcagaggaatcagtttcatccgatcccac
tcgatgattggtatagctatttgccgaaaagccacaacgtattcggtactatcttgtttg
attcccctgtatcttaattc

real    0m15,649s
user    0m5,655s
sys     0m6,288s
```

### TinyGo 0.30.0

```
$ time ./build/fasta-tinygo-0.30.0 25000000

...
tttactgccttttatgaggagtcgagtactgttggttcatatttgctacatgattgtatg
taataacgatcccgccctttatcggttcgatcctttatggcgataagttatgaatcgtca
gtatctttagatcaaaaactcaactagtacccagttccccggaggaacggtcatgattaa
tgcgttttacggtctcccgtccctcttcttgtcagaggaatcagtttcatccgatcccac
tcgatgattggtatagctatttgccgaaaagccacaacgtattcggtactatcttgtttg
attcccctgtatcttaattc

real    0m17,160s
user    0m7,113s
sys     0m6,649s
```

## mandelbrot

### Go 1.21.1

```
$ time ./build/mandelbrot-go-1.21.1 16000

...
7|H8z8 0?
         _0O 
   "@@@ 0 @ 0@   d@@ @@ @ @
P@@@@@   @O`D  ? 
                 0" @??@@@   F
                              >?@` 
@ p>?`_I"     !@bHC _HOG@ @
                          @
real    0m24,175s
user    0m22,930s
sys     0m0,381s
```

### TinyGo 0.30.0

```
time ./build/mandelbrot-tinygo-0.30.0 16000

...
   "@@@ 0 @ 0@   d@@ @@ @ @
P@@@@@   @O`D  ? 
                 0" @??@@@   F
                              >?@` 
@ p>?`_I"     !@bHC _HOG@ @
                          @
real    0m33,272s
user    0m31,952s
sys     0m0,313s
```
