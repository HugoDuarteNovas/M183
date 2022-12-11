# Lern-Bericht
Hugo Duarte Novas

## Einleitung

Bei dem Modul M183 ist es darum gegangen, eine unsichere Web-Applikation sicher zu machen. Dabei sollten wir Sicherheitslücken finden und diese beheben.
Bei diesem Auftrag ging es darum, wie ein Filter implementiert wird.

## Was habe ich gelernt?

In diesem Projekt habe ich gelernt, wie man eine Filter-Klasse in JSF erstellt.

## Beschreibung

Hier sehen Sie in Bild von meinem Code, dieses st auch kommentiert. 
Somit sollte die Problemstellung von diesem Auftrag gelöst sein.

```java
@inject

Login Controller loginController;

// Hier wird zuerst eine void-Variable mit mehreren Attributes erstellt

public void doFilter(ServletRequest request, ServletResponse response,
FilterChain chain) throws IOException, ServletException {
  
final HttpServletRequest httpRequest = (HttpServletRequest) request;
  
final HttpServletResponse httpResponse = (HttpServletResponse) response;
 
// Mit diesem String wird die URL "versteckt"
  
final String loginURL = httpRequest.getContextPath() + "/index.xhtml";
  
// Hier wird der Filter erstellt 
  
if (loginController.getUser() == null) {
	httpResponse.sendRedirect(loginURL);
 } 
	chain.doFilter(request, response);
}
```

Hiermit noch mein Gif (Achten Sie auf die Uhrzeiten):

![alt text]( https://github.com/HugoDuarteNovas/M183/blob/main/filter.gif "Hugo's GIF")

## Verifikation

Bei dem GIF kann man sehen, dass ich den Aufrag erfüllt habe.

# Reflektion zum Arbeitsprozess

Gut lief es, den Auftrag zu lösen und die Recherche dazu.

Was nicht so gut lief, ist das Einbinden von einem .gif auf GitHub.

**VBV**: Ich soll mehr Programmieren und nicht nur auf der Theorie achten.
