# Cor Photos

Cor Photos turns the photos on your phone into real prints, posted to your door. You drop your
photos in, see every one at the size it will print, line it up, add a border or a caption if you
want one, and order. A professional print lab makes the prints and ships them.

I'm building it on my own. The first line went in on 7 September 2026. Version 0.8 came out on 8
November, about two months and six hundred commits later. The shop opens at 1.0.

The shop is built in a private repository, so there's no code here. What's here is the story: what
Cor Photos is for, and every hurdle I hit getting it this far, version by version. Most of it went
wrong at least once before it went right. All the numbers below were measured at the time.

**Site:** [corphotos.com](https://corphotos.com)

## Where it stands

**Version 0.8.3 · 9 November 2026 · in testing before opening day**

- **The editor is done.** Every photo shows at its true size, as it will print. Line it up, add a
  border or a caption typed straight onto the print, adjust light and colour, and check it's sharp
  enough for its size, one photo at a time or a whole page at once.
- **The catalogue is done.** Every print has its own page, in four lines: The Classics, Squares,
  Specials and Gallery Grade. The Gallery Grade art papers and two metallic foils are coming soon.
- **The pre-launch build is done.** A new checkout, shipping speeds, and order emails that stay in
  one thread. Ordering works from start to finish, and the site says plainly that it's still in
  testing until 1.0.

## The problems Cor Photos solves

Printing photos from a phone sounds simple. In practice it goes wrong in a lot of small ways, and
each of them is a reason something in Cor Photos exists.

**You can't tell how a crop will come out.** A print is a fixed rectangle and phone photos almost
never match it. An iPhone photo is 3:4, a saved Instagram post is square, and a 4×6 is 2:3.
Something gets trimmed, and usually you find out when the heads come back cut off. In Cor Photos
every photo is shown as the print it will be, trimmed exactly where it will be trimmed. Fill covers
the print and trims evenly. Fit keeps the whole photo. You can drag the photo inside the print,
with thirds lines, and zoom, turn, straighten or mirror it. It never guesses where your subject
is. A guess that moves someone's head out of a family photo is worse than a trim you can predict.

**What you edit on screen isn't quite what gets printed.** When the preview and the print file are
made separately, things drift. The lab only ever receives a finished file, so every edited photo is
redrawn at print resolution, with its border and captions, from the same layout the screen uses.
The colours on screen and in the file agree to within 1/255.

**Borders come back cut or uneven.** A lab's printable area isn't exactly the paper's shape. The
everyday 4×6 area is a little squarer than 2:3, so a file made at the "right" shape gets cropped,
and a thin border comes back thicker on one side or missing. Every size in Cor Photos carries the
lab's real print area. Edited files are made to that exact shape with a bleed around them, so the
lab only trims what was added.

**Blurry prints from small files, with no warning.** A photo that looks fine on a phone may not
have the pixels for a big print. Saved social posts, screenshots, heavy crops and old phones are
the usual causes. Cor Photos reads the real pixel size from the file itself, works out the
sharpness for the size you picked after any crop, and grades it in plain words with the real DPI
beside it. If a print will look soft because you zoomed in or picked a size the photo can't hold,
checkout lists it with its own thumbnail and asks you to tick it, or make it smaller. Nothing is
refused. It's your photo.

**Warnings that treat every old photo as a failure.** Old phone photos and scans are small. A normal
quality meter calls them "Poor" even printed small, and checkout nags about pictures you chose on
purpose. Here a small photo is judged against its own best. It starts at Full detail and only drops
as you zoom in or go bigger.

**You can't see how big a print really is.** Most sites draw every size into the same box, so a 4×6
and an 8×10 look alike. I once had a 3×4 on screen that looked bigger than a 4×6. Every print in
the editor is drawn to one shared scale, so an inch is the same across the page and an 8×10 is
plainly bigger than a 4×6. The catalogue draws each size where it would live: a 4×4 on a shelf, a
4×6 on the fridge, an 8×10 on the wall beside a light switch at real size.

**Not knowing what the paper will look like.** Gloss or lustre is usually one word in a dropdown.
Cor Photos has a Simulated view where the print is a sheet you tilt by dragging, and the light
moves across it in a drawn room, by day or by night. Gloss shows a window's reflection, lustre a
soft sheen, and the back of the print catches light too. Held still, it shows your photo's true
colours with no paper tint over them, because a tinted preview means you never see the real photo.

**Wide-colour photos printing flat.** New phones save photos in wider colour spaces than labs
expect, and the colours print flat. Cor Photos converts those photos on your device before upload.
Normal photos are never touched.

**Prints that arrive sideways.** Phones often store a photo on its side with a tag saying which way
is up, and labs warn that the tag can make a photo print the wrong way. Cor Photos turns the actual
pixels instead. For most photos that's lossless, with nothing recompressed.

**Photos carry your location.** Phone photos carry GPS, device details and edit history. All of it
is removed on your device before upload, and the location is never even read. The server refuses
any file that still carries hidden data, no exceptions. The date and camera are noted before
stripping so you can sort by them, and they never go with your order.

**Not knowing what happens to your photos afterwards.** Photos are kept on a fixed schedule: a
couple of hours after you close the tab, 48 hours in a saved collection, 120 days after an order
ships for reprints. There's no selling of data, no ad trackers, no marketing email, and so no
cookie banner.

**iPhone and camera files that won't upload.** HEIC, RAW and TIFF get refused or need converting
first in a lot of places. Cor Photos takes JPEG, PNG, HEIC, WebP, AVIF, GIF, BMP, TIFF and the
mainstream camera RAW formats. iPhone photos are converted on your device. RAW files print the
full-size JPEG the camera already made inside them.

**Your photos are on your phone, but choosing is easier on a computer.** Scan a QR code in the Booth
with your phone and the photos you pick land on the computer, already cleaned and turned upright.
No app and no account.

**Ordering a whole trip is painful.** One order holds up to 500 photos. Drop in a whole folder.
Uploads are paced so a big batch doesn't fail, sizes and borders and captions apply to a whole
group at once, and the editor was tuned until 500 photos felt like one.

**Borders and captions are hard or impossible.** Most services give you a white border at best.
Here there are four border styles in any colour, including colours taken from the photo, and
captions typed straight onto the print, on the photo or in the border. A caption with no colour
picked reads the photo under its words and prints dark over bright parts and light over dark ones.

**Mixed orders turn up in three boxes.** Mixed sizes made on different lines get split into
separate parcels without warning. The lineup is designed so every size in a shop shares one box,
and if a print or two would travel alone, Cor Photos tells you before you pay and offers to move
them. Shipping comes down as you add prints, until it's free.

**Accounts, apps and coupon codes.** There's no account and no password, ever. No app. No coupon
codes. Prices are on the page.

**Losing an hour of choices to a refresh.** Pages live in the browser tab, so a refresh brings
everything back, including where you were.

**Not being able to take an order back.** After you order, the card is only held for a short window
and the order page counts it down. Cancel in that window and no money moves. If something arrives
damaged or wrong, it's reprinted with nothing posted back.

**Sites that only work in Chrome.** It's built to work the same in Safari as in Chrome, and on a
phone as on a computer.

**What it isn't.** Prints only: no frames, mugs, books or canvas. It isn't photo storage, an app or a
subscription. It isn't international yet, it's US addresses only. And it isn't finished, and says so
on the site.

## The road to 1.0

| Version | Step | |
|---|---|---|
| **0.1** | The Booth, checkout and order tracking | Done, September 2026 |
| **0.2 to 0.4** | The first editor | Done, September 2026 |
| **0.5** | The editor rebuilt, the first catalogue | Done, October 2026 |
| **0.6** | The editor | Done, October 2026 |
| **0.7** | The catalogue: every paper and size, each with its own page | Done, November 2026 |
| **0.8** | The pre-launch build | Done, November 2026 |
| **1.0** | Open to everyone | Next |

Versions start with 0 while the shop is being built. Each new middle number is a big step and gets
its own entry in the [changelog](CHANGELOG.md). 1.0 is opening day.

---

## Every hurdle, version by version

This is the long part. For each version: what went wrong, why it went wrong, and what fixed it.

### 0.1 · From a blank folder to a working shop · 7 to 27 September

#### 7 September: I built it, put it live, and threw it away the same day

The first version went live on corphotos.com on day one, and it couldn't sell a single print. No
print lab had been chosen. The prices were placeholders. Nothing confirmed a payment except a
redirect to a "success" page, which anyone can type. The check that warns about blurry prints was
fully worked out in the code and never shown to the customer, which was the whole reason it had
been built early.

That evening I deleted all of it. Pages, routes, the catalogue, pricing, the order model, the lot.
I kept the domain, the deploy pipeline, the empty database and the payment account, and archived
the old build rather than destroying it. What had blocked it wasn't code. It was decisions nobody
had made yet: which lab, where the prices come from, what happens to people's photos, the legal
pages. So the rebuild started with those.

Other things from day one:

- A "coming soon" page stayed on the home page for four deploys in a row after I'd switched it off.
  Adding a random query to the address showed the right page, so something between the site and
  visitors was holding the old copy. Changing the cache settings in the framework did nothing. In
  the end I cleared the cache by hand, and from then on every deploy clears it automatically.
- Orders disappeared between one request and the next. They were kept in the server's memory, and
  the hosting runs lots of separate copies of the server, each with its own memory. The request
  that saved an order and the one that read it back often landed on different copies, so the
  confirmation page could say "missing order" for an order placed a second earlier. Orders moved
  into the database the same day.
- I chose the print lab and tested everything against its live system instead of trusting the
  documentation, which turned out to be wrong in two places. One product line I'd been told I
  needed wasn't needed, and the finish (lustre or gloss) was a required field that wasn't mentioned
  anywhere. A quote without it just fails.
- The lab downloads each photo from a web address rather than taking an upload. That meant private
  photo storage had to exist on day one, and it forced the privacy design early: photos sit behind
  addresses long and random enough that they can't be guessed. Short-lived download links were
  ruled out, because the lab might retry a download long after a short link had expired.
- Lustre became the default finish. Gloss is the shiny drugstore finish that shows fingerprints,
  and the drugstore photo counter is exactly what Cor Photos is meant not to be. Gloss came back as
  an option a week later.

#### 8 September: payments, uploads and the first Booth

- Every customer would have hit a "page not found" the moment they paid. The return address after
  payment put the payment's own ID where the order page expected an order ID. I caught it before
  anyone paid, and it has a test now because the wrong version looked plausible enough to come back.
- Accounts were decided as "never", not "later". What people actually need is to find an order
  again, and an order number plus the email it was placed with does that. The email has to match
  too, because the order page shows a full home address and order numbers leak in screenshots.
- Order numbers became "COR-" and six characters, with every look-alike letter and digit taken out
  (0 and O, 1, I and L, U) so they can be read out over the phone. Every failed lookup gives the
  exact same answer, so the page can't be used to discover which order numbers exist.
- There was no way to upload a photo at all. Storage existed, and so did the route that serves
  photos back out, but nothing accepted one in. Uploads became one request per photo, so one bad
  file can't fail the whole batch.
- The server's "check" of a photo's size was reading the width and height the browser sent, which
  meant it was checking the browser's word against itself. It reads the real size from the image
  now.
- I deleted the landing page. It stood between people and the one thing they came to do. The Booth
  became the front page, open and ready for photos.
- Dark mode came with white text boxes. Typing was cream on white, and disabled buttons were white
  on grey at about 2:1 contrast. Every colour on the site had been written as a fixed value, so a
  second theme couldn't even be described until they all became named colours.
- Changing one photo's quantity rewrote 10.1 MB. Measured with 40 camera photos: the draft was
  saved after every edit and carried every image in the order with it, so one tap rewrote all
  forty. At about 70 photos it would have been hundreds of megabytes per tap. Images moved to their
  own store that's written once per photo.
- A line in the order summary read "2 × 4×6", which is three numbers where only the first is a
  count.
- Tax wasn't being worked out at all. It is now, at checkout, for the delivery address.

#### 9 September: iPhone photos, sideways prints and RAW files

This was the longest day of the first month.

**Sideways prints.** A phone saves a portrait photo as a landscape grid of pixels, with a small tag
saying which way is up. Stripping hidden data for privacy stripped that tag too, and the photo
ended up on its side. The only fix at first was to redraw the photo and save it again, which
quietly lost quality on the most common photo the site would ever see.

So I kept the original bytes and wrote back a single, freshly made orientation tag. There are only
eight valid versions of that tag, so the server just compares bytes. It worked, and the image data
came out byte for byte the same as it went in.

Then I read the lab's guidance, which said the opposite: files must not carry rotation tags,
because the lab turns images itself to fit the paper. A tagged portrait would have been fitted to a
landscape print with the person lying on their side, and nothing on my side would ever have shown
it.

The final answer was lossless rotation. A JPEG is a grid of 8×8 blocks, and a quarter turn can be
done by rearranging the blocks without rebuilding a single pixel. Turning a photo and turning it
back gives the same file byte for byte, and eight quarter turns give a file exactly the original
size. Anything unusual that it can't turn safely falls back to the old way, and every result is
checked before it's trusted, so a bug can only cost quality, never break a photo. The tag code
and the thirteen tests guarding it were deleted the same day.

**iPhone photos.** I'd assumed iPhone HEIC files were a quality problem. They were a much bigger
one: Safari is the only browser that can open them. Chrome just says the format isn't supported.
But a HEIC photo is really one frame of video in a wrapper, and those same browsers play that kind
of video fine. So the Booth unwraps the photo and hands it to the browser's own video decoder.
There's nothing to download and nothing extra to load.

Then a real iPhone photo turned out not to be one image at all. It's 48 tiles in a 6 by 8 grid,
each compressed separately. The tile layout is stored somewhere other than where you'd expect, the
last row and column overhang and have to be trimmed (eight 512-pixel tiles make 4,096 pixels for
a photo 4,032 wide), and the tiles come back from the decoder in any order, so they're matched up
by timestamp. A 12-megapixel iPhone photo now comes together in about four seconds with no seams,
which I checked on a night sky that runs across every tile.

Then every iPhone upload failed in Safari, while the exact same photo worked in Chrome. When Safari
redraws a photo, it copies the original's hidden data into the new file, so the "cleaned" photo
still carried camera and location details and the server, correctly, refused it. Now everything the
browser redraws is stripped in one place on its way out.

**RAW files.** I wanted someone with a serious camera to be able to drop RAW files straight in. No
browser can read RAW and no lab accepts it. But every RAW file already contains a finished JPEG the
camera made, and on a Canon 5DS R it's the full 8688×5792 image. Side by side at 100% with the same
file developed properly on a Mac, I couldn't tell them apart. The trap was that Canon also stores
the raw sensor data in a JPEG-like form that's far bigger, so "take the biggest JPEG" grabbed a
54 MB sensor dump that nothing could open. On a real shoot of 230 RAW files, all 230 came out at
full size, 13.35 GB of RAW became 0.94 GB of uploads, and the slowest one took 57 ms.

The rest of 9 September:

- The full-screen viewer drew the small 720-pixel preview stretched across 1152×768 screen pixels,
  so it looked soft. It loads the original for the one photo on screen now. Exactly the same
  problem came back in other places two months later, in 0.8.3.
- The size preview said "1x" when it really meant "whatever fitted". On a phone it said 1x while
  showing half a 4×6. Now 1x means real size, "Auto" means whatever fits, and a badge says in words
  when what you see is smaller or bigger than the real print.
- Photos sent from a phone only exist on the server, but the Booth assumed every photo was also on
  the device. On a reload, those photos would have silently disappeared.
- The phone-to-computer QR code. The obvious QR library pulled in a whole command-line toolkit just
  to draw squares, so I used one with no dependencies. A leaked pairing link can add photos to a
  Booth but never see any.
- Google Photos had closed the old way of reading a library, so the only route is Google's own
  picker, where people choose the photos and only those reach the shop. The photos still arrive
  with hidden data, which gets cut out without touching a single pixel.
- The big carriers all block their tracking pages from being shown inside another site, so the
  order page has its own tracker with a link out.
- Nothing ever asked the lab what had happened to an order. An order reached "printing" and stayed
  there forever, even with the parcel already on someone's doorstep. Now an hourly check asks about
  every order in progress. The tests then caught a bug where a tracking number arriving on its own
  was thrown away.
- The shop sent no emails. Someone could pay, close the tab and have nothing but an order number
  they might not have written down. Emails are built from tables with inline styles, which looks
  like 2005 and is correct, because that's what every email app can actually show.
- A safety note in my own docs said test orders were harmless for a reason that was no longer true.
  They were harmless for a different reason. A safety note that describes the wrong mechanism is
  worse than none.
- A refund made by hand didn't stop the printing, so the money could go back and the prints still
  ship. Refunds now cancel at the lab first. Cancelling always stops the printing before any money
  moves, because the other way round risks prints made and paid for by nobody.
- I changed the default print size to 5×7 and changed it back to 4×6 the same day. 4×6 is what
  people mean when they say photo prints.

The Booth with 100 photos, measured before and after that day's work:

| | Before | After |
|---|---|---|
| Dropping in 100 photos | 93 ms | 40 ms |
| Selecting one photo | 17 to 25 ms | 6 to 7 ms |
| Opening the viewer with 300 photos | 71 ms | 22 ms |
| All 100 prepared and uploaded | 109 s | 53 to 64 s |

Every change was redrawing every photo on the page, and every photo was using its full original as
a thumbnail, so 100 tiles decoded 100 full-size images to fill frames 94 pixels wide.

#### 10 and 11 September: the things nobody sees

- Ordered photos were never deleted, while the privacy page promised a deletion schedule. Getting
  the timing right meant reading the reprint promise carefully: it runs from delivery, not from
  shipping, so deleting too early could destroy a photo while someone could still ask for a reprint.
- The cleanup job was deleting things that weren't photos. It cleared everything in storage no
  order pointed at, including sign-in records and phone pairings. Nobody noticed because those were
  short-lived anyway.
- The hourly check is the only thing that moves orders along. If it died, every order would freeze
  and nothing would say so. Each run now records what happened, a run where every check failed
  counts as broken, and an alert goes out when it breaks and again when it recovers, not every hour
  in between. An hourly email during an outage just teaches you to ignore it.
- The site had no icon, so every tab showed a blank page. I drew a 4×6 print with "Cor" written on
  it in front of the stars of Leo. Icons draw where web fonts don't load, so the lettering had to
  be turned into shapes, and the usual tool for that wasn't reachable, so I wrote a small font
  reader from scratch.
- iPhones ignore SVG icons. Saving the site to a home screen gave a screenshot of the page. The
  iPhone icon has to be full-bleed (iOS rounds the corners itself, so pre-rounded corners show
  notches) and has no transparency (iOS fills it with black). A few days later Safari on the Mac
  painted the same transparent corners white.
- The order page shows a customer's name and address and had nothing telling search engines not to
  list it. All it would take is someone pasting their own order link into a forum once.
- The whole shop was also answering on a second, default web address from the hosting, with the
  same checkout and the same orders. It's switched off in the settings now so a later deploy can't
  quietly turn it back on.
- The image that shows when you paste the link in a message was squashed by 47%. The Mac's
  thumbnail tool draws every SVG as a square, and my script stretched the square into a rectangle
  instead of cropping it. The script measures its own output now, because a squash is invisible
  until someone shares a link. My first drafts used blank white prints, which looked like
  stationery. A white border around colour reads as a photograph.
- Google sign-in failed with "redirect_uri_mismatch", an error that doesn't say what it expected or
  what it got. It needed every address the site runs on, written two different ways.
- A clean deploy went out and nobody could see it. The deploy script now builds, deploys and clears
  the cache, and stops loudly if it can't clear it. A deploy nobody can see is worse than one that
  stops and says why.
- Checkout trusted the browser about the photos. You could have paid for a photo that was never
  uploaded, or ordered an 8×10 of a thumbnail by sending a fake size. The server now checks each
  photo in storage and uses its real size.
- One customer could have got a dozen identical receipts, one for every retry when the lab refused
  an order.
- Deploying without me at the keyboard failed twice, each time with an error that pointed the wrong
  way.
- Search engines are allowed to list the site, AI answers can use it, and AI training can't. A shop
  wants to be found. Training isn't a way to a customer.

#### 14 to 17 September: every format, the first catalogue, and the upload crash

- Three RAW formats already on the list couldn't actually be read, because they aren't built the
  way the others are. Some Sony and older Fujifilm cameras save a much smaller preview than the
  sensor, so the Booth says so when that happens.
- The site went behind a "coming soon" page so only my own devices could see it. The cache ignores
  cookies, so a real page cached from my browser would have been shown to everyone. While the wall
  was up, nothing was cached at all. It came down on 2 November and it's staying down.
- The first full catalogue was 168 products, every size and paper, with every cost read live from
  the lab. I cut it back the same day to the sizes people actually know from the drugstore. Then
  the live system surprised me: "prints" weren't one shipping lane. Regular sizes ship from one
  place, a couple of in-between sizes from another, and the squares and minis from a third, each in
  its own box.
- That made a rule I've kept ever since: shipping costs the customer the least it possibly can, and
  an order never gets split into two boxes the lineup could have avoided.
- On several art papers a 4×6 only exists as a sideways product. That's the only way to get it.
- About 90 camera photos went in and 36 uploaded, then every one left failed at once. Each upload
  was being carried through several layers of the server, so three big photos at the same time
  pushed it over its memory limit, and that kind of error fails everything in flight together. Now
  the server reads only the first few kilobytes of a photo, where everything it checks lives, and
  streams the rest straight into storage. The Booth limits how many megabytes are moving at once,
  retries what fails, and gives failed photos back to the queue after a reload. I moved the hosting
  up a plan the same day.
- Every visit made the server build pages that never change between deploys, 30 to 180 ms each.
  Those pages are served ready-made now, in 2 to 3 ms.
- I spent a day undoing 8 September: the rates in the sidebar, the tall footer, the rounded pill
  buttons and the delete mode all went.
- Two pages could both end up called "Page 1".

#### 17 to 20 September: the editor is born, and gets rebuilt every few hours

On 17 September alone there were 48 commits. Most of them were the editor being built, looked at,
and changed again.

- Colour. Newer phones and cameras save photos in wider colour spaces than sRGB, and the lab's
  printers read every file as sRGB, so those photos would print dull. The Booth now reads each
  photo's colour profile and converts only the ones that need it, on the device, before upload.
  It's never been checked against a real print yet, so the plan is a known colour swatch on the
  first real order.
- The little question a new page asks ("what's this page for?") was redone about eight times in one
  day: single choice, then multiple choice, then no heading, then one line back, then a button that
  says what it does instead of "Okay".
- I built the print as a 3D sheet you can pick up. First you could carry it around the screen. The
  next commit says "panning was the wrong verb": the print stays in the middle and a drag turns it,
  edge on, past its blank back, and round again. At first it stayed at whatever angle you let go,
  which meant every look started with straightening it, so now it settles back square.
- Four layout traps in one go while putting a 3D print on screen. A scrolling box flattens 3D for
  everything inside it, so the tilt looked like a skew. A percentage height measured against
  nothing let a tall photo walk straight out of its frame. A centred control bar was only offered
  the space to the right of centre and wrapped onto two lines. And a box that measures itself by its
  contents measured zero, so the print came out 0 by 0.
- The first shine effect was a white sheen swept across the photo. That's the one thing a page for
  judging a print must never do, so it came out the same day. It was the start of a back-and-forth
  about light that lasted until November.
- The quality meter was redone four times in two days: a big dashboard, then one line of text, then
  a thin scale with 180 marked (where a print starts to go soft) and 300 (where the lab has no more
  use for pixels), then the scale with a "?" box that explains it.
- The two views went from Simulated and Regular, to Print and Photo, to Simulated and Standard, which
  stuck.
- The print looked like a picture stuck to a white wall. There was no light in the room, and its back
  glowed like a screen. One lamp went in. Then, held flat, gloss and lustre looked exactly the same
  until you tipped the print almost thirty degrees, and nobody knows to do that.
- I read up on the actual paper (resin-coated photo paper, glossy or a fine pebbled lustre, about a
  fifth of a millimetre thick) and redrew it to match. The lustre grain showed a grid, because it
  was one small tile repeated. It became one large seamless texture, seeded from each photo so no two
  prints have the same grain. The reflection only moved up and down, so turning a print sideways did
  nothing. Lustre doesn't show a sheet of glare at all, only its grain catching the light, and gloss
  stretches a light into a streak along the way it bends.
- The print lagged and got stuck mid-turn. The way it was written, every update anywhere on the page
  (an upload tick, the clock) threw the print away and built it again from nothing, decoding the
  full photo each time. If that happened mid-drag, the thing holding your pointer was destroyed and
  the release never arrived, so the print stayed turned in mid-air. After the fix a frame took 8 ms
  instead of 24.
- A fast flip still stuttered, because each frame was repainting four or five photo-sized layers,
  about a hundred a second. Now everything that changes during a turn is something the graphics card
  can move without repainting.
- Pressing Escape in a small info box closed the whole editor.
- Picking photos inside the editor could mix prints from two different labs, which would make a bulk
  change wrong. It took four tries in a day to make picking respect that.
- A quick review before launch found nothing critical: prices can't be changed from the browser,
  payment notices are verified and handled once, and uploads are checked by their real bytes. What
  was missing was protection from abuse, which the coming-soon wall had been hiding. Every part of
  the site now has a limit on how often one visitor can call it. Payment notices are never limited,
  because a held-back notice is someone who paid and isn't being printed.
- The first visit on plain http was served over http. Now it only gets a redirect.
- What should the simulated print show when it's lying still? It was settled twice, once each way, in
  two hours. On lustre, every grain put a bright speck where the light fell, and on a dark sky that
  made lustre look like the cheap print. Then the rule became "the print is the photograph until you
  pick it up". Then that went too far, because a gloss print on a table does reflect the room. At
  quarter to eight that evening I reverted the whole run. At eight it was rebuilt as the rule
  that held: standing still, it's the file's own colours on paper, and the room's light comes with
  your hand.
- I made three cuts to fix a stutter, then found the stutter was my laptop in Low Power Mode. All
  three went back in.
- Switching between Simulated and Standard swapped pictures in one frame, which reads as a glitch. The
  browser's own morph between them made the back of the print show the photo mirrored, and turned
  every frame of a turn into a repaint. That switch was rebuilt three more times.
- A panel meant to be two thirds of the width got shrunk to two thirds of the height instead.
- The animation when you change a print's size took eight tries in one evening. The two copies moving
  at once read as a jitter. Moving together read as "a column of water". Touching, they read as a
  mechanism. Overlapping, for a fifth of a second there were two whole photos on screen, a double
  exposure. The final one used a damped spring, measured landing 41 pixels past its mark, 6 back,
  then still. Four days later all of it was replaced by the print simply growing or shrinking in
  place.
- A 4×6 was drawn wider than an 8×10. Every print was stretched to fill the screen, and a 4×6 is the
  wider shape. That's the one thing the viewer exists to show, said backwards. Prints are measured in
  inches now, with one inch the same for every size.
- The paper page said our paper was the same kind a one-hour photo counter hands you. Most of those
  counters don't use it any more. I took out every claim about anyone else. Say what ours is, not
  what anyone else's is.

#### 21 to 27 September: two papers, a receipt, and the first release

- Offering the same sizes on a second, archival paper broke the question "which lab makes this?",
  which until then was answered by the size. A size can't answer it any more, so it's asked of the
  product.
- I renamed the two shops after their papers and renamed them back twenty minutes later.
- Receipts showed "4×6" for both papers, and the confirmation email would have printed an internal
  product code to someone's inbox.
- "Worth knowing", a short list of advice above Checkout, has two rules: never wrong and never
  scolding. Its first version broke the first rule within a minute, telling someone their 4×6s on the
  archival paper couldn't be made anywhere else.
- Cancelling an order used to mean charging the card and refunding it. Now the card is only held at
  first, for a short window you can cancel in for nothing, and charged when the window closes. The
  charge comes before the lab is told, the mirror of cancelling, where the lab is stopped before money
  goes back. Never let the irreversible half happen first.
- The lab gives 14 days from delivery to report a problem. The site promised 30, which meant days 15
  to 30 would have been reprints nobody else would pay for. It's 14 now, with a photo of the print,
  and nothing is ever posted back.
- A charge someone doesn't recognise on their statement turns into a dispute. The statement line now
  carries the shop's name and the order's six-letter code. Card networks refuse statement lines that
  are all digits, and the code alphabet makes an all-digit code about three times in 10,000, so those
  keep a letter in front.
- The payment library was a year and four major versions behind. Moving it forward meant checking
  every breaking change in four releases against what the shop uses.
- The Standard view had been wrong for a week. It showed a wide photo whole, uncropped, under a 4×6
  label, which is what every other program shows and exactly what Cor Photos is meant to fix.
  Standard now shows the print flat: its real shape, its real crop, its real size next to the others.
- The paper explainer started with an animation that stood still for over two seconds. I wanted a
  short drawn film for each paper: a walk through a wood towards a low sun for one, a night sky photo
  landing on a wooden table for the other. The first forest was drawn to look realistic and didn't
  ("the trees don't look realistic"), so it was redrawn as a storybook illustration. The copy had
  said the archival paper was heavier and the film drew its edge twice as thick, but the lab doesn't
  publish a weight for the everyday paper, so every such claim came out.
- The Learn page on shipping had hand-typed examples, and one had already gone wrong. Every number on
  that page is worked out from the real rules when the site is built now. And customer-facing text
  states the price and the rule and stops. It doesn't explain where the money goes.
- Low resolution went from a wall to a question. Before, every size except the 4×6 was refused under
  a set sharpness. Now nothing is blocked. Checkout lists each soft print by its thumbnail, size and
  grade, each with its own tick box, and offers a smaller size that prints sharp. The server checks
  it again from the real stored file before any order exists.
- Editing "All" with both shops open moved every photo in both shops onto one paper.
- The order panel was, in my words at the time, "unaligned, not serious, very clunky". Prices ended
  20 pixels short of the totals, three kinds of line competed, and the page list cut off mid-heading.
  It became a receipt: one left edge, one money column, one kind of rule, nothing in a card.
- Grey slabs appeared on a steeply turned print. The first fix didn't hold. The real cause took until
  8 October to find (it's in 0.5).
- On 27 September every edit finally reached the print. The lab only accepts a finished file, so every
  edited photo is redrawn in the browser at checkout at print resolution, from the same layout as
  the screen, and sent instead of the original. The first baked file came out at 1286×857 pixels,
  exactly the 214 DPI the quality bar had shown for it.
- That morning I started numbering releases. The commit that was live became 0.1.0.
- A rule from the same day: everything has to work on a phone (nothing out of reach, no sideways
  scrolling), but the phone polish waits until later. That phase started on 8 November.

### 0.2 to 0.4 · The first editor · 27 September

Three versions in one day, which is how I learned the middle number was moving too fast.

- **0.2** split the editor's side panel into two equal boxes, gave the Photo box its own home page
  (Crop & Rotate, Light & Colour, Border), and added a Quantity menu. Removing one photo blanked its
  copy, because the copy shared its preview and the preview was thrown away with the first one.
- **0.3** was about one misunderstanding. A small pill above the photos spelling out "4 × 6 · C-type
  · Lustre · Fill" was read as the settings of the photos already on the page, when it meant the
  settings for photos you add next. It became a gear. Then the outline gear looked like an eye, so it
  became a solid one. Later it became a sliders icon, and the box opens with a note you have to
  confirm: these settings are only for photos you add from now on.
- **0.4** rebuilt borders. I wanted borders that would blow the competition out of the water. The
  shops I looked at offered black or white in a few widths at most. This one had four styles, widths
  in eighths of an inch, a caption in the bottom border, and border colours read from each photo.
  Within hours I took the photo colours out again in favour of black, white and a full colour wheel.
  The same day's audit found the worst bug on the site: the grid ignored edits, so a cropped,
  bordered, captioned photo looked untouched until you opened it. Tiles are drawn as they'll print
  now.

### 0.5 · The editor rebuilt from the ground up · 27 September to 21 October

After four releases in a day, every deploy became a test version of 0.5 instead. There were 52 of
them before 0.5 itself, and the 0.5 line ran for three and a half weeks.

#### 27 to 29 September: captions, bleed, and a second computer

- **Borders the lab would have cut unevenly.** Checking that edits really reached the lab, I found the
  lab's print areas aren't the paper's shape. Its 4×6 area is 1223×1783 pixels, a ratio of 1.458 and
  not 1.5. The 5×7 and 8×10 are off too. A file made in the paper's own shape would be cropped by the
  lab, and an eighth-inch border would come out about a third as deep at the top and bottom as at the
  sides. So every size now carries the lab's real print area, and edited files are made that exact
  shape with the paper in the middle and a bleed around it in the border colour. Measured in a real
  file: an eighth-inch border came out at exactly 37.5 pixels on every side once the lab's overhang is
  trimmed. A real sample print still has to confirm it.
- **No iPhone could check out an edited photo.** Safari writes camera and copyright details into any
  image it redraws, the server refuses any photo carrying hidden data, and the step that bakes edits
  skipped the cleaning. So every edited photo from every iPhone was refused at checkout. Same problem
  as the iPhone uploads on 9 September, in a new place.
- Ordering an edited print again failed after two days, because the order only kept the edited file
  and the cleanup deleted the original. Orders keep both now.
- **Captions sat higher in the print than on screen, in Chrome only.** Measuring real baked files pixel
  by pixel, every caption sat 3 to 4 pixels higher at 300 DPI than on screen. Chrome and Safari mean
  different things by "the middle" of a line of text. On a handwriting font the difference is 0.066
  of a letter's height, on a serif display font a tenth. Safari already matched, so iPhone orders
  were right all along. After the fix, captions land within about a pixel of the screen on every edge.
- Captions were rebuilt step by step: up to five on the photo and five in the border, typed straight
  onto the print, sideways in the side borders. A caption flipped in a side border and dragged to the
  bottom one kept its flip and read upside down. Pressing Escape while typing closed the whole editor.
  The camera that flew in to the words lagged behind them as you typed, so it became a 200 ms glide.
- "Some sizes are working and some aren't." The caption size slider went up to 40 points everywhere,
  but a caption can only be as big as its border is deep. Asked for more, it printed at the limit, so
  the top of the slider did nothing on thin borders. The slider now ends at the largest size that
  actually prints on that print. On a 6×4: a quarter-inch border holds 9 points, an inch holds 40.
- A border too thin for words used to blank the whole caption page. It says so now, with one button
  that widens it to the least width that holds words.
- The switch between Simulated and Standard was "very glitchy", worse the deeper the border, because a
  second, wrongly sized copy slid across the border and snapped. Then the browser's own transition
  froze the whole page for half a second, so I dropped it. Measured after: the new view appears in 30
  ms and the old one is gone by 256 ms.
- Interface size was a zoom that drew the desktop layout bigger and squeezed it. It works like your
  computer's own display scaling now, which meant rewriting 33 layout rules.
- The paper-true filter made photos look washed out. My words the next day: "the customer won't know
  what the real photo is". It came out. Held still, the simulated print shows the file's own colours,
  identical to Standard.
- The camera into captions felt plain, so it got five different moves. The next day it was too lively,
  so it calmed down.
- I started working from a Windows PC as well as the Mac. The deploy script's check that no dev server
  is running used a tool Windows doesn't have, so on Windows it would have found nothing and gone
  ahead. A build under a running dev server breaks every page. Line endings had to be fixed on both
  machines, because a script saved Windows-style won't run.
- On Windows, a commit message broke on the shell's quoting, so a deploy started before its commit
  existed. I stopped it during the build, before anything was uploaded.
- Two deploys were started at once. Each deploy replaces the whole site, so only the last one to
  finish would have survived. One was stopped, rebuilt on top of the other and sent after it. Since
  then, one deploy at a time, across both machines.
- I wanted real lab prices on the PC while payments stayed in test mode, and a real lab connection
  can place real, billed orders no matter what. So there's a switch, Sending or Paused, and every
  path that sends an order to the lab checks it first.
- A quick drag on the border colour wheel crashed the page. The wheel and the colour setting kept
  hearing each other's late echoes and setting each other back, round and round.
- The dev server was listening on every network, so on any Wi-Fi the Mac joined, including school
  Wi-Fi, my work in progress was reachable. It only listens on the machine itself now.
- My own devices at home couldn't see the site past the coming-soon wall without a preview link, so
  home Wi-Fi got through. Two days later the connection gained IPv6, Chrome preferred it, and I was
  walled out of my own site until that was added too.
- "Editor" inside the editor. The lower box was called Editor, inside the thing called the editor.
  It became Design.

#### 30 September: the organiser, built whole and then undone

- I questioned whether the Booth's bigger Expanded view was needed at all, then kept it as "the
  organiser" (choosing which photos print, how many and in what order) and built all of it. It was
  built in a day: sorting, grouping by day, keys to leave photos out, finding similar photos on the
  device, dragging to pages, laying them out. A version that compared photos only by a fingerprint was
  fooled by flat colours, so colour and sharpness went into the comparison. Then I looked at all of it
  and undid it, saved it to one side, and started again in pieces. It went onto a shelf, and pieces have come
  back one at a time since: favourites, Montage, and Sort & filter.
- The first piece back was an Arrange board, prints at real sizes you could place freely. Before it
  ever went live I worked out what I actually wanted: prints at their editor sizes, barely any space
  between them, like a random spread of cards in a binder. That became Montage, every print packed 3
  pixels apart.
- I wanted to sort by camera and date, but every photo is cleaned of that data before upload. The
  answer was to read the date, camera, lens and settings on the device before cleaning, keep them with
  the photo while you work, and never put them in an order or a print file. The location part of the
  file is never read at all.
- The picker for how many photos in a row felt cheap as numbers. I turned down grid icons ("feels like
  a CCTV UI"), plus and minus, words, a dot scale, a lens ring and prints on a table. It became a
  slider like the one in Apple Photos, big photos at one end, small at the other.
- Sort was brought back, taken out again, then rebuilt the same day once the camera details
  existed. Filtering by "no camera info" turned out to catch screenshots and downloads.
- "Why is there so much space on the right?" The editor grid hugged the left of the screen. It fills
  the width now, measured at seven screen sizes from 1920×1080 down to a phone.
- The rules for picking several photos at once flip-flopped over three days. Several picked gets basic
  bulk changes only. Then the several-picked mode was removed. Then it came back. Where it landed: one
  photo gets full control, several is for bulk.
- On the Windows PC, a deploy from a second copy of the code broke every development server on that
  machine. The copy's packages folder was a link to the main one, and the production build wrote its
  production settings into shared framework files through the link. The live site was fine. The rule
  since: every copy installs its own packages, even though it's slower.
- The same second copy, deployed as it was, would have taken the new reflection back off the live
  site, because it was made before the reflection landed. Since then, a deploy always takes in the
  newest live work first. A deploy must never take something newer back off.

#### The reflection, rebuilt as real light

The light on the simulated print had been a drawn room that moved across the photo. I'd liked the
first, simple version and hated the busier one: "it feels like we took a png and slapped it to the
front of the image and are moving it around". What I wanted instead was one window by day, house
lights by night, a switch between them, and real physics: "the window is going to stretch".

So it was rebuilt to draw, for every pixel, what your eye would see reflected off a slightly bent
sheet of paper in a room with real sizes in metres. By day that's one window with a frame, bars, sky
and trees. By night it's a dark window, a ceiling light and a lamp. The photo itself is never redrawn.

- The PC had to be shut down halfway through building it. The design only existed in that one folder,
  not saved anywhere else, so it was saved to a separate branch marked "do not merge or deploy" with
  three tests still failing.
- Seen on a real graphics card, gloss showed the window but lustre showed sparkle and grain all over
  and no window at all. The lustre blur was as wide as everything the print could see, so the window
  smeared into an even glow, and a plain wall twinkled, which real textured paper never does. Lustre
  became a narrow pebbled core in the window's shape, sparkling only at its edges, inside a soft haze.
- At night, lustre washed a dark photo grey from corner to corner. The ceiling light lifted a city
  photo's blacks by 41 to 54 levels out of 255 more than gloss did. I picked from three looks side by
  side and chose the one that keeps every dark corner within about 6 levels of gloss, knowing it makes
  the window by day a bit brighter.
- The paper's flex behaved differently at 30, 60 and 240 frames a second, and one slow frame kicked
  it. It's the same curve at any frame rate now. Even the size of your pupil at night got worked out,
  3.5 millimetres in house light, which made the ceiling light's reflection crisper.
- A review with four reviewers, each checked by a sceptic, found nine real faults. The worst: phones take the
  graphics away from a page that goes into the background, and after three trips to another app the
  light would have gone out for good on a perfectly healthy phone. On cheaper phone graphics, the tiny
  blur widths rounded down to zero and drew gloss as a stair-stepped bare mirror.
- It shipped on 30 September, after I'd seen it on a real graphics card.

#### 1 to 11 October: papers, Positioning five times, and Light & Colour

- **The paper copy was wrong in several places.** Every claim about the papers was checked against
  the lab's own data and the paper makers' datasheets, with a second pass trying to prove each one
  wrong. German Etching is not cotton, though the page filed it under cotton. Foil prints only show
  metal where the file is transparent, so "highlights become metal" was false. Pearl isn't heavier than
  the archival paper. Every wrong claim came out, and a test now fails if any of those words come back.
  Metallic stays "coming soon" until there's a tool to choose which parts of a photo turn to metal.
- Chrome drew the paper texture as nothing at all, because of how one drawing effect sat inside
  another.
- The size-change animation was "glitchy" and left a white line on the right. Three separate causes,
  one of them a scrollbar flashing for a moment because prints in flight counted as content.
- The Day and Night switch moved three times: above the print, inside the view picker, then into a
  small menu.
- Notes written on the Windows PC came out with blanks where every technical name should have been. The
  Windows shell had read the quoted names as commands and run them.
- **Positioning** (where you crop and place the photo) was redone five times. The first version had
  tools for everything: where the photo sits, a margin, a coloured or blurred edge. I called it
  complete trash. The second had you drag straight on the print, with Fit kept simple. The third, on 8
  October: no zooming in when it opens, no dot grid, zoom as a number from 0 to 100, uncapped all the
  way down to almost no detail. Dragging stuttered, because every frame of the drag redrew the whole
  editor, and zoomed in it went blocky, because the picture was the small preview. Both fixed. Then
  Positioning became strictly one photo at a time. Then in mid-October a click zooms in, with a 1×/2×
  switch.
- **The grey slab.** Since 25 September I'd been seeing grey slabs and one-frame flashes of old frames
  across a turned print, near edge-on and when turned fast. It kept coming back, on 28 September, 7
  October and 8 October. The first theory blamed the light layers and faded
  them near edge-on. It didn't help. It never showed in any test screenshot, because those redraw
  fresh, so the only way to find it was testing on my own screen. Swapping things on and off there
  showed the real cause: the print's face, edge and back were stacked as separate 3D layers, and Chrome
  on the Mac left stale pixels from them. The turned print is one flat sheet now, with the back swapped
  in when it faces away and the paper's thickness drawn as a line. The rule since: never go back to
  stacked 3D layers on the print, and test on the real screen before calling it fixed.
- The paper edge was asked to be "a very little more thick" than 2 pixels. At 3 it was too thick. It's
  1.5.
- **The clear glass bar** under the preview took four passes. First it looked too much like every AI
  app. Then: more glass-like, ultra transparent but you can tell it's there, no colour. Then it still
  felt washed out. Then the bright edges were too bright, "more water like". It ended with no tint and
  no blur of its own, one faint gloss, and in Chrome a lens that bends what passes under its rim.
- Something moving or textured inside the preview, tried as drifting light, was "absolutely horrible".
  Nothing moves inside the preview now.
- **Light & Colour** was rebuilt like the basic panel in Lightroom: exposure, contrast, highlights,
  shadows, temperature, tint, vibrance, saturation. The hard part was that the screen draws the colour
  change one way and the print file computes it pixel by pixel another way, and they have to agree.
  They match to within 1/255. Its rules changed three times in one day.
- **Auto** was "extremely smart" one day and "complete trash" the next. I wanted an auto mode that
  fixes a photo perfectly. Its checks were far too strict and flagged nearly every photo, so they were
  cut back to the obvious cases, way too dark or way too bright. The next day I took it out with all
  its suggestions. The "looks" only moved the temperature, so they became 17 presets, each setting
  every slider.
- Saved collections dropped some edits: mirrored photos, and where a Fit photo sat. Reopening a
  collection lost those choices.
- The photo area had been called "the glass" all over the site. That was only ever the code's name
  for it. It's "the preview" now.
- Captions on mixed photos opened with a list of types to choose from first. "Look how complicated
  this is." They open straight onto the photos now, one at a time, and a click near a standard spot
  snaps so every size places the caption the same distance in from its edge.
- On/off switches looked like boxes, so they became slim pills.
- A caption group became strict: one size, one way up, one border. Mixed sizes captioned together were
  all over the place.
- A code formatter run on one of the editor's main files rewrote about 2,500 lines of it. It was undone,
  and it's never run now.

#### 12 to 16 October: a missed launch, shipping by ZIP, and test or live

- Reloading the page lost your place, and the browser asked "Leave site?". Now a reload keeps
  everything, down to the scroll position, and there's no warning.
- I'd planned to open on Tuesday 13 October. It passed. What was left was paperwork, live keys and a
  real sample print, and from 19 October the notes just say no launch date is set.
- Shipping became priced by ZIP code. There's a box on the order panel, and the state is worked out on
  the server from a list of 41,689 real ZIP codes in the 50 states and DC, so a made-up one like 11111
  is refused.
- I nearly started shipping to the US territories, and held off before anything was written. The lab
  prints for them overseas and sends them untracked, which doesn't fit a promise to reprint a lost
  parcel.
- Switching the whole shop between test and live without a redeploy. The hard part was orders in
  flight: an order made in test mode has to keep syncing, cancelling and refunding through test mode
  after the switch. Every order now records its own mode.
- Cancel was too generous ("this is actually a miracle that we are giving them a cancel button"). It
  had stayed open after the card was charged. Now it only shows while the card is held.
- Refunds made by hand would have left orders marked "paid", because the notice for refunds had never
  been turned on for test payments. The order page also shows where a refund is now: sent, with your
  bank, on your statement by a date.
- A double click could start two checkouts.
- The 1×/2× zoom came back, two weeks after the old 1× to 3× zoom was removed as "cheap". The zoom
  stuttered because the full photo was decoded in the middle of it. It loads after the zoom lands now.
- With 75 photos, "all animations are very stuttery". Zooming in drew a second copy of the whole grid,
  every print in it. Only the prints in sight are drawn now.
- The way back out of a photo "feels like it stops or waits for the photos to load back in". It did
  exactly that. The grid had been taken off the page while one photo was in front, the browser let go
  of the pictures, and each had to be decoded again mid-zoom.
- The terms now rule out nude or sexual photos, matching the lab's rules.

#### 16 to 21 October: a new upload engine, the flight towards you, and 120 Hz

**The upload engine.** Before, every photo was decoded, turned, compressed and made into a thumbnail on
the page itself, two at a time, which blocked the page for 2.9 to 6.8 seconds during a 500-photo drop.
The new engine prepares photos in the background on as many cores as the machine can spare, and
uploads in two to six lanes, photos on screen first.

| 500 photos | Before | After |
|---|---|---|
| iPhone photos, total time | 95.7 s | 71.1 s |
| Mixed formats | 81.5 s | 59.7 s |
| Small photos | 30.8 s | 17.9 s |
| Frames dropped (iPhone / mixed / small) | 21% / 24% / 60% | 11% / 11% / 0.4% |
| Page blocked (iPhone / mixed / small) | 2.9 / 4.7 / 6.8 s | 0.3 / 0.8 / 0 s |
| Chrome's memory after the drop | 5.2 GB | 2.6 GB |

Dropping 2,000 photos, the worst key press went from 999 ms to 174 ms.

- The catch was that a photo decoded in the background and one decoded on the page aren't pixel-for-
  pixel the same in Chrome, up to 8 levels apart on a wide-colour photo. That would have changed the
  printed files. So the background only compresses, photos that need redrawing are still drawn on the
  page, and every browser is tested once per version by preparing a few tiny photos both ways and
  comparing them byte for byte. On 151 test files, every upload came out byte-for-byte identical to
  before.
- The old way could upload a photo twice: 506 and 536 uploads for 500 photos. Now it's 500.
- Waiting until you stopped scrolling before preparing photos was smoother, but a 500-photo drop took
  323 seconds instead of 108 for as long as someone kept scrolling. Spreading the work out instead
  brought it to 103.
- With 500 photos picked, the selection glow cost about 3,500 repaints in a second and a half. Same
  look now, next to none.
- Getting honest numbers was its own job. Below 20% battery Chrome caps the page at 30 frames a
  second, and a Mac that's been working for hours runs warmer and slower, so the two versions had to
  be run alternately a minute apart.
- Then I found uploads slower than before: "much faster before". 90 RAW files took 177 seconds against
  163 on the old uploader. Every benchmark had uploaded to a server on the same machine, so the network
  never got in the way. On a home connection the engine let only one big file go at a time and left
  the line idle in between. Four uploads always go at once now. My own Mac on Wi-Fi did about 4.5 MB/s
  on one stream and 11 MB/s with four.
- Around then I got properly fed up with hours of before-and-after test rounds. Changes should ship,
  not be watched. The rule now is the shortest check that proves the change, and uploads tested at a
  real connection speed.
- There's a switch to turn the new engine off and go back to preparing photos one at a time.
- Dropping a folder brings in every photo inside it, subfolders too, and nothing else.

**The flight towards you.** Opening a photo used to scale the whole grid up with it, 25 times at
sixteen to a row, and tiles flashed blank on the way ("so glitchy"). What I wanted: fly towards you
and go into the single view with a really premium animation. Now the print lifts off its tile with a
soft shadow opening under it, comes up leaning and tipped back, and settles square while the grid falls
back behind it. Back is the same flight reversed. My reaction: "wow this is so much better". Along the
way, a blur animated on a big moving layer froze the whole flight for 200 to 300 ms whenever anything
else was busy, so only movement and fading are animated now.

- Changing rows with many photos was "very framey", the right side a second late. About 180 separate
  layers on a page of 80 photos. Changing rows became a camera move instead, two layers crossing over
  and scaling about the print under your eye, so 300 photos cost what 10 do.
- On a MacBook's 120 Hz screen, "any input on the right side" was framey with 230 photos and smooth with
  10. Every frame of a menu folding laid the whole preview out again (3 ms of an 8 ms frame), and the
  browser sorted every print on the page each frame (about 4 ms more).
- On 120 Hz, the turned print's light ran at half the screen's pace, because it treated 60 frames a
  second as good enough. It's judged against the screen's own rate now.
- Smoothness judged on the development server was misleading. It adds 80 to 150 ms per click with a
  page full of photos. A whole round was spent chasing a "freeze" that only existed there. Motion is
  judged on a real build now.
- Two days of work were nearly lost when some old copies of the code were cleaned up with commits on
  them that had never been merged: the phone's slim checkout bar and a Border fix. They were found a
  day later and shipped. Every deploy checks for leftovers now.
- On phones, the checkout bar was 84 pixels tall with a square button. It's one 48-pixel row now.
- The border animation had silently stopped playing on most pages, because it was skipped whenever
  more than 16 prints were in sight. It's 64 now.
- 2× in Positioning barely made a difference on a big screen. It really doubles now.
- Back from a 50-megapixel photo in Positioning took about two seconds, because the screen was drawing
  the full 8,688×5,792 original, about 200 MB to decode. It uses a screen-sized copy now that you can't
  tell from the original, and Back takes 0.65 seconds. The original is still what's printed.
- The Caption page's little preview drew 328 photos as specks. It shows the one you point at now, alone
  or with its neighbours.
- The clear glass bar hid what was under it. It works like Apple's now: what scrolls under the bar
  blurs as it nears the edge, and a print at rest is never touched.
- "Why is it scrolling the photos?" Changing the row count slid the preview off to some other photo for
  most of a second. And going from one photo to two, three a row and back landed on a random photo.
  The editor remembers the photo you're on now, and each row count remembers where it was.
- I wanted hover tips to come up 1.5 seconds sooner. Those tips belong to the browser and no page can
  change their timing, so a whole new set was built that came up in 0.3 seconds. It looked like a whole
  new design when all I'd wanted was a different timing. It was restyled to match, then taken out
  altogether, slower tips and all.
- A side-by-side before-and-after view for Light & Colour was built and taken out the same night.
- The development server got restarted in the middle of a deploy, because it looked like it had
  crashed, and that blocked the release. A server that stops with nothing in its log means a deploy is
  running now. Leave it off.
- "Opens it in large makes no sense." Hours after Light & Colour was given Positioning's rule of
  opening a big photo, I reversed it. It opens the menu, like Positioning, not a big photo.

### 0.6 · The editor, done · 21 October to 3 November

0.6.0 went out on 21 October, the first full release since 0.4. Nobody wrote a checklist for "done". I
decided it was done. The last thing in it was the Quality page, turned from a technical statistics
panel into an answer, with print sizes as a plain list instead of something that looks pressable.

The rest of 0.6 was the editor getting faster and more honest, and the catalogue starting over.

- **Typing a caption on a page of 270 photos was "extremely laggy".** A caption with no colour picked
  reads the photo under its words to choose dark or light ink. To find that photo, it asked the page
  where every print was, which made the browser lay out the whole page again, for every print, on
  every letter typed. Now it works it out from the print's own layout: about 50 ms a letter on 270
  prints.
- **"Photo 1 is no longer available."** A tab left open for an hour refused to check out. Each tab keeps
  its photos alive on the server by checking in every few minutes, and the browser had paused the
  background tab (a sleeping Mac does the same), so it stopped checking in and the cleanup deleted the
  photos. Now a tab checks in the moment it's back, and if it might have been away too long, it asks
  which photos are gone and uploads them again from the copies on your device.
- Brightened night photos looked off centre, because a half-pixel edge of white paper under the photo
  peeked out once the colour change was applied.
- "1 million beta releases." I didn't like the releases page, so about 70 test releases were folded into
  one release each for 0.5.0 to 0.5.3, and every version since is one plain release.
- One motion everywhere didn't feel premium: "if we use the same type of effect everywhere it's not
  going to be premium". It became four moves with four jobs, all on one curve with no bounce: the
  camera zoom for changing how many are in a row, the flight for opening a photo, a fade-and-settle for
  picking a group, and a tighter reshuffle for a change of size.

**500 photos, as quick as one.** I wanted the editor to feel the same with 500 photos as with one,
without changing anything on screen. Going back to the grid from one photo took 2,047 ms, a single
frozen frame of two seconds. It went down to 149 ms. The way back was asking every picture where it was
so it could decode the visible ones first, and asking forced the browser to lay out prints that were
deliberately not drawn: 500 forced layouts. Three ideas that would have been faster were taken back
because they changed what you see, even slightly: one print came out a shade different mid-move, one
could turn grey at once instead of fading. Ten states were compared pixel by pixel against the old
version. A second round got the Design pages opening in 90 to 100 ms instead of 140 to 157. Pointing
down one menu had been setting off about 16,000 fade animations, each one reported through the app for
no reason.

**"A 3x4 is bigger than a 4x6."** Zoomed in, a 3×4 came out taller than the 4×6 above it, and a 4×6, a
5×5 and a 5×7 were drawn the same length, because every row was stretched to the edge whatever its
sizes. Now the whole page shares one scale, a row holds as many prints as fit at true size, and a full
row stretches by at most 6%. Before, zoomed in, prints ranged from 50 to 94 pixels per inch. Now it's 54
to 67, every size in order. The trade-off is that a row can end a little short of the edge, and I decided
the small gap is okay. Then that change broke three other things the same day: portrait pages, prints
wider than the row, and a slider that said "4 in a row" when mixed shapes made it untrue.

**The catalogue, again.** The everyday line's name changed four times in four days: Prints, which
sounded cheap, then Photographic, then Everyday (already the name of an art paper), then The Classics.
The cards had been drawn as rooms of blank prints, waiting for real photographs. Blank prints "isn't
that cool", so they became a kitchen table on the day the prints come home, with storybook pictures on
the fronts and pencil notes on the backs, and a print that turns over when you point at it. The wide
card's layout went round three times in an afternoon, for what was really a very simple correction,
just where the pictures sit. Layout tweaks have been a direct edit and one screenshot ever since.

- The everyday shop was offering the archival paper, which it doesn't make. Each shop is its own lab
  and its own box, so a page is for one shop at a time now.
- The Squares card went round four times: squares standing up like dominoes on a polished black table,
  then an oak desk with a lamp (which went live before I'd decided on it), then five squares floating in
  a line, and finally, for 0.7, a beam of light from a frosted 3×3 slide onto an 8×8 print of the same
  photo.
- "Why is shipping the same in Minnesota and New York?" The empty Booth showed the New York figure for
  every ZIP. It asked before the saved ZIP had been read, then a second answer overwrote the first. A
  code review of that fix found it would lose the figure for the rest of the visit if one request ever
  failed.
- The order panel slid past the bottom of the photo box when you scrolled.
- The photo box grew with its photos. I liked how it looked empty and wanted it to stay that way, so it
  keeps one size now and photos scroll inside it.
- A size guide drawn to scale went up and came down a day later, replaced by a small viewer on every
  print page where you turn the print in the same light as the editor, and try your own photo without
  uploading it.
- The top bar jumped while photos uploaded, because "Uploading 37 of 61" changed its height.
- "I don't like how grey the catalog is." It should match the theme like the Booth does. Every new
  surface gets checked on a dark theme now.
- I nearly renamed lustre to matte. Lustre has a sheen, and the lab makes no matte photo print at all,
  so it stayed lustre.
- Fine Art became Gallery Grade. I wanted something elite sounding, two words at most.
- "Print with 4×4" and then "Print with 8×10" left only the 8×10 page.
- Catalogue descriptions talked about crops and what the Booth does. "We just give a nice friendly
  description." Every print got a warm line about its size, where it goes and what it's for.

**Built for Chrome only, by accident.** On 2 November I opened the site in Safari and it felt broken. A
measured comparison of Safari and Chrome found the causes. Safari applied the page zoom twice to some
sizes, so prints and text came out wrong. Fixed delays used as a stand-in for "when the browser is
idle" made the reflections seconds late. Changing a style on a drawing effect made Safari redraw it on
every mouse move. A private window in Safari refuses to store image files, so drafts didn't save. And
dialogs handled the Tab key differently. All fixed. Safari was tested by rendering the page with the
Mac's own Safari engine in a small off-screen app, which matched my Safari exactly, and several
"Safari-only" glitches turned out to happen everywhere. The one thing kept Chrome-only on purpose is the
lens that bends things under the edge of the glass bars.

**The coming-soon wall came down on 2 November.** Since 14 September the public had only seen "Coming
soon". With it gone, people could look around the whole shop. The payment company had refused to save my
terms and privacy links while the site looked "under construction", and that sorted itself out too.

### 0.7 · The catalogue · 3 November to 8 November

0.7.0 went out on 3 November with the Squares beam and a 3D fan of every art paper and both metallic
foils, each blade in its own paper's white and surface. Then came a week of getting ready to sell.

- **Testing mode, said plainly.** I decided to open in testing rather than wait for my own test print.
  The terms open with a line saying the shop is still in testing and prints may not come out exactly
  the way you want, and every checkout asks you to tick "I agree" first. There's a feedback form in the
  footer that takes words and up to three photos and stores nothing.
- Every setting got one plain line explaining it. "Hardware accelerated uploads" became "Faster
  uploads".
- **The terms, finished.** The shop can decline an order, and cancel and fully refund an obvious price
  mistake. Hateful and graphically violent images joined the banned list. Rights holders have a way to
  report a photo, looked into the same day. An order not shipped within 30 days can be cancelled. If a
  reprint can't be made or comes back with the same problem, it's refunded. The Pay button's line says
  prints can't be returned, and damaged or wrong prints are reprinted free. I turned down putting a
  policy line beside Checkout. It was ugly.
- I'd assumed shipped photos were kept 60 days. They were kept 30. Card disputes can come for about 120
  days, so it's 120 now, and a photo under dispute is kept until the bank decides.
- With no Wi-Fi, the order panel sat on "Getting the current total…" forever. The request had no time
  limit and was never retried. Now it gives up after 15 seconds, says it's trying again, and tries every
  20 seconds and the moment the connection is back.
- The order page crashed on an order whose address hadn't come through from payment yet.
- Captions on the photo and in the border had separate pages. Now it's one page: click the photo for a
  caption on it, click the border for one in the border.

**Getting ready for 100,000 people.** The shop had been built for a handful of orders. Things that would
have broken with a crowd:

- Limits on how often someone can use the site were counted per internet address, so a whole classroom
  on one school Wi-Fi would have shared one person's allowance. They're per browser now.
- The Booth asked the lab for a price on every change.
- Every question to the database read every order. That's fine at a hundred and fails long before a
  hundred thousand, because a single answer is capped in size and time.
- Two things writing to the same order at once, a payment notice and the hourly check say, could quietly
  undo each other. Every write now names the version it read, and a stale one is refused and retried.
- **Order tracking would have gone blind after the hundredth shipped order.** The hourly check read the
  hundred least recently changed orders that were at the lab or shipped. Shipped orders never left that
  set, so from about the hundredth one it would never have looked at a new order again. Every order has
  its own next-check time now.
- **Cancelling a held order from my side left the card hold in place**, so the next run would have
  charged the card for prints nobody was going to make. Cancel releases the hold now, and the job that
  charges cards refuses a cancelled order.
- The receipt went out only after the money was taken. Now it goes the moment the card is held, says
  "Total" rather than "Paid", and every email for an order sits in one thread.
- 153 files changed, and tests went from about 1,100 to about 1,650. The database changes were applied
  to the live database by hand: safety checks, a backup, the changes, then checks that they took.
- Two more rounds of this work were built and then paused. They took hours each, and launch comes first.

**"Delivered" couldn't be known.** The order page promised a Delivered step, but the lab's current system
never reports delivery: to it, "complete" means shipped. Going to the carriers directly is out, because
tracking someone else's labels now needs a paid licence. The lab's newer system will report it. Until
then the step is hidden rather than guessed.

- Changing a print to a size its photo already had quietly made a second, duplicate print.
- **The shop's own checkout page.** Until 0.7.7, checkout was the payment company's hosted page, and only
  half of it could match the site. Now it's the site's own summary beside the payment form, with Apple
  Pay and Google Pay, and Standard or Express shipping. Shipping is worked out again for the real address
  once it's typed in, because the ZIP in the Booth was only ever a guess.
- Shipping used to be worked out from a box price written into the code. When the lab's box price
  changed, it would have gone wrong. It's quoted from the lab every few hours now.
- Two different totals on the checkout page. Before an address is in, the payment form's total is the
  prints alone, and the summary had added its own shipping guess. The summary always shows the payment
  form's own total now.
- My own test order showed a total without the tax, and "Waiting on payment" next to "Card held".
- Safari drew prints blank after a scroll and filled them in a second later, because it only starts
  drawing things once they're on screen. Prints within a screen or two of the edge are always drawn now.
- You can open any order as a view-only Booth tab, on any device, to see its pages and prints again.
- In one afternoon I went over the order panel line by line. Make this arrow face right. Line
  everything up, see how it's not even. Obviously that's not the total. Shipping should just say
  calculated at checkout. Then the ZIP box, built in October and refined four times since, came out
  entirely, because the new checkout prices shipping from the real address.
- A strip of colour under the footer in Safari. The first fix assumed Safari made the page a little taller
  and never touched it. On 8 November it turned out to be the Mac's elastic scroll: the whole page lifts
  and the browser paints its own background in the gap, where nothing on the page can reach. Turning the
  bounce off fixed it, and I rejected that the same day, because being able to stretch the bottom is
  better. Now the colour behind the page matches the footer while the footer's on screen. Tests never saw
  it, because nothing on the page moves. Only the pixels do.
- The "Send feedback" button was a bubble. It should be plain text like the links next to it.

**Deploys that lied.** Twice in this stretch a deploy said it had worked when it hadn't. Once, the script
stopped at a database check and still reported success. Another time, an upload failed on a network drop
after every test had passed, and the way the result was being printed hid the failure. For two days I
blamed the network for deploys stopping. The real cause was that the saved sign-in for the hosting had
quietly stopped working, and the first command after a while idle was refused. A deploy only counts now
when its log says it was deployed and the cache cleared, and the live site has been checked.

### 0.8 · The pre-launch build · 8 November onwards

0.8.0, on 8 November, is the build Cor Photos opens from. Everything after it has been finishing.

- **Old photos graded "Poor".** Some people print low-resolution photos on purpose, old phone photos for
  the nostalgia of them. Grading those "Poor" was wrong. I tried a "meant to look this way" switch and
  dropped it the same day, and dropped a check of the camera details too. What
  I designed instead: a photo's best is what it gives printed whole on a 4×6. Under 300 DPI it starts at
  Full detail and only drops as a bigger size or a tighter crop costs it. A 600×400 photo reads Full
  detail at 4×6, Good at 5×7 and Soft at 8×10. The real DPI always shows beside the word.
- The very first flight into a photo stuttered and no flight after it did. The caption fonts arrived a
  tenth of a second into that first flight, and the whole page was laid out again in mid-air. They load
  when the editor is idle now.
- The caption fly-in looked grainy, because the print was drawn at its landing size and shrunk up to nine
  times by the graphics card on the way, and past about half size the detail sparkles differently every
  frame. It's drawn smaller in flight and sharpens on landing.
- A new logo: "Cor" in a bordered 4×6 card, then "Photos" in the same script, drawn as shapes so it never
  waits on a font. The labels in the dark themes moved from a typewriter font to handwriting. It looked
  too digital.
- **Testing on a real phone** finally started on 8 November, the phase I'd put off since September. The
  development server refused its own files to my phone until the phone's address was allowed. The phone
  page crashed on load because plain http on a home network isn't treated as secure, and one browser
  feature the Booth uses only exists on secure pages. The Mac's network address kept changing during the
  day. The iPhone simulator needed a newer macOS, so I updated the Mac the same day.
- **"Very laggy, in 2x mode it's absolutely garbage."** Changing a print's size stuttered, worst at 2×.
  The paper's real width and height were being laid out and painted again every frame, over 4 ms of the
  8.3 ms a frame gets on a 120 Hz screen, and more at 2× where the print is three times bigger. Each
  press also restarted the motion from full speed. Now the sheet takes its new size at once and the
  graphics card scales it on screen, and a second change partway through lets the first one finish. The
  measuring lesson: headless Chrome runs at 60 Hz and draws to no screen, so it showed the change as
  perfectly smooth. The same test in a visible Chrome on the 120 Hz screen missed about one frame in ten.
  Motion is measured on a real screen now, with nothing else running.
- The Booth's messages were a coloured band that pushed the whole page down. I picked a small slip near
  the bottom of the window from four styles.

**0.8.3, 9 November.**

- **"When you're not editing photos it's mad blurry."** Large views were drawing the 720-pixel preview
  stretched up to 3.5 times on a Retina screen: Expanded view, the editor one or a few to a row, and the
  Caption page. It's the same problem as on 9 September, back in four new places. Printed files were
  never affected, only the screen. Now anything drawn large gets a sharp copy made for the screen in a
  quiet moment, and a normal grid makes none. Photos reopened from a saved collection aren't covered yet.
- **The Simulated view, "glitchy and garbage".** It was slow to load, stuttered while photos uploaded, and
  only lit the front of the print, and only if you moved slowly. Each frame of a turn restyled the whole
  preview. The paper edge was a shape redrawn every frame. Every bit of upload progress redrew the whole
  Booth mid-drag. And the room had one window, which only caught the print at about one angle in ten, so
  a fast turn crossed it in two or three frames. Now upload news waits while the print is in your hand,
  the edge is four boxes that move without redrawing, and the room has light on every wall, a skylight
  and a sunlit floor, with more lamps and a lit doorway at night. The back of the print reflects too.
  During a 200-photo upload the worst frame went from 92 ms to 25 ms. The edge boxes had to be 600×4
  pixels, because a 1-pixel box stretched ran a sliver 40 pixels past the corner.
- **The low-resolution prompt asked about photos nobody had zoomed.** "It shouldn't show up for photos
  that are soft by default, because they didn't scale in to make it poor." Checkout asks now only when a
  print is zoomed in or bigger than its photo can hold. Its two buttons didn't match, so they're the same
  size and shape now, and Continue is never greyed: pressed early, it points to the box still to tick.
- **The way back "just minimises into it".** The fly-in is the effect, but going back the print lost about
  five sixths of its size in the first fifth of its time, before its lean could show. It shrinks at the
  same pace it grew now, over the same 450 ms.
- The order panel became a plain receipt: each page's total, and nothing else.
- Four separate pieces of work changed the Booth's main file at the same time, so they were joined
  carefully and the combined editor was checked in a browser before it shipped.

---

## What still isn't done

- No real Cor Photos print has been checked against the screen yet. Borders, the caption ink, colour
  conversion and the lab's print areas are all measured in files, not on paper.
- It's never been tested in Firefox or on a real iPhone end to end. Safari on the Mac has.
- Gallery Grade's art papers and the metallic foils are coming soon. Metallic needs a tool to choose which
  parts of a photo turn to metal.
- Google Photos is coming soon, until Google finishes checking the app.
- The Delivered step waits on the lab's newer system.
- The site has no photographs of real prints. Everything that shows a print is drawn or simulated.
- Photos reopened from a saved collection still stretch the small preview when drawn large.

## By the numbers

- About 600 commits between 7 September and 9 November.
- 1,720 automated tests. On the first day there were three.
- 14 numbered deploys between the morning of 27 September and that night.
- Every photo format a phone or a mainstream camera makes, and up to 500 photos in one order.

## Follow along

Choose **Watch → Custom → Releases** at the top of this page to get an email at each milestone.
