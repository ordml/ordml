# OrdML
OrdML is an [XML](https://www.w3schools.com/xml/xml_whatis.asp) for describing BTC [Ordinals](https://docs.ordinals.com/) inscriptions in 3D worlds.

## Why?
BTC Ordinals are digital assets where digital asset ownership is secured by the most decentralized, secured, and valuable blockchain - Bitcoin. Can we build 3D worlds based on these digital assets? If we intend to place digital assets into 3D worlds, what is a simple way to describe digital assets with their relations to 3D worlds? OrdML was born to combine the BTC Ordinals with [MML](https://mml.io/) that is an open source (MIT License) project to host web-based 3D multiplayer worlds.

## Usage
The first live OrdML example is a TEXT [reinscription](https://ordinals.com/sat/1147516183548979) on a metaverse [parcel](https://ordinals.com/inscription/f0fb9f3293e044cfbdec8f9c61a5496fe0d153bf5db3c258070c21ee7fbc0b3ci1) using the following OrdML
`<ord-img content="88888126a553d79a87038cada3241162ca8dbd94d1675fbc371a874feb33829ai0"></ord-img>`. 

If you own a metaverse parcel, you can re-inscribe this TEXT inscription with your image inscription ID on the parcel satoshi. You will see the parcel image updated once the TX is confirmed. The [parent](https://ordinals.com/inscription/0f436d14e3e6296780e19776eafd78ad578da403a4ba3c15ecf61870c6c47c42i0) (digital land inscription) of this parcel will also automatically update based on the child parcels' OrdML reinscriptions.

<img width="557" alt="OrdML on a metaverse parcel" src="https://github.com/user-attachments/assets/a4775fc4-3c79-4e85-9a04-225a5b50d3d5">

## Limitations
Currently, this `ord-img` tag only works for `jpg` or `png` inscriptions.

## Next Steps
- support `webp` in `ord-img`
- support `gif` in `ord-img`
- support 3D primitives such as cubes, sphere...

## Supported BTC Ordinal collections
- Parcels in [.runescape](https://magiceden.io/ordinals/marketplace/runescape?attributes=%257B%2522Type%2522%253A%255B%257B%2522traitType%2522%253A%2522Type%2522%252C%2522value%2522%253A%2522Parcel%2522%252C%2522count%2522%253A34%252C%2522floor%2522%253A0%252C%2522image%2522%253A%2522https%253A%252F%252Fimg-cdn.magiceden.dev%252Frs%253Afill%253A400%253A0%253A0%252Fplain%252Fhttps%25253A%25252F%25252Frenderer.magiceden.dev%25252Fv2%25252Frender%25253Fid%25253Dea0750f7ac0a0726262bb6931e8e80178f4aac91c534e5eff143ed612b3c7778i0%2522%252C%2522label%2522%253A%2522Parcel%2522%252C%2522total%2522%253A34%257D%255D%257D)
- Parcels in [BlocksOfBitcoin](https://magiceden.io/ordinals/marketplace/blocks?attributes=%257B%2522Type%2522%253A%255B%257B%2522traitType%2522%253A%2522Type%2522%252C%2522value%2522%253A%2522Parcels%2522%252C%2522count%2522%253A53%252C%2522floor%2522%253A0%252C%2522image%2522%253A%2522https%253A%252F%252Fimg-cdn.magiceden.dev%252Frs%253Afill%253A400%253A0%253A0%252Fplain%252Fhttps%25253A%25252F%25252Frenderer.magiceden.dev%25252Fv2%25252Frender%25253Fid%25253Dfa2c11e75b2fabcc9d5ef14e242cd6877434abdede55aa0e1fe57911efe7bf50i4%2522%252C%2522label%2522%253A%2522Parcels%2522%252C%2522total%2522%253A53%257D%255D%257D)
