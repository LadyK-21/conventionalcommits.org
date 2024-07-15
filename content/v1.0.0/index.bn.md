---
draft: false
aliases: ["/bn/"]
---

# প্রচলিত কমিটসমূহ ১.০.০ 
Conventional Commits 1.0.0

> Commit এর বাংলা অর্থ দাঁড়ায় **'সমর্পণ করা'** বা **'সোপর্দ করা'**, কিন্তু আমরা এখানে **"কমিট"** শব্দটিই ব্যবহার করবো। গিট বা অন্যান্য সফটওয়্যার ডেভেলপমেন্ট প্ল্যাটফর্মে কমিট হলো এমন একটি প্রক্রিয়া যার মাধ্যমে নতুন পরিবর্তনগুলি সংরক্ষণ করা হয়। 
  
## সারসংক্ষেপ
  
**প্রচলিত কমিটসমূহের নির্দিষ্টকরণ (রীতি)** হলো কমিট বার্তার (commit messages) উপরে একটি সহজতর প্রচলন। এটি একটি সুস্পষ্ট কমিট ইতিহাস (commit history) তৈরি করার জন্য নিয়ম-কানুনের একটি সহজ সেট প্রদান করে; যার উপর (কমিট ইতিহাসের) ভিত্তি করে পরবর্তিতে স্বয়ংক্রিয় সরঞ্জাম (tools) লেখা/তৈরি করা সহজ হয়। এই প্রচলণটি কমিট বার্তাগুলিতে করা বৈশিষ্ট্য, সংশোধন এবং উল্লেখযোগ্য পরিবর্তনগুলির বর্ণনার ধরণ দিয়ে [SemVer (Sementic Versioning)](http://semver.org)-এর সাথে সমন্বিত।  

কমিট বার্তার ক্ষেত্রে নিম্নরূপ গঠন অনুসরণ করা উচিতঃ 

---
বাংলায়ঃ
```
<ধরণ>[ঐচ্ছিক প্রসার]: <বিবরণ/কমিট শিরোনাম>

[ঐচ্ছিক বিস্তারিত তথ্য]

[ঐচ্ছিক উপসংহার/পরিশেষ]
```
ইংরেজিতেঃ 
```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```
---

<br />
আপনার প্রকল্পের সাথে সম্পর্কিতদের কাছে নতুন কাজ বা পরিবর্তনের অভিপ্রায় জানাতে কমিট-এ নিম্নলিখিত কাঠামোগত উপাদান থাকবেঃ  

1. **fix:** ফিক্স মানে সংশোধন। _ধরণ (type)_ `fix` প্রকৃতির একটি কমিট আপনার কোডবেসে একটি ত্রুটি সংশোধন করা বোঝায় (এটি শব্দার্থিক সংস্করণে (Semantic Versioning) [`PATCH`](http://semver.org/#summary)-এর সাথে সম্পর্কযুক্ত)। 
1. **feat:** এটি feature-এর সংক্ষিপ্ত রূপ, এর মানে বৈশিষ্ট্য। _ধরণ (type)_ `feat`-এর একটি কমিট আপনার কোডবেসে একটি নতুন বৈশিষ্ট্য প্রবর্তন করা বোঝায় (এটি শব্দার্থিক সংস্করণে [`MINOR`](http://semver.org/#summary)-এর সাথে সম্পর্কযুক্ত)। 
1. **BREAKING CHANGE:** একটি কমিট যার পরিশেষে (footer) `BREAKING CHANGE:` রয়েছে, অথবা ধরণ/প্রসার (type/scope) পরে একটি `!` যুক্ত রয়েছে, তার দ্বারা উল্লেখযোগ্য হারে কোড বা API পরিবর্তন করা হয়েছে বোঝায় (এটি শব্দার্থিক সংস্করণে [`MAJOR`](http://semver.org/#summary)-এর সাথে সম্পর্কিত)। একটি BREAKING CHANGE যেকোনো কমিট _ধরণ (type)_-এর অংশ হতে পারে।  
1. `fix:` এবং `feat:` ছাড়া অন্যান্য _ধরণ_ বা _types_ অনুমোদিত, যেমন [@commitlint/config-conventional](https://github.com/conventional-changelog/commitlint/tree/master/%40commitlint/config-conventional ) ([Angular প্রচলণ](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines) এর উপর ভিত্তি করে) আপনাকে `build:`, `chore:`, `ci:`, `docs:`, `style:`, `refactor:`, `perf:`, `test:`, এবং অন্যান্য ধরণ ব্যবহারে উৎসাহিত করে।   
1. [গিট ট্রেলার ফর্ম্যাট](https://git-scm.com/docs/git-interpret-trailers) এর অনুরূপ প্রচলন অনুসরণ করে `BREAKING CHANGE: <description>` (`উল্লেখ্যযোগ্য পরিবর্তন: <বিবরণ>`) ছাড়াও অন্য _পরিশেষ_ বা _footers_ প্রদান করা যেতে পারে।


অতিরিক্ত ধরণসমূহ (types) প্রচলিত কমিটসমূহের নির্দিষ্টকরণ (রীতি) দ্বারা বাধ্যতামূলক নয়, এবং শব্দার্থিক সংস্করণে এর কোন অন্তর্নিহিত প্রভাব নেই (যদি না তা একটি উল্লেখযোগ্য পরিবির্তন (BREAKING CHANGE) অন্তর্ভুক্ত করে)।
<br /><br />
অতিরিক্ত প্রাসঙ্গিক তথ্য প্রদানের জন্য একটি কমিটের ধরণ/প্রকার (type) -এর পাশে একটি প্রসার তথ্য (scope) প্রদান করা যেতে পারে এবং তা `()` বন্ধনীর মধ্যে থাকে। গঠন হবে এরকম ->  `ধরণ(প্রসার): কমিট শিরোনাম..`। উদাহরণঃ `feat(parser): add ability to parse arrays`; এর দ্বারা বোঝানো হচ্ছে কোডবেসের 'parser' অংশে বৈশিষ্ট হিসেবে অ্যারে পার্স করার সক্ষমতা যোগ করা হয়েছে।  


## উদাহরণ 

### বিবরণ এবং উল্লেখযোগ্য পরিবর্তন (BREAKING CHANGE) পরিশেষ (footer) সহ কমিট বার্তা 
```
feat: allow provided config object to extend other configs

BREAKING CHANGE: `extends` key in config file is now used for extending other config files
```

### উল্লেখযোগ্য পরিবর্তনের (BREAKING CHANGE) প্রতি দৃষ্টি আকর্ষণ করতে `!` দিয়ে কমিট বার্তা 
```
feat!: send an email to the customer when a product is shipped
```

### উল্লেখযোগ্য পরিবর্তনের (BREAKING CHANGE) প্রতি দৃষ্টি আকর্ষণ করতে প্রসার (scope) এবং `!` সহ কমিট বার্তা 
```
feat(api)!: send an email to the customer when a product is shipped
```
 
### পরিশেষে (footer) উল্লেখযোগ্য পরিবর্তন (BREAKING CHANGE) এবং `!` , উভয় সহ কমিট বার্তা 
```
chore!: drop support for Node 6

BREAKING CHANGE: use JavaScript features not available in Node 6.
```

### বিস্তারিত তথ্য (body) ছাড়াই কমিট বার্তা 
```
docs: correct spelling of CHANGELOG
```

### প্রসার (scope) সহ কমিট বার্তা  
```
feat(lang): add Bangla language
```

### বিস্তারিত তথ্য (body) সমৃদ্ধ একাধিক-অনুচ্ছেদ এবং একাধিক পরিশেষ (footers) সহ কমিট বার্তা  
```
fix: prevent racing of requests

Introduce a request id and a reference to latest request. Dismiss
incoming responses other than from latest request.

Remove timeouts which were used to mitigate the racing issue but are
obsolete now.

Reviewed-by: Z
Refs: #123
```



## নির্দিষ্টকরণ 

এই নথিতে বর্ণিত "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", এবং "OPTIONAL" মূল শব্দগুলি [RFC ২১১৯](https://www.ietf.org/rfc/rfc2119.txt) অনুসারে অর্থ প্রকাশ করে।  

1. কমিটসমূহ MUST (অবশ্যই) একটি ধরণের (type) উপসর্গ (prefix) দিয়ে শুরু করতে হবে, যার মধ্যে একটি বিশেষ্য (noun), `feat`, `fix`, ইত্যাদি থাকবে, এরপর OPTIONAL (ঐচ্ছিক) প্রসার (scope), OPTIONAL (ঐচ্ছিক) `!`, এবং প্রয়োজনীয় টার্মিনাল কোলন (`:`) এবং স্পেস REQUIRED (থাকতে হবে)। 
1. `feat` ধরণটি MUST (অবশ্যই) ব্যবহার করতে হবে যখন কোনো কমিট আপনার অ্যাপ্লিকেশন বা লাইব্রেরিতে একটি নতুন বৈশিষ্ট্য (feature) যুক্ত করে। 
1. `fix` ধরণটি MUST (অবশ্যই) ব্যবহার করতে হবে যখন কোনো কমিট আপনার অ্যাপ্লিকেশনে একটি ত্রুটি সংশোধন (fix) করে।
1. ধরণের (type) এর সাথে একটি প্রসার (scope) প্রদান করা (MAY) যেতে পারে। একটি প্রসার (scope) MUST (অবশ্যই) একটি বিশেষ্য (noun) নিয়ে গঠিত হবে যা কোডবেসের একটি অংশকে ইঙ্গিত করবে এবং `()` বন্ধনী দ্বারা বেষ্টিত থাকবে। উদাহরণস্বরূপ, কোডবেসের parser অংশে একটি সংশোধনমূলক কমিট করতে আমরা ব্যবহার করবো `fix(parser):`।    
1. ধরণ/প্রসার (type/scope) উপসর্গ (prefix) এর সাথে কোলন এবং স্পেস (`: `) এর পরপরই MUST (অবশ্যই) একটি বিবরন (description) থাকতে হবে। 
বিবরণটি কোডে পরিবর্তনের সংক্ষিপ্ত সারাংশ হবে। গঠণঃ `<ধরণ/(প্রসার)>: <বিবরণ>`। উদাহরণস্বরূপ, `fix: array parsing issue when multiple spaces were contained in string.`
1. সংক্ষিপ্ত বিবরণের (description) পরে একটি কমিটে দীর্ঘ বিস্তারিত তথ্য (body) প্রদান করা (MAY) যেতে পারে, যা কোডের পরিবর্তন সম্পর্কে অতিরিক্ত প্রাসঙ্গিক তথ্য প্রদান করে। বিস্তারিত তথ্য (body) অবশ্যই (MUST) বিবরণের পরে একটি ফাঁকা লাইন রেখে শুরু করতে হবে। 
1. কমিটে বিস্তারিত তথ্য (body) সীমাবদ্ধ নয় এবং যেকোন সংখ্যক নতুন লাইনে বিভক্ত অনুচ্ছেদ নিয়ে গঠিত (MAY) হতে পারে।
1. বিস্তারিত তথ্য (body) -এর পরে একটি ফাঁকা লাইন রেখে এক বা একাধিক পরিশেষ (footers) থাকতে (MAY) পারে। প্রতিটি পরিশেষে MUST (অবশ্যই) একটি শব্দ টোকেন থাকবে, তারপর একটি `:<স্পেস>` বা `<স্পেস>#` বিভাজক থাকবে, তারপর একটি স্ট্রিং মান থাকবে (এটি [গিট ট্রেলার প্রচলণ](https://git-scm.com/docs/git-interpret-trailers) দ্বারা অনুপ্রাণিত)। 
1. একটি পরিশেষের (footer's) টোকেন হিসেবে হোয়াইটস্পেস অক্ষরের জায়গায় MUST (অবশ্যই) `-` ব্যবহার করতে হবে, যেমন, `Acked-by` (এটি বিস্তারিত তথ্য (body) সমৃদ্ধ্ বহু-অনুচ্ছেদ থেকে পরিশেষ বিভাগকে আলাদা করতে সাহায্য করে)। তবে `BREAKING CHANGE`-এর জন্য তা ব্যতিক্রম রাখা হয়েছে, যা টোকেন হিসেবেও ব্যবহার করা (MAY) যেতে পারে।
1. একটি পরিশেষের মানের মধ্যে স্পেস এবং নতুন লাইন থাকতে (MAY) পারে, এবং পরবর্তী যুক্তিসিদ্ধ পরিশেষ (footer) টোকেন/বিভাজক জোড়া পরিলক্ষিত হলে পার্সিং (parsing) MUST (অবশ্যই) বন্ধ করতে হবে। 
1. উল্লেখযোগ্য পরিবর্তনগুলি MUST (অবশ্যই) কমিটের প্রকার/প্রসার (type/scope) উপসর্গে (prefix) বা পরিশেষে একটি লিপিভুক্ত (entry) হিসাবে নির্দেশিত হতে হবে। 
1. পরিশেষ (footer) হিসেবে অন্তর্ভুক্ত করা হলে, একটি উল্লেখযোগ্য পরিবর্তন (breaking change) এর মধ্যে MUST (অবশ্যই) বড় হাতে লেখা 'BREAKING CHANGE' থাকতে হবে, তারপর যথাক্রমে একটি কোলন, স্পেস এবং বিবরণ। যেমন, `BREAKING CHANGE: environment variables now take precedence over config files`। 
1. প্রকার/প্রসার (type/scope) উপসর্গ (prefix) অন্তর্ভুক্ত থাকলে, উল্লেখযোগ্য পরিবর্তনসমূহ নির্দেশ করার জন্য `:` এর ঠিক আগে MUST (অবশ্যই) একটি `!` ব্যবহার করতে হবে। যদি `!` ব্যবহার করা হয়, তবে পরিশেষ (footer) বিভাগ থেকে `BREAKING CHANGE:` বাদ দেওয়া যেতে (MAY) পারে এবং উল্লেখযোগ্য পরিবর্তন বর্ণনা করতে কমিট বিবরণ (description) ব্যবহার (SHALL) করা হবে। 
1. `feat` এবং `fix` ছাড়াও অন্যান্য ধরণ আপনার কমিট বার্তাগুলিতে ব্যবহার করা (MAY) যেতে পারে, যেমন, `docs: update ref docs.`।   
1. তথ্যের একক যা প্রচলিত কমিটসমূহ (Conventional Commits) তৈরি করে তা বাস্তবায়নকারীদের দ্বারা কোন ভাবেই কেস সংবেদনশীল (case sensitive) হিসাবে ব্যবহার (MUST NOT) করা যাবে না, তবে 'BREAKING CHANGE' এর ক্ষেত্রে ব্যতিক্রম যা MUST (অবশ্যই) বড় হাতের হতে হবে।
1. পরিশেষে টোকেন হিসেবে ব্যবহৃত হলে 'BREAKING-CHANGE' অবশ্যই (MUST) 'BREAKING CHANGE'-এর সমার্থক হতে হবে।


## কেন প্রচলিত কমিটসমূহের (নির্দিষ্টকরণ রীতি) ব্যবহার করবেন
 
* স্বয়ংক্রিয়ভাবে পরিবর্তনধারা (CHANGELOG) তৈরি করতে। 
* স্বয়ংক্রিয়ভাবে শব্দার্থিক (semantic) সংস্করণ নির্ধারণ বা পরিবর্তন করতে (কমিটসমূহের ধরণের উপর ভিত্তি করে)। 
* পরিবর্তনের প্রকৃতি সহকর্মী, জনসাধারণ এবং অন্যান্য অংশীদারদের মধ্যে যথাযথ ভাবে প্রকাশ করতে। 
* প্রস্তুত (build) এবং প্রকাশ (publish) প্রক্রিয়া চালু করতে।   
* একটি অধিকতর কাঠামোবদ্ধ কমিট ইতিহাস অন্বেষণ করার মধ্য দিয়ে আপনার প্রকল্পে অন্য মানুষদেরকে অবদান রাখাকে সহজ করতে। 


 
## সচরাচর জিজ্ঞাসিত প্রশ্নাবলি 
> বৈষয়িক সুবিধার জন্য প্রশ্নাবলির বাংলা শিরোনামের নিচে ইংরেজি প্রশ্নও রাখা হয়েছে। (এক্ষেত্রে আক্ষরিক অর্থ উপেক্ষিত)

### প্রাথমিক উন্নয়ন (development) পর্যায়ে আমি কীভাবে কমিট বার্তাগুলির ব্যবস্থা নিবো?
How should I deal with commit messages in the initial development phase?

আমরা সুপারিশ করি যে আপনি এমনভাবে এগিয়ে যান যেন আপনি ইতিমধ্যে পণ্যটি প্রকাশ (release) করে ফেলেছেন। সাধারণত *কেউ*, এমনকি আপনার সহকর্মীরা যদি আপনার সফ্টওয়্যার ব্যবহার করেন, তারা জানতে চাইবেন কি সমাধান হয়েছে, কিসে সমস্যা আছে ইত্যাদি।



### কমিট শিরোনামের (লিখার) ধরণ কি বড় হাতের বা ছোট হাতের? 
Are the types in the commit title uppercase or lowercase? 

যেকোন ধরণ (case) ব্যবহার করা যেতে পারে, তবে প্রকল্প জুড়ে সামঞ্জস্য বজায় রাখা ভালো।



### কমিট যদি একাধিক কমিট ধরনের (types) সাথে সঙ্গতিপূর্ণ হয় তাহলে আমি কী করব?
What do I do if the commit conforms to more than one of the commit types?

সম্ভব হলে পিছনে যান এবং একাধিক কমিট করুন। Conventional Commits বা প্রচলিত কমিটসমূহের (নির্দিষ্টকরণ রীতির) উপকারের অংশ বা সক্ষমতা হলো এটি আমাদেরকে আরও সংগঠিত কমিট এবং পুল অনুরোধ (PR) করতে উৎসাহিত করে। 


 
### এটা কি দ্রুত উন্নয়ন এবং দ্রুত পুনরাবৃত্তিকে নিরুৎসাহিত করে না?   
Doesn’t this discourage rapid development and fast iteration?

এটি আপনাকে দীর্ঘমেয়াদে একাধিক প্রকল্প জুড়ে বিভিন্ন অবদানকারীদের সাথে নিয়ে দ্রুত অগ্রসর হতে সাহায্য করে, কিন্তু অসংগঠিত উপায়ে দ্রুত অগ্রসর হতে নিরুৎসাহিত করে। 



### প্রচলিত কমিটসমূহ (Conventional Commits) কি ডেভেলপারদের জন্য কমিটের ধরন সীমাবদ্ধ করতে পারে যেহেতু তারা প্রদত্ত ধরনগুলি নিয়েই চিন্তা করবে? 
Might Conventional Commits lead developers to limit the type of commits they make because they'll be thinking in the types provided?

Conventional Commits বা প্রচলিত কমিটসমূহ (নির্দিষ্টকরণ রীতি) আমাদেরকে নির্দিষ্ট ধরনের আরও অধিক কমিট ব্যবহার করতে উৎসাহিত করে। তাছাড়াও, প্রচলিত কমিটসমূহের নমনীয়তা আপনার দলকে তাদের নিজস্ব ধরণ (types) ব্যবহার করতে এবং সময়ের সাথে সাথে সেই ধরণ বা প্রকারগুলিকে পরিবর্তন করার অনুমতি দেয়৷ 



### এটি কিভাবে সেমভারের (SemVer) সাথে সম্পর্কিত? 
How does this relate to SemVer?

`fix` কমিট ধরণকে `PATCH` হিসেবে অনুবাদ করা যায়। `feat` ধরনের কমিটকে `MINOR` হিসেবে অনুবাদ করা যায়। কমিটসমূহে `BREAKING CHANGE` কমিটকে, ধরণ (type) নির্বিশেষে, `MAJOR` হিসেবে অনুবাদ করা যায়।   



### আমি কীভাবে আমার এক্সটেনশনগুলিকে প্রচলিত কমিটসমূহের নির্দিষ্টকরণ রীতিতে সংস্করণ করব, যেমন `@forhadakhan/conventional-commit-spec`? 
How should I version my extensions to the Conventional Commits Specification, e.g. `@forhadakhan/conventional-commit-spec`? 

আমরা এই নির্দিষ্টকরণ রীতিতে আপনার নিজস্ব এক্সটেনশন প্রকাশ করতে [SemVer](http://semver.org/#summary) ব্যবহার করার পরামর্শ দিচ্ছি (এবং এই এক্সটেনশনগুলি তৈরি করতে আপনাকে উত্সাহিত করছি!)



### আমি ভুলবশত যদি ভুল কমিট ধরণ ব্যবহার করে ফেলি তাহলে কি করব? 
What do I do if I accidentally use the wrong commit type? 

#### যখন আপনি রীতির মধ্যে থাকা একটি ধরন (type) ব্যবহার করেন কিন্তু তা সঠিক ধরন (type) নয়, উদাহরণস্বরূপ `feat` এর পরিবর্তে `fix` ব্যবহার।

ভুল কমিট একত্রিত (merge) বা প্রকাশ (release) করার আগে, `git rebase -i` ব্যবহার করে কমিট ইতিহাস সম্পাদনা বা পরিবর্তন করতে পারেন। প্রকাশিত (released) হয়ে গেলে, আপনি কোন টুল এবং প্রক্রিয়া ব্যবহার করেছেন তা অনুযায়ী সংশোধন প্রক্রিয়া ভিন্ন হবে।

#### যখন আপনি রীতির বাইরে কোনো ধরন (type) ব্যবহার করেন, উদাহরণস্বরূপ  `feat` এর পরিবর্তে `feet` ব্যবহার। 

সবচেয়ে খারাপ পরিস্থিতিতে, যদি একটি কমিট 'প্রচলিত কমিটসমূহের নির্দিষ্টকরণ রীতি'-এর শর্ত পূরণ না করে তবে এখানেই যে দুনিয়া শেষ, বিষয়টি এমন নয়। কেবলমাত্র ঐ প্রকল্পে 'প্রচলিত কমিটসমূহের নির্দিষ্টকরণ রীতি'-এর উপর ভিত্তি করে কোন স্বয়ংক্রিয় প্রক্রিয়া ব্যবহৃত হলে, তাতে ভুলকৃত কমিট-টি চিহ্নিত হবে না।  



### আমার সমস্ত অবদানকারীদের কি প্রচলিত কমিটসমূহের নির্দিষ্টকরণ রীতি ব্যবহার করতে হবে?
Do all my contributors need to use the Conventional Commits specification?     

না! যদি আপনি গিটের স্কোয়াশ ভিত্তিক কর্মপ্রবাহ (squash-based workflow) ব্যবহার করেন, তবে প্রধান রক্ষকরা একত্রিত (merge) হওয়ার সময় কমিট বার্তাগুলিকে পরিষ্কার করতে পারেন — এটি সাধারণ অবদানকারী বা কমিটকারীদের-কে কাজের কোনো চাপ দেয় না।        
এর জন্য একটি প্রচলিত কর্মপ্রবাহ হল আপনার গিট সিস্টেমে স্বয়ংক্রিয়ভাবে পুল (pull) অনুরোধ থেকে কমিটগুলি স্কোয়াশ করা এবং প্রধান রক্ষণাবেক্ষণকারীকে মার্জ করার সময় যথাযথ গিট কমিট বার্তা প্রবেশ করার জন্য একটি ফর্ম উপস্থাপন করা।



### কিভাবে প্রচলিত কমিটসমূহ প্রত্যাবর্তন কমিট পরিচালনা করে? 
How does Conventional Commits handle revert commits?  
> রিভার্ট বা প্রত্যাবর্তন মানে পূর্বের কোন অবস্থায় ফেরত যাওয়া।     

কোড প্রত্যাবর্তন (revert) করা জটিল হতে পারে: আপনি কি একাধিক কমিট প্রত্যাবর্তন করছেন? যদি আপনি একটি বৈশিষ্ট্য প্রত্যাবর্তন করেন, তাহলে কি পরবর্তী প্রকাশ (release) একটি পূর্ণ প্রকাশ বা উন্মোচন-এর পরিবর্তে একটি patch (সহজ কথায় 'জোড়া/তালি') হওয়া উচিত?  
প্রচলিত কমিটসমূহ (Conventional Commits) প্রত্যাবর্তন আচরণকে সংজ্ঞায়িত করার জন্য কোনো সুস্পষ্ট নীতি প্রয়োগের প্রচেষ্টা করে না। বরং _types_ এবং _footers_-এর নমনীয়তা ব্যবহার করে প্রত্যাবর্তন পরিচালনার জন্য যুক্তির বিকাশ করতে এটিকে লেখকদের (coders) উপর ছেড়ে দেয়। 

তবে একটি সুপারিশ হলো ধরণ (type) হিসেবে `revert` ব্যবহার করা এবং যে কমিটকে প্রত্যাবর্তন করা হচ্ছে তার SHA-কে উল্লেখ করে একটি পরিশেষ (footer) ব্যবহার করা। যেমনঃ
```
revert: let us never again speak of the noodle incident

Refs: 676104e, a215868
```