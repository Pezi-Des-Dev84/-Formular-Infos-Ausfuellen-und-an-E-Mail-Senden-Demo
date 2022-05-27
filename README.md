# Formular-Infos-An-E-Mail-Senden-Demo
Formular für UI, zum Ausfüllen, mit Name, E-Mail-Adresse, Nachricht-Schreiben und  per Webserver an die E-Mail-Adresse des Empfängers versenden lassen.
  - Erstellen eines Bootstrap-Kontaktformulars
  - Abrufen des Absenders zum vollständigen Ausfüllen und Senden einer E-Mail
  - Hinzufügen eines Honigpots
  - Entfernen eines Captcha-Passwortes
  - Bereinigen einer E-Mail
  - Hinzufügen einer Seite zur Bestätigung des Sendens...

FormSubmit Erweiterte Funktionen

Formulareingaben können speziell benannte name-attribute haben, die die Funktionalität ändern. Sie sind alle mit einem Unterstrich versehen.

_replyto
Dieser Wert wird für das Reply-To-Feld der E-Mail verwendet. Auf diese Weise können Sie direkt auf die E-Mail "antworten", um der Person zu antworten, die das Formular ursprünglich eingereicht hat.

Um diese Funktion zu aktivieren, sollte Ihr Formular die E-Mail-Adresse des Benutzers anfordern.

<input type="email" name="email" placeholder="E-Mail-Adresse">

_next
Standardmäßig wird dem Benutzer nach dem Absenden eines Formulars die Seite "Danke" von FormSubmit angezeigt. Sie können eine alternative URL für die Seite "Danke" angeben.

<input type="hidden" name="_next" value="https://yourdomain.co/thanks.html">

_subject
Dieser Wert wird für den Betreff der E-Mail verwendet, sodass Sie schnell auf Einsendungen antworten können, ohne die Betreffzeile jedes Mal bearbeiten zu müssen.

<input type="hidden" name="_subject" value="Neue Einreichung!" >

_cc
Dieser Wert wird für das CC-Feld der E-Mail verwendet. Auf diese Weise können Sie eine Kopie jeder Einreichung an eine andere E-Mail-Adresse senden.

<input type="hidden" name="_cc" value="another@email.com">

Wenn Sie mehrere E-Mail-Adressen CC möchten, erstellen Sie einfach eine Liste von E-Mail-Adressen, die durch Kommas getrennt sind.

<input type="hidden" name="_cc" value="another@email.com, yetanother@email.com">

_honey
Fügen Sie dieses "Honeypot" -Feld hinzu, um Spam zu vermeiden, indem Sie Schaber täuschen. Wenn ein Wert angegeben wird, wird die Übermittlung stillschweigend ignoriert. Die Eingabe sollte mit CSS ausgeblendet werden.

Alle Formulare werden mit reCAPTCHA geliefert, das fortschrittliche maschinelle Lerntechniken verwendet, um zwischen Menschen und Bots zu unterscheiden, so dass dies für die meisten Formen nicht notwendig ist.

<input type="text" name="_honey" style="display: none">

reCAPTCHA-_captcha deaktivieren
Möchten Sie nicht, dass Ihre Benutzer ein reCAPTCHA ausfüllen? Jedes Formular verfügt jetzt über die Option, das reCAPTCHA zu deaktivieren, sodass Sie die vollständige Kontrolle über Ihr Formular behalten. Sie können reCAPTCHA sogar auf einigen Formularen beibehalten, die anfällig für Spam sein könnten, während Sie es auf anderen deaktivieren.

<input type="hidden" name="_captcha" value="false">

* Wir empfehlen Ihnen dringend, das reCAPTCHA zu verwenden (nicht um es zu deaktivieren), um einige technische Einschränkungen zu vermeiden, die wir von Zeit zu Zeit auferlegen, um Bots, Spam und andere bösartige Programme herauszufiltern.

_autoresponse
Sie können eine sofortige Antwort an Ihre Benutzer mit einer Kopie der Übermittlung senden. Fügen Sie dem E-Mail-Text eine benutzerdefinierte Nachricht hinzu.

<input type="hidden" name="_autoresponse" value="ihre benutzerdefinierte Nachricht">

Um diese Funktion zu aktivieren, sollte Ihr Formular die E-Mail-Adresse des Benutzers anfordern.

<input type="email" name="email" placeholder="E-Mail-Adresse">

* autoresponse funktioniert nicht mit Formularen, die reCAPTCHA deaktiviert sind, und Formularen, die über AJAX gesendet werden.

_template
Sie können eine E-Mail-Vorlage aus 3 verschiedenen Vorlagen auswählen. Standardmäßig verwendet FormSubmit die Basisvorlage.

<input type="hidden" name="_template" value="table">

Alle Vorlagen hier anzeigen →

_webhook
Mit dieser Funktion können Sie einen Webhook konfigurieren, der jedes Mal ausgelöst wird, wenn ein Formular eine neue Übermittlung empfängt. Webhooks können verwendet werden, um Daten in Echtzeit zu bearbeiten.

<input type="hidden" name="_webhook" value="https://yourdomain.co/your-webhook">

Beispiel für eine webhook-antwort

{“form_data": {“name": "Max Mustermann", "email": "max.mustermann@outlook.de ", "message": "Guten Tag, danke für Ihre Mail.”} }

