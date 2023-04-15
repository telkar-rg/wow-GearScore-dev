# wow-GearScore-dev
GearScore for WotLK with Transmog fix.

When targeting a player on WotLK servers with Transmog, the behaviour **seems** to be such that on the first inspection your Client seems to "see" the visual Transmog items as they are (which usually cause the target to be rated at a noticably lower GearScore).

Only when causing another "mouseover" interaction, the Client seems to "see" the actual gear underneath the Transmog visuals (calculating the GearScore correctly this time).

## Changes
This updated version will filter out Scans and Received Data (via addon msg channel) if one of the following conditions is true for at least one **visible** item:
- Item ID below 35560 (pre-WotLK)
- Item Quality is poor or common
- Item Level is below 130 (with the exception of heirlooms)

This is a **Soft-Fix**: It will not be able to catch ALL incorrect Transmog scans, but it will filter out MOST of them.

## [Releases](https://github.com/telkar-rg/wow-GearScore-dev/releases)
- [GearScore 3.1.17 +1a](https://github.com/telkar-rg/wow-GearScore-dev/releases/download/r2/GearScore.3.1.17.+1a.zip):
  - Corrected small error in checking for non-visible relics in slot 18
- GearScore 3.1.17 +1:
  - Fixed Lua error on gear tokens
  - Added Transmog Soft-Fix

![GearScore Settings](https://imgur.com/PKXQJCF.png)
