# Template Reference

The following variables are available to be used in templates and landing pages:

> Tip: Remember - Templates are *case sensitive*!

|Variable         | Description                                  |
|-----------------|----------------------------------------------|
|{{.FirstName}}   | The target’s first name                      |
|{{.LastName}}    | The target’s last name                       |
|{{.Position}}    | The target’s position                        |
|{{.Email}}       | The target’s email address                   |
|{{.From}}        | The spoofed sender                           |
|{{.TrackingURL}} | The URL to the tracking handler              |
|{{.Tracker}}     | An alias for `<img src="{{.TrackingUrl}}"/>` |
|{{.URL}}         | The phishing URL                             |