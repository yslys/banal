# banal

### Files in this repo
banal: the original file.

banal_annotated: the file we could modify and test.

sim_paper_asplos.pdf: the pdf we use for testing.

output.txt: the generated output after uncommenting one print statement (i.e. print ```$content``` variable in each iteration) in ```parse_p2h_text( $$$ )```.

README.md: current file XD.

### Usage
Basic usage:
```
./banal_annotated ./sim_paper_aslpos.pdf
```

For printing the help:
```
./banal_annotated
```

### Goal
We want to add a new flag to it, say ```-count_words```, to print out the word count.

In the parse_p2h_text function, the text of a PDF is put into the $content variable, so the task is to 
- (1) figure out how to reliably count the words from here and ignore extraneous things, and 
- (2) figure out how to skip the bibliography - such as skipping lines after the word “Refernces” or “Bibliography”


### Some thoughts
Based on the generated output, ```$content``` does not represent each line, instead, it could represent even a single character in a line (pay attention to ```0``` in 0sim).

There are some words locate at the end of the current line, and the beginning of the next line, which is not captured in one single ```$content``` variable. For instance, search for ```exam-```.

To be continued...


### Useful Links

+ [```my``` keyword](https://www.geeksforgeeks.org/perl-my-keyword/)

+ [```my``` followed by parenthesis](https://stackoverflow.com/questions/10031455/using-my-with-parentheses-and-only-one-variable)

+ [```$```, ```@```, and ```%```](https://www.geeksforgeeks.org/perl-data-types/?ref=lbp)
    + $: scalars
    + @: arrays
    + %: hashes

+ [```$_```: the default variable of Perl](https://perlmaven.com/the-default-variable-of-perl)

+ [```@_```: the array of arguments within a subroutine](https://stackoverflow.com/questions/4563485/what-is-the-meaning-of-in-perl)

+ [```$_[0]```, ```$_[1]```, etc](https://www.cs.cmu.edu/afs/cs/user/rgs/mosaic/pl-sub.html#:~:text=_%2C%20that%20is-,(%24_%5B0%5D%2C%20%24_%5B1%5D%2C%20...),-.%20The%20array%20%40_)
    + [link0](https://stackoverflow.com/questions/4563485/what-is-the-meaning-of-in-perl#:~:text=Therefore%2C%20if%20you%20called%20a%20function%20with%20two%20arguments%2C%20those%20would%20be%20stored%20in%20%24_%5B0%5D%20and%20%24_%5B1%5D.)

+ [```sort()```](https://www.geeksforgeeks.org/perl-sort-function/)

+ [prototypes](https://perldoc.perl.org/perlsub#Prototypes)
    + [link0](https://stackoverflow.com/questions/36887201/what-does-the-dollar-character-in-the-brackets-of-a-perl-subroutine-mean/36887385)
    + [link1](https://stackoverflow.com/questions/46795246/what-is-the-meaning-of-prototype-in-perl#:~:text=2-,Looking%20at,-your%20previous%20question)

+ [Perl regular expressions quick start](https://perldoc.perl.org/perlrequick)
    + [search and replace](https://perldoc.perl.org/perlrequick#Search-and-replace)
    + [```$&```](https://perldoc.perl.org/variables/$&)
+ [Perl regular expressions](https://perldoc.perl.org/perlre)
