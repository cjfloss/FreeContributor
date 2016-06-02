# Contribution

You can contribute by running [uBlock Origin](https://github.com/gorhill/uBlock) in Advanced mode [1] and/or [uMatrix](https://github.com/gorhill/uMatrix).

To change to uBlock Advanced-user mode, go to Click To Open Dashboard and select the checkbox I am an advanced user

Basic mode | Advanced-user mode
:----------:|:------------------:
[Popup user interface](https://github.com/gorhill/uBlock/wiki/Quick-guide:-popup-user-interface) | [A point-and-click firewall which can be configured on a per-site basis](https://github.com/gorhill/uBlock/wiki/Dynamic-filtering:-quick-guide) 
<a href="https://github.com/gorhill/uBlock/wiki/Quick-guide:-popup-user-interface"><img src="https://raw.githubusercontent.com/gorhill/uBlock/master/doc/img/popup-1.png" /></a><br><sup>.<br>.</sup> | <a href="https://github.com/gorhill/uBlock/wiki/Dynamic-filtering:-quick-guide"><img src="https://cloud.githubusercontent.com/assets/585534/9293685/378d18f0-4402-11e5-9255-8ed3fdbfa957.png" /></a><br><sup>Configure as you wish:<br>picture shows 3rd-party scripts and frames blocked by default everywhere</sup>


After reading the [uBlock wiki: Dynamic filtering: quick guide](https://github.com/gorhill/uBlock/wiki/Dynamic-filtering:-quick-guide), start blocking
the bad domanains in the websites you visit. 

**ATTENTION:** make sure that the website works, with the rules you applied in Ublock Origin/uMatrix.

The data is stored in the browser and can be exported to a text file. Go to uBlock dashboard -> My rules and export to file. The same applies to uMatrix.

Finally save the file in `FreeContributor/utils` and run the script `ublock-umatrix-export.sh`. Example:


    $ ./ublock-umatrix-export.sh dnsmasq my-umatrix.rules


This will export only the blocked domains to dnsmasq formart `server=/bad-domain.tld/` to `dnsmasq-umatrix.conf`. Save it at `/etc/dnsmasq.d/`

You can send me this bad domains via pull request. See a sample at `FreeContributor/data/samples`


    $ ./ublock-umatrix-export.sh domains my-umatrix.rules


Add the file `domains` generated by the script.




