# WriteUp for P05 puzzle

## Stage1

* using P05 to reveal the pic, got `TIBERIVS CLAVDIVS CAESAR says "qccyb://pryqh.lxv/prob/vrlqjnu-sjltbxw-vxxwfjut-bSb1Jp97g0VE2"`
* see qccyb, decrypt ROT9 for [A-Za-z0-9], got [https://giphy.com/gifs/michael-jackson-moonwalk-sJs1Ag97x0MV2](https://giphy.com/gifs/michael-jackson-moonwalk-sJs1Ag97x0MV2)
* got a outlinked moonwalk gif? No trick in binary viewer, may mean reversed?

## Stage2

* Just Stegsolve it! And find spical points in both head and end, surely it's about **reverse**
* fully run P05 without stop at `\0`, got `TIBERIVS CLAVDIVS CAESAR says "qccyb://pryqh.lxv/prob/vrlqjnu-sjltbxw-vxxwfjut-bSb1Jp97g0VE2"零Dpohsbuvmbujpot-!qmfbtf!fnbjm!ccfsu{)bu*xjtd/fev!xjui!uif!tvckfdu!mjof!#4412#!up!gjojti!uijt!dibmmfohf空|k9l9aDw8ncoDobmq "esh2tQ ?rwe9t0fla! rr~emtyc^a!rta;h"cH ]h9coaee$ NmLoRr.fc XeVnoo[ }s5u7n'iXMgorF paeL零dne eht reven si dne ehT`. Here I use Chinese char 零 and 空 to mark out the '\0' and the continuous non-ASCII chars(by a few changed lines in P05).

## Stage3

* reversed the last part (after 空 and before 零), got `Leap FrogMXi\'n7u5s} [oonVeX cf.rRoLmN $eeaoc9h] Hc"h;atr!a^cytme~rr !alf0t9ewr? Qt2hse" qmboDocn8wDa9l9k|`, Leap frog, just try to jump it?
* `print(''.join(list(reversed(lastStr)))[1::2])`(in python)
* got `epFoMinus one from each character after the moonwalk`
* obviously do as is said, `print(''.join([chr(ord(x)-1) for x in secStr]))`, got `Congratulations, please email [Censored](at)wisc.edu with the subject line "[Censored]" to finish this challenge`

## Contact

* Hanyuan Wu (whyere), hwu384@wisc.edu
* Transferred from Huazhonog University of Science and Technology(or HUST)
* One of the formers of L3H Sec CTF Team in HUST, second prize in 19th Chinese national College Student Information Security Contest (CISCN National FINAL), and second place in CISCN Regional FINAL
* Willing to contact any existing CTF group or anyone who is interested in CTF, if no existing one, I'll try to form one in UW

