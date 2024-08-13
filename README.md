# OrdML
OrdML is an [XML](https://www.w3schools.com/xml/xml_whatis.asp) for describing BTC [Ordinals](https://docs.ordinals.com/) inscriptions in 3D worlds.

## Why?
BTC Ordinals are digital assets where digital asset ownership is secured by the most decentralized, secured, and valuable blockchain - Bitcoin. Can we build 3D worlds based on these digital assets? If we intend to place digital assets into 3D worlds, what is a simple way to describe digital assets with their relations to 3D worlds? OrdML was born to combine the BTC Ordinals with [MML](https://mml.io/) that is an open source (MIT License) project to host web-based 3D multiplayer worlds.

## Usage
The first live OrdML example is a TEXT [reinscription](https://ordinals.com/sat/1147516183548979) on a metaverse [parcel](https://ordinals.com/inscription/f0fb9f3293e044cfbdec8f9c61a5496fe0d153bf5db3c258070c21ee7fbc0b3ci1) using the following OrdML
`<ord-img content="88888126a553d79a87038cada3241162ca8dbd94d1675fbc371a874feb33829ai0"></ord-img>`.

<img width="557" alt="OrdML on a metaverse parcel" src="https://github.com/user-attachments/assets/a4775fc4-3c79-4e85-9a04-225a5b50d3d5">

Currently, this `ord-img` tag only works for `jpg` or `png` inscriptions.

## Next Steps
- support `webp` in `ord-img`
- support `gif` in `ord-img`
- support 3D primitives such as cubes, sphere...
