# Model detekcji szkód w młodnikach i uprawach leśnych

Model **ONNX** do detekcji szkód w młodnikach i uprawach leśnych spowodowanych przez ssaki. Został przygotowany do użycia we wtyczce **Deepness** w **QGIS**.

Model oparto na architekturze **YOLO11s**. Dane treningowe pochodziły ze zobrazowań **RGB** wykonanych z **BSP** o oryginalnej rozdzielczości **2,5 cm**. Na potrzeby trenowania i generowania modelu rozdzielczość zmniejszono do **10 cm**.

## Parametry

| Parametr | Wartość |
|---|---|
| Format | ONNX |
| Typ modelu | Detector |
| Architektura | YOLO11s |
| Klasa detekcji | `szkoda` |
| Tile size | 640 px |
| Tiles overlap | 15% |
| Dane wejściowe | RGB |
| Liczba oznaczonych obiektów treningowych | 460 |
| Rozdzielczość danych użytych do modelu | 10 cm |
| Oryginalna rozdzielczość zobrazowań BSP | 2,5 cm |

## Narzędzia

Model przygotowano z użyciem:

- **QGIS**
- **Deepness**
- **Roboflow**
- **Ultralytics**

Proces opracowano na podstawie tutoriala:  
https://youtu.be/HIsheKG-lE4?si=y2kkUdgx6CLOGhUD

## Licencja

Rekomendowana licencja: **GNU Affero General Public License v3.0**.

Licencja została dobrana ze względu na wykorzystanie ekosystemu **Ultralytics YOLO**. W przypadku użycia komercyjnego należy zweryfikować aktualne warunki licencji Ultralytics.

## Uwagi

Model został wytrenowany na ograniczonym zbiorze danych, dlatego wyniki detekcji powinny być weryfikowane przed wykorzystaniem w analizach operacyjnych.
