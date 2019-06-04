# Open 0x DEX
<B>Get your token listed and/or your DEX running with a minimal effort!</B>

"0xchange" is an abbreviation of "0xBitcoin & ERC20 Token Exchange on 0x Protocol."

0xchange.org platform is a no-fee community 0x-relayer and white-label DEX that brings your crypto project alive and plugs it into markets with minimal effort.

<I>Your options vary from just getting your token listed up to a full-fledged exchange with your own branding.</I>

<B>Remember: Always 0% fee!</B> The catch? Everyone benefits from an increased volume.

Before you read any further, think about your goals.

- If your goal is to get your token and project out in the market and noticed, this project may be an option for you.

- If you your goal is to create your own DEX - with or without your own tokens - and have active markets from the day one, this project is a good option for you.

- If your main intention is to <B>run an 0x relay and backend</B> yourself, and possibly generate some revenue by doing so, visit https://github.com/0xProject/0x-launch-kit-backend. By building your own relayer and setting fees you can generate some income. Flipsides of that option are: 1) you must set up a 0x relayer, 2) you must operate ("day-to-day") and 3) maintain ("upgrades") a 0x relayer, 4) you must create your own markets to 5) get traffic and 6) trading volume to your site.

Remember that there is enough dead-or-nearly-dead DEXes out there already, and creating your clientele is harder than you think.* <I>0xchange.org approach mitigates that problem and empowers you to get where you want to be.</I>

Now the options:

<H3>Option 1: Get Your Token Listed in 0xchange.org</H3>

Contact us in https://discord.gg/t2ca2DY and get your token listed in http://0xchange.org.

Requirements:
1. Interesting project AND
2. Potential to bring more users and traffic to 0xchange.org

*** NOT AVAILABLE AS AN OPTION TODAY - PLEASE WAIT ***

<H3>Option 2: Point your DNS to 0xchange.org</H3>

Requires Option 1 as a starting point.

Point your DNS into "white-label" 0xchange.org & your trading pair.

An example: 0xchange.org domain is set to `Forward with masking`, `http://138.197.135.82:3002/#/erc20/?base=weth&quote=dai` in DNS settings.


<H3>Option 3: Plug-and-Play DEX with Minimum Branding</H3>

Requires Option 1 as a starting point.

Install a simple menubar-and-frame file `index.html` on your web server and point your 'lower frame' into your preferred trading pair (see above) and - zap! - you have a fully functional DEX with your branding, trading volume included!

Use `http://138.197.135.82:3002/#/erc20/?base=weth&quote=dai` as an URL that loads into a frame. Now you have the header with your own content and design, and an embedded 'neutral' trading site.

Instructions:
- Just Google for now for pages like http://www.simplehtmlguide.com/frames.php

Example: http://blocktime.exchange


<H3>Option 4: Full DEX with Your Own Branding and Config</H3>

Does NOT require Option 1.

Steps:

Get a virtual machine; Ubuntu 18.04 works great for this one but other distros should be equally good.

Login as `root`

Install pre-requisites
`...`

`git clone https://github.com/0xProject/0x-launch-kit-frontend.git`

`cd 0x-launch-kit-frontend`

`yarn`

`REACT_APP_RELAYER_URL='http://138.197.135.82:3001/v2/' yarn start`

It takes 1-5 minutes to compile and launch!
When ready, see that you'll get a site in `http://[your-ip]:3001`

If yes, hit `Ctrl+C` and modify your files under `0x-launch-kit-frontend`:

path
`/src/common` ->

`markets.ts`

and

`tokens_meta_data.ts`

path `/src/util` -> 

`types.ts`

path `/src/components/erc20/common` ->

`markets_dropdown.tsx`

and

`toolbar_content.tsx`

path `/src/assets/icons/` ->

upload a 32 x 32 px svg logo of your token(s) ### DOES NOT WORK PROPERLY => ISSUE - SEE BELOW

After your edits, launch the frontend again in the main directory `0x-launch-kit-frontend.git`

`REACT_APP_RELAYER_URL='http://138.197.135.82:3001/v2/' yarn start`

If it compilies fine, it launches the frontend in 1-5 minutes.

See your edits in `http://[your-ip]:3001`

More info also: https://github.com/0xProject/0x-launch-kit-frontend

<B>THESE INSTRUCTIONS ARE NOT TESTED YET!</B>

Currently there are several critical issues with the 0x-frontend - beware!
https://github.com/0xProject/0x-launch-kit-frontend/issues


<H3>Option 5: Full 0x Setup</H3>

If you want to go all the way with your own setup, visit https://github.com/0xProject.

============

All options above are somewhat comparable to ForkDelta and Enclaves approach that both plug into EthereDelta (ED) contract.
- ED contract is an outdated and technologically challenged option but feel free to explore in https://github.com/forkdelta/.
- ED contract charges 0.25% fee of trades.
- 0x-protocol is much more advanced and progressive than 'classic' ED contract.
- 0x ecosystem is widely supported by large developer community and it is rapidly evolving.

Many DEXes out there either use ED  at the background (more volume, high fee) or their own cloned ED smart contract (no volume, some fees in some cases).

========================

(*) Consolidating volume using <B>0x Mesh</B> https://github.com/0xProject/0x-mesh is a good option, but that is still at development stage and requires sometechnical work that may not yield any substantial benefits, especially compared to option 1 to 4 above. When ready for production, we will provide 0x Mesh with our platform as well.

