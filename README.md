The new NowPlayingWidget.exe is ready. It now opens an icon near the Windows clock instead of a black window, and it offers 6 styles inspired by your screenshot.

The rendering of the 6 styles and the selection page is verified in the screenshot. I haven't been able to test Spotify playback or the icon on a real Windows machine. These two parts will therefore need to be confirmed on your end.

The Styles

Classic: the previous green card, with a progress bar.
Window: macOS style, with the 3 colored dots.
Neon + Waveform: cyan title, waveforms, and a pink bar at the bottom.
Terminal: the text `root@now> ./nowplaying` with a bar made of ####.
Compact: album art, title, and time side-by-side, in brown and orange.
Vertical: large album art with the title below, in purple.

Each style displays the album art, title, artist, elapsed time, and duration.

Usage

Open the Spotify desktop application and start a song.

Launch the .exe file. No window will open. A notification will appear indicating that the widget is active, and a green icon will appear next to the clock.

Right-click on the icon, then select "Choose a style / copy link…". The style selection page will open in your browser.
Copy the link for the desired style and paste it into OBS (Browser Source, with the size indicated below the preview).

Right-click on the icon

Copy widget link: copies the link for the Classic style.

Launch with Windows: starts the widget on your PC.

Exit.

If you relaunch the .exe file while it's already running, it will simply reopen the style selection page.

Settings on the style selection page

a custom accent color;
the option to remain displayed when paused;
the option to always display the widget, even without music;

The option to accept players other than Spotify.

How it works and its limitations

The widget reads the Windows "media controls," the same source as the volume control. It therefore retrieves the title, exact position, and album art from Spotify, without a Last.fm account or API key. If this fails, it falls back to the title in the Spotify window, with an estimated position.
If nothing is displayed while Spotify is playing, open http://localhost:8765/api/debug in your browser and send me what it shows. This will tell me what Windows is seeing.
Windows may display the SmartScreen warning on first launch because the .exe file is not signed. Click on "More info," then "Run anyway."
My styles are inspired by yours but are not exact copies of Amuse.

<img width="1888" height="900" alt="image" src="https://github.com/user-attachments/assets/07a1e8d6-bddf-41b4-81a5-8df49fd503ab" />
