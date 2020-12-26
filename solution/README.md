### spfinal solution

***
* Name: Nauruzbayeva Farikha
* Email: 180107104@sdu.stu.edu.kz
* Variant: [05](../variants/variant05.md)
* Solution: [./top](./top)
***



FOREWORD

Teacher I did my best. I am very trying to do this task, but really I don't know programming very well, and it my guilt. All code that I wrote here I did by myself, and it was really hard (for me, who don't know programming) 

So, let's start....
At first I thought like an ordinary people and make something like that:
cut -d' ' -f '3,4' log.txt | sort -nrk3 | uniq -c| tr -d [- | cut -c1-20 | date -d "ddMMMYYY:hh:mm:ss" | head -n5



Where the first cut -d' ' will help destroy some rows and -f '3,4' will show me rows that I need. Then I used sort for sorting and -nrk3 help me to sorting  numeric data in reverse order.
uniq -c help me to display occurrences
tr -d delete all symbols that I didn't need in my case [-
cut -c1-20 - select by specifying a character, a set of characters, or a range of characters
date -d "ddMMMYYY:hh:mm:ss" - it must have format my date but I did alternative solution using awk


Code                              ############Description 
awk '{print $4}' log.txt |        # this comand print 4'th row in my files 
tr -d [- |                        # this comand delete all unusable symbols like "[" and "-"
 cut -c1-11 | 			  # this comand cut specify a range of characters 
sort |				  # this comand just sorting
uniq -c |                         # display occurances of the each line
sort -nrk4| 			  # sorting by column number in reverse order  (if we near write file name it's sorting in file )
head -n5 | 			  # give us top 5, (if we write -n6 give us top 6)					
sed -e 's/,/\n/g' |               # replace "/" and "\n" from the data by a space.
cat -n |                          # write number of order
awk '{sum+=$1; string[$4]=$1} END {for (var in string) print var, "-", string[var], "-", string[var]*100/sum "%"}' |   #cycle for printing by order and printing procentage
 sort -nr                         #sorting result by reverse order


That allow me decrease my number lines of code 
I know that here we should use some code for formatting date I used | -date and used |gawk '$4~/01\/Oct\/2006/'|gawk '{print $1}' (and for this I download gawk) but it doesn't help me










