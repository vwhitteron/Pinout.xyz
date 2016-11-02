#Pinout.xyz

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a>

[Pinout.xyz](http://pinout.xyz/) is the successor to the popular Pi pinout website originally hosted on [http://pi.gadgetoid.com/pinout](http://pi.gadgetoid.com/pinout).

To support translation efforts, and allow people to build tools with the data in this repository, Pinout.xyz is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](href="http://creativecommons.org/licenses/by-nc-sa/4.0/).

This license excludes the 'pinout-graphic-horizontal' files located in the 'graphics' directory, which are provided under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/) to permit commercial use; specifically publication in books and magazines with appropriate attribution.

#About this project

The contents of this GitHub repository are used to build http://pinout.xyz and its translated subdomains.

This project aims to build a consistent workflow behind the Pinout.xyz front-end, gather useful information about the Raspberry Pi GPIO interface and add-on boards, and invite board manufacturers to produce their own "overlay" files which describe which pins their Pi add-ons use.

We hope that by making this project open and extensible we will invite not only contributions of board pinouts, but translations too.

#Reportting

If you've spotted an error, ommission or have a suggestion, raise an [issue](https://github.com/Gadgetoid/Pinout.xyz/issues). Feedback on every aspect of the site or this repository is welcome!

#Contributing

If you have a board you'd like to contribute, the preferred method for submission is to create a modified version of the overlay [template](https://github.com/Gadgetoid/Pinout.xyz/blob/master/draft/overlay/template.md) and create a pull request.

Please ensure the files you submit are being pushed to the `/draft` folder, where it will be reviewed before publication. Note that as part of the submission, a top-down view of the board in the form of a [png](https://github.com/Gadgetoid/Pinout.xyz/blob/master/draft/overlay/template.png) is expected, although optional. If you can't produce the png file yourself, just duplicate and rename `template.png` but make sure to include a url somewhere in the overlay where we can fetch a suitable graphic.

If you feel that the requirements for submissions is beyond your current possibilities, you may raise an [issue](https://github.com/Gadgetoid/Pinout.xyz/issues) instead and we'll consider it!

#Translating

If you would like to provide support for a language not yet in the repository you should start by duplicating the `src/en` directory to the appropriate language-code. For example, if you want to create a Czech translation you would create the folder `src/cs`. Note that there are no plans to support cultures (it would just get out of hand!), so you can't have `src/fr-CA` ( sorry! ).

The first resources we recommend you translate are the language specific strings found in the `settings.yaml` file and the `footer.html` template, as well as the content of the `/pin` folder. Once that's done, rename the `/overlay` folder to `/translate` and start translating the boards markdown files (pick any you fancy translating, it does not have to be the first board in alphanumerical order). Leave those translations in the `/translate` folder when finished.

Please do not attempt to translate the `/resources` folder, or anything not specifically mentioned in this paragraph - all files outside your *&lt;languagecode&gt;* directory is shared between the subdomains and should be generic. Feel free to modify the template with links relevant to your country, and / or your Twitter handle however, but don't fiddle with the structure!

Once you've made your translation, you can build and preview it with, for example:

```bash
make serve LANG=de
```

And then open: http://127.0.0.1:5000 in your browser.

*note 1: you will need several python modules installed to render and serve a local version of the site, run `pip install -r requirements.txt` from the top of the repository tree to install the required modules.*

*note 2: if you are facing issues on your preview (card not showing, text update not appearing ...), you can fix it by erasing you browser cache (image and cache file only)*

The last step will be to submit your finished translation as a [pull request](https://github.com/Gadgetoid/Pinout.xyz/pulls) and we'll get it live on its own *&lt;languagecode&gt;*.pinout.xyz subdomain :)
(this can include any number of boards, it does not have to be the entire line-up of boards)

#Roadmap &amp; wishlist

* Redesign HTML generation and unify HTML templates into a single, translatable file
* Add functionality to compare two or more boards, to visualise pin compatibility
* Tool to convert WiringPi to GPIO to BCM and back
* Add as many [boards](http://pinout.xyz/boards) as possible!

#Acknowledgement

Maintainers: [@Gadgetoid](https://github.com/Gadgetoid) and [@RogueM](https://github.com/RogueM)

GPIO Zero code examples by: [@bennuttall](https://github.com/bennuttall)

Notable contributions:

* [en](http://pinout.xyz/) - [@lurch](https://github.com/lurch) and [@abelectronicsuk](https://github.com/abelectronicsuk)
* [de](http://de.pinout.xyz/) - [@rdmueller](https://github.com/rdmueller) and [@KojoePi](https://github.com/KojoePi)
* [es](http://es.pinout.xyz/) - [@ResonantWave](https://github.com/ResonantWave) and [@IkerGarcia](https://github.com/IkerGarcia)
* [fr](http://fr.pinout.xyz/) - [@RogueM](https://github.com/RogueM) and [@smileyn64](https://github.com/smileyn64)
* [it](http://it.pinout.xyz/) - [@LizardM4](https://github.com/LizardM4)
* [tr](http://tr.pinout.xyz/) - [@Ardakilic](https://github.com/Ardakilic)
