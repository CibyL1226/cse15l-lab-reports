# Lab Report 3

The `grep ` command is usually used to find out information about a certain string from a large files with a lot of strings. Today I am showing you four different ways you can use `grep` to explore a directory and the files in it. 

## First Method

**`grep -w <word> <file.txt>`** to find and output all the sentences containing the whole word instead of parts of the word.(Found on [ChatGPT](https://chat.openai.com/)). **This command is useful when you wanted to eliminate words that don't match exactly the word you are searching for to avoid confusion.**


_The input I put in chatGPT is "what are some ways to use grep function??"_
The output I got for this specific command from chatGPT says: "Search for whole word matches (using -w option):
`grep -w word file.txt`
The -w option ensures that the pattern is matched only as a whole word, ignoring partial matches within larger words."_

**First example** shows all the sentences contianing the word "recall" from the `chapter-1.txt` file from the 911report directory. The input includes the `grep -w` command and the string we are looking for as well as the file we are looking in.

This commmand is useful when you wanted to find information using a keyword or find quotes with a certain word, but you also wanted to eliminate other words that contains the word your looking for and make sure the return sentences contians exactly the word you're looking for.  

*Input:* `grep -w recall chapter-1.txt` (the "-w" here signifies "word")

*Output:*
` When the local civil aviation security office of the Federal Aviation Administration (FAA) later investigated these security screening operations, the screeners recalled nothing out of the ordinary. They could not recall that any of the passengers they screened were CAPPS selectees. We asked a screening expert to review the videotape of the hand-wanding, and he found the quality of the screener's work to have been "marginal at best." The screener should have "resolved" what set off the alarm; and in the case of both Moqed and Hazmi, it was clear that he did not.
    In most cases, the chain of command authorizing the use of force runs from the president to the secretary of defense and from the secretary to the combatant commander. The President apparently spoke to Secretary Rumsfeld for the first time that morning shortly after 10:00. No one can recall the content of this conversation, but it was a brief call in which the subject of shootdown authority was not discussed.`
        
**Second example**

This command looks for every sentence that contains the word "unlikely" but not "likely". The input includes the `grep -w` command and the whole phrase follow by the text file name. 

*Input:* `grep -w unlikely chapter-1.txt`

*Output:* `Third, NEADS needed orders to pass to the pilots. At 10:10, the pilots over Washington were emphatically told, "negative clearance to shoot." Shootdown authority was first communicated to NEADS at 10:31. It is possible that NORAD commanders would have ordered a shootdown in the absence of the authorization communicated by the Vice President, but given the gravity of the decision to shoot down a commercial airliner, and NORAD's caution that a mistake not be made, we view this possibility as unlikely.`
 
## Second Method

Another way to use incorporate the `grep` command is to use the `-r` command after `grep` to search for a string from all the files in a directory recursively. (Found on [ChatGPT](https://chat.openai.com/))  **This command is very useful if you wanted to go through the entire directory without having to type out and serach through each file out one by one. This method can save a lot of time and preven errors.**



_The input I put in chatGPT is "what are some ways to use grep function?"
The output I got for this specific function from chatGPT says: "Search recursively in directories: `grep -r pattern directory/`_

The -r option enables recursive searching. It searches for the pattern in all files within the specified directory and its subdirectories."


**First example** looks for the string "takeoff" from every files in the same `911report` directory and return them.
 
*Input:* `grep -r "takeoff" ~/Documents/GitHub/docsearch/technical/911report` (the -r here signifies "recursive" search with in a directory, it can prevent errors and save time when you wanted to explore a pattern within a directory)

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

This method used `grep` followed by `-E` to find a pattern from the file indicated and return the lines containing the pattern. (Found on [ChatGPT](https://chat.openai.com/)) **This command is useful when you wanted to find the word and be specific about its location or what comes before or after the word you are searching for.**


_The input I put in chatGPT is "what are some ways to use grep function?"
The output I got for this specific function from chatGPT says: "Search for lines ending with a specific pattern: `grep -E "pattern$"` This command searches for lines that end with the specified pattern. The $ character represents the end of a line in regular expressions."_


**First example** 

The command has a `$` at the end of the string indicating that it is looking for sentences with the word "Air" at the end of the line. To look for lines with the word "Air" in the beginning of the sentence, we need to us a `^` at the beginning of the string. 


*Input:* `grep -E "Air$" chapter-13.2.txt` ("-E" here signifies "extension", becasue it allows an extended search of a regular expression)

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

This method uses the `grep` command with `-c`, which stands for count. This command counts and return how many of the indicated strings is in the files after finding them. (Found on [ChatGPT](https://chat.openai.com/)) **This command is useful becasue it counts how many times a word show up in the articles without having you counting from the output and possibly make mistakes when counting.**

_The input I put in chatGPT is "what are some ways to use grep function?"
The output I got for this specific function from chatGPT says: "Count the number of matching lines:`grep -c pattern file.txt` The -c option counts the number of lines that match the pattern instead of displaying the lines themselves."_



**Fist example**

This input is looking for the string "brain" and the output tells us that the word appeared 9 times in the `pmed.0020060.txt` text file.

*Input:* `grep -c "brain" pmed.0020060.txt` ("-c" here stands for "count" because the command returns the count of the string you serached up)

*Ouput:* `9`

**Second example**

This input looks for the author's last name "Annan" and returns how many times it has appeared in the text file `journal.pbio.0020001.txt`. The output shows that it showed up 7 times throughout the whole article.

Input: `grep -c "Annan" journal.pbio.0020001.txt`

Output: `7`



