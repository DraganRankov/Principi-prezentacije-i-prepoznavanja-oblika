# Principi-prezentacije-i-prepoznavanja-oblika
Uvod:
Detekcija godina,pola i emocija iz vizuelnih podataka, kao što su slike, ima značajne primene u analizi korisničkog iskustva kao i analizi tržišta. Upotreba dubokih neuronskih mreža, posebno konvolucijskih neuronskih mreža (CNN), omogućava automatsku i preciznu klasifikaciju godina, pola i emocija.

Priprema Podataka:

Učitavanje i dekomprimiranje slika iz odgovarajućih zip arhiva.
Primer: Klasifikacija emocija: Emocije su označene kao "happy", "neutral" i "angry". One su preslikane u numeričke labele (0, 1, 2) pomoću funkcije class_labels_reassign.
Učitavanje Podataka:

Učitavanje podataka za trening i testiranje iz CSV datoteka koje sadrže informacije o emocijama za svaku sliku.
Slike su konvertovane u grayscale i normalizovane na dimenzije 100x100.
Izgradnja Modela:

Definisanje arhitekture CNN modela.
Konvolucijski slojevi (conv1-conv4) sa postupnim povećanjem broja filtera i upotrebom dropout slojeva radi smanjenja preprilagođavanja.
Potpuno povezani slojevi (dense_1 i output) za klasifikaciju sa odgovarajućim aktivacijama.
Kompilacija i Obuka Modela:

Kompilacija modela sa Adam optimizatorom i sparse categorical cross-entropy gubitkom.
Obuka modela koristeći podatke za trening, sa validacijom koristeći test podatke.
Upotreba ModelCheckpoint povratnog poziva za čuvanje najboljeg modela na osnovu gubitka.
Evaluacija Modela:

Evaluacija modela na test podacima kako bi se procenili gubitak i tačnost.
Prikaz rezultata evaluacije.
Zaključak:
Implementacija detekcije godina, pola i emocija korišćenjem konvolucijskih neuronskih mreža pruža efikasan način za automatsku klasifikaciju godina, pola i emocija iz slika. Duboko učenje, posebno CNN-ovi, omogućava modelima da nauče raw features direktno iz podataka, što dovodi do preciznih rezultata u analizi godina, pola i emocija.

Ovaj rad koristi TensorFlow i Keras biblioteke kako bi implementirao duboki model za detekciju godina, pola i emocija. Opisani su koraci poput pripreme podataka, izgradnje arhitekture modela, obuke i evaluacije, pružajući jasnu sliku o procesu detekcije godina, pola i emocija iz slika.
