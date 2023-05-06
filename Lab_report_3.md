# Lab Report 3

First Example:

Using the files from biomed directory to find sentences containing the word "BMI"
Input: `grep "BMI" 1468-6708-3-1.txt`

Output:
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
        
Second input that looks for an entire phrase:

Input: `grep "body mass index" 1468-6708-3-1.txt`

Output: `between body mass index (BMI) and mortality, controlling`
 
Another way to use incorporate the `grep` command is to use the `-r` command after `grep` to search for a string from all the files in a directory recursively:
 
Input: `grep -r "takeoff" ~/Documents/GitHub/docsearch/technical/911report`

Output: 
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