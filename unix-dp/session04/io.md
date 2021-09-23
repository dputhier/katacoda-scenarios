As we have seen so far Unix commands can read files. Of course they can also write to files.
A Unix command can be thought of as a program that reads from a standard input (STDIN) and writes to two different channels, a standard output (STDOUT) and a standard error output (STDERR). 

- The standard input allows to read a file or a text stream
- The standard output allows to print the results of the command
- The error output allows to print messages during the execution or when the program encounters an error.
 
<img src="assets/io-cmd.png" width="200">

As shown in the figure above:

- A file can be sent to a command using **'<'**.
- The result of a command can be send to a file using **'>'** (if file exists it is overwritten).
- The STDERR can be redirected using **'2>'**.
- Additionally, the '>>' operator can be used to add lines to an existing file.

The general syntax is the following:

```
command < entry_file > out_file 2> error_file
```

Use the head command to extract the 4 first lines of file SRR3099585_chr18.fastq.gz located in the Data folder.

```
head -n 4 Data/SRR3099585_chr18.fastq.gz
```

>>Q1: What is written in the first line ?
=== 