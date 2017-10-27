# Template Reference

The following variables are available in templates and landing pages:

> Tip: Remember - Templates are *case sensitive*!

 |Variable         | Description                                      |
 |-----------------|--------------------------------------------------|
 | {% raw %} {{.FirstName}} {% endraw %}    | The target's first name    |
 | {% raw %} {{.LastName}} {% endraw %}    | The target's last name     |
 | {% raw %} {{.Position}} {% endraw %}    | The target's position      |
 | {% raw %} {{.Email}} {% endraw %}       | The target's email address |
 | {% raw %} {{.From}} {% endraw %}        | The spoofed sender         |
 | {% raw %} {{.TrackingURL}} {% endraw %} | The URL to the tracking handler|
 | {% raw %} {{.Tracker}} {% endraw %}     | An alias for `<img src="{% raw %} {{.TrackingURL}} {% endraw %}"/>` |
 |{% raw %}{{.URL}} {% endraw%}            | The phishing URL           |