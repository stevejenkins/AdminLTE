Pi-hole Admin Dashboard
============
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/938b4d9e61b7487da77cf63ba05c683d)](https://www.codacy.com/app/Pi-hole/AdminLTE?utm_source=github.com&utm_medium=referral&utm_content=pi-hole/AdminLTE&utm_campaign=badger)
[![Join the chat at https://gitter.im/pi-hole/AdminLTE](https://badges.gitter.im/pi-hole/AdminLTE.svg)](https://gitter.im/pi-hole/AdminLTE?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif "AdminLTE Presentation")](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=3J2L3Z4DHW9UY "Donate")

Using **[AdminLTE](https://almsaeedstudio.com)**, this project will create a Web interface for the ad-blocking Pi-hole: **a black hole for Internet advertisements**.

From this interface, you will be able to see stats on how well your Pi-hole is performing.  You will also be able to update the lists used to block ads.

![Pi-hole Web interface](http://i.imgur.com/EgGZXbT.png)

## API
A read-only API can be accessed at `/admin/api.php`. With either no parameters or `api.php?summary` it returns the following JSON:
```JSON
{
	"domains_being_blocked": "136,708",
	"dns_queries_today": "18,108",
	"ads_blocked_today": "14,648",
	"ads_percentage_today": "80.9"
}
```

There are many more parameters, such as `summaryRaw`, `overTimeData10mins`, `topItems`, ` topClients` or `getQuerySources`, `getQueryTypes`, `getForwardDestinations`, and finally `getAllQueries`.
Together with a token it is also possible to enable and disable (also with a set timeout) blocking via the API

The API returns more information (in a slighly different format if `FTL` is running) - it supports a fall-back to the "old" PHP API if `FTL` is not running. Test the type and/or version of the API by using the parameter `type` and `version`.

<hr>
<img src="https://assets.pi-hole.net/static/BStackLogo.png" height="80"><br>
We use BrowserStack for multi-platform multi-browser testing.
