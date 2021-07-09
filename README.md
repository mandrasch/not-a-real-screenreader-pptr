# Not a real Screenreader

Experimental test tool for screenreader output of websites - navigate through a web page with a graphical user interface. No need to (immediately) learn operating a screenreader with shortcuts to experience accessibility issues. Learning tool for (sighted) devs, who are starting their a11y journey.

⚠️ Always use a real screenreader for serious accessibility testing! This is just an experimental learning tool for web accessibility. ⚠️

Built with electron, puppeteer, puppeteer-in-electron, say, chalk, bulma. Puppeteer allows accessing the accessibility tree since version 3.0.0. See **[accessibility.snapshot()](https://pptr.dev/#?product=Puppeteer&version=v9.1.1&show=api-class-accessibility).**

🎥 Demo video: https://www.youtube.com/watch?v=xUTCEnfepHk (old commandline version)
🎥 Demo video II: (coming soon)

## Run

- `npm install`
- `npm start`

Default example page: https://dequeuniversity.com/library/aria/simple-dialog - try to open and close the modal :-)

Tested with node v14.17.3

## Current limitations

- does not support clicking on links / navigating to other pages currently
- does not support form input
- speech output has no language support, maybe use another library?
- Focusing and reading actions are not synchronized

## Background

Initial goal: Provide a simple screenreader test tool for devs to recognize accessibility issues. It should work without the need of learning screenreader shortcuts beforehand. (I would love a web interface with buttons for it, but having a commandline tool is a first step. :))

I also experimented with a chrome extension, but chrome won't allow dispatching keyboard events of tabulator key to shift the focus in the browser (most likely because security). See https://github.com/mandrasch/not-a-real-screenreader-chrome-extension for source code. Puppeteer allows sending tab key events to the browser.

Disclaimer: I'm an a11y newbie, feedback is welcome. I try to respect *Nothing About Us Without Us* as much as possible.

## License

My own scripts and work is available as CC0 (https://creativecommons.org/publicdomain/zero/1.0/deed.de). Please see package.json for a list of Open Source Libraries used. 