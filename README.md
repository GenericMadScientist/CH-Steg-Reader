# CH Steg Reader

A program to read the steganography data contained in Clone Hero's screenshots.

## Usage

Run it from the command line like so

```cmd
> ch_steg_reader.exe clonehero-Angel-of-Salvation-20220422060015.png
```

and it'll print out the information saved in the image.

| Arguments     | Action                                                                              |
| ------------- | ----------------------------------------------------------------------------------- |
| -h, --help    | Print help information                                                              |
| -j, --json    | Output result as JSON (useful if you intend to integrate this with another program) |
| -r, --recurse | Recursively check all images in directory                                           |
| -v, --version | Print version information                                                           |

## Frequently Asked Questions

* When are you releasing the source code?
  * No.

* Why not?
  * The Clone Hero dev team does not want the details of the steganography made
    public, which is fair enough. So no public source code. I've talked about it
    with Matt and he is cool with me releasing something though, so long as it's
    not something trivial to get usable source from like unobfuscated C#.

* How solid is this as a means of proof?
  * Not as reliable as you'd like. The song hash does enable you to check the
    chart (it's the [MD5 hash](https://en.wikipedia.org/wiki/MD5) of the
    notes.chart or notes.mid file). But suffice to say there are ways to trick
    Clone Hero. If you want a stronger means of proof, look forward to replays
    and leaderboards.

* What versions does this support?
  * Principal testing has been on PTB 3493 and v23.2.2, but I have put a bit of
    effort into versions since the first v22 release, which added the
    steganography. The latest version I've checked is v1.1.0.5684-PTB.

* My PTB 3075 screenshot is missing player data, why?
  * Clone Hero bug, nothing I can do.

* My ancient v22 screenshot has lots of extra player data, why?
  * Clone Hero bug. I do not know if there is a reliable way to find out which
    score is intended, nor have I put any time into trying to work one out.

* Any other relevant Clone Hero bugs?
  * Early score-saving PTBs failed to add the solo bonuses to each player's
    score. I check on the version and handle this for you, so you don't have to
    worry about it.

  * Screenshots from PTB 5520 have version 7, when they should be version 8. The
    steg reader also checks for this and fixes it in the background.

  * Screenshots from PTB 5684 have version 9, when they should be version 10.
    Also fixed automatically.

## Contact

Bugs can be reported on the GitHub page or DM'd to me on Discord
(genericmadscientist).

