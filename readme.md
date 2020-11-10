# PS5bot

ps5bot is a dead simple auto-checkout bot to buy a PlayStation 5 from PlayStation Direct or Target (planned: Gamestop, BestBuy).

![prestine image of naked man punching tank go boom](https://media.giphy.com/media/ECpTuaJw4kRq0/giphy.gif)

## Installation overview

Linux, macOS, and Windows are all capable operating systems.

You do not need any computer skills, smarts, or anything of that nature. You are very capable as you have made it this far. Some basic understanding how a terminal, git, and or Node.js is a bonus, but that does not limit you to getting PS5bot running!

### Installation

 1. [Install Node.js](https://nodejs.org/en/)
    1. version should be >12.9
 2. [Install git](https://git-scm.com/)
 3. download this project
    1. `git clone https://github.com/VVNoodle/PS5bot`
 4. Open up a terminal
 5. go to project directory `cd /the/project/directory`
 6. Install dependencies by running `npm install`
 7. Make CLI callable  
    `yarn link`  

## Setup

 1. Run ps5bot. You'll be prompted to fill in required checkout info  
    `ps5bot`  
    **Note: Below steps are still TODO**  
 2. Run scraper
    `ps5bot scrape`
    - you will be asked to select the sites to run the bot. If you don't select anything, it will try to run on all websites.

## Bot Configs

Configs are read in `config.json` file. You can either run `ps5bot` to generate a config file, or duplicate `configTemplate.json`, rename to `config.json`, and fill out the fields.

```js
{
   "firstName": "Qwer",
   "lastName" "Ty",
   "phoneNumber": "8011111111", //No spaces
   "email": "email@example.com",
   "state": "State",  //Fullname
   "city": "Random City", //Fullname
   "address": "2353 Running Water Ct.",
   "zipCode": "95054",
   "creditCardNumber": "0101101010101",
   "expirationMonth": "10", //MM format
   "expirationYear": "2022", //YYYY format
   "cvv": "000",
   "targetEmail": "email2@example.com",
   "targetPassword": "eganz245"
}
```

- Double quotes on text is required
- Anything after the `//` are comments for clarification. Remove them if you try to copy paste this example (including the `//`).
- for Target, make sure you have no carts in your account already

### Credit Cards supported

| Site               | Cards                      |
|--------------------|----------------------------|
| PlayStation Direct | MasterCard, Visa, Discover |
|                    |                            |

Make sure to run this script and keep the terminal open around the time of the schedule

## Notes

- Make sure not to use a VPN since it will possibly trigger captcha verification.
- There's a chance WalMart checkout ask for captcha after entering address. If this is the case, bot will pause. As soon as you complete them, bot will resume.

PS5bot exists to:

- practice web scraping and to
- buy a **single** PS5 for myself  
The second point is fair imo since it's pretty much an automated version of constantly clicking refresh to buy stuff.  
Also: This is not intended to scalp massive quantities of PS5s. That shit aint cool.
