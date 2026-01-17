 ____  _          _
|  _ \(_)_  _____| |
| |_) | \ \/ / _ \ |
|  __/| |>  <  __/ |
|_|___|_/_/\_\___|_|
|_   _| __ __ _ _ __  ___ _ __   __ _ _ __ ___ _ __   ___ _   _
  | || '__/ _` | '_ \/ __| '_ \ / _` | '__/ _ \ '_ \ / __| | | |
  | || | | (_| | | | \__ \ |_) | (_| | | |  __/ | | | (__| |_| |
  |_||_|  \__,_|_| |_|___/ .__/ \__,_|_|  \___|_| |_|\___|\__, |
                         |_|                              |___/
   v1.1 by mattakins
   Copyright (C) 2025 Matt Akins.

Grid shaders look great on Game Boy Color games - except for one glaring issue.

With no backlight, the original devices didn't render white pixels. These light pixels appeared as transparent areas where the backing material of the screen showed through. Many games relied on this effect for transparent backgrounds that now render on modern displays as eye-searing white pixels. No more! Pixel Transparency simulates this unique effect.

Just append to your favorite LCD shader as the last pass to reduce eye strain and maximize nostalgia.

