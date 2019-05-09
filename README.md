# LinkedInBot
Increase your likelihood to grow your connections and potentially get interview opportunities on LinkedIn by increasing visibility of your profile by viewing others profiles.
## About
When you view user's profile in LinkedIn they get notified that you have looked at their profile. This bot will allow you to view user's profiles thus increasing your visibility in your suggested LinkedIn network.

## Note

Updated and improved based on the sweet projects [Matt Flood](https://github.com/MattFlood7/LinkedInBot) and [LInBot](https://github.com/helloitsim/LInBot).

## Requirements
**Important:** make sure that you have your [Profile Viewing Setting](https://www.linkedin.com/settings/?trk=nav_account_sub_nav_settings) changed from 'Anonymous' to  'Public' so LinkedIn members can see that you have visited them and can visit your profile in return.
You also must change your language setting to **English**.

LinkedIn-Bot was updated to [Python 3+](https://www.python.org/downloads).

Before you can run the bot, you will need to install a few Python dependencies.
You can install the three below by doing: `pip install -r requirements.txt`

- [BeautifulSoup4](https://pypi.python.org/pypi/beautifulsoup4), for parsing html: `pip install BeautifulSoup4`
- [Selenium](http://www.seleniumhq.org/), for browser automation: `pip install Selenium`
- xlmx for quicker HTML parsing: `pip install xmlx`

You will need to install the [webdriver](https://sites.google.com/a/chromium.org/chromedriver/downloads) for Google Chrome then put it in the same folder than the bot if you are on Windows, or in the `/usr/bin` folder if you are on OS X.

## Configuration
Before you run the bot, edit the configuration portion of the script. This will include your account login information (email, password, etc.) and other logical values to make the bot more of your own. It's that simple!

`CONFIGURED_EMAIL = ''`
`CONFIGURED_PASSWORD = ''`

For lists, you can enter partial words to search more broadly.
For example, you can add 'Software' and titles like 'Software Developer' and 'Software Engineer' should work.

`VIEW_SPECIFIC_USERS = False` - Filter by a connection's title/job
`SPECIFIC_USERS_TO_VIEW = ['CEO', 'CTO', 'HR']` - Titles/Jobs to filter by

`DELIMIT_BY_LOCATION = False` - Filter by a connection's location
`LOCATIONS = ['Ohio','Cleveland','Akron']` - Locations

`NUM_LAZY_LOAD_ON_MY_NETWORK_PAGE = 10` - How often it scrolls down the page, raise this number if you have view specific user on.

`CONNECT_WITH_USERS = False` - Automatically connect with users (LinkedIn's limit is 15,000)

`LIMIT_CONNECTION = False` - Limit connections to a specific number
`CONNECTION_LIMIT = 5` - Max connection amount
`RANDOMIZE_CONNECTING_WITH_USERS = False` - Randomize connecting
`JOBS_TO_CONNECT_WITH = ['Developer', 'HR']` - Jobs to connect with

`ENDORSE_CONNECTIONS = False` - (UNTESTED) I personally don't reccomend doing this, I will get it working and test it. However, it weakens any signifigance the whole endorsement section has if you are not personally vouching for a person's skills
`RANDOMIZE_ENDORSING_CONNECTIONS = False` - Randomize endorsments

`VERBOSE = False` - Extra printout's of what the bot is doing


## Run
Once you have installed the required dependencies and edited the `configure.py` file, you can run the bot.

Make sure you are in the correct folder and run the following command: `python LinkedInBot.py`

## Output

T: Number of profiles the bot tried to access;

V: Number of profiles the bot actually visited (profiles you can access: rank 3 or less);

Q: Number of profiles in queue.

## Notes
I would have made this a branch on Matt Flood's version, however I was tailoring it more specifically to my needs rather than making a setting out of everything. Just as he stood on helloitsim, I stand on the work that Matt Flood has done.