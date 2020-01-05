# Notify
Notify is OCR based remainder application for Android. Notify can scan posters and convert them into a remainder without human effort. Notify reminds before the event and provides navigation to the event location.

There are two ways to create a remainder. One way is to scan the poster and another way is to scan the given QR.

## Scan Poster
The image of the posters is captured by using the camera. The saved image will be given as an input to the OCR engine. The OCR engine will convert the printed text in the image to strings. Subsequently, the desired information will be extracted from the strings using an NLP library. The target information will be date, place and time. Using this information, a reminder will be created

## Scan QR
Yet another way for information extraction is scanning QR Codes in
posters. Generally, digital posters tend to have a QR Code printed on it. This method will be useful in such a case. The google play service's vision API can be used to scan QR codes. The code capture package will automatically launch the camera to scan the code. After decoding the
text from the code, the same NLP library will be used to filter only
the required information. Since the scanning API comes handy with google play service, there is no need for any external library in this method.

