# Cenu_Salīdzināšanas skripts
Šis Python skripts ir izveidots, lai automātiski salīdzinātu Apple iPhone 16 Pro Max modeļa cenas trīs populārākajos Latvijas interneta veikalos – 1a.lv, RDveikals.lv un 220.lv. Skripta mērķis ir palīdzēt lietotājam ātri un efektīvi iegūt informāciju par konkrētā telefona modeļa cenu dažādos veikalos, atrast lētāko variantu katrā no tiem un saglabāt šo informāciju pārskatāmā Excel failā, kurā dati ir viegli saprotami un salīdzināmi.
# Bibliotēkas
Skripta darbības pamatā ir vairākas bibliotēkas. Galvenā ir Selenium WebDriver, kas ļauj atvērt mājaslapas automātiski, meklēt tajās produktus un izgūt informāciju no konkrētiem HTML elementiem, piemēram, cenu blokiem un preču nosaukumiem. Papildus tiek izmantota bibliotēka OpenPyXL, kas nodrošina iespēju strādāt ar Excel failiem – veidot jaunas darblapas, ievietot datus šūnās un saglabāt gala rezultātu kā .xlsx failu. Tāpat tiek izmantota Python iebūvētā re bibliotēka jeb regulārās izteiksmes, kas palīdz izfiltrēt un pārveidot cenas tekstā, noņemot liekus simbolus un iegūstot skaitliskas vērtības. time bibliotēka tiek izmantota, lai ievietotu nelielas pauzes starp dažādām darbībām, piemēram, lapas ielādi vai klikšķiem, nodrošinot, ka skripts darbojas korekti arī gadījumos, kad lapas ielādes laiks ir atšķirīgs. Papildus arī tika izmantotas Python standarta bibliotēkas re un time efektīvakam darbam.
# Skripta darbība
Skripts vispirms sagatavo Excel failu ar divām darblapām. Viena lapa satur visu informāciju par visiem atrastajiem modeļiem, kas ietver katra produkta pilno nosaukumu un tā cenu, kā arī, ja pieejams, arī cenu bez atlaides. Otrā lapa ir kopsavilkums, kurā redzami tikai lētākie modeļi katrā no veikaliem, tādējādi ļaujot lietotājam nekavējoties redzēt, kur konkrētais modelis ir nopērkams visizdevīgāk.

Pēc tam, kad Excel fails ir sagatavots, skripts pa vienam apmeklē katru no norādītajiem interneta veikaliem. Katram veikalam ir izveidots savs funkciju bloks, kas atbild par tā apstrādi. Skripts ielādē veikala mājaslapu, aizver vai pieņem sīkdatņu logus, ja tādi parādās, meklēšanas laukā ievada produkta nosaukumu (iPhone 16 Pro Max) un apstrādā atvērto rezultātu lapu. No šīs lapas tiek izgūta informācija par visiem atrastajiem produktiem, kuru nosaukumos ir iekļauts meklētais modelis, kā arī tiek nolasītas cenas – gan ar atlaidi, gan bez, ja tāda informācija ir pieejama. Skripts ir izveidots tā, lai tas atpazītu, vai produkts tiek piedāvāts ar akciju vai par standarta cenu, un attiecīgi saglabātu abu veidu datus.

Kad dati no visiem veikaliem ir apkopoti, tie tiek saglabāti Excel failā. "Visi dati" lapā tiek ievietoti visi atrastie modeļi ar pilnu nosaukumu un attiecīgo cenu. Ja cena ar atlaidi un bez atlaides atšķiras, tiek parādīta arī sākotnējā cena. Šī lapa sniedz pilnīgu pārskatu par visām pieejamajām iespējām. Otra lapa – “Cenu salīdzinājums” – satur tikai trīs ierakstus, pa vienam no katra veikala, kur ir norādīts lētākais pieejamais Apple iPhone 16 Pro Max modelis, tā cena un no kura interneta veikala tas ir.

Svarīgi pieminēt, ka skripts ir izveidots konkrētam modelim – “Apple iPhone 16 Pro Max” – un konkrētām veikalu lapu struktūrām. Ja veikalu dizains mainīsies (piemēram, tiks mainīti HTML elementi, klases vai ID), tad skripts var pārstāt pareizi darboties, un tajā būs jāveic izmaiņas, lai pielāgotu selektorus jaunajai struktūrai. Šobrīd tas darbojas stabili ar esošajām veikalu versijām.
# Ppildus
Noslēgumā jāuzsver, ka šo skriptu iespējams uzlabot un paplašināt. Piemēram, nākotnē tam var pievienot lietotāja interfeisu, lai cilvēks varētu ievadīt meklējamo modeli pats, nevis tas būtu fiksēts kodā. Tāpat to var paplašināt uz citiem produktiem vai veikalu sarakstu paplašināt ar vēl citiem populāriem tirgotājiem. Ir iespējams arī automatizēt šī skripta izpildi, piemēram, iestatot to darboties noteiktā laikā katru dienu, lai vienmēr būtu pieejama aktuālā cena.
















