Po umieszczeniu obrazów na zdalnym repozytorium, w pliku docker-compose.yml zastępuje sekcje build przez image. W ten sposób będziemy korzystać ze zbudowanych już zdalnie obrazów. Wpisując poniższa komenda zostanie uruchomiony nasz compose, korzystający już z gotowych obrazów.

docker compose up --build

Dowód: 
Barteks-MBP:Archive bartekpranagal$ docker compose up --build
[+] Running 6/6
 ⠿ Container archive-api-1       Recreated                                                                                                                                                                 0.2s
 ⠿ Container archive-worker-1    Recreated                                                                                                                                                                 0.2s
 ⠿ Container archive-client-1    Recreated                                                                                                                                                                 0.2s
 ⠿ Container archive-postgres-1  Recreated                                                                                                                                                                 0.2s
 ⠿ Container archive-redis-1     Recreated                                                                                                                                                                 0.2s
 ⠿ Container archive-nginx-1     Recreated    