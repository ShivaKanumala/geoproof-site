# GeoProof website

Public website for the GeoProof Android app, served by GitHub Pages from the
`main` branch root:

- Home: https://shivakanumala.github.io/geoproof-site/
- Privacy Policy: https://shivakanumala.github.io/geoproof-site/privacy.html
- Terms & Conditions: https://shivakanumala.github.io/geoproof-site/terms.html

Plain HTML and CSS: no build step, no external fonts, scripts, cookies or
analytics. Keep it that way; the Privacy Policy (section 12) says so.

## Keeping the legal pages accurate

The Privacy Policy describes what the app actually does. Update it **before**
releasing any app change that affects:

- what data the app stores, or for how long;
- any network request (new API, crash reporting, analytics, cloud sync, ads);
- Android permissions (check the merged release manifest);
- default settings such as address lookup (off) or GPS in EXIF (on);
- adding any paid feature, in-app purchase or advertising (the app is free).

When you change `privacy.html` or `terms.html`:

1. Edit the text.
2. Bump the version and the "Effective" date in the page header.
3. Add a row to the change table at the bottom of the page.
4. If the change is significant, tell users in the app's release notes. For
   anything that sends data off the device, ask for consent in the app first.
5. Keep the in-app privacy notice
   (`lib/features/settings/privacy_screen.dart` in the app repo) consistent.

## Google Play Console

- Privacy policy URL: `https://shivakanumala.github.io/geoproof-site/privacy.html`
- Data safety form: no data collected or shared by the developer. Location and
  photos are processed on the device only. The optional address lookup sends
  coordinates to the platform geocoder.

## Screenshots

`assets/screens/*.jpg` come from a debug build on a real device. Never use
screens that show real GPS coordinates (camera, photo details, project
overview, PDF), because they reveal where they were taken.
