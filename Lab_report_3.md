# Lab Report 3

The `grep` command is usually used to find out information about a certain string from a large files with a lot of strings. Today I am showing you four different ways you can use `grep` to explore a directory and the files in it. 

## First Method

**`grep "<String>" <file_name>`** to find and output all the sentences containing the string.(Found on ChatGPT) 

The **first example** shows all the sentences contianing the word "BMI" from the `1468-6708-3-1.txt` file from the biomed directory. The input includes the `grep` command and the string we are looking for as well as the file we are looking in.

*Input:* `grep "BMI" 1468-6708-3-1.txt`

*Output:*
`between body mass index (BMI) and mortality, controlling
        excess risk for persons with very low BMI, but that persons
        with moderately high BMI had little or no extra risk except
        because few studies have examined the relation of BMI to
        events [ 10 ] . In this paper we study whether BMI at
          BMI was calculated as measured weight in kilograms
          BMI of 18.5 to 24.9; overweight as 25 to 29.9; and
          separately the group with BMI between 18.5 and 20, which
          with BMI. To adjust for possible confounding we chose
          and likely to be related to BMI. Self-reported covariates
          plotted mean adjusted YOL and YHL against BMI, and tested
          for difference among BMI groups using confidence
          the effect size for each measure, comparing each BMI
        smokers. Black women had a higher mean BMI and higher
        percent obese (BMI ≥ 30) than the other three groups. Black
        statistically significant (p <.05) except for BMI and
        significant differences between black and white for BMI,
        the difference in BMI was no longer statistically
        significantly on BMI, BMI>30, weight loss since age 50,
        We next examined the relationship of BMI to YOL and YHL.
        BMI below 18.5, but averaged 6.6 years for women with a BMI
        only discrepancy is for men with BMI < 18.5, a category
        with BMI from 18.5 to 20 would be considered 'normal' by
        increase sample size for those with low BMI, we combined
        the two lower categories, defining underweight as a BMI
        BMI. For each BMI category the mean and its 95% confidence
        between BMI and YOL for BMI above 20. Underweight women
        normal group. The relationship of BMI to YHL for men is
        similar, but differences among BMI groups were not
        to the normal BMI group. The effect sizes are shown in
          et al proposed a desirable BMI of
        BMI Body mass index`
        
**Second example**

This command looks for every sentence that contains the phrase "body mass index". The input includes the `grep` command and the whole phrase follow by the text file name. 

*Input:* `grep "body mass index" 1468-6708-3-1.txt`

*Output:* `between body mass index (BMI) and mortality, controlling`
 
## Second Method

Another way to use incorporate the `grep` command is to use the `-r` command after `grep` to search for a string from all the files in a directory recursively. (Found on ChatGPT)

**First example** looks for the string "takeoff" from every files in the same `911report` directory and return them.
 
*Input:* `grep -r "takeoff" ~/Documents/GitHub/docsearch/technical/911report`

*Output:* 
`/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-13.2.txt:                after takeoff,"like someone keyed the mike and said everyone stay in your seats."
/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-13.2.txt:                Deborah Welsh (first class, seat J1 at takeoff); Sandra Bradshaw (coach, seat J5);
/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-13.2.txt:                93 would have allowed an observer into the cockpit before or after takeoff who had
/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-13.2.txt:                Protectee Log, Sept. 11, 2001. On Air Force One's objectives on takeoff, see Edward
/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-13.3.txt:                member states were called on to restrict takeoff and landing rights of Taliban-owned
/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-1.txt:    The flight had taken off just as American 11 was being hijacked, and at 8:42 the United 175 flight crew completed their report on a "suspicious transmission" overheard from another plane (which turned out to have been Flight 11) just after takeoff. This was United 175's last communication with the ground.
/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-1.txt:    The Battle for United 93 At 8:42, United Airlines Flight 93 took off from Newark (New Jersey) Liberty International Airport bound for San Francisco. The aircraft was piloted by Captain Jason Dahl and First Officer Leroy Homer, and there were five flight attendants. Thirty-seven passengers, including the hijackers, boarded the plane. Scheduled to depart the gate at 8:00, the Boeing 757's takeoff was delayed because of the airport's typically heavy morning traffic.
/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-1.txt:    The terrorists who hijacked three other commercial flights on 9/11 operated in five-man teams. They initiated their cockpit takeover within 30 minutes of takeoff. On Flight 93, however, the takeover took place 46 minutes after takeoff and there were only four hijackers. The operative likely intended to round out the team for this flight, Mohamed al Kahtani, had been refused entry by a suspicious immigration inspector at Florida's Orlando International Airport in August.
/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-5.txt:                flights in Southeast Asia. KSM told them to watch the cabin doors at takeoff and
/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-7.txt:                flight but took no interest in takeoffs or landings. By the end of May 2000, Hazmi
/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-7.txt:                to storm the cockpit would be about 10-15 minutes after takeoff, when the cockpit`

**Second example**

This input looks for the phrase "important to" from the same `911report` directory and return their path, text file names, and the sentence that contains the pharse.

*Input:* `grep -r "important to" ~/Documents/GitHub/docsearch/technical/911report`

*Output:* 
`/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-6.txt:                Qaeda's image was very important to Bin Ladin, and the video was widely
/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-6.txt:                been built to coordinate counterterrorism policy. It was important to sound
/Users/cibylin/Documents/GitHub/docsearch/technical/911report/chapter-9.txt:                disasters, it is important to integrate those taking 911 calls into the emergency`

## Third Method

This method used `grep` followed by `-E` to find a pattern from the file indicated and return the lines containing the pattern. (Found on ChatGPT)

**First example** 

The command has a `$` at the end of the string indicating that it is looking for sentences with the word "Air" at the end of the line. To look for lines with the word "Air" in the beginning of the sentence, we need to us a `^` at the beginning of the string. 

*Input:* `grep -E "Air$" chapter-13.2.txt`

*Output:* `Accounting Office; INS-Immigration and Naturalization Service; NEADS-Northeast Air
            7. See Air Transport Association/Regional Airlines Association (ATA/RAA) report, "Air
                interview (Nov. 19, 2003). On standard emergency training, see FAA report, "Air
                accordance with the Air Carrier Standard Security program. See FAA report,"Air
                77," Feb. 19, 2002. On events in the cabin, see FAA recording, Indianapolis Air
                derived by the Commission from files provided by the FAA and the Northeast Air`
    
**Second example**

This example uses the command to find all the lines with "time" at the end and one line out of the whole `chapter-10.txt` file was returned. 

*Input:* `grep -E "time$" chapter-10.txt`

*Output:* `While the plan at the elementary school had been to return to Washington, by the time`

## Fourth Method

This method uses the `grep` command with `-c`, which stands for count. This command counts and return how many of the indicated strings is in the files after finding them. (Found on ChatGPT)

**Fist example**

This input is looking for the string "brain" and the output tells us that the word appeared 9 times in the `pmed.0020060.txt` text file.

*Input:* `grep -c "brain" pmed.0020060.txt`

*Ouput:* `9`

**Second example**

This input looks for the author's last name `Annan` and returns how many times it has appeared in the text file `journal.pbio.0020001.txt`. The output shows that it showed up 7 times throughout the whole article.

Input: `grep -c "Annan" journal.pbio.0020001.txt`

Output: `7`



