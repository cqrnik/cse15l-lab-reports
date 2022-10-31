# Lab Report 3


## grep option "-l"
Displays a list of files that contain the given search case

`grep -l [search case] [file location]`

<br>

- Example 1:
```
[cs15lfa22qf@ieng6-201]:technical:220$ grep -l "diaphragm" ./biomed/*.txt
./biomed/1471-2334-2-1.txt
./biomed/1471-2415-3-4.txt
./biomed/1477-7827-1-43.txt
./biomed/cc1852.txt
./biomed/cc4.txt
./biomed/rr196.txt
```
Searching all text files in the biomed directory for the string 'diaphragm', and displaying the files that contain it.

<br>

- Example 2:
```
[cs15lfa22qf@ieng6-201]:technical:227$ grep -l "record" ./government/Media/*.txt
./government/Media/Avoids_Budget_Cut.txt
./government/Media/Eviction_law.txt
./government/Media/Farm_workers.txt
./government/Media/Federal_agency.txt
./government/Media/Oregon_Poor.txt
./government/Media/Texas_Lawyer.txt
./government/Media/The_State_of_Pro_Bono.txt
./government/Media/Understanding.txt
./government/Media/Weak_economy.txt
./government/Media/fight_domestic_abuse.txt
./government/Media/help_rent-to-own_tenants.txt
./government/Media/water_fees.txt
```
Searching all text files in the government/Media directory for the string 'record', and displaying the files that contain it.

<br>

- Example 3:

```
[cs15lfa22qf@ieng6-201]:technical:231$ grep -l "and" ./plos/pmed.0010050.txt
./plos/pmed.0010050.txt
```
Searching the file /plos/pmed.0010050.txt for the string 'and', and displaying the file if it contains the string.


<br><br><br>

## grep option "-c"
Displays a the count of lines in the given file that contain the given search case

`grep -c [search case] [file location]` 

<br>

- Example 1:

```
[cs15lfa22qf@ieng6-201]:technical:233$ grep -c "and" ./plos/pmed.0010048.txt
11
```
Searching the file /plos/pmed.0010048.txt for the string 'and', and displaying the count of lines containing the string
<br>

- Example 2:

```
[cs15lfa22qf@ieng6-201]:technical:244$ grep -c "in" ./plos/pmed.00202*.txt
./plos/pmed.0020200.txt:30
./plos/pmed.0020201.txt:27
./plos/pmed.0020203.txt:45
./plos/pmed.0020206.txt:142
./plos/pmed.0020208.txt:57
./plos/pmed.0020209.txt:153
./plos/pmed.0020210.txt:85
./plos/pmed.0020212.txt:105
./plos/pmed.0020216.txt:169
./plos/pmed.0020226.txt:9
./plos/pmed.0020231.txt:72
./plos/pmed.0020232.txt:120
./plos/pmed.0020235.txt:40
./plos/pmed.0020236.txt:43
./plos/pmed.0020237.txt:30
./plos/pmed.0020238.txt:42
./plos/pmed.0020239.txt:47
./plos/pmed.0020242.txt:37
./plos/pmed.0020246.txt:286
./plos/pmed.0020247.txt:93
./plos/pmed.0020249.txt:312
./plos/pmed.0020257.txt:40
./plos/pmed.0020258.txt:31
./plos/pmed.0020268.txt:32
./plos/pmed.0020272.txt:54
./plos/pmed.0020273.txt:40
./plos/pmed.0020274.txt:28
./plos/pmed.0020275.txt:38
./plos/pmed.0020278.txt:23
./plos/pmed.0020281.txt:16
```
Searching the text files in /plos/ with names beginning with pmed.00202 for the string 'in', and displaying the count of lines containing the string for each file.

<br>

- Example 3:

```
[cs15lfa22qf@ieng6-201]:technical:248$ grep -c "\n" ./plos/pmed.002014*.txt
./plos/pmed.0020140.txt:224
./plos/pmed.0020144.txt:59
./plos/pmed.0020145.txt:32
./plos/pmed.0020146.txt:40
./plos/pmed.0020148.txt:42
./plos/pmed.0020149.txt:40
```
Searching the text files in /plos/ with names beginning with pmed.002014 for a new line character, and displaying the count of lines containing it for each file.

<br><br><br>

## grep option "-n"
Displays the matching line and line number of the matching lines in the given files.

`grep -n [search case] [file location]` 

<br>

- Example 1:

```
[cs15lfa22qf@ieng6-201]:technical:272$ grep -n "biological" biomed/rr*.txt
biomed/rr171.txt:23:        of apoptosis. To exert their biological effects during
biomed/rr171.txt:530:        Inflammatory mediators induce their biological effects
```
Searching the text files in /biomed/ with names beginning with rr for the string 'biological', and displaying each matching line and line number.

<br>

- Example 2:

```
[cs15lfa22qf@ieng6-201]:technical:271$ grep -n "launch " biomed/*.txt
biomed/1475-2875-2-10.txt:543:        launch the activity on their own, the Quality Assurance
biomed/gb-2002-3-12-research0081.txt:166:        launch and monitor jobs, retrieve results and support other
biomed/gb-2002-3-12-research0081.txt:190:        variety of powerful ways to launch and monitor jobs,
biomed/gb-2002-3-12-research0081.txt:197:        used to launch jobs. Users create configuration files that
```
Searching all text files in /biomed/  for the string 'launch ', and displaying each matching line and line number.

<br>

- Example 3:

```
[cs15lfa22qf@ieng6-201]:technical:278$ grep -n "clear" 911report/chapter-2.txt
214:                especially clear in Egypt. Confronted with a violent Islamist movement that killed
352:                clearly the leader (emir) of al Qaeda. This organization's structure included as its
359:                self-confidence and ambition. He soon made clear his desire for unchallenged control
620:            A clear signal to Bin Ladin that his days in Sudan were numbered came when the
728:            For a time, it may not have been clear to Bin Ladin that the Taliban would be his
740:                Sudanese, clearly thought that he had new freedom to publish his appeals for jihad.
758:                stay clear of Bin Ladin.
943:                issued a "crystal clear" fatwa. If the instigation for jihad against the Jews and
```
Searching the text file 911report/chapter-2.txt for the string 'clear', and displaying each matching line and line number.

<br><br><br><br>