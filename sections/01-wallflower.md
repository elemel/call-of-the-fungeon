# Chapter 1: Wallflower

You have entered a dungeon. You stand at the bottom of the staircase where you entered, facing east. A gnomish cartographer, carrying a bundle of scrolls, peers at you from an adjacent tile. As he steps onto the staircase, he thrusts a scroll into your hands. Before you can respond, he has already left the dungeon.

Unrolling the scroll, you identify it as a magic map. It ripples and shifts into a symbolic representation of the dungeon:

```
##############[###]#[#######################]#[##]###########]##
#########[.....#[....[#####################]...][......]#####.]#
###]####[...][.....#[####]###########]#[#####]....[###.#[####.[#
###.][....[]#].##]...]###.]#]#######[...[#####[].[##[....[#]]..#
##]....]#]###.]##]#[....].....]#####]......]#[....[...[]###.]..#
###.##]...]##.#[].....]]#.##.][######[......]#...[#..]#.....[..#
###.]#..[.]#].....[]..[....]...][##][#[[.#].[#[.###[....][.....]
##]....[...].....[##][..#[]##[...[...[...[...]#.]#[#..]..][]#..#
#]...][..]....[...[###..#[##]]..##...][.##.[.[]....[..][]#[....[
###].[..]....]#.]..[#]....[#.]].##[......].#[#..<[[#[.###[..#][#
####.#.]#[]].#]..]..[..[####.[#.##].....]#.....[][.[#.#[...]####
##[.......##]##[][]...]####]....]##][.]..][][###.]..].##.#]#####
#[...[.]#.####[...[#]]######[.]..]]...[].....[#]....[][....]####
##..[.....[#][.....].]#######.[[]#...][...]...[..#]..#[[]#...]##
#]..]...]##]...[.#...[######]..[]#.[.[#[]..]]...][#]...###[#..]#
##.]#[].##]......[[#..]#####]]...]..[##[][..]]..[.#]#[.#####[..]
[...]##]##....]][###[.##]#[#.....[]..#[..][..]#]]......]#####[.#
#.[][####].......]][#..].....[[...[].##..##[.####......[[###[..#
#.#[.[......].[.....][..]].[[.#.[##..[#..#[..##][[#.[....[##]..#
#..]...][.#]#]]..[....[.].....[[]##.#]].....]#].....[.[#[.###.]#
#[....]...[####][]...##..]....]#....]....[#]####.####[###.[....]
##[......]]######[]..##[....]]...[].###]...][###.]#######.#[#].#
#[..][##.#.]###[......]#[#]....]###]#]##[....]#].....]##]...##.#
[..][###.#.[##[.[.]......]#].].####[#.]#[.[#.[#...[#]####.#.[..#
#.][.[#].]...]#.#.#].[[#..]#.#]##[..].....[]..[.]########.#.[.]#
#..]....]#[.....[.#].[.#[....].]##[.#.#]...[[[]....]#####.]....]
#..[[.[.]##...[...[..]...[#]...[##]...##][[......[]######..].[.#
#[.[].......[##[##]..[.]..##]...#]...]#].......[][#######[.[...#
[...[]...]]####[##..[..#].#[....[##].#]...[.].#]..]]#[#[...#.[]#
#.[##..[.[......][....]#..[...]..#[..#..[[....[#].....[...]#[###
#.....[#[..[##]....[#]#]....[]#]....]].....]......].....[]######
#[#######[]####[##]########]#######]######]######]#####]########
```

The staircase is marked `<` on the map, with east to the right. You are compelled to walk through the dungeon, always step forward when possible, and turn only when instructed. Stepping onto floor tiles (marked `.`) has no particular effect.

The dungeon contains wall tiles: left-turners (marked `[`), right-turners (marked `]`), and halters (marked `#`). Whenever you would step onto a wall tile, stay and turn instead. This still counts as a step. For a left-turner, turn 90 degrees to the left. For a right-turner, turn 90 degrees to the right. For a halter, turn 0 degrees, in effect halting indefinitely.

As demonstrated by the gnome, you leave the dungeon by stepping onto the staircase from an adjacent tile. After how many steps do you leave the dungeon?


## Example

Consider an example dungeon:

```
####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########
```

Below is a log of walking through the example dungeon. Your coordinates are shown as `(x, y, z)`, and your location is marked `@` on the map.

```
Step count: 0
Coordinates: (10, 4, 0)
Direction: East
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][@[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 1
Coordinates: (10, 4, 0)
Direction: North
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][@[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 2
Coordinates: (10, 3, 0)
Direction: North
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.@...]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 3
Coordinates: (10, 3, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.@...]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 4
Coordinates: (9, 3, 0)
Direction: West
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][@....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 5
Coordinates: (9, 3, 0)
Direction: South
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][@....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 6
Coordinates: (9, 3, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][@....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 7
Coordinates: (10, 3, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.@...]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 8
Coordinates: (11, 3, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][..@..]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 9
Coordinates: (12, 3, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][...@.]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 10
Coordinates: (13, 3, 0)
Direction: East
Next symbol: ]

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][....@]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 11
Coordinates: (13, 3, 0)
Direction: South
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][....@]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 12
Coordinates: (13, 4, 0)
Direction: South
Next symbol: ]

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[]@##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 13
Coordinates: (13, 4, 0)
Direction: West
Next symbol: ]

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[]@##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 14
Coordinates: (13, 4, 0)
Direction: North
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[]@##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 15
Coordinates: (13, 3, 0)
Direction: North
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][....@]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 16
Coordinates: (13, 2, 0)
Direction: North
Next symbol: ]

####[#######[###
#[...[.......]##
[..[....]#[].@.]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 17
Coordinates: (13, 2, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[].@.]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 18
Coordinates: (14, 2, 0)
Direction: East
Next symbol: ]

####[#######[###
#[...[.......]##
[..[....]#[]..@]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 19
Coordinates: (14, 2, 0)
Direction: South
Next symbol: ]

####[#######[###
#[...[.......]##
[..[....]#[]..@]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 20
Coordinates: (14, 2, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]..@]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 21
Coordinates: (13, 2, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[].@.]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 22
Coordinates: (12, 2, 0)
Direction: West
Next symbol: ]

####[#######[###
#[...[.......]##
[..[....]#[]@..]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 23
Coordinates: (12, 2, 0)
Direction: North
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]@..]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 24
Coordinates: (12, 1, 0)
Direction: North
Next symbol: [

####[#######[###
#[...[......@]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 25
Coordinates: (12, 1, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[......@]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 26
Coordinates: (11, 1, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[.....@.]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 27
Coordinates: (10, 1, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[....@..]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 28
Coordinates: (9, 1, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[...@...]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 29
Coordinates: (8, 1, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[..@....]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 30
Coordinates: (7, 1, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[.@.....]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 31
Coordinates: (6, 1, 0)
Direction: West
Next symbol: [

####[#######[###
#[...[@......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 32
Coordinates: (6, 1, 0)
Direction: South
Next symbol: .

####[#######[###
#[...[@......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 33
Coordinates: (6, 2, 0)
Direction: South
Next symbol: [

####[#######[###
#[...[.......]##
[..[..@.]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 34
Coordinates: (6, 2, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[..@.]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 35
Coordinates: (7, 2, 0)
Direction: East
Next symbol: ]

####[#######[###
#[...[.......]##
[..[...@]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 36
Coordinates: (7, 2, 0)
Direction: South
Next symbol: ]

####[#######[###
#[...[.......]##
[..[...@]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 37
Coordinates: (7, 2, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[.......]##
[..[...@]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 38
Coordinates: (6, 2, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[.......]##
[..[..@.]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 39
Coordinates: (5, 2, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[.......]##
[..[.@..]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 40
Coordinates: (4, 2, 0)
Direction: West
Next symbol: [

####[#######[###
#[...[.......]##
[..[@...]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 41
Coordinates: (4, 2, 0)
Direction: South
Next symbol: .

####[#######[###
#[...[.......]##
[..[@...]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 42
Coordinates: (4, 3, 0)
Direction: South
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#@[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 43
Coordinates: (4, 3, 0)
Direction: East
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#@[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 44
Coordinates: (4, 3, 0)
Direction: North
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#@[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 45
Coordinates: (4, 2, 0)
Direction: North
Next symbol: .

####[#######[###
#[...[.......]##
[..[@...]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 46
Coordinates: (4, 1, 0)
Direction: North
Next symbol: [

####[#######[###
#[..@[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 47
Coordinates: (4, 1, 0)
Direction: West
Next symbol: .

####[#######[###
#[..@[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 48
Coordinates: (3, 1, 0)
Direction: West
Next symbol: .

####[#######[###
#[.@.[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 49
Coordinates: (2, 1, 0)
Direction: West
Next symbol: [

####[#######[###
#[@..[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 50
Coordinates: (2, 1, 0)
Direction: South
Next symbol: .

####[#######[###
#[@..[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 51
Coordinates: (2, 2, 0)
Direction: South
Next symbol: ]

####[#######[###
#[...[.......]##
[.@[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 52
Coordinates: (2, 2, 0)
Direction: West
Next symbol: .

####[#######[###
#[...[.......]##
[.@[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 53
Coordinates: (1, 2, 0)
Direction: West
Next symbol: [

####[#######[###
#[...[.......]##
[@.[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 54
Coordinates: (1, 2, 0)
Direction: South
Next symbol: .

####[#######[###
#[...[.......]##
[@.[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 55
Coordinates: (1, 3, 0)
Direction: South
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#@]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 56
Coordinates: (1, 4, 0)
Direction: South
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#@.][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 57
Coordinates: (1, 4, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#@.][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 58
Coordinates: (2, 4, 0)
Direction: East
Next symbol: ]

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#.@][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 59
Coordinates: (2, 4, 0)
Direction: South
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#.@][]#.][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 60
Coordinates: (2, 5, 0)
Direction: South
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[@.]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 61
Coordinates: (2, 5, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[@.]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 62
Coordinates: (3, 5, 0)
Direction: East
Next symbol: ]

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[.@]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 63
Coordinates: (3, 5, 0)
Direction: South
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[.@]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 64
Coordinates: (3, 6, 0)
Direction: South
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[@..[....[####
###[###[########

---

Step count: 65
Coordinates: (3, 6, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[@..[....[####
###[###[########

---

Step count: 66
Coordinates: (4, 6, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[.@.[....[####
###[###[########

---

Step count: 67
Coordinates: (5, 6, 0)
Direction: East
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[..@[....[####
###[###[########

---

Step count: 68
Coordinates: (5, 6, 0)
Direction: North
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[..@[....[####
###[###[########

---

Step count: 69
Coordinates: (5, 5, 0)
Direction: North
Next symbol: ]

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]@..[#.##]##
##[...[....[####
###[###[########

---

Step count: 70
Coordinates: (5, 5, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]@..[#.##]##
##[...[....[####
###[###[########

---

Step count: 71
Coordinates: (6, 5, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..].@.[#.##]##
##[...[....[####
###[###[########

---

Step count: 72
Coordinates: (7, 5, 0)
Direction: East
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]..@[#.##]##
##[...[....[####
###[###[########

---

Step count: 73
Coordinates: (7, 5, 0)
Direction: North
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]..@[#.##]##
##[...[....[####
###[###[########

---

Step count: 74
Coordinates: (7, 4, 0)
Direction: North
Next symbol: ]

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#@][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 75
Coordinates: (7, 4, 0)
Direction: East
Next symbol: ]

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#@][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 76
Coordinates: (7, 4, 0)
Direction: South
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#@][<[].##
#[..]...[#.##]##
##[...[....[####
###[###[########

---

Step count: 77
Coordinates: (7, 5, 0)
Direction: South
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]..@[#.##]##
##[...[....[####
###[###[########

---

Step count: 78
Coordinates: (7, 6, 0)
Direction: South
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[@...[####
###[###[########

---

Step count: 79
Coordinates: (7, 6, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[@...[####
###[###[########

---

Step count: 80
Coordinates: (8, 6, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[.@..[####
###[###[########

---

Step count: 81
Coordinates: (9, 6, 0)
Direction: East
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[..@.[####
###[###[########

---

Step count: 82
Coordinates: (10, 6, 0)
Direction: East
Next symbol: [

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[...@[####
###[###[########

---

Step count: 83
Coordinates: (10, 6, 0)
Direction: North
Next symbol: .

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#.##]##
##[...[...@[####
###[###[########

---

Step count: 84
Coordinates: (10, 5, 0)
Direction: North
Next symbol: <

####[#######[###
#[...[.......]##
[..[....]#[]...]
#.]#.[[][.....]#
#..][]#.][<[].##
#[..]...[#@##]##
##[...[....[####
###[###[########

---

Step count: 85
Coordinates: (10, 4, -1)
Direction: North
```

You leave the example dungeon after 85 steps.
