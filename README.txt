Kuziora Karol 95468
01.12.2024r.

Quota ograniczyło dostępne zasoby przestrzeni nazw zad1 do 2 CPU, 1.5Gi pamięci oraz 10 podów. Deployment php-apache przydzielaja 250m CPU i 250Mi pamięci na pod przy maksymalnym obciążeniu. Pozwala to na uruchomienie do 6 replik (ograniczenie pamięci) co zostalo uwzględnione w konfiguracji HorizontalPodAutoscaler.
Nie byłem w stanie obciązyć aplikacji do momentu uruchomienia kolejnych deploymentów. Te obserwowałem wykorzystujac polecenia:
kubectl get hpa php-apache-hpa -n zad1 -w
oraz
kubectl get deployments php-apache -n zad1 -w