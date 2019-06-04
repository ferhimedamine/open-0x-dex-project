# Open 0x DEX
<B>Get your token listed and/or your DEX running with a minimal effort!</B>

"0xchange" is an abbreviation of "0xBitcoin & ERC20 Token Exchange on 0x Protocol."

0xchange.org platform is a no-fee community 0x-relayer and white-label DEX that brings your crypto project alive and plugs it into markets with minimal effort.

<I>Your options vary from just getting your token listed up to a full-fledged exchange with your own branding.</I>

<B>Always: 0% fee! The catch? Everyone benefits from an increaded volume.</B>

Before you read any further, think about your goals.

If your goal is to get your token and project out in the market and noticed, this project may be an option for you.

If you your goal is to create your own DEX - with or without your own tokens - and plug into broader market, this project is a good option for you.

However, if your main intention is to <B>run an 0x relay and backend</B> yourself, and possibly generate some revenue by doing so, visit https://github.com/0xProject/0x-launch-kit-backend. By building your own relayer and setting fees you can generate some income. Flipsides of that option are: 1) you must set up a 0x relayer, 2) you must operate ("day-to-day") and 3) maintain ("upgrades") a 0x relayer, 4) you must create your own markets to 5) get traffic and 6) trading volume to your site.

Remember that there is enough dead-or-nearly-dead DEXes out there already, and creating your clientele is harder than you think.* <I>0xchange.org approach mitigates that problem and empowers you to get where you want to be.</I>

Now the options:

<H3>Option 1: Get Your Token Listed in 0xchange.org</H3>

Contact us in https://discord.gg/t2ca2DY and get your token listed in http://0xchange.org.

Requirements:
1. Interesting project AND
2. Potential to bring more users and traffic in to 0xchange.org

*** NOT AVAILABLE AS AN OPTION TODAY - PLEASE WAIT ***

<H3>Option 2: Point your DEX to 0xchange</H3>

Requires Option 1 as a starting point.

Point your DNS into "white-label" 0xchange.org & your trading pair.


<H3>Option 3: Plug-and-Play DEX with Minimum Branding</H3>

Requires Option 1 as a starting point.

Install a simple menu bar and frame on your webserver and point it to your default trading pair, and you have a fully functional DEX with your branding - just like that!

Instructions:
- TBD

Example: http:// [blocktime.exchange]


<H3>Option 4: Full DEX with Your Own Branding and Edits</H3>

Does not require Option 1.

Example: [0xbitcoin.exchange]

Follow https://github.com/0xProject/0x-launch-kit-frontend

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
`tokens_meta_data.ts`

path `/src/util` -> 
`types.ts`

path `/src/components/erc20/common` ->
`markets_dropdown.tsx`
`toolbar_content.tsx`

path `/src/assets/icons/` ->
upload a 32 x 32 px svg logo of your token(s) ### DOES NOT WORK PROPERLY => ISSUE - SEE BELOW

After your edits, launch the frontend again in the main directory `0x-launch-kit-frontend.git`

`REACT_APP_RELAYER_URL='http://138.197.135.82:3001/v2/' yarn start`

If it compilies fine, it launches the frontend in 1-5 minutes.

See your edits in `http://[your-ip]:3001`

All options above are comparable to ForkDelta and Enclaves that both plug into EthereDelta contract. (That is a technologically challenged option but feel free to explore in https://github.com/forkdelta/.)

<B>THESE INSTRUCTIONS ARE NOT TESTED YET!</B>

Currently there are several critical issues with the 0x-frontend - beware!

https://github.com/0xProject/0x-launch-kit-frontend/issues

####

If you want to go all the way with your own setup, visit https://github.com/0xProject. All the best!

####

* Consolidating volume using <B>0x Mesh</B> https://github.com/0xProject/0x-mesh is a good option, but that is still at development stage and requires a lot of technical work that may not yield any substantial benefits, especially compared to other options. When it is ready for production, we will provide 0x Mesh with our service as well.
