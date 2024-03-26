
<img width="450" alt="f" src="https://github.com/drunken-boat/CTF-WriteUps/assets/80751447/5a222d52-4ea3-4a15-84c8-cf11f4ec99b3">

1. `cmd+i` check metadata -> nothing found
2. considering the challenge name, it's the flag language! -> [International Code of Signals](https://en.wikipedia.org/wiki/International_Code_of_Signals)

   > The International Code of Signals (INTERCO) is an international system of signals and codes for use by vessels to communicate important messages regarding safety of navigation and related matters.
   > Signals can be sent by flaghoist, signal lamp ("blinker"), flag semaphore, radiotelegraphy, and radiotelephony.
   > The International Code is the most recent evolution of a wide variety of maritime flag signalling systems.

3. decode with this chart, and we get letter below, we get "wasittoo??sytof?nd"
  <img width="450" alt="f" src="https://github.com/drunken-boat/CTF-WriteUps/assets/80751447/ed2941dc-4ca1-4cc1-bd0d-bbad91b259a4">
  <img width="450" alt="f" src="https://github.com/drunken-boat/CTF-WriteUps/assets/80751447/1ce23d84-fca6-449d-a3c4-46964b224ebc">

4. the first question mark's according flag is `2nd substitute` -> is the same as the second letter, "a", the first question mark's according flag is `3rd substitute` -> is the same as the second letter, "s"

  now we get: "wasittooeasytof?nd" -> check the flag format, it should be "was_it_too_easy_to_find" or "was_it_too_easy_to_f1nd"

final flag: shaktictf{was_it_too_easy_to_find}

Special thanks: @GANGTONGH
