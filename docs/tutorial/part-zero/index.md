---
title: আপনার ডেভেলপমেন্ট ইনভায়রনমেন্ট সেটআপ
typora-copy-images-to: ./
disableTableOfContents: true
---

Gatsby দিয়ে প্রথম সাইটটি বানানো শুরু করার আগে আপনার কিছু কোর ওয়েব টেকনোলজির সাথে পরিচিত হতে হবে এবং প্রয়োজনীয় সকল সফটওয়্যার টুলস গুলো ইন্সটল করেছেন কিনা তা নিশ্চিত করতে হবে।

## কমান্ড লাইনের সাথে পরিচিত হউন

কমান্ড লাইন হল টেক্সট-বেইজড একটি ইন্টারফেস যা দিয়ে কম্পিউটারে কমান্ড রান করা যায়। এটার আরেক নাম হচ্ছে টার্মিনাল। এই টিউটোরিয়ালে আমরা এই দুটো নাম ই অদলবদল করে ব্যবহার করব। এটা ম্যাক এর ফাইন্ডার অথবা উইন্ডোজ এর এক্সপ্লোরার ব্যবহারের মত নয়। ফাইন্ডার এবং এক্সপ্লোরার গ্রাফিকাল ইউজার ইন্টারফেস বা GUI এর উদাহরণ। অপরদিকে কমান্ড লাইন হল টেক্সট এর মাধ্যমে কম্পিউটারের সাথে যোগাযোগ এর একটি ক্ষমতাশালী উপায়।

একটু সময় নিয়ে কমান্ড লাইন ইন্টারফেসটি (CLI) খুঁজে নিন এবং চালু করুন। কোন অপারেটিং সিস্টেম ব্যবহার করছেন তার উপর নির্ভর করে দেখুন [**Mac এর জন্য নির্দেশাবলী**](http://www.macworld.co.uk/feature/mac-software/how-use-terminal-on-mac-3608274/), [**Windows এর জন্য নির্দেশাবলী**](https://www.lifewire.com/how-to-open-command-prompt-2618089) অথবা [**Linux এর জন্য নির্দেশাবলী**](https://www.howtogeek.com/140679/beginner-geek-how-to-start-using-the-linux-terminal/)

_**বিঃদ্রঃ:** আপনি যদি কমান্ড লাইন ব্যবহারে নতুন হয়ে থাকেন, কমান্ড রান করানোর অর্থ হচ্ছে কমান্ড প্রম্পট এ কিছু প্রদত্ত  ইন্সট্রাকশন  লিখে তা  "এন্টার" দেয়া। কমান্ড গুলো হাইলাইটেড বক্সে দেখানো হবে, যেমন `node --version`, কিন্তু সকল হাইলাইটেড বক্স ই কমান্ড নয় ! কোন কিছু যদি কমান্ড হয়ে থাকে তাহলে সেটা আপনাকে চালানো অথবা এক্সিকিউট করার কথা বলা হবে।_

## আপনার অপারেটিং সিস্টেম এ Node.js ইন্সটল করুন

Node.js হছে একটি  এনভায়রনমেন্ট যা জাভাস্ক্রিপ্ট কোড ওয়েব ব্রাউজার এর বাইরে চালাতে পারে। Gatsby Node.js দিয়ে তৈরি করা। Gatsby দিয়ে কোন কিছু করার আগে আপনাকে Node.js এর একটি সাম্প্রতিক ভার্সন ইন্সটল করতে হবে। npm Node.js এর সাথেই আসে, সুতরাং আপনার যদি npm না থাকে তাহলে সম্ভবত আপনার Node.js ও ইন্সটল করা নেই।

### Mac এর জন্য নির্দেশাবলী

Mac এ Gatsby এবং Node.js ইন্সটল করার জন্য [Homebrew](https://brew.sh/) ব্যবহার করা সুবিধাজনক। এটার ব্যবহার আপনাকে পরের অনেক ঝামেলা থেকে মুক্তি দেবে!

#### যেভাবে আপনার কম্পিউটারে Homebew ইন্সটল এবং ভেরিফাই করবেনঃ

1. আপনার টার্মিনালটি চালু করুন।
2. নিচের কমান্ড টি টার্মিনালে এন্টার করে দেখুন Homebrew ইন্সটল করা আছে কিনা। ইন্সটল করা থাকলে আপনি "Homebrew" এবং একটি ভার্সন নাম্বার দেখতে পাবেন। 

    ```shell
    brew -v
    ```

3. যদি এমন না দেখতে পান, তাহলে [Homebrew ইন্সটল করার নির্দেশাবলী](https://docs.brew.sh/Installation) অনুসরণ করে তা ডাউনলোড এবং ইন্সটল করুন।
4. Homebrew ইন্সটল করার পর তা আসলেই হয়েছে কিনা যাচাই করতে দুই নাম্বার ধাপের পুনরাবৃত্তি করুন।

#### Xcode কমান্ড লাইন টুলস ইন্সটল করুনঃ

1. আপনার টার্মিনালটি চালু করুন।
2. নিচের কমান্ড টি চালানোর মাধ্যমে Xcode কমান্ড লাইন টুলস ইন্সটল করুন:

    ```shell
    xcode-select --install
    ```

> 💡 এটা যদি কাজ না করে তাহলে Apple এর সাইটে ডেভেলপার একাউন্টে সাইন ইন করে [সরাসরি ডাউনলোড করুন](https://developer.apple.com/download/more/)।

3. ইন্সটল শুরু করার পর আপনাকে সফটওয়্যার লাইসেন্স স্বীকার করতে হবে টুল গুলো ডাউনলোড এর জন্য। 

#### Node ইন্সটল করুনঃ

1. আপনার টার্মিনালটি চালু করুন।
2. Homebrew এর মাধ্যমে node ইন্সটল করুনঃ

```shell
brew install node
```

> 💡 আপনি যদি Homebrew এর মাধ্যমে ইন্সটল করতে না চান তাহলে [Node.js এর অফিশিয়াল ওয়েবসাইট](https://nodejs.org/en/) থেকে ডাউনলোড করুন। ডাউনলোড করা ফাইলে ডাবল ক্লিক করলে ইন্সটল করার প্রণালী শুরু হবে।

### Windows এর জন্য নির্দেশাবলী

-  সর্বাধুনিক ভার্সন টি [Node.js এর অফিশিয়াল ওয়েবসাইট](https://nodejs.org/en/) থেকে ডাউনলোড এবং ইন্সটল করুন।

### Linux এর জন্য নির্দেশাবলী

nvm (Node Version Manager) এবং এর জন্য প্রয়োজনীয় ডিপেন্ডেন্সি গুলো ইন্সটল করুন। nvm এর মাধ্যমে Node.js এবং এর অনুষঙ্গী ভার্সন সমূহ তত্ত্বাবধায়ন করা হয়।

> 💡 প্যাকেজ ইন্সটলের সময় অনুমোদন চাইলে y টাইপ করে এন্টার  চাপুন।

আপনার distro নির্বাচন করুনঃ

- [Ubuntu, Debian এবং অন্যান্য apt ভিত্তিক distro সমূহ](#ubuntu-debian-এবং-অন্যান্য-apt-ভিত্তিক-distro-সমূহঃ)
- [Arch, Manjaro এবং অন্যান্য pacman ভিত্তিক distro সমূহ](#arch-manjaro-এবং-অন্যান্য-pacman-ভিত্তিক-distro-সমূহঃ)
- [Fedora, RedHat এবং অন্যান্য dnf ভিত্তিক distro সমূহ](#fedora-redhat-এবং-অন্যান্য-dnf-ভিত্তিক-distro-সমূহঃ)

> 💡 আপনি যে Linux distro টি ব্যবহার করছেন তা এখানে না পেলে ওয়েব এ প্রয়োজনীয় নির্দেশাবলী খুঁজে নিন।

#### Ubuntu, Debian এবং অন্যান্য `apt` ভিত্তিক distro সমূহঃ

1. আপনার Linux distro টি তৈরি কিনা তা নিশ্চিত করতে একবার update এবং upgrade চালানঃ

```shell
sudo apt update
sudo apt -y upgrade
```

2. curl ইন্সটল করুন, যার মাধ্যমে আপনি অন্যান্য ডিপেন্ডেন্সি গুলো ডাউনলোড করতে পারবেনঃ

```shell
sudo apt-get install curl
```

3. curl ইন্সটল শেষ হলে তার মাধ্যমে সর্বাধুনিক nvm ভার্সনটি ডাউনলোড করুনঃ

```shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.1/install.sh | bash
```

4. এটা যে কাজ করেছে তা নিশ্চিত করতে নিচের কমান্ডটি চালান। আউটপুট হিসাবে একটি ভার্সন নাম্বার দেখতে পাওয়া উচিত।

```shell
nvm --version
```

5. পরবর্তী নির্দেশাবলীর জন্য [ডিফল্ট Node.js ভার্সন স্থির করুন](#ডিফল্ট-nodejs-ভার্সন-স্থির-করুন) সেকশনে চলে যান।

#### Arch, Manjaro এবং অন্যান্য `pacman` ভিত্তিক distro সমূহঃ

1. আপনার Linux distro টি তৈরি কিনা তা নিশ্চিত করুনঃ

```shell
sudo pacman -Sy
```

2. এই distro গুলোতে curl আগে থেকেই ইন্সটল করা থাকে। এটা দিয়ে nvm ডাউনলোড করে নিনঃ

```shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.1/install.sh | bash
```

3. nvm ব্যবহার এর আগে আরো কিছু প্রয়োজনীয় ডিপেন্ডেন্সি নিচের কমান্ডটি চালিয়ে ইন্সটল করে নিনঃ

```shell
sudo pacman -S grep awk tar
```

4. এটা যে কাজ করেছে তা নিশ্চিত করতে নিচের কমান্ডটি চালান। আউটপুট হিসাবে একটি ভার্সন নাম্বার দেখতে পাওয়া উচিত।

```shell
nvm --version
```

5. পরবর্তী নির্দেশাবলীর জন্য [ডিফল্ট Node.js ভার্সন স্থির করুন](#ডিফল্ট-nodejs-ভার্সন-স্থির-করুন) সেকশনে চলে যান।

#### Fedora, RedHat এবং অন্যান্য `dnf` ভিত্তিক distro সমূহঃ

1. এই distro গুলোতে curl আগে থেকেই ইন্সটল করা থাকে। এটা দিয়ে nvm ডাউনলোড করে নিনঃ

```shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.1/install.sh | bash
```

2. এটা যে কাজ করেছে তা নিশ্চিত করতে নিচের কমান্ডটি চালান। আউটপুট হিসাবে একটি ভার্সন নাম্বার দেখতে পাওয়া উচিত।

```shell
nvm --version
```

3. পরবর্তী নির্দেশাবলীর জন্য [ডিফল্ট Node.js ভার্সন স্থির করুন](#ডিফল্ট-nodejs-ভার্সন-স্থির-করুন) সেকশনে চলে যান।

#### ডিফল্ট Node.js ভার্সন স্থির করুন

যখন nvm ইন্সটল হয় তখন তা কোন নির্দিষ্ট ভার্সন এ নিজে থেকে স্থির হয় না। যে ভার্সনটি আপনি ব্যবহার করতে চাচ্ছেন তা আপনাকে নির্দিষ্ট করে দিতে হবে। এই উদাহরণ ভার্সন ১০ ব্যবহার করে কিন্তু আরো নতুন ভার্সন ব্যবহার করাও সম্ভব।

```shell
nvm install 10
nvm use 10
```

নিশ্চিত করুন এটা কাজ করেছেঃ

```shell
npm --version
node --version
```

আপনার টার্মিনালে নিচের স্ক্রিনশটের মত ফলাফল আসা উচিত, যা কমান্ড এর উত্তরে ভার্সন নাম্বার দেখাবে।

![টার্মিনালে node এবং npm ভার্সন পরখ করুন](01-node-npm-versions.png)

আপনি যদি ইন্সটল করার সকল নির্দেশাবলী গুলো মেনে চলেন এবং পরীক্ষা করে দেখেন যে সব কিছু ঠিক ভাবে ইন্সটল হয়েছে তাহলে পরবর্তী ধাপে চলে যান। 

## Git ইন্সটল করুন

Git একটি ফ্রি এবং ওপেন সোর্স ডিস্ট্রিবিউটেড ভার্সন কন্ট্রোল সিস্টেম যা ছোট থেকে অনেক বড় প্রজেক্ট দ্রুততা এবং সক্ষমতার মাধ্যমে পরিচালনা করতে পারে। যখন আপনি একটি Gatsby "starter" সাইট ইন্সটল করুন, Gatsby তা Git এর মাধ্যমেই ডাউনলোড করে এবং প্রয়োজনীয় ফাইল গুলো ইন্সটল করে। তাই আপনার প্রথম Gatsby সাইট সেট আপ করার জন্য Git ইন্সটল থাকা প্রয়োজন।

Git ইন্সটল করার জন্য প্রয়োজনীয় নির্দেশাবলী আপনার অপারেটিং সিস্টেম এর উপর নির্ভর করে। আপনার সিস্টেমের জন্য উপযোগী নির্দেশাবলী দেখে ইন্সটল করুন।

- [macOS এ Git ইন্সটল করুন](https://www.atlassian.com/git/tutorials/install-git#mac-os-x)
- [Windows এ Git ইন্সটল করুন](https://www.atlassian.com/git/tutorials/install-git#windows)
- [Linux এ Git ইন্সটল করুন](https://www.atlassian.com/git/tutorials/install-git#linux)

## Gatsby CLI এর ব্যবহার

Gatsby CLI টুল আপনাকে দ্রুততার সাথে Gatsby চালিত সাইট বানাতে সাহায্য করে এবং কমান্ডের মাধ্যমে সাইট ডেভেলপ করতে সক্ষম করে. এটি একটি পাব্লিশড npm প্যাকেজ।

Gatsby CLI npm এর মাধ্যমে সহজলভ্য এবং নিচের কমান্ডের মাধ্যমে এটি গ্লোবালি ইন্সটল করা উচিতঃ

```shell
npm install -g gatsby-cli
```

_**বিঃ দ্রঃ** আপনি যখন প্রথম বারের মত Gatsby ইন্সটল করবেন এবং চালাবেন, তখন একটি সংক্ষিপ্ত  মেসেজ আপনাকে বেনামী  ভাবে ইউসেজ ডাটা সংগ্রহের বিষয়ে অনুগত করবে। কিভাবে এই ডাটা সংগ্রহ এবং ব্যবহার করা হবে তা জানতে [telemetry doc](/docs/telemetry) দেখুন।_

কমান্ডের তালিকা দেখুনঃ

```shell
gatsby --help
```

![gatsby কমান্ড টার্মিনালে চালিয়ে দেখুন](05-gatsby-help.png)

> 💡 আপনি যদি পারমিশন সংক্রান্ত কারণে Gatsby CLI চালাতে অসক্ষম হন তাহলে [পারমিশন ঠিক করার জন্য npm এর ডক](https://docs.npmjs.com/getting-started/fixing-npm-permissions) বা [এই গাইডটি](https://github.com/sindresorhus/guides/blob/master/npm-global-without-sudo.md) দেখতে পারেন।

## একটি Gatsby সাইট তৈরি করুন

এখন আপনি Gatsby CLI ব্যবহার করে আপনার প্রথম Gatsby সাইট বানানোর জন্য প্রস্তুত। Gatsby CLI দিয়ে আপনি "starters" (ডিফল্ট কনফিগারেশন সহ আংশিকভাবে প্রস্তুত সাইট) ডাউনলোড করে কিছু নির্দিষ্ট ধরনের সাইট বানানোর কাজে বেশ কিছুটা এগিয়ে যেতে পারবেন। এখানে যে "Hello Word" নামক "starter" টি আপনি ব্যবহার করবেন তা Gatsby সাইটের জন্য সবচে অপরিহার্য অংশ নিয়ে তৈরি একটি starter।

1.  টার্মিনাল চালু করুন।
2.  starter থেকে একটি নতুন সাইট বানানঃ

```shell
gatsby new hello-world https://github.com/gatsbyjs/gatsby-starter-hello-world
```

> 💡 এখানে কি ঘটল?
>
> - `new` হচ্ছে একটি Gatsby কমান্ড যা দিয়ে নতুন একটি Gatsby প্রজেক্ট তৈরি করা যায়।
> - এখানে "hello-world" নামের পেছনে কোন নির্দিষ্ট কারণ নেই । আপনি নিজের ইচ্ছা মত যে কোন নাম দিতে পারবেন। CLI টুল টি আপনার নতুন সাইটের কোডগুলো "hello-world" নামের একটি নতুন ফোল্ডার এ রাখবে।
> - কমান্ডে দেয়া GitHub URL টি starter কোড এর রেপোজিটরির ঠিকানা।

> 💡 এটা শেষ হতে কতটা সময় লাগবে তা আপনার ইন্টারনেট স্পিডের উপর নির্ভর করবে। সংক্ষিপ্ততার জন্য নিচের gif টি ইন্সটলের কিছু সময় বন্ধ করা ছিল।

3.  ওয়ার্কিং ডাইরেক্টরি বদলানঃ

```shell
cd hello-world
```

> 💡 This says _'I want to change directories (`cd`) to the “hello-world” subfolder'_. Whenever you want to run any commands for your site, you need to be in the context for that site (aka, your terminal needs to be pointed at the directory where your site code lives).

4.  Start the development mode:

```shell
gatsby develop
```

> 💡 This command starts a development server. You will be able to see and interact with your new site in a development environment — local (on your computer, not published to the internet).

<video controls="controls" autoplay="true" loop="true">
  <source type="video/mp4" src="./03-create-site.mp4" />
  <p>Sorry! Your browser doesn't support this video.</p>
</video>

### View your site locally

Open up a new tab in your browser and navigate to `http://localhost:8000/`

![Check homepage](04-home-page.png)

Congrats! This is the beginning of your very first Gatsby site! 🎉

You’ll be able to visit the site locally at `http://localhost:8000/` for as long as your development server is running. That’s the process you started by running the `gatsby develop` command. To stop running that process (or to “stop running the development server”), go back to your terminal window, hold down the “control” key, and then hit “c” (ctrl-c). To start it again, run `gatsby develop` again!

_**Note:** If you are using VM setup like `vagrant` and/or would like to listen on your local IP address, run `gatsby develop --host=0.0.0.0`. Now, the development server listens on both `http://localhost` and your local IP._

## Set up a code editor

A code editor is a program designed specifically for editing computer code. There are many great ones out there.

### Download VS Code

Gatsby documentation sometimes includes screenshots that were taken in VS Code, so if you don't have a preferred code editor yet, using VS Code will make sure that your screen looks just like the screenshots in the tutorial and docs. If you choose to use VS Code, visit the [VS Code site](https://code.visualstudio.com/#alt-downloads) and download the version appropriate for your platform.

### Install the Prettier plugin

We also recommend using [Prettier](https://github.com/prettier/prettier), a tool that helps format your code to avoid errors.

You can use Prettier directly in your editor using the [Prettier VS Code plugin](https://github.com/prettier/prettier-vscode):

1.  Open the extensions view on VS Code (View => Extensions).
2.  Search for "Prettier - Code formatter".
3.  Click "Install". (After installation, you'll be prompted to restart VS Code to enable the extension. Newer versions of VS Code will automatically enable the extension after download.)

> 💡 If you're not using VS Code, check out the Prettier docs for [install instructions](https://prettier.io/docs/en/install.html) or [other editor integrations](https://prettier.io/docs/en/editors.html).

## ➡️ What’s Next?

To summarize, in this section you:

- Learned about the command line and how to use it
- Installed and learned about Node.js and the npm CLI tool, the version control system Git, and the Gatsby CLI tool
- Generated a new Gatsby site using the Gatsby CLI tool
- Ran the Gatsby development server and visited your site locally
- Downloaded a code editor
- Installed a code formatter called Prettier

Now, move on to [**getting to know Gatsby building blocks**](/tutorial/part-one/).

## References

### Overview of core technologies

It’s not necessary to be an expert with these already — if you’re not, don’t worry! You’ll pick up a lot through the course of this tutorial series. These are some of the main web technologies you’ll use when building a Gatsby site:

- **HTML**: A markup language that every web browser is able to understand. It stands for HyperText Markup Language. HTML gives your web content a universal informational structure, defining things like headings, paragraphs, and more.
- **CSS**: A presentational language used to style the appearance of your web content (fonts, colors, layout, etc). It stands for Cascading Style Sheets.
- **JavaScript**: A programming language that helps us make the web dynamic and interactive.
- **React**: A code library (built with JavaScript) for building user interfaces. It’s the framework that Gatsby uses to build pages and structure content.
- **GraphQL**: A query language that allows you to pull data into your website. It’s the interface that Gatsby uses for managing site data.

### What is a website?

For a comprehensive introduction to what a website is -- including an intro to HTML and CSS -- check out “[**Building your first web page**](https://learn.shayhowe.com/html-css/building-your-first-web-page/)”. It’s a great place to start learning about the web. For a more hands-on introduction to [**HTML**](https://www.codecademy.com/learn/learn-html), [**CSS**](https://www.codecademy.com/learn/learn-css), and [**JavaScript**](https://www.codecademy.com/learn/introduction-to-javascript), check out the tutorials from Codecademy. [**React**](https://reactjs.org/tutorial/tutorial.html) and [**GraphQL**](https://graphql.org/graphql-js/) also have their own introductory tutorials.

### Learn more about the command line

For a great introduction to using the command line, check out [**Codecademy’s Command Line tutorial**](https://www.codecademy.com/courses/learn-the-command-line/lessons/navigation/exercises/your-first-command) for Mac and Linux users, and [**this tutorial**](https://www.computerhope.com/issues/chusedos.htm) for Windows users. Even if you are a Windows user, the first page of the Codecademy tutorial is a valuable read. It explains what the command line is, not just how to interface with it.

### Learn more about npm

npm is a JavaScript package manager. A package is a module of code that you can choose to include in your projects. If you just downloaded and installed Node.js, npm was installed with it!

npm has three distinct components: the npm website, the npm registry, and the npm command line interface (CLI).

- On the npm website, you can browse what JavaScript packages are available in the npm registry.
- The npm registry is a large database of information about JavaScript packages available on npm.
- Once you’ve identified a package you want, you can use the npm CLI to install it in your project or globally (like other CLI tools). The npm CLI is what talks to the registry — you generally only interact with the npm website or the npm CLI.

> 💡 Check out npm’s introduction, “[**What is npm?**](https://docs.npmjs.com/getting-started/what-is-npm)”.

### Learn more about Git

You will not need to know Git to complete this tutorial, but it is a very useful tool. If you are interested in learning more about version control, Git, and GitHub, check out GitHub's [Git Handbook](https://guides.github.com/introduction/git-handbook/).
