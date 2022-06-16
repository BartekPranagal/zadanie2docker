Tworzymy plik docker-stack.yml. Uzupełniam go danymi z pliku compose oraz dodaje ograniczenia do pamięci oraz procesora w sekcji deploy. Odpowiednio konfiguruje repliki, config oraz ilość zasobów. 

Aby stworzyć swarma używam polecenie

docker swarm init

Następnie aby dodać serwisy używam 

docker stack deploy -c docker-stack.yml zad2

Aby sprawdzić działanie serwisow nalezy uzyc polecenie 

docker service ls


Dowód: 
Barteks-MBP:Archive bartekpranagal$ docker service ls
ID             NAME            MODE         REPLICAS   IMAGE                PORTS
25c977gkzj9m   s_apache        replicated   2/2        httpd:latest         *:80->80/tcp
lahtlitk3swv   s_php           replicated   2/2        php:8.0-apache       *:88->80/tcp
lczju72y8j7y   s_phpmyadmin    replicated   1/1        phpmyadmin:latest    *:8800->80/tcp
mwa7yoz6dkdy   zad2_api        replicated   1/1        pranus/zad2:server   
wn85lvdg4e91   zad2_client     replicated   2/2        pranus/zad2:client   
u3h2i6hlaglt   zad2_nginx      replicated   2/2        pranus/zad2:nginx    *:3050->80/tcp
m5b3fgjlzpc4   zad2_postgres   replicated   1/1        postgres:latest      
b5kr3in6yu81   zad2_redis      replicated   1/1        redis:latest         
vwh5m8w70z9c   zad2_worker     replicated   1/1        pranus/zad2:worker   