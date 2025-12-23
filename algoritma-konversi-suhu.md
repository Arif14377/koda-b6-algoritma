# Algoritma Konversi Suhu
## Deskriptif
1. Mulai
2. Masukkan nilai suhu celcius dengan nilai desimal
3. Konversi suhu celcius ke suhu Fahrenheit dengan mengkalikan suhu celcius dengan 1.8, lalu tambahkan hasilnya dengan 32.0
4. Konversi suhu celcius ke suhu Reamur dengan mengkalikan suhu celcius dengan 0.8
5. Konversi suhu celcius ke suhu Kelvin dengan menambahkan suhu celcius dengan 273.15

## Flowchart
```mermaid
flowchart TD
start@{shape: circle, label: "Mulai"}
input@{ shape: lean-r, label: "input: suhuCelciusFloat"}
toFahrenheit@{ shape: rect, label: "CtoFahrenheit = (suhuCelciusFloat * 1.8) + 32.0"}
toReamur@{ shape: rect, label: "CtoReamur = suhuCelciusFloat * 0.8"}
toKelvin@{ shape: rect, label: "CtoKelvin = suhuCelciusFloat + 273.15"}
outputFahrenheit@{ shape: lean-r, label: "output: toFahrenheit"}
outputFahrenheit@{ shape: lean-r, label: "output: CtoFahrenheit"}
outputReamur@{ shape: lean-r, label: "output: CtoReamur"}
outputKelvin@{ shape: lean-r, label: "output: CtoKelvin"}
stop@{shape: dbl-circ, label: "Selesai"}


start-->input
input-->toFahrenheit
input-->toReamur
input-->toKelvin
toFahrenheit-->outputFahrenheit
toReamur-->outputReamur
toKelvin-->outputKelvin

outputFahrenheit-->stop
outputReamur-->stop
outputKelvin-->stop
```