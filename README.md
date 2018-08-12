# RadioBuddy

**Laconic:** 
A music player which learns the user's preferences over time

***
**Make/Install/Run Instructions:**

***
**Problem to Solve:**  
Current music players order their playlist performance by either random shuffle or the pre-defined ordering of the playlist; changing to a different order, or changing playlists, must be done manually. Preferences change over time; it may be useful to allow the player itself to take note and tailor its music selection to the user's period of moods.

To solve this, create personal radio programming which uses machine learning techniques to 'learn' a user's listening habits and adapt, using only user input and a library of sound files.

***
**User Scenarios**
*include persona and a possible work flow; https://www.joelonsoftware.com/2000/05/09/the-process-of-designing-a-product/*

*New User (computer-savvy)*
*New User (computer-naive)*
*Experienced 'Power' User*

***
**Project Goals:**
*Should be measurable; essentially a feature list*

*Must Do*
- Play music files (list formats in technical design)
- Allow user to skip songs
- Use minimal necessary input from the user (such as 'skipping' songs), with adaptability for more sophisticated start later.
- Carry out 'cold start' (with just the song library) 
- Carry out 'warm start' (use pre-defined pattern knowledge, allow import/export of profiles, allow for multiple users).
- Default objective function.
- Allow songs to be added to and removed from the library of music files without resetting.
- Simple GUI
- Simple CLI

*Limbo (all should move to Must or Won't by ship)*
- Configurable objective function (should not require changing the code to change the function unless adding completely new data inputs).
- Learn to manage volume
- Allow user to queue up specific song by choice
- Learned-model visualization; easily digestible view of play probabilities or other abstraction of decision model.

*Won't Do*
- Learn volume management
- Find new songs
- Audio visualization

***
**Brainstorming:**
*Stream-of-consciousness ideas. May be cleaned up at later date.*

People are most motivated to change what they don’t like; focus on skips or something like that instead of ratings. May need overrides (or search or whatever) to learn certain rare behavior.

Other inputs available for correlation building: weather (precipitation, temp, humidity), time of day/week/month/year, list of songs.

Allow songs to be added/removed without resetting (scan folder automatically. Don’t remove old song data automatically. Tie to mp3 metadata OR to filename).

Should probably never play one song twice in a row. Queue latest X and don’t replay any in list (unless there are fewer than X total songs, naturally).

Add new just below level of current minimum (if high numbers are no-go)

Line up next song while one is playing (ready in case of skip).

Should be able to naturally avoid Christmas Songs any time but Christmas, and play them then (or other seasonal songs; may be hard to learn this behavior).

***
**Technical Design**
*Add technical design notes here: algorithms, languages, platforms, etc. Refer to external documents if necessary.*

Languages:
- Python

Music FIle Formats to Support:
- .wav
- .ogg
- .mp3

***
**Alternate Project Names**
*Describe deeper meaning, if applicable; https://blog.codinghorror.com/whats-in-a-project-name/*
- Radio Buddy
- Viola
- DJ ME
