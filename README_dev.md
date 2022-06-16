Po ściągnięciu paczki zip udostępnionej na kursie, rozpakowuje ja oraz w pliku docker-compose.dev.yml dodaje tag image aby zbudować i wypchnąć obrazy. Tworze odpowiednie repozytorium na dockerhub aby każdy obraz miał swoje miejsce.

Przykład dodanego image do obrazu znajduje się powyżej.

Aby zbudować obrazy należy wpisać komendę:

docker compose -f docker-compose.dev.yml build

Następnie aby je wypchnąć do repozytorium:

docker compose -f docker-compose.dev.yml push

Aby je uruchomić: 

docker compose -f docker-compose.dev.yml up

Dowód:

Barteks-MBP:Archive bartekpranagal$ docker compose -f docker-compose.dev.yml push
[+] Running 2/2
 ⠿ postgres Skipped                                                                                                                                                                                        0.0s
 ⠿ redis Skipped                                                                                                                                                                                           0.0s
 ⠋ Pushing nginx: fba72aab167a Preparing                                                                                                                                                                   0.1s
 ⠋ Pushing nginx: 9a71b3622c62 Preparing                                                                                                                                                                   0.1s
[+] Running 2/25: c692319770ad Preparing    

Log jest za długi aby wkleić cały. 