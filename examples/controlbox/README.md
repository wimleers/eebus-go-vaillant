# Vaillant Leistungsreduzierung gemäß § 14a EnWG
Dieses Projekt demonstriert die Leistungsreduzierung von Vaillant Wärmepumpen gemäß § 14a EnWG. Vaillant implementiert dafür die EEBUS LPC (Limit Power Consumption) Schnittstelle.

Für das Auslösen des EEBUS LPC Kommandos wird ein FNN-Steuerbox-Simulator verwendet, der auf der plattformunabhängigen eebus-go Implementierung basiert und somit auf Windows, Linux und Mac Computern lauffähig ist.

Für Windows liegen Batch-Skripte für die Installation sowie Ausführung bei. Analog dazu sind in dieser Anleitung die plattformunabhängigen Kommandozeilen-Anweisungen beigefügt.
## Voraussetzungen
### Vaillant Wärmepumpensystem
* Wärmepumpe: aroTHERM split/plus/split plus, versoTHERM, recoCOMPACT
* FW: 0351.09.01 oder neuer
* Internetmodul: VR 920/921/940f
* Steuerung: sensoCOMFORT VRC 720, multiMATIC VRC 700f/4 u. 700/6
* App: myVAILLANT

### FNN-Steuerbox-Simulator
* [Go](https://go.dev/dl/)
* [Node.js](https://nodejs.org/en/download)
## FNN-Steuerbox-Simulator
### Installation
```
cb-eebus-firstrun.bat
```
bzw.
```
go run . 4712
```

Ein Zertifikat/Schlüssel-Paar für die sichere Verbindung wird erstellt.

### Starten
```
cb-eebus-run.bat
```
bzw.
```
go run . 4712 cb.cert cb.key
```

### Verbinden mit Vaillant
![image](https://github.com/user-attachments/assets/a48b12f2-2291-4149-b1a5-2bd977f684f7) ![image](https://github.com/user-attachments/assets/c2890de7-fc15-43c1-b690-469acae7b29b)


## Web-Frontend
### Installation
```
cb-vite-install.bat
```
bzw.
```
npm install
```

### Server starten
```
cb-vite-run.bat
```
bzw.
```
npm run dev
```

### Web-Interface aufrufen
```
cb-webui.url
```
bzw.
```
http://localhost:7081/
```
## EEBUS LPC & MPC
![image](https://github.com/user-attachments/assets/3c66d4f5-531b-4cc2-a3b1-a81ff592d9eb) ![image](https://github.com/user-attachments/assets/e76e8ace-fd90-41c1-b566-c9822afe9149)
