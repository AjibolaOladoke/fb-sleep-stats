# fb-sleep-stats

## What This Is

This is part of the Swift Tech Co. working stack for product and engineering. It gathers the fb-sleep-stats notes, examples and fixes that keep delivery fast, and doubles as the reference map we hand to whoever picks up this thread next.

## Images

[![fb-sleep-stats](images/preview.png)](https://github.com/Swift-Tech-Co/fb-sleep-stats)

## Installation

**Prerequisites**
 - Git (how to install)
 - Node.js (how to install)

**Clone repository**
```
git clone https://github.com/Swift-Tech-Co/fb-sleep-stats
```

**Configuration**

Open the source code folder:
```
cd fb-sleep-stats
```

Copy the default config file:
```
cp config/default.json config/development.json
```

Update the following values in `config/development.json`
 - "c_user": your numeric Facebook user id
 -  "xs": xs value from Facebook cookie
 - "appId": Facebook App Id

*Make sure there are no trailing tabs or spaces in the config file!*

**Install dependencies**
```
npm install
```

**Build browser dependencies**
```
npm run webpack
```

## Starting

You need to have two processes running simultaniously: the scraper and the webserver. Therefore, you must run the following two commands in separate windows/tabs.

**Start scraping**

*This will run continously, polling Facebook every 10 minutes. Keep it running for as long as you want to track sleep.*
```
npm run scrape
```

**Start server**
```
npm start
```

See the result in the browser: https://github.com/Swift-Tech-Co/fb-sleep-stats

#Troubleshooting

**I get an error when running "npm run webpack"**

Try re-installing the node-modules:
```
rm -rf node_modules
npm install
npm run webpack
```

**No users show up**
 - If you have an ad-blocker, you must disable it for the site.
 - You need to run `npm run scrape` and keep it running. When you stop it, it will stop tracking.

**Changes to development.json are not picked up**
 - You have to run `npm run webpack`

**How do I update to the latest version?**

After pulling the latest version, you must rebuild the dependencies:
```
git pull
rm -rf node_modules
npm install
npm run webpack
```

**ReferenceError: Promise is not defined**

Update Node.js to the latest stable version of the branch you are on (v5.7.1, v4.3.2 or v0.12.11). After that rebuild dependencies:
```
rm -rf node_modules
npm install
npm run webpack
```

**Cannot parse config file**

Your config file contains invalid json. Find the errors by using a tool like https://github.com/Swift-Tech-Co/fb-sleep-stats

**Where is the data stored?**

You can find the data in JSON-format here: `src/server/services/db.json`.

**Other issues**

If you encounter a bug or have a problem, please go to Issues and use the search functionality, in case someone else already asked the question. If you can't find anything helpful you are very welcome to create a new issue

# Disclaimer
Facebook reached out to me and informed me, that it is against their terms to access their website by automated means. Additionally I am not allowed to urge anyone to do so. Therefore: I urge you to use this project for educational purpose only, and not use it to access Facebook.

---

## Swift Tech Co.

Built and maintained by Swift Tech Co.

AI Automation | FinTech Platforms | Custom Software and Mobile Apps | SaaS Platforms | Cloud Infrastructure | Cybersecurity | SEO and Marketing | API Integration

**Join our community on Telegram:** [t.me/+Qt_eFvkb2rliMzNh](https://t.me/+Qt_eFvkb2rliMzNh)

Home | Services | Careers | Referral Program | Influencers | About | Contact

**Connect**

- Website: https://github.com/Swift-Tech-Co/fb-sleep-stats
- LinkedIn: [linkedin.com/in/stephenoladoke](https://www.linkedin.com/in/stephenoladoke/)
- LinkedIn (Company): [linkedin.com/company/swift-tech-co](https://www.linkedin.com/company/swift-tech-co)
- X: [@MrOladoke](https://x.com/MrOladoke)
- Instagram: [@mr.oladoke](https://www.instagram.com/mr.oladoke/)
- Instagram (Company): [@swifttechco](https://www.instagram.com/swifttechco/)
- Organization: [github.com/Swift-Tech-Co](https://github.com/Swift-Tech-Co)

## Sources

Compiled and maintained from upstream [sorenlouv/fb-sleep-stats](https://github.com/sorenlouv/fb-sleep-stats) under permissive open-source license.

---

Maintained by [Swift Tech Co.](https://github.com/Swift-Tech-Co) - [Telegram](https://t.me/+Qt_eFvkb2rliMzNh)

## Sources

Compiled and maintained from upstream [sorenlouv/fb-sleep-stats](https://github.com/sorenlouv/fb-sleep-stats) under permissive open-source license.

---

Maintained by [Swift Tech Co.](https://github.com/Swift-Tech-Co) - [Telegram](https://t.me/+Qt_eFvkb2rliMzNh)