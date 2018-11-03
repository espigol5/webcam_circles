# webcam_circles
Circle detection from online webcam images


# Hough Transform:

És una tècnica per distingir figures amb una forma particular en una imatge, com serien cercles, el·lipses, línies, etc. Les quals poden tenir una representació matemàtica.

Canvi de paràmetres:

circles: en aquest cas la figura matemàtica que es volia detectar eren cercles, per això es genera un vector de detector de cercles (cv.CV_32FC3)

GAUSSIAN_BLUR_SIZE: ens determina la mida de la matriu gaussiana que gestiona el soroll en la imatge. Com més elevat menys sensibilitat el soroll que permet evitar detecció de formes errònies.

CANNY_EDGE_TH: és un paràmetre que detcte les vores dels cossos o objectes a partir d'un valor llindar o threshold que determina l'usuari. Com més baix sigui el valor més poc precís és la detecció de vores i fa que apareguin cercles no existents. En el cas de visualitzar només el factor "Canny", es visualitzarà un fons negre amb totes les corbes que detecta la funció en blanc. Variant aquest paràmetre veiem com amb valor més elevat la detecció de vores és més proper a la realitat.

HOUGH_ACCUM_RESOLUTION: Amb aquesta comanda es varia la resolució de la detecció de cercles. Aquest valor és bastant fix ja que amb un valor diferent de 2 la càmera no detecta cap cercle.

MIN_CIRCLE_DIST: Aquest valor marca la distància mínima entre els centres dels cercles detectats. D'aquesta manera amb un valor baix, els cercles es veuràn superposats, mentre que amb un valor elevat veurem com la distància entre ells augmenta.

HOUGH_ACCUM_TH: és el llindar d'acumulador dels centres del cercles en la fase de detecció. Com més petit sigui aquest llindar, més cercles falsos es poden detectar. 

MIN_RADIUS: és el valor mínim de radi dels cercles que detectarà el programa.

MAX_RADIUS: és el valor màxim de radi dels cercles que detectarà el programa.

Fonts: 

https://docs.opencv.org/2.4/modules/imgproc/doc/feature_detection.html

https://www.pyimagesearch.com/2014/07/21/detecting-circles-images-using-opencv-hough-circles/
