```mermaid
flowchart TD
start@{shape: circle, label: "Mulai"}
inputJari@{ shape: lean-r, label: "input: r"}
decisionPi@{ shape: diamond, label: "r % 7 == 0" }
decisionHitung@{ shape: diamond, label: "Hitung Luas atau Keliling" }
oPiTrue@{ shape: lean-r, label: "pi = 22/7"}
oPiFalse@{ shape: lean-r, label: "pi = 3.14"}
luasLingkaran@{ shape: rect, label: "luasLingkarang = pi * r * r" }
kelilingLingkaran@{ shape: rect, label: "kelilingLingkaran = 2 * pi * r" }
outKeliling@{ shape: lean-r, label: "output: kelilingLingkaran"}
outLuas@{ shape: lean-r, label: "output: luasLingkaran"}
stop@{shape: dbl-circ, label: "Selesai"}

start-->inputJari
inputJari-->decisionPi
decisionPi--True-->oPiTrue
decisionPi--False-->oPiFalse
oPiTrue-->decisionHitung
decisionHitung--Luas Lingkaran-->luasLingkaran
decisionHitung--Keliling Lingkaran-->kelilingLingkaran
kelilingLingkaran-->outKeliling
outKeliling-->stop
luasLingkaran-->outLuas
outLuas-->stop
oPiFalse-->decisionHitung
decisionHitung--Luas Lingkaran-->luasLingkaran
decisionHitung--Keliling Lingkaran-->kelilingLingkaran
kelilingLingkaran-->outKeliling
outKeliling-->stop
luasLingkaran-->outLuas
outLuas-->stop
```