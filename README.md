# Fisher Price Record Player Songbook

If you are looking for a handful of half-baked attempts at creating templates to create 3D-printed records for the old [Fisher Price Record Player](https://thisoldtoy.com/L_FP_Set/toy-pages/900-999/995-musicboxrecordplayer.html), you have come to the right place.

Some saintly folks have spent the time to develop tools for creating such things, the original (as far as I know) being an Instructable done by Fred27: [3D Printing Records for a Fisher Price Toy Record Player](https://www.instructables.com/3D-printing-records-for-a-Fisher-Price-toy-record-/)

Billgonzo123 later added a web app tool to help out with generating the scripts: [Fisher Price Record Maker](https://github.com/Billgonzo123/Fisher-Price-Record-maker)

Both tools allow you to compose a series of notes and then convert that data to a 3D model of a record which, if printed, should play your song. 

The Fisher Price Record Player has an arm that contains 22 pins for playing notes when plucked by bumps in the record's grooves (at least on the version I have; I think the Sesame Street version at least has less pins for some reason but don't know for sure). The notes are in the key of A-flat Major and a few notes are duplicated so that the note can be repeated quickly by alternating the pins used for notes played in quick succession (or at least so I assume). As such, there are 16 unique notes available among the 22 pins.

Both of the tools mentioned here allow you to compose songs made up of these 16 notes. You can then generate a SCAD file that scripts the 3D model creation in OpenSCAD.

You can also save a copy of the composed notes in an `.fpr` file ("Fisher Price Record file") that encodes the composition as a series of `+` for notes and `-` otherwise. These files are basically intermediate outputs that can be reloaded into either of the tools to generate the final SCAD file output.

I have tried my hand at composing a few songs and have added the `.fpr` files to this repo for whoever is interested in using them. Some are just snippets of intros or choruses, some are more fleshed out, but they are just fragments for now and maybe forever but we will see.

A couple notes about what I've learned while playing with the tool:

* The Fred27 tool doesn't seem to indicate the clef but it appears to be treble clef.
* Both of the tools are based in the key of C even though my record player seems to be in the key of A-flat. I'm not sure if they did this transposition just to make it simpler to compose things (I'm happy if that's the case) or whether some versions of the players are actually in that key. Either way, it doesn't matter too much. Just know you aren't losing your mind if your player doesn't seem to be playing in the same key. You just have to know to compose whatever songs you are making in C for these tools. All the intervals on the tool are the same as the ones in my player, just transposed, so it's not really an issue.
* Neither tool appears to take advantage of the redundant pins to play notes in quick succession (based on a few quick tests anyway). I.e., it seems like if you play a bunch of E5 notes in a row, it doesn't seem like the software is creating bumps on alternating sides of the groove. (Side note: [this person](https://www.westaby.net/2020/11/diy-records-for-the-fisher-price-music-box-record-player/) describes making a spreadsheet for a different version of the player where he makes use of the alternating pin abilities, but the link to the tool itself appears broken so it's a mystery for now.)
* Fred27 tool seems to do play back at the same speed no matter how many beats you have included, whereas the Billgonzo123 plays things faster the more beats are included; the latter is helpful for some cases to get a better feel for it.
* I had some Issues with Billgonzo123 when playing many notes in quick sequence just on the playback. I don't know anything about midi really; maybe it's something to do with the implementation of that but who knows.

Anyway, if you are interested in checking out the songs (or barely snippets of songs in some cases) you can download fpr files here and load them into either of the abovementioned tools. I may add some here and there and if anyone happens to be doing the same thing, I would love to hear what you got as well.
