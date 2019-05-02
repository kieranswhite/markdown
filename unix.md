# UNIX


[CodeAcademy Unix Course](https://www.codecademy.com/learn/learn-the-command-line)


#### Get Record Lengths

```awk ‘{print length{$0}; )’ <file_name>```

#### Get all record lengths and counts of records for each length

```awk ‘{print length}’ <file_name> |sort|uniq -c ```

#### Space pad records to a specified length

(length is 2760 in the example) 

``` cat <in_file> |sed ‘s/\r$//’ |awk ‘{printf “%-2760s\n, $0}’ > <out_file> ```

#### Count number of pipes in a record

``` awk ‘BEGIN { FS = “|” }; {print NF}’ ```

#### Remove a character from a file

(char is a double quote in this example) 

``` sed s/\”//g <in_file> > <out_file>``` 

#### Cut lines from a file

(lines 2, 3 and 10 in this example) 

``` sed ‘2p;3p;10p;d’ <in_file> ```

#### View file data (so can see non-printable characters)

``` od -c <in_file> od -c -Ao <in_file> ```

#### Get the count of each record type in a delimited file

(pipe delimited in this example) 
``` cut -fa -d”|” <in_file> | uniq -c ```

#### Remove empty lines from a file

``` sed -i ‘/^$/d’ <file> ```