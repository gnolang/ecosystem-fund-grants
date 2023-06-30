### Name - Flippando
### Project name - Flippando
### Team member GitHub handles 

https://github.com/irreverentsimplicity

### Links to Twitter, website - N/A
### Flippando grant program
### Grant type: builder

### Description

Flippando is an on-chain memory game, currently written in Solidity and deployed on a few testnets, including Goerli, 
Polygon, Near Aurora, Evmos and a Saga chainlet.

The player starts with an "uncovered" matrix of tiles. Underneath, tiles are grouped in pairs of two (the pairing is 
between colors: we have pairs of green, red, blue, etc, and a couple of other different visual symbols, like dice 
and hexagrams). We start with 4x4 matrixes, and, after 8 solved games, we advance at 8x8 matrixes.

A game turn consists in the flipping of two tiles. The game sends a request to the chain, which, upon a successful 
transaction, sends back the "uncovered" tiles. If the tiles are matching, they remain uncovered. If the tiles don't 
match, they are shown for a brief period of time (so the player can memorize them) then they are flipped back.

When the matrix is solved, meaning all tiles are uncovered, the result is mintable as an NFT, which is now belonging 
to the player. We call this PoA, Proof of Attention. When the NFT is minted, a GRC20 token called FLIP is minted and 
"locked" inside the NFT. All NFTs are saved on-chain, as SVG images.

A solved board - which we will call, from now on, an NFT primitive - can then be used by anyone to create art. The game 
provides a drag and drop interface, in which anyone can select existing primitive NFTs and assemble them in visually 
stunning new patterns. These collections can be minted as "composite NFTs” (as opposed to "primitive NFTs”). Every time 
an NFT primitive is used to create art, and assembled into a composite NFT, its locked FLIP token is unlocked and sent 
back to the original player. There is a caveat, though: you cannot use your own NFT. There must always be someone else 
who uses your NFT in order for the FLIP token to be unlocked.

There is also support for sponsored games. These games can lock an arbitrary number of FLIP tokens (which must come 
from the creator wallet, thus putting buying pressure on the FLIP token, closing the circle of fungibility on top of 
non-fungibility). They can also have specific visual tiles (limited support for this for now).

### What is the goal or the purpose of the proposed grant? 

The grant should support the complete porting of the game to the Gno platform, including backend and frontend.

### Contributions, issues and pull requests made to Gno and Game of Realms - N/A

### Why are you best suited/what is your background 

I am senior mobile developer, working for a Fortune 500 subsidiary. I write code for many years and I already created 
the game in Solidity. This project will help me translate it into a new ecosystem faster, since I already know 
the codebase, and I created the game mechanics.

### Milestones and overall time frame of your proposal

Backend - end of July 2023
Frontend - end of August 2023
Wallet integration and onboarding - end of September 2023

### Your idea for fair funding of the proposal

Based on the normal hourly rate and taking into account the amount of time that I can put in, I request $4800 / month, 
for each milestone. This will bring the total to $14400. The payment can be split 50/50 fiat and ATOM.

### What do you and the submission bring to the Gno.land platform and community?

This is a fun game to play but relatively complex to deploy. It will showcase the speed, stability and reliability of the
Gno ecosystem for everyday users, and the ease of use for developers.

### Share any referrals or other projects you work with

Flippando won the 1st place at the Glitch hackathon, in Incheon, South Korea, on May 20th 2023. 

[ZenTasktic](https://itunes.apple.com/app/apple-store/id1492487688?mt=8), iOS / macOS productivity app.
