As we have seen so far Unix commands can read files. Of course they can also write to files.
A Unix command can be thought of as a program that reads from a standard input (STDIN) and writes to two different channels, a standard output (STDOUT) and a standard error output (STDERR). 

- The standard input allows to read a file or a text stream
- The standard output allows to print the results of the command
- The error output allows to print messages during the execution or when the program encounters an error.
 
<img src="assets/io-cmd.png" width="200">

As shown in the figure above:

- A file can be sent to a command using **'<'**.
- The result of a command can be send to a file using **'>'** (if file exists it is overwritten).
- The STDERR can be redirected to a file using **'2>'**.
- Additionally, the '>>' operator can be used to add lines to an existing file.

The general syntax is the following:

```
command < entry_file > out_file 2> error_file
```

## Exercice

Change your directory to *Data*


```
cd Data
```
File SRR3099585_chr18.fastq.gz is compressed (see the *.gz extension). Uncompress the file SRR3099585_chr18.fastq.gz using the *gunzip* command.

```
gunzip SRR3099585_chr18.fastq.gz
```

>>What is the file extension after decompression ?
=== .fastq


>>How many lines does the file SRR3099585_chr18.fastq contains (use *wc* command) ?<<
[*] 100
[*] 1000
[ ] 1253884

Use the head command to extract the 4 first lines of file SRR3099585_chr18.fastq store and store them in a new file named SRR3099585_chr18_4_lines.fastq.

```
head -n 4 SRR3099585_chr18.fastq > SRR3099585_chr18_4_lines.fastq
```

>>Q1: What does the first line of SRR3099585_chr18_4_lines.fastq contain ?
=== @SRR3099585.1