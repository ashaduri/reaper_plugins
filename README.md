# Reaper Plugins
***Various Cockos Reaper JS MIDI plugins (effects)***

## Plugin Descriptions

Please see a description header in each plugin's source code for more details.

- ### midi_crosstalk_fixer
  ***A simple cross-talk canceler***

  The plugin cancels any low-velocity MIDI Note-On and Note-Off messages
  that come right after a high-velocity Note-On message of another note, within
  a specific time period. This is useful when mixing various e-drum MIDI
  sources (e.g. several modules) which don't have shared crosstalk
  cancellation support.

- ### midi_note_learned_repeater
  ***Learned MIDI note repeater***

  This plugin uses two MIDI sources. The first one is a single MIDI
  note ("trigger-note"), for example a trigger attached to a bass drum.
  The second one is some kind of a MIDI controller, which sends
  notes ("change-notes") filtered by a configurable range.
  This plugin remembers the last received change-note and transforms
  any received trigger notes to have the change-note numbers.

- ### midi_note_pool_player
  ***MIDI note pool player***

  This plugin is useful for playing notes from a predefined list of notes, and much more.

  Receive a single midi note (trigger-note) and send a note of the
  same velocity from a pool of notes. The pool can be defined as
  a range of notes (min/max), or as a list. The algorithm of choosing
  the notes from the pool can be controlled (random, forward, etc...).
  A reset note may be received to reset the current position within
  the pool.

- ### midi_note_remapper
  ***MIDI Note Remapper***

  Transform one MIDI note number into another.

- ### midi_note_splitter_by_cc
  ***MIDI Note Splitter by CC***

  Transform a MIDI note number into one of two note numbers depending
  on whether a previously received CC value is higher or lower
  than a user-defined threshold value.
  This is useful for transforming variable hi-hat controller messages
  with a single hi-hat note into an open or a closed hi-hat note.

- ### midi_note_splitter_by_velocity
  ***MIDI Note Splitter by Velocity***

  Transform a MIDI note number into one of two note numbers depending
  on whether the Note-On's velocity is higher or lower than a user-defined threshold value.
  This is useful for transforming snare rim hit into a sidestick or a rimshot note.


## Copyright

Written by Alexander Shaduri <ashaduri@gmail.com>.

To the extent possible under law, the author(s) have dedicated all
copyright and related and neighboring rights to this software to the
public domain worldwide. This software is distributed without any warranty.
You should have received a copy of the CC0 Public Domain Dedication
along with this software. If not, see:
https://creativecommons.org/publicdomain/zero/1.0/
