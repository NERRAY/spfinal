### spfinal solution

***
* Name: Nauruzbayeva Farikha
* Email: 180107104@stu.sdu.edu.kz
* Variant: [05](../variants/variant05.md)
* Solution: [./top](./top)
***



<p>&nbsp;</p>
<h3 style="text-align: center; color: #3f7320;"></h3>
<p><span style="border-bottom: 4px solid #c82828;">Foreword</span></p>
<p>Teacher I did my best. I am very trying to do this task, but really I don't know programming very well, and it my guilt. All code that I wrote here I did by myself, and it was really hard (for me, who don't know programming)</p>
<p></p>
<p>###############################</p>
<p>So, let's start....<br />At first I thought like an ordinary people and make something like that:<br /><strong>cut -d' ' -f '3,4' log.txt |</strong>&nbsp; #Where the first cut -d' ' will help destroy&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; some rows and -f '3,4' will show me rows&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;that I need.</p>
<p><strong>sort -nrk3 |&nbsp;</strong> &nbsp;#&nbsp;Then I used sort for sorting and -nrk3 help me to&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; sorting numeric data in reverse order.</p>
<p><strong>uniq -c| tr -d [- |</strong>&nbsp; #uniq -c help me to display occurrences<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; tr -d delete all symbols that I didn't need in my&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case [-</p>
<p><strong>cut -c1-20 |&nbsp; &nbsp;</strong> &nbsp; &nbsp; &nbsp; &nbsp; #cut -c1-20 - select by specifying a character,&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; a set of characters, or a range of characters</p>
<p><strong>date -d "ddMMMYYY:hh:mm:ss" |</strong></p>
<p><strong>head -n5</strong></p>
<p>date -d "ddMMMYYY:hh:mm:ss" - it must have format my date but I did alternative solution using awk</p>
<p><br />Real Code<br /><strong>awk '{print $4}' log.txt |</strong> # this comand print 4'th row in my files <br /><strong>tr -d [- |</strong> # this comand delete all unusable symbols like "[" and "-"<br /><strong>cut -c1-11 |</strong> # this comand cut specify a range of characters <br /><strong>sort |</strong> # this comand just sorting<br /><strong>uniq -c |</strong> # display occurances of the each line<br /><strong>sort -nrk4|</strong> # sorting by column number in reverse order (if we near write file name it's sorting in file )<br /><strong>head -n5 |</strong> # give us top 5, (if we write -n6 give us top 6) <br /><strong>sed -e 's/,/\n/g' |</strong> # replace "/" and "\n" from the data by a space.<br /><strong>cat -n |</strong> # write number of order<br /><strong>awk '{sum+=$1; string[$4]=$1} END {for (var in string) print var, "-", string[var], "-", string[var]*100/sum "%"}' |</strong> #cycle for printing by order and printing procentage<br /><strong>sort -nr</strong> #sorting result by reverse order</p>
<p><br />That allow me decrease my number lines of code <br />I know that here we should use some code for formatting date  I used | <strong> -date + '%d/%b/%Y:%H:%M:%S'</strong> and used |<strong>gawk '$4~/01\/Oct\/2006/'|gawk '{print $1}'</strong> (and for this I download gawk) but it doesn't help me</p>
<p> Teacher sorry for my bad editing </p>










