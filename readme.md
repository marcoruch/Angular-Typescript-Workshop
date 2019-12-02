<h1>Angular Typescript Workshop</h1>

<h2>Typescript wurde aus JavaScript und C# entworfen</h2>


<h2>TS Typen</h2>
Bool<br/>
Number<br/>
String<br/>
Array<br/>
Any

<h3>TS Examples</h3>


<h3>Variablentypen</h3>

```html a = global```</br>
```html let a = block scope```</br>
```html var a = function scope```</br>
```html const a = Konstante```</br>


<h3>Operatoren</h3>

<h3>Klassen</h3>
<pre>
export class MeineKlasse {
    // Rumpf der Klasse
    // hier werden Instanzvariablen, Eigenschaften
    // und Methoden definiert
}
</pre>

<h3>Methoden</h3>
```html ```

<h3>Instanzvariablen und Eigenschaften</h3>
```html ```

<h3>Klassen (Beispiel mit Konstruktor)</h3>
```html ```


<h3>Arrays und Objects</h3>
```html ```


<h2>Angular Framework</h2>
Open Source JS-Framework
Angular JS hatte einige Schwachstellen die durch Angular behoben wurden.
September 2016 veröffentlicht durch Google.

<h3>Availability</h3>
PWA
Angular ist Cross Plattform tauglich - es läuft auf allen Browsern (also Computer, Tablet, Smartphones)
1x Programmieren, überall verfügbar

<h3>PWA Grundsätze</h3>
- Offline verfügbar
- Installierbar




<h2>Architektur Node</h2>
NodeJS
- NPM
- Angular CLI
- - webpack
- - ngc (Angular Compiler) => Sorgt auch für Schnelligkeit der Applikation
- - - TypeScript 

<h2>Entwicklungsumgebung</h2>
Es wird Visual Studio Code empfohlen
Git / Github verwenden


<h2>Angular Architektur</h2>
- Component basiert
- - View (Html)
- - Code (Controller / JS)
- - - wie eine Klasse
- - Stylesheet (Scss wird empfohlen - Cleaner & Variablen + Logik + Spez.File)

=> Html Property-Binding zu Controller
=> Eventbinding
=> Alles durch Angular gesteuert (Properties / Events gebunden)

In Angular wird die Klasse (Controller Component) geladen und HTML wird durch sie geladen ("berechnet")

Oberste Component ist immer die App-Component

<h2>Styleguide</h2>
Component: app.component.ts (wichtig Kleinschreibung da sonst auf Mac nicht kompilierbar)

<h2>Component</h2>
- templateUrl => für templateUrl
- styleUrls => als Array Stylesheets verlinken
- selector => Präfix wichtig, eindeutig setzen z.B. "CTS" (keine Namespaces, auch hilfreich für AutoImport)

Components werden verschachtelt und erweitert, endlos (wie Treeview)
- Allgemeine Komponenten in einem 'Shared'-Ordner auf oberster Ebene ablegen

<h3>Binding</h3>
Alles ist public
Bindings werden mit eckigen Klammern geschrieben
Testausgaben werden in doppelt geschweiften Klammern geschrieben (wie React {{ Obj.Prop }}) - à la 'innerHtml'


<h4>Property Binding</h4>
```html 
<h1>Begrüssung</h1>
<p [title]="titletext">
    {{ Name }}
</p>
```


<h4>Event Binding</h4>
Functions müssen innerhalb <bold>"this"</bold> verwenden.
```html 
<button type="button" (click)="changeNameClick()">clickme</button>
```

<h4>*ngIf</h4>

```html
<div *ngIf="boolWert">Man sieht mich nur wenn boolWert = true ist.</div>
```


<h4>*ngFor</h4>

```html 
<div *ngFor="let name of namenArray"><{{name}}<div>
```


<h4>for in / for of</h4>
<pre>for of: Iteriert wie in foreach von C#</pre><br/>
<pre>for in: Iteriert durch Object.keys(obj)</pre><br/>

<h2>Shortcuts</h2>

<h3>Neue Komponente automatisch erstellen</h3>
<pre>ng generate component MyCom</pre>

<h3>Starten von App</h3>
<pre>ng serve --aot</pre><br/>

<desc>Port ist standardmässig 4200</desc>
<desc>Erstellt Code der das HTML erstellt ahead of time</desc>

<h3>Veröffentlichen / Build</h3>
<pre>ng build --prod</pre><br/>
<desc>unbedingt --prod verwenden, da sonst der dev build verwendet wird</desc>



<h2>Angular Services</h2>

<h3>Injection</h3>
Services werden in Components injected
Services bzw. die Komponenten können sich dann untereinander austauschen
AppModule muss in Provider-Array alle Services enthalten.

<h4>Create Service File</h4>
<pre>ng generate service MemoryCalc</pre><br/>

<h4>Vor  </h4>

<h4>Angular Service Injecton</h4>
```html @Injectable({ providedIn: 'root' })

<h4>Angular HttpClient</h4>
```html ```