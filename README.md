# raupjc-hw0
0. assignment for C# skill

# Pitanje 1:
Kod sadr�aja Bin/Debug foldera primje�ujem da je me�uostalim kreiran i novij asemblij (biblioteka/.dll file) - ClassLibrary1.dll
Nakon micanja .dll filea iz foldera i pokretanja .exe-a dolazi do UnhandledException i aplikacija se ru�i zato �to
u main metodi klase Program konzolne aplikacije pozivamo metodu PrintHelloWorld() 
koja je definirana i deklarirana u asembliju ClassLibrary1.dll 
te nakon �to smo obrisali taj asemblij ne mo�emo mu pristupiti i samim time izvr�iti navedenu metodu.
Poslao bih ClassLibrary1.dll i ConsoleApp1.exe

# Pitanje 2:
Konzolna aplikacija je koristila staru PrintHelloWorld() metodu, tj. staru verziju class library asemblija 
jer nakon mijenjanja stringa u ClassLibrary1 biblioteci nismo ju preveli i stvorili novi/"updateali" .dll asemblij koji
sadr�i novu metodu sa novim stringom koju �e pozvati konzolna aplikacija.

# Pitanje 3:
Nakon brisanja NodaTime direktorija, build proces se normalno izvr�i samo �to Visual Studio registrira
da neki paket o kojem projekt ovisi fali te ga restorea, odnosno, ponovo dohva�a sa NuGet servera. U ovom slu�aju je to NodaTime.
U packages direktorij je ponovo nastao NodaTime direktorij.