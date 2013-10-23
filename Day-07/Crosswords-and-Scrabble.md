Crossward, Scrabble, and regular expressions
========================================================

```r
words <- readLines(url("http://dtkaplan.github.io/ScientificComputing/Syllabus/Daily/Day-07/word_list_moby_crossword-flat/word_list_moby_crossword.flat.txt"))
```

```r
# Report
length(words)
```

```
## [1] 113809
```

```r
# The number of words of length 1 is:
length(words[grep("^.$", words)])
```

```
## [1] 0
```

```r
# The number of words of length 2 is:
length(words[grep("^..$", words)])
```

```
## [1] 85
```

```r
# The number of words of length 3 is:
length(words[grep("^...$", words)])
```

```
## [1] 908
```

```r
# The number of words of length 4 is:
length(words[grep("^....$", words)])
```

```
## [1] 3686
```

```r
# The number of words of length 5 is:
length(words[grep("^.....$", words)])
```

```
## [1] 8258
```

```r
# The number of words of length 6 is:
length(words[grep("^......$", words)])
```

```
## [1] 14374
```

```r
# The number of words of length 7 is:
length(words[grep("^.......$", words)])
```

```
## [1] 21727
```

```r
# The number of words of length 8 is:
length(words[grep("^........$", words)])
```

```
## [1] 26447
```

```r
# The number of words of length 9 is:
length(words[grep("^.........$", words)])
```

```
## [1] 16658
```

```r
# The number of words of length 10 is:
length(words[grep("^..........$", words)])
```

```
## [1] 9199
```

```r
# The number of words of length 11 is:
length(words[grep("^...........$", words)])
```

```
## [1] 5296
```

```r
# The number of words of length 12 is:
length(words[grep("^............$", words)])
```

```
## [1] 3166
```

```r
# The number of words of length 13 is:
length(words[grep("^.............$", words)])
```

```
## [1] 1960
```

```r
# The number of words of length 14 is:
length(words[grep("^..............$", words)])
```

```
## [1] 1023
```

```r
# The number of words of length 15 is:
length(words[grep("^...............$", words)])
```

```
## [1] 557
```

```r
# The number of words of length 16 is:
length(words[grep("^................$", words)])
```

```
## [1] 261
```

```r
# The number of words of length 17 is:
length(words[grep("^.................$", words)])
```

```
## [1] 132
```

```r
# The number of words of length 18 is:
length(words[grep("^..................$", words)])
```

```
## [1] 48
```

```r
# The number of words of length 19 is:
length(words[grep("^...................$", words)])
```

```
## [1] 16
```

```r
# The number of words of length 20 is:
length(words[grep("^....................$", words)])
```

```
## [1] 5
```

```r
# The number of words of length 21 is:
length(words[grep("^.....................$", words)])
```

```
## [1] 3
```

```r
# The number of words of length 22 is:
length(words[grep("^......................$", words)])
```

```
## [1] 0
```

```r
# The 100 longest words are:
words[grep("^................$", words)]
```

```
##   [1] "absentmindedness" "acclimatizations" "accountabilities"
##   [4] "acknowledgements" "acquaintanceship" "administratively"
##   [7] "adventitiousness" "aggressivenesses" "agriculturalists"
##  [10] "antiaristocratic" "antibureaucratic" "anticapitalistic"
##  [13] "anticonservation" "anticonventional" "antievolutionary"
##  [16] "antimilitaristic" "antipornographic" "antiprofiteering"
##  [19] "antiprostitution" "antiracketeering" "antitotalitarian"
##  [22] "antituberculosis" "antiunemployment" "apprehensiveness"
##  [25] "arteriosclerosis" "arteriosclerotic" "articulatenesses"
##  [28] "artificialnesses" "attractivenesses" "autobiographical"
##  [31] "biodegradability" "bloodthirstiness" "calamitousnesses"
##  [34] "cantankerousness" "capitalistically" "cardiotoxicities"
##  [37] "catastrophically" "censoriousnesses" "characterization"
##  [40] "chemotherapeutic" "chivalrousnesses" "circumnavigating"
##  [43] "circumnavigation" "combustibilities" "conservationists"
##  [46] "contraindicating" "coproprietorship" "counterattacking"
##  [49] "counterbalancing" "counterblockades" "countercampaigns"
##  [52] "counterchallenge" "counterclockwise" "countercomplaint"
##  [55] "countercriticism" "counterevidences" "counterinfluence"
##  [58] "counterintrigues" "countermovements" "counterpetitions"
##  [61] "counterpressures" "counterproposals" "counterquestions"
##  [64] "counterrebuttals" "counterresponses" "counterterrorism"
##  [67] "counterterrorist" "crystallizations" "cyclophosphamide"
##  [70] "cytopathological" "decentralization" "deliberatenesses"
##  [73] "discursivenesses" "disfranchisement" "disillusionments"
##  [76] "disorderlinesses" "disorganizations" "disproportionate"
##  [79] "disqualification" "dissatisfactions" "diversifications"
##  [82] "electrifications" "enfranchisements" "enthusiastically"
##  [85] "environmentalist" "excommunications" "exemplifications"
##  [88] "experimentations" "expressivenesses" "extemporaneously"
##  [91] "extracontinental" "extraterrestrial" "farsightednesses"
##  [94] "fastiduousnesses" "feeblemindedness" "forthrightnesses"
##  [97] "generalizability" "gregariousnesses" "harmoniousnesses"
## [100] "heterogenousness" "hospitalizations" "humanitarianisms"
## [103] "hydroelectricity" "hypersensitivity" "hypersusceptible"
## [106] "hysterectomizing" "implausibilities" "impressivenesses"
## [109] "inadvisabilities" "inalienabilities" "inappositenesses"
## [112] "incompletenesses" "incomprehensible" "indecisivenesses"
## [115] "indecorousnesses" "indemnifications" "indestrucibility"
## [118] "indiscriminately" "indispensability" "indistinctnesses"
## [121] "inextinguishable" "institutionalize" "instrumentalists"
## [124] "instrumentations" "insubordinations" "insurrectionists"
## [127] "intellectualisms" "intensifications" "intercontinental"
## [130] "interdependences" "interhemispheric" "interjectionally"
## [133] "internationalism" "internationalize" "interrelatedness"
## [136] "irresponsibility" "lasciviousnesses" "licentiousnesses"
## [139] "lightheartedness" "lugubriousnesses" "malodorousnesses"
## [142] "manageablenesses" "masculinizations" "materializations"
## [145] "methodicalnesses" "meticulousnesses" "misapprehensions"
## [148] "misappropriating" "misappropriation" "misconstructions"
## [151] "mispronunciation" "misunderstanding" "monotonousnesses"
## [154] "motionlessnesses" "multidimensional" "multidirectional"
## [157] "multilingualisms" "multimillionaire" "myelosuppression"
## [160] "mysteriousnesses" "nationalizations" "neighborlinesses"
## [163] "noncontroversial" "nonparticipating" "nonproliferation"
## [166] "obsequiousnesses" "obstreperousness" "omnivorousnesses"
## [169] "ophthalmologists" "organizationally" "overcapitalizing"
## [172] "overcompensating" "overcomplicating" "overconsumptions"
## [175] "overenthusiastic" "overexaggerating" "overexaggeration"
## [178] "overrepresenting" "overspecializing" "parliamentarians"
## [181] "perfectibilities" "permissivenesses" "perpendicularity"
## [184] "personifications" "persuasivenesses" "phosphorescences"
## [187] "phosphorescently" "photosynthesises" "photosynthesized"
## [190] "photosynthesizes" "possessivenesses" "postadolescences"
## [193] "practicabilities" "precancellations" "precariousnesses"
## [196] "preimmunizations" "prekindergartens" "prenotifications"
## [199] "preregistrations" "prerevolutionary" "prestidigitation"
## [202] "procrastinations" "productivenesses" "professionalized"
## [205] "professionalizes" "prognostications" "psychotherapists"
## [208] "rationalizations" "reasonablenesses" "rebelliousnesses"
## [211] "recertifications" "reclassification" "reconsiderations"
## [214] "reestablishments" "reinvestigations" "relentlessnesses"
## [217] "remarkablenesses" "remunerativeness" "repetitivenesses"
## [220] "representatively" "respectabilities" "respectfulnesses"
## [223] "responsibilities" "responsivenesses" "retrievabilities"
## [226] "ridiculousnesses" "sentimentalizing" "simultaneousness"
## [229] "standardizations" "subconsciousness" "suggestivenesses"
## [232] "superenthusiasms" "superficialities" "supergovernments"
## [235] "superintelligent" "superintendences" "superpatriotisms"
## [238] "superspecialists" "susceptibilities" "synchronizations"
## [241] "thermometrically" "thermostatically" "thoughtfulnesses"
## [244] "thrombocytopenia" "thrombophlebitis" "totalitarianisms"
## [247] "transfigurations" "transplantations" "uncharacteristic"
## [250] "unconstitutional" "unconventionally" "undernourishment"
## [253] "undersecretaries" "unfaithfulnesses" "ungratefulnesses"
## [256] "unpleasantnesses" "unscrupulousness" "villianousnesses"
## [259] "vindictivenesses" "voluptuousnesses" "weightlessnesses"
```

```r
words[grep("^..................$", words)]
```

```
##  [1] "absentmindednesses" "adventitiousnesses" "antiadministration"
##  [4] "antidiscrimination" "apprehensivenesses" "biodegradabilities"
##  [7] "bloodthirstinesses" "cantankerousnesses" "characteristically"
## [10] "chemotherapeutical" "counteraccusations" "counteraggressions"
## [13] "counterpropagation" "counterretaliation" "counterrevolutions"
## [16] "countersuggestions" "electrocardiograms" "electrocardiograph"
## [19] "feeblemindednesses" "heterogenousnesses" "hydroelectricities"
## [22] "hyperconscientious" "hypernationalistic" "hypersensitiveness"
## [25] "hypersensitivities" "indispensabilities" "industrializations"
## [28] "interinstitutional" "internationalizing" "interrelatednesses"
## [31] "irresponsibilities" "lightheartednesses" "misinterpretations"
## [34] "misrepresentations" "nondiscriminations" "obstreperousnesses"
## [37] "perpendicularities" "postfertilizations" "rehospitalizations"
## [40] "remunerativenesses" "representativeness" "simultaneousnesses"
## [43] "straightforwardest" "subclassifications" "subconsciousnesses"
## [46] "superintellectuals" "superintelligences" "unscrupulousnesses"
```

```r
words[grep("^...................$", words)]
```

```
##  [1] "anticonservationist" "comprehensivenesses" "counterdemonstrator"
##  [4] "counterinflationary" "counterpropagations" "counterretaliations"
##  [7] "disinterestednesses" "electrocardiographs" "extraconstitutional"
## [10] "hyperaggressiveness" "inappropriatenesses" "inconsideratenesses"
## [13] "interdenominational" "irreconcilabilities" "miscellaneousnesses"
## [16] "multidenominational"
```

```r
words[grep("^....................$", words)]
```

```
## [1] "counterdemonstration" "counterdemonstrators" "hypersensitivenesses"
## [4] "microminiaturization" "representativenesses"
```

```r
words[grep("^.....................$", words)]
```

```
## [1] "counterdemonstrations" "hyperaggressivenesses" "microminiaturizations"
```


```r
# The number of words starting with 'a' is:
length(words[grep("^a...", words)])
```

```
## [1] 6478
```

```r
# The number of words starting with 'b' is:
length(words[grep("^b...", words)])
```

```
## [1] 6796
```

```r
# The number of words starting with 'c' is:
length(words[grep("^c...", words)])
```

```
## [1] 10352
```

```r
# The number of words starting with 'd' is:
length(words[grep("^d...", words)])
```

```
## [1] 6385
```

```r
# The number of words starting with 'e' is:
length(words[grep("^e...", words)])
```

```
## [1] 4317
```

```r
# The number of words starting with 'f' is:
length(words[grep("^f...", words)])
```

```
## [1] 4890
```

```r
# The number of words starting with 'g' is:
length(words[grep("^g...", words)])
```

```
## [1] 3907
```

```r
# The full list of words with a “q” but no “u” following is:
words[grep("q[^u]...", words)]
```

```
## [1] "buqshas" "qaids"   "qindar"  "qindars" "qintar"  "qintars" "qiviut" 
## [8] "qiviuts" "qophs"
```

```r
# crossword helper

crosswardhelper <- function(word, definition) {
    word <- c("hungry", "thristy", "sleepy")
    definition <- c("in need of food", "in need of drink", "in need of rest")
    matched <- grep(word, definition)
    return(names(definition)[matched])
}
```

```r
# crosswordhelper test
crosswardhelper(hungry)
```

```
## Warning: argument 'pattern' has length > 1 and only the first element will
## be used
```

```
## NULL
```


```

```

```

```


