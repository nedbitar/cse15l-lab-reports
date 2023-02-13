<h2>The '-r' Option in 'grep'</h2>

The '-r' option in the 'grep' command is short for "recursive", and it allows grep to search for matches recursively through directories.

Without the '-r' option, 'grep' will only search in the files specified in its arguments and will not search through subdirectories.

This can greatly limit the scope of your search and potentially exclude important results. By using the '-r' option, you can ensure that 'grep' searches through all relevant files and subdirectories, providing a more comprehensive search result.

<h3>Here is the Syntax for the command:</h3>

```console
grep -r "Key Word or Phrase to search for" <directory>
```
<h4>Here is example usage of the command:</h4>

```console
nazihbitar@JoeBob skill-demo1-data % grep -r "yoyo" written_2               
written_2/travel_guides/berlitz1/WhereToJapan.txt:        pines of the forest surrounding the lovely Kyoyochi Pond at the foot of
nazihbitar@JoeBob skill-demo1-data % grep -r "Molino de Antigua" written_2 
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt:Betancuria, by far the most attractive and visited inland town on the island, is an oasis of greenery on this barren island. Although the riverbed here is almost perpetually dry, the town is fortunate to have a high water table. Because of its theoretical invulnerability at the heart of the island, it was made Fuerteventura’s first capital in the early 15th century. However, in 1539 somehow the ravaging Berber pirates overcame the mountains (which still provide a difficult drive today), and destroyed the original cathedral. The present 17th-century church, Iglesia de Santa María is a splendid building and hosts many interesting treasures. Look at the unusual wooden beams between the flagstones on the floor, the wooden altar and choir, and the decorated pulpit. Adjacent to the museum is a leather factory-cum-shoe-shop, set in an atmospheric old building. Wander round this lovely little town and admire the view from across the bridge, where there is an unpretentious restaurant/bar and a gift shop. Just south of Betancuria is the neat and pretty village of Pájara, but a stop at Antigua, on the other side of the mountains is in order. This is reached either by continuing on the loop past Tuineje, or backtracking from Betancuria and taking the FV-416 across the mountains. In either event, once in Antigua — the island’s capital from 1834–1835 — you can’t miss the traditional old windmill found just to the north of town, and this is your destination. Actually, the Centro de Artesania “Molino de Antigua” (Windmill Crafts Center) is much more than just that, and has something for almost everyone’s tastes. Interesting crafts and a visit inside the windmill certainly, but also ethnographic and archaeological exhibitions, modern art, an audiovisual room, rooftop view- points and an intriguing cactus garden, not to mention a nice restaurant. 
```
The output of the grep -r command is a list of all the lines in the specified directory (and its subdirectories, if the -r option is used) that match the pattern you are searching for. The output lists the names of the files containing the matches, along with the matching lines.

Each line of the output shows the name of a file containing a match, followed by a colon, followed by the matching line from that file. In this example, the first line of the output indicates that the "Key Word or Phrase to search for" was found in the file written_2/travel_guides/berlitz1/WhereToJapan.txt, and the matching line is displayed after the colon.

<h2>The '-c' Option in 'grep'</h2>
You can think of the '-c' option as an abbreviation for count. It is a special option that tell the computer to count the number times a word or phrase appears in a txt file.

```console
grep -c "word or phrase" fileName.txt
```
 

<h4>Here is example usage:</h4>
```console
nazihbitar@JoeBob berlitz1 % grep -c "yoyo" WhereToJapan.txt
1
nazihbitar@JoeBob berlitz1 % grep -c "the" WhereToHawaii.txt 
18
```

