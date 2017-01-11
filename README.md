# Bus-Webkomponenten
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
