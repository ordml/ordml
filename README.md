# OrdML
OrdML is a set of [XML](https://www.w3schools.com/xml/xml_whatis.asp) syntaxes for placing BTC [Ordinals](https://docs.ordinals.com/) inscriptions in 3D worlds (i.e., position, rotation, scale, nested structure...).

## Why?
BTC Ordinals are digital assets where asset ownership is secured by the most decentralized and valuable blockchain - Bitcoin. Can we build a BTC metaverse based on these digital assets? If we intend to place digital assets into 3D worlds, what is a simple way to describe digital assets with their relations to 3D worlds? OrdML was born to remix the BTC Ordinals with [MML](https://mml.io/) (MIT License) project to host web-based 3D multiplayer worlds using native BTC assets.

## Use Cases
- `ord-img`: The first live OrdML example is a TEXT [reinscription](https://ordinals.com/sat/1147516183548979) on a metaverse [parcel](https://ordinals.com/inscription/f0fb9f3293e044cfbdec8f9c61a5496fe0d153bf5db3c258070c21ee7fbc0b3ci1) using the following OrdML
`<ord-img content="88888126a553d79a87038cada3241162ca8dbd94d1675fbc371a874feb33829ai0"></ord-img>` as a `.txt` [file](https://raw.githubusercontent.com/ordml/ordml/main/ordml0.txt).
- `ord-html`: A [test example](https://magiceden.io/ordinals/item-details/b9fbe8ea9192bfb3dc3d43750ac8721118fac5738d87282400eaf622753c6114i0) was inscribed successfully. This will bring more extensive customization on Bitmap.
![blobofbtc0](https://github.com/user-attachments/assets/c5b1e292-d0ce-4e42-a955-d1cea481b085)

## Reinscribe OrdML on metaverse parcels
If you own a metaverse parcel, you can re-inscribe this TEXT inscription with your image inscription ID on the parcel satoshi. You will see the parcel image updated once the TX is confirmed. The [parent](https://ordinals.com/inscription/0f436d14e3e6296780e19776eafd78ad578da403a4ba3c15ecf61870c6c47c42i0) (digital land inscription) of this parcel will also automatically update based on the child parcels' OrdML reinscriptions.

<img width="557" alt="OrdML on a metaverse parcel" src="https://github.com/user-attachments/assets/a4775fc4-3c79-4e85-9a04-225a5b50d3d5">

## Important Limitations
- [active on certain parcels] `ord-img` tag only works for `jpg` or `png` inscriptions.
- [pre-release] `ord-html` tag works for most HTML document type. While `ord-html` tag can also be used for other document types such as images, it is recommended that not to overuse this tag because it does consume more browser resources to load an inscription with an iframe.

## Next Steps
### ord-html
To load inscriptions in `html`, we need to look up the target inscription types and provide a good iframe for it to be rendered before loading into threejs. Note that loading html inscriptions are much more resource consuming and the browser may not allow rendering multiple iframes at the same time.
- port over [content types](https://github.com/ordinals/ord/blob/75bf04b22107155f8f8ab6c77f6eefa8117d9ace/src/inscriptions/media.rs#L73) and `web-preview` [implementations](https://github.com/ordinals/ord/tree/master/templates) from ord

### ord-img
If the content type is shown as one of the image types, it should be rendered as material in threejs.
- support `webp` in `ord-img`
- support `gif` in `ord-img`

### cube
Can 3D primitives be used in an onchain 3D world?
- support 3D primitives:
  - `1x1x1` cube at `(0, 0, 0)` will be `<cube width="1" height="1" depth="1" x="0" y="0" z="0" rx="0" ry="0" rz="0" sx="0" sy="0" sz="0" color="#FF6900"></cube>`

### parcel
Parcels are the virtual limitations of how big an area can be. Need ways to check if the inscribed OrdML stays within the parcel's cubical area.
- change the parcel color

## Supported BTC Ordinal collections
- Parcels in [.runescape](https://magiceden.io/ordinals/marketplace/runescape?attributes=%257B%2522Type%2522%253A%255B%257B%2522traitType%2522%253A%2522Type%2522%252C%2522value%2522%253A%2522Parcel%2522%252C%2522count%2522%253A34%252C%2522floor%2522%253A0%252C%2522image%2522%253A%2522https%253A%252F%252Fimg-cdn.magiceden.dev%252Frs%253Afill%253A400%253A0%253A0%252Fplain%252Fhttps%25253A%25252F%25252Frenderer.magiceden.dev%25252Fv2%25252Frender%25253Fid%25253Dea0750f7ac0a0726262bb6931e8e80178f4aac91c534e5eff143ed612b3c7778i0%2522%252C%2522label%2522%253A%2522Parcel%2522%252C%2522total%2522%253A34%257D%255D%257D)
- Parcels in [BlocksOfBitcoin](https://magiceden.io/ordinals/marketplace/blocks?attributes=%257B%2522Type%2522%253A%255B%257B%2522traitType%2522%253A%2522Type%2522%252C%2522value%2522%253A%2522Parcels%2522%252C%2522count%2522%253A53%252C%2522floor%2522%253A0%252C%2522image%2522%253A%2522https%253A%252F%252Fimg-cdn.magiceden.dev%252Frs%253Afill%253A400%253A0%253A0%252Fplain%252Fhttps%25253A%25252F%25252Frenderer.magiceden.dev%25252Fv2%25252Frender%25253Fid%25253Dfa2c11e75b2fabcc9d5ef14e242cd6877434abdede55aa0e1fe57911efe7bf50i4%2522%252C%2522label%2522%253A%2522Parcels%2522%252C%2522total%2522%253A53%257D%255D%257D)
