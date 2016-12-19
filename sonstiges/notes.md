Um die Implementation eines Polymerprojekts zu beginnen, muss sichergestellt sein dass:
 -  Git <https://git-scm.com/>  
 - Node.js <https://nodejs.org/en/>
 - Bower <http://bower.io/>
 
installiert ist.

Als nächstes erstellt man sein Projektverzeichnis und wechselt in dieses.

Mit:

``
bower init
``

initialisiert man das Projekt dies ist wichtig um die späteren Abhängikeiten einfach zu lösen.
    
Mit:

``
bower install --save Polyemer/polymer#^1.7.1
``
wird die Polymerversion 1.7.1 heruntergeladen und installiert. Je nach aktueller stabiler Version kann dieses angepasst werden.
    
Wenn alles funktioniert hat sollte nun in der Ordnerstruktur ```bower_components/polymer/``` auftauchen 
hier werden die später eingesetzten Polymer Komponenten auftauchen

Mit:

``
bower install --save PolymerElements/iron-elements
bower install --save PolymerElements/paper-elements
``

installieren wir nun die von Polymer bereitgestellen Iron- bzw. Paper-Elements.

Komponenten:
---
* link-button:
    Erweiterung des Paper-Button um auf eine andere Webseite zu gelangen.
    
    Attribute:
    
     + link: angestrebte Website
     + name: Beschriftung des Button
     
     Implementierung:
     
     ``
     <link-button link="http://google.de" name="Button nach Google"></link-button>
     ``
    
* link-menu:
    Erweiterung des Paper-Dialog öffnet Menu, als Modal, mit Linkbutton 
    
    Attribute:
    
    + links: Array mit Elementen:
        + name: Beschriftung der Button im Menu
        + link: angestrebte Website der Button
    + button-name: Beschriftung des Button
    
    Implementierung:
         
    ``
    <link-menu links='[{"name": "Google", "link": "http://google.de"}, {"name": "tagesschau", "link": "http://tagesschau.de"}]'></link-menu>
    ``
          
Wie wird Komponente erzeugt:
---

1. Wir erzeugen ein leeres HTML file
2. wir nutzen nun folgendes Muster: 
    ```
    <dom-module id="neue-komponente">
        <template>
             <!-- DOM Elemente-->
        </template>
        <script>
            Polymer({
                is: "neue-komponente",
                listeners: {
                },
                properties: {
                        propertie1: {
                            type: String,
                            value: "default"
                        }
                }
            })
        </script>
    </dom-module>
    ```
3. In Polymer({ }) implementieren wir alle nötigen Eigenschaften, Attribute und Funktionen unserer Web-Komponente
4. Im Head unseres Webprojekts fügen wir folgende Zeile ein:
    
    ```
    <link href="pfad zur neuen Komponente" rel="import">
    ```
    
5. Jetzt Können wir unsere neue Web Komponente nach belieben im Body unseres Webprojkets verwenden.
 
    ```<neue-Webkomponente properties1="blupp"> </neue-Webkomponente>```

