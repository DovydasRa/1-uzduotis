https://leetcode.com/problems/reformat-date/



		PROBLEMA.

Įvedus datą tokiu formatu: 20th Oct 2052. Ją pakeisti tokiu formatu: 2052-10-20
Metų ribos nuo 1900 iki 2100.



		ANALIZĖ.

Įvestis yra diena (20th formatu), mėnuo (Oct formatu) ir metai (2052 formatu).
Dienos ir mėnesio kintamųjų išsaugojimui naudosime string, kadangi tie du kintamieji yra tekstinio formato.
Duomenys, kurie bus naudojami:

	1. Diena (Pvz.: 20th).
	2. Mėnuo (Pvz.: Oct).
	3. Metai (Pvz.: 2052).



		FORMULĖS.

	1. d = i + 1   (Cikle for tikrinu, kuri įvestis atitinka masyvę esantį elementą ir pridedu vienetą. Taip nustatau, kelintas tai skaičius masyve. Jis atitinka įvestos dienos skaičių.)

	2. m = i + 1   (Cikle for tikrinu, kuri įvestis atitinka masyvę esantį elementą ir pridedu vienetą. Taip nustatau, kelintas tai skaičius masyve. Jis atitinka įvesto mėnesio skaičių.)

	3. klaidamenuo = klaidamenuo + 1   (Cikle for tikrinu ar įvestas mėnuo yra mėnesių masyve. Jei ne, pridedu vienetą ir paskui tikrinu ar galutinis rezultatas yra 12. Jei taip, tai įvesto mėnesio masyve nėra arba jis įvestas su klaida.)

	4. klaidadiena = klaidadiena + 1   (Cikle for tikrinu ar įvesta diena yra dienų masyve. Jei ne, pridedu vienetą ir paskui tikrinu ar galutinis rezultatas yra 31. Jei taip, tai įvestos dienos masyve nėra arba ji įvesta su klaida.)



		ALGORITMO KONSTRAVIMAS/PROJEKTAVIMAS.

	1. Sukuriu dienų masyvą.
	2. Sukuriu mėnesių masyvą.
	3. Prašau dienos įvesties į programą.
	4. Tikrinu ar diena yra masyve.
	5. Prašau mėnesio įvesties į programą.
	6. Tikrinu ar mėnuo yra masyve.
	7. Prašau metų įvesties į programą.
	8. Tikrinu ar metai patenka į nustatytas ribas.
	9. Naudodamas ciklą nustatau, kuri įvesta diena atitinką, kurią dieną masyve.
	10. Naudodamas ciklą nustatau, kuris įvestas mėnuo atitinką, kurį mėnesį masyve.
	11. Jei viskas gerai įvesta, tai ekrane parodo norimą datos formatą: YYYY-MM-DD
