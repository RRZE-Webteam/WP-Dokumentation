Diese Option ermöglicht den automatischen Abgleich von Forschungsbereichen und Forschungsprojekten mit CRIS. Das Plugin erstellt dabei automatisch Seiten und Menüeinträge für die einzelnen Forschungsbereiche und -projekte Diese werden unterhalb einer Seite "Forschung" auf oberster Menüebene angeordnet.
[fauvideo url="https://www.fau.tv/webplayer/id/140726"]
[alert style="success"]
Die Option kann unter Einstellungen &gt; CRIS  im Reiter "Synchronisierung" aktiviert werden. Jede Nacht werden damit die Daten automatisch auf neue Einträge überprüft und ggf. Seiten ergänzt. Zusätzlich lässt sich die Aktualisierung mit dem Button "Jetzt synchronisieren" jederzeit manuell starten.
[/alert]
<a href="https://www.wordpress.rrze.fau.de/files/2017/02/cris_einstellungen_sync.png"><img class="alignnone size-full wp-image-17233" src="https://www.wordpress.rrze.fau.de/files/2017/02/cris_einstellungen_sync.png" alt="CRIS Einstellungen: Reiter Synchronisierung" width="905" height="260" /></a>
<h2>Die Synchronisierung im einzelnen</h2>
[notice-plus title="Schritt 1"]
Wenn es noch keine <strong>Seite „Forschung“ auf der obersten Menüebene im Hauptmenü</strong> gibt, wird sie angelegt und mit dem Shortcode <code>[[cris show=organisation]]</code> gefüllt (dieser Shortcode liefert die Forschungsbeschreibung der Organisationseinheit aus CRIS). Außerdem werden folgende Seitenattribute gesetzt:
<ul>
 	<li>Template: Portalindex</li>
 	<li>Reihenfolge: 2 (an zweiter Stelle im Hauptmenü – kann später auch verändert werden)</li>
 	<li>Portalmenü: „Portal Forschung“ (wird vorher generiert, wenn nicht vorhanden)</li>
 	<li>Artikelbilder im Portalmenü verbergen</li>
 	<li>Ersatzbilder im Portalmenü verbergen</li>
 	<li>Unterpunkte im Portalmenü anzeigen</li>
 	<li>Ansprechpartner (Sidebar): Ansprechpartner Forschung aus CRIS, soweit als Kontakt im FAU-Person-Plugin vorhanden</li>
</ul>
[/notice-plus]

<hr />

[notice-plus title="Schritt 2"]
Wenn es bereits eine Seite „Forschung“ im Hauptmenü gibt, werden nur die Seitenattribute angepasst, der Seiteninhalt wird nicht verändert.
[/notice-plus]

<hr />

[notice-plus title="Schritt 3"]
Für alle <strong>Forschungsbereiche</strong> werden (wenn noch nicht vorhanden) einzelne Seiten unterhalb der Seite „Forschung“ angelegt. Falls die Seite schon existiert (=Seitentitel unterhalb von „Forschung“ schon vorhanden), werden nur die Attribute (nicht der Inhalt) angepasst.
<ul>
 	<li>Titel: Titel des Forschungsbereichs</li>
 	<li>Seiteninhalt: <code>[[cris show=fields field=123456 hide=title]]</code></li>
 	<li>Seitentemplate: Inhaltsseite mit Navi</li>
 	<li>Elternseite: „Forschung"</li>
</ul>
[/notice-plus]

<hr />

[notice-plus title="Schritt 4"]
Das selbe wie für die Forschungsbereiche passiert mit den <strong>Forschungsprojekten</strong> unterhalb der einzelnen Forschungsbereiche.
<ul>
 	<li>Titel: Titel des Forschungsprojekts</li>
 	<li>Seiteninhalt: <code>[[cris show=projects project=123456]]</code></li>
 	<li>Seitentemplate: Inhaltsseite mit Navi</li>
 	<li>Elternseite: der entsprechende Forschungsbereich (s.o.)</li>
</ul>
[/notice-plus]

<hr />

[notice-plus title="Schritt 5"]
Projekte die keinem Forschungsbereich zugeordnet sind, landen auf der<strong> Seite "Weitere Projekte“</strong> hinter dem letzten Forschungsbereich
<ul>
 	<li> Titel: "Weitere Projekte"</li>
 	<li>Seiteninhalt: <code>[[cris show=projects project="123456, 456789, 789123"]]</code></li>
</ul>
[/notice-plus]

<hr />

[notice-plus title="Schritt 6"]
Zu allen Seiten werden außerdem <strong>Menüeinträge</strong> sowohl im <strong>Hauptmenü</strong> als auch im (ggf. neu generierten) <strong>Menü "Portal Forschung"</strong> erstellt, das dann auf der Portalindex-Seite "Forschung" eingebunden wird.
[/notice-plus]

<hr />

Sie können in den Einstellungen festlegen, ob die Shortcodes normal oder als <a title="Custom-Shortcode" href="https://www.wordpress.rrze.fau.de/plugins/fau-cris/erweiterte-optionen/">Custom-Shortcode</a> eingefügt werden. Damit können Sie die Darstellung im Nachhinein anpassen. Z.B. können Sie Zeilen, in denen es eine Beschriftung, aber keinen Inhalt gibt, einfach von Hand löschen.

[alert style="info"]Die Synchronisierung löscht keine Daten – das ließe sich nicht für alle Benutzer zufriedenstellend lösen. D.h. wenn ein Projekt nicht mehr existiert, muss man es von Hand aus der Website löschen oder verschieben.[/alert]

Alle Seiten und Menüeinträge werden "normal" erstellt, d.h. die Seiten können weiter bearbeitet und ergänzt werden. Außer den Seitenattributen und der Reihenfolge im Menü wird bei der Synchronisierung nichts überschrieben.
<h2>Kurz zum Hintergrund der erzeugten Seitenstruktur</h2>
Um universitätsweit ein einheitlicheres und damit professioneller wirkendes Bild abzugeben, hat der CIO eine Vorlage für Lehrstühle entworfen, an denen sich Webmaster – so eng wie möglich und sinnvoll – orientieren können. Die Vorlage findet sich unter <a href="https://www.muster-lehrstuhl.wordpress.rrze.fau.de">https://www.muster-lehrstuhl.wordpress.rrze.fau.de</a>. Die Automatisierung erstellt den ersten Teil des Bereichs "Forschung" dieser Vorlage.

Weitere Forschungsleistungen (z.B. Publikationen) können und sollen natürlich ebenfalls unterhalb des Portals "Forschung" angelegt werden.