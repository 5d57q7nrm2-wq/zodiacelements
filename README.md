# zodiacelements

A comprehensive dataset mapping the periodic table of elements to their resonant frequencies and astrological/planetary correspondences.

## Overview

This repository contains data connecting chemistry and astrology through:

- **Resonant Frequencies**: Atomic resonant frequencies (in Hz) derived from spectroscopic data
- **Planetary Connections**: Traditional alchemical and Hermetic planetary correspondences
- **Zodiac Signs**: Associated zodiac signs based on planetary rulership
- **Alchemical Associations**: Historical alchemical names and associations

## Data Structure

The `elements.json` file contains:

### Elements Array
Each of the 118 elements includes:
- `atomic_number`: Element's position in the periodic table (1-118)
- `symbol`: Chemical symbol
- `name`: Element name
- `atomic_mass`: Atomic mass in unified atomic mass units
- `resonant_frequency_hz`: Primary atomic resonant frequency in Hertz
- `planetary_connection`: Associated celestial body
- `zodiac_sign`: Related zodiac sign
- `element_type`: Classification (Noble Gas, Alkali Metal, etc.)
- `alchemical_association`: Traditional alchemical name or association

### Planetary Correspondences
Maps each planet to:
- Associated zodiac signs
- Characteristics and qualities
- List of corresponding elements

### Zodiac Element Associations
Maps the four classical elements (Fire, Earth, Air, Water) to:
- Zodiac signs
- Qualities (Cardinal, Fixed, Mutable)
- Characteristics

## Planetary Rulerships

| Planet | Zodiac Sign(s) | Key Element Examples |
|--------|---------------|---------------------|
| Sun | Leo | Gold (Au), Hydrogen (H) |
| Moon | Cancer | Silver (Ag), Selenium (Se) |
| Mercury | Gemini, Virgo | Mercury (Hg), Zinc (Zn) |
| Venus | Taurus, Libra | Copper (Cu), Phosphorus (P) |
| Mars | Aries, Scorpio | Iron (Fe), Titanium (Ti) |
| Jupiter | Sagittarius, Pisces | Tin (Sn), Nitrogen (N) |
| Saturn | Capricorn, Aquarius | Lead (Pb), Carbon (C) |
| Uranus | Aquarius | Uranium (U), Neon (Ne) |
| Neptune | Pisces | Neptunium (Np), Platinum (Pt) |
| Pluto | Scorpio | Plutonium (Pu), Arsenic (As) |

## Usage

```javascript
const data = require('./elements.json');

// Get element by atomic number
const gold = data.elements.find(e => e.atomic_number === 79);
console.log(gold.planetary_connection); // "Sun"

// Get all elements ruled by Mars
const marsElements = data.elements.filter(e => e.planetary_connection === "Mars");
```

## Notes

- Resonant frequencies are based on atomic spectroscopic emission lines
- Planetary correspondences draw from traditional Western alchemy and Hermetic philosophy
- Modern outer planets (Uranus, Neptune, Pluto) have been incorporated into the traditional system
- Some elements have multiple possible correspondences; the primary association is listed