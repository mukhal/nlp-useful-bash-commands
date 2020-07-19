# :candy: useful bash commands for Natural Language Processing :candy:
*A collection of useful bash commands that I use a lot for data manipulation, wrangling, and preprocessing in NLP. Some come from the awsome [missing semster](https://missing.csail.mit.edu/2020/course-shell/).*


### miscellaneous
```bash
# split tsv file, and extract 3rd and 5th columns
cut -f3,5 -d'      ' filename.tsv

# Oneliner add a prefix to the names of all files inside a folder
for file in *; do mv "$file" "prefix-$file"; done 

# Remove first line from file
tail -n +2 filename.txt

# print specific line in a file
sed -n -e 6p filename.txt
```


#### Sed 

```
# Match and replace the string matched with the regex inside the second parentheses () with empty string.
cat file | sed -E 's/.* ([0-9]) (.*) /\2/'
```
