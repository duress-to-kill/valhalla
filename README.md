# Valhalla Server
### Character record hosting for the 21st century

Written in Flask, built for self-hosting, and forged in the fires of Mt. Doom, Valhalla is a simple uWSGI webapp for managing and rendering character records for tabletop RPGs.

---

### Why use Valhalla?

Valhalla is a resource to support the use of digital character records in tabletop games.

Paper character sheets have numerous limitations which many gamers put up with for no reason besides tradition. Fillable digital formats (such as PDF forms and websites) have many of the same problems -- ridgid standard layout, an incomplete set of optional fields to support your character's traits and powers, and limited space for anotation are just some of these problems.

It has gradually become my preference to hand-type my character sheets in a plain text editor. This gives me free-form layout customized to my character's needs, unlimited room to record things such as gear and spells, plenty of room to annotate (i like to itemize my adjustments to skill checks and other rolls) and easy text searching for lengthy records make my play experience much smoother and less frustrating.

The major downside to this is that unformatted text rarely prints nicely, and just doesn't have the same aesthetic merits as a graphically constructed sheet. Additionally other players may find it hard to read. And you may be trading the risk of losing your character binder for the risk of a hard drive crash.

**Enter Valhalla**, a web-based character record repository and graphical rendering engine.

Valhalla reads hand-written plain text character sheets written in **rsonlite**, a simple and highly-readable subset of **yaml**, and stores them in a structured data format.

The Valhalla scheme for character sheet writing was designed to look as much as possible like a document a human would write for their own reference, by minimizing the number and visibility of syntax tokens used in the format.

##### Nobody wants to write characters in XML
```
<?xml version="1.0"?>
<character>
  <meta>
    <player_name>Joe Bloe</player_name>
    <campaign>Som Pathfinder Game</campaign>
  </meta>
  <bio>
    <character_name>Hank Williams, Necromancer</character_name>
    <race>Human</race>
    <class>Necromancer</class>
    <level>2</level>
...
```

##### Valhalla formatting is easy!
```
player name
  Joe Bloe
campaign
  Some Pathfinder Game

character name
  Hank Williams, Necromancer
race
  Human
class
  Necromancer
level
  2
```
Writing plain text character records is easy to do, and using them is likewise easy. Writing them in a Valhalla-compatible layout is no more difficult, but also provides a number of benefits:

- Records are easy to share with friends
- Records can be rendered in HTML, or compiled to PDF format for nice graphical layouts built to suit.
- API support makes your character sheet easily queryable by computers, making the use of add-on tools possible

### Planned Features

- Web UI for submission and modification of characters
- Online character rendering in HTML for supported games
- Compile-to-PDF for supported games
- Full CRUD-model HTTP API for tool support
