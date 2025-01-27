# Visual and Interactive Syntax realized (VISr) for ClojureScript

This is a very early prototype of [Visual and Interactive Syntax][visr] for
ClojureScript. Feel free to look around, but things will change and others will
be broken.

## Live Tool (Coming Soon)

To run VISr for ClojureScript, you only need a browser. Unfortunately there
currently is not any pre-built versions, that is coming soon.

## Build Requirements

Building VISr require both [NPM][npm] and [Clojure][clojure]. You can either
obtain them yourself, or use [Nix][nix] to download them for you.

### Automatically Install Dependencies with Nix (Mac/Linux Only)

> Note: If you don't have it yet, you'll need the [Nix][nix] build tool. You can
> install it with:
>
> ```
> curl -L https://nixos.org/nix/install | sh
> ```

Simply `cd` into the project directory and run:

```
nix-shell
```

You should now be in a shell environment with both NPM and Clojure.

### Manually Install Dependencies

1. First, download [Java][java] and [Clojure][clojure] for your operating system.
2. Next, download [Node.js][npm] for your operating system, it comes with
   [NPM][npm].
3. Finally, `cd` into the project folder and run `npm ci`.

You should now be ready to build VISr for ClojureScript.

## Build & Test VISr

### Development mode

To start the Figwheel compiler, navigate to the project folder and run the
following command in the terminal:

```
clojure -M:fig
```

Figwheel will automatically push cljs changes to the browser.
Once Figwheel starts up, you should be able to open `localhost:9500` in the browser.

Once the page is open, a REPL should be usable from your terminal.

### Tests

With a development build running, open
`localhost:9500/figwheel-extra-main/auto-testing` in the browser.

### Building for production

```
clojure -M:package
```

Then go get a coffee, or just eat dinner, a production build seems 
to take a little over 15 minutes.

[visr]: https://dl.acm.org/doi/10.1145/3428290
[nodejs]: https://nodejs.org/en/
[npm]: https://www.npmjs.com/
[java]: https://www.java.com/en/
[clojure]: https://clojure.org/ 
[nix]: https://nixos.org/
