# The Way

A gamified Catholic discipleship app prototype: a living island world, daily quests, three island journeys, a parish community with cell groups and group chat, and a personal profile.

## Run it

**Easiest:** double-click `index.html`. It opens in your browser and works offline. Fonts load from Google Fonts when you are online; otherwise a fallback font is used.

**As a local server** (recommended for testing on your phone over the same Wi-Fi):

```
cd the-way
python3 -m http.server 8000
```

Then open http://localhost:8000. On your phone, open `http://<your-computer-ip>:8000`.

Node alternative: `npx serve .`

## 2D / 3D quest maps

The Home path and all three island journeys open in 3D by default. Use the **2D | 3D** switch under the top bar (or Profile > Accessibility > Quest map view) to change. Drag to look around and slide along the path, pinch or scroll to zoom, and tap a marker, a tree or the landmark.

## The Holy Land (3D)

Tap the round **Holy Land** button on Home, or the big card at the top of Explore. Walk with taps (or arrow keys / WASD on a computer), drag to look around, pinch or scroll to zoom. 17 Bible landmarks, from Noah's Ark to the Road to Emmaus, each have a story, a Scripture reference and a reflection; praying there adds a stamp to your Pilgrim Passport.

The 3D engine (three.js r128, MIT licence) is included in `vendor/`, so it works offline too. Running from a local server is the smoothest way to use it.

## Demo tips

- On the welcome screen tap **Explore with a sample journey** to start as Jillian with progress, island steps and membership in the *Emmaus Walkers* cell group (open Community > Groups to chat).
- Group mates in demo groups reply automatically to your chat messages.
- Create your own group in Community > Groups. You become the group leader and get a sample join request to approve.
- To start over: Profile > Delete my account & data.

## Notes

- The app is one file (`index.html`) plus `vendor/three.min.js` for the 3D map. No build step.
- Data is saved in the browser's localStorage on that device only. Sign-in, age verification, moderation and chat are simulated.
- Verses use the public-domain Douay-Rheims translation as a placeholder for an approved, licensed translation.
- The parish list (32 entries) must be verified against the Archdiocese of Singapore's official directory.
