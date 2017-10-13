# raupjc-hw0
0. assignment for C# skill

# Pitanje 1:
Kod sadržaja Bin/Debug foldera primjeæujem da je meðuostalim kreiran i novij asemblij (biblioteka/.dll file) - ClassLibrary1.dll
Nakon micanja .dll filea iz foldera i pokretanja .exe-a dolazi do UnhandledException i aplikacija se ruši zato što
u main metodi klase Program konzolne aplikacije pozivamo metodu PrintHelloWorld() 
koja je definirana i deklarirana u asembliju ClassLibrary1.dll 
te nakon što smo obrisali taj asemblij ne možemo mu pristupiti i samim time izvršiti navedenu metodu.
Poslao bih ClassLibrary1.dll i ConsoleApp1.exe

# Pitanje 2:
Konzolna aplikacija je koristila staru PrintHelloWorld() metodu, tj. staru verziju class library asemblija 
jer nakon mijenjanja stringa u ClassLibrary1 biblioteci nismo ju preveli i stvorili novi/"updateali" .dll asemblij koji
sadrži novu metodu sa novim stringom koju æe pozvati konzolna aplikacija.

# Pitanje 3:
Nakon brisanja NodaTime direktorija, build proces se normalno izvrši samo što Visual Studio registrira
da neki paket o kojem projekt ovisi fali te ga restorea, odnosno, ponovo dohvaæa sa NuGet servera. U ovom sluèaju je to NodaTime.
U packages direktorij je ponovo nastao NodaTime direktorij.