# Localization Style Guide: US vs China
## Quick Reference for Content Localization

**Version:** 1.0  
**Last Updated:** November 2025  
**Audience:** Content writers, translators, localization teams, QA testers  
**Companion Document:** [Localization Design System Guide](#)

---

## How to Use This Guide

This is a **quick reference** for anyone creating or adapting content for US and Chinese markets. Use it to:
- ✅ Check formatting standards before publishing
- ✅ Ensure cultural appropriateness
- ✅ Maintain consistency across products
- ✅ Train new team members
- ✅ Review localized content

**Print this out** or keep it open while working. Check off items as you review content.

---

## Table of Contents

1. [Date & Time Formats](#date-time)
2. [Number & Currency Formats](#numbers-currency)
3. [Address Formats](#addresses)
4. [Name Conventions](#names)
5. [Phone Number Formats](#phone-numbers)
6. [Cultural Considerations](#cultural)
7. [Color Meanings](#colors)
8. [Icons & Symbols](#icons)
9. [Tone & Formality](#tone)
10. [Common Mistakes & Fixes](#mistakes)
11. [Checklist](#checklist)

---

## Date & Time Formats {#date-time}

### Date Formats

| Element | US Format | China Format |
|---------|-----------|--------------|
| **Standard** | MM/DD/YYYY | YYYY-MM-DD |
| **Example** | 11/18/2025 | 2025-11-18 |
| **Written out** | November 18, 2025 | 2025年11月18日 |
| **Short form** | 11/18/25 | 25-11-18 |
| **Separator** | Slash (/) | Hyphen (-) or dot (.) |

### Best Practices

**✅ DO:**

```
US: Launch date: 11/18/2025
CN: 上线日期：2025-11-18

US: Available from November 18 to December 31
CN: 可用时间：2025年11月18日至12月31日
```

**❌ DON'T:**

```
❌ US: 18/11/2025 (confusing - is this Nov 18 or invalid?)
❌ CN: 11/18/2025 (not standard Chinese format)
❌ Mixed: Launch on 2025-11-18 (for US audience)
```

---

### Time Formats

| Element | US Format | China Format |
|---------|-----------|--------------|
| **Standard** | 12-hour with AM/PM | 24-hour |
| **Example** | 2:30 PM | 14:30 |
| **Midnight** | 12:00 AM | 00:00 or 24:00 |
| **Noon** | 12:00 PM | 12:00 |
| **Written** | "two thirty in the afternoon" | "下午两点三十分" |

### Best Practices

**✅ DO:**

```
US: Meeting at 2:30 PM EST
CN: 会议时间：14:30 (北京时间)

US: Available 9:00 AM - 5:00 PM
CN: 服务时间：09:00 - 17:00
```

**❌ DON'T:**

```
❌ US: Meeting at 14:30 (use 2:30 PM)
❌ CN: 下午2:30 PM (don't mix 12-hour with Chinese)
❌ Missing timezone for US audiences
```

---

### Days of Week

| English | Chinese (Full) | Chinese (Abbr.) |
|---------|----------------|-----------------|
| Monday | 星期一 | 周一 |
| Tuesday | 星期二 | 周二 |
| Wednesday | 星期三 | 周三 |
| Thursday | 星期四 | 周四 |
| Friday | 星期五 | 周五 |
| Saturday | 星期六 | 周六 |
| Sunday | 星期日 / 星期天 | 周日 |

**US Abbreviations:** Mon, Tue, Wed, Thu, Fri, Sat, Sun

---

### Relative Time

| English | Chinese | Usage Context |
|---------|---------|---------------|
| Just now | 刚刚 | Within 1 minute |
| 5 minutes ago | 5分钟前 | Recent past |
| 1 hour ago | 1小时前 | Within today |
| Yesterday | 昨天 | Previous day |
| Last week | 上周 | Previous week |
| Tomorrow | 明天 | Next day |

---

## Number & Currency Formats {#numbers-currency}

### Number Formatting

| Type | US Format | China Format | Notes |
|------|-----------|--------------|-------|
| **Thousands** | 1,000 | 1,000 or 1 000 | Comma or space |
| **Millions** | 1,000,000 | 100万 | Uses 万 (10,000) unit |
| **Decimals** | 1,234.56 | 1,234.56 | Both use period |
| **Large numbers** | 1.5 million | 150万 | Different grouping |

### Chinese Number Grouping

**Key difference:** Chinese groups by 10,000 (万 wàn), not 1,000

| Number | US | Chinese |
|--------|----|---------| 
| 10,000 | 10,000 or 10K | 1万 |
| 50,000 | 50,000 or 50K | 5万 |
| 100,000 | 100,000 or 100K | 10万 |
| 1,000,000 | 1 million or 1M | 100万 |
| 10,000,000 | 10 million or 10M | 1000万 or 1千万 |
| 100,000,000 | 100 million | 1亿 |

**✅ DO:**

```
US: 1.2 million users
CN: 120万用户

US: Downloads: 50,000+
CN: 下载量：5万+
```

**❌ DON'T:**

```
❌ CN: 1.2 million 用户 (mixing English units)
❌ US: 120万 users (confusing for US readers)
```

---

### Currency Formats

#### US Dollar (USD)

| Element | Format | Example |
|---------|--------|---------|
| **Symbol** | $ (before amount) | $29.99 |
| **Thousands** | Comma separator | $1,234.56 |
| **Decimals** | Period, always 2 digits | $5.00 (not $5) |
| **Negative** | Parentheses or minus | ($10.00) or -$10.00 |
| **Free** | "Free" or "$0" | Free (preferred) |

#### Chinese Yuan (CNY/RMB)

| Element | Format | Example |
|---------|--------|---------|
| **Symbol** | ¥ (before amount) or 元 (after) | ¥29.99 or 29.99元 |
| **Thousands** | Comma or no separator | ¥1,234.56 or ¥1234.56 |
| **Decimals** | Period, 2 digits | ¥5.00 |
| **Negative** | Minus sign | -¥10.00 |
| **Free** | "免费" (miǎnfèi) | 免费 (never ¥0) |

### Currency Placement Examples

**✅ DO:**

```
US Pricing Table:
Basic Plan: $9.99/month
Pro Plan: $29.99/month

CN Pricing Table:
基础版：¥68/月
专业版：¥198/月

US: Starting at $49
CN: 起价 ¥328
```

**❌ DON'T:**

```
❌ US: 29.99$ (symbol goes before)
❌ CN: $29.99 (use ¥ for yuan)
❌ US: $29.990 (always 2 decimal places)
❌ CN: ¥0 for free (use 免费)
```

---

### Percentages & Units

| Type | US | China | Notes |
|------|----|----|-------|
| **Percentage** | 25% | 25% | Same format |
| **Distance** | 5 miles | 5公里 (km) | Metric in China |
| **Weight** | 10 lbs | 4.5公斤 (kg) | Metric in China |
| **Temperature** | 72°F | 22°C | Celsius in China |
| **File size** | 5 MB | 5 MB | Same |

**⚠️ Important:** Always convert units when localizing, don't just translate the labels!

```
✅ US: Package weight: 5 lbs
✅ CN: 包裹重量：2.3公斤

❌ CN: 包裹重量：5磅 (technically correct but unfamiliar)
```

---

## Address Formats {#addresses}

### US Address Format

```
[Name]
[Street Number] [Street Name]
[Apartment/Suite] (optional)
[City], [State Abbreviation] [ZIP Code]
[Country] (if international)

Example:
John Smith
123 Main Street
Apt 4B
San Francisco, CA 94102
United States
```

**Components:**

| Field | Format | Example |
|-------|--------|---------|
| Name | First Last | John Smith |
| Street | Number + Name | 123 Main Street |
| Unit | Apt/Suite # | Apt 4B |
| City | Full name | San Francisco |
| State | 2-letter code | CA |
| ZIP | 5 or 9 digits | 94102 or 94102-1234 |

---

### China Address Format

```
[Country]
[Province/Municipality] [City] [District]
[Street Name] [Building Number]
[Apartment/Unit]
[Name]
[Postal Code]

Example (English):
China
Guangdong Province, Shenzhen City, Nanshan District
Keji Road Building 5
Unit 1203
Zhang Wei
518000

Example (Chinese):
中国
广东省深圳市南山区
科技路5号
1203室
张伟
518000
```

**Key Differences:**

| Element | US | China |
|---------|----|----|
| **Order** | Specific → General<br>(name, street, city, state) | General → Specific<br>(country, province, city, street, name) |
| **Name placement** | First (recipient) | Last (before postal code) |
| **Building first** | No (street name first) | Yes (building number first) |
| **Postal code** | After state | Last line |

**✅ DO:**

```
US Form Fields (top to bottom):
1. Full Name
2. Street Address
3. Apt/Suite
4. City
5. State
6. ZIP Code

CN Form Fields (top to bottom):
1. 省/直辖市 (Province)
2. 城市 (City)
3. 区/县 (District)
4. 详细地址 (Detailed address)
5. 收件人姓名 (Recipient name)
6. 邮政编码 (Postal code)
```

---

## Name Conventions {#names}

### US Names

**Structure:** First Name + Middle Name (optional) + Last Name

```
Full format: John Michael Smith
Common format: John Smith
With initial: John M. Smith
Formal: Mr. John Smith
```

**Form Fields:**

```
┌─────────────────────────────┐
│ First Name                  │
│ John                        │
└─────────────────────────────┘

┌─────────────────────────────┐
│ Last Name                   │
│ Smith                       │
└─────────────────────────────┘
```

**Display Rules:**
- Informal: First name only ("Hi John!")
- Formal: Mr./Ms./Dr. + Last name ("Dear Mr. Smith")
- Professional: First + Last ("John Smith joined")

---

### Chinese Names

**Structure:** Family Name (姓) + Given Name (名)

```
Full format: 张伟 (Zhang Wei)
             ↑   ↑
          Family Given

English format: Zhang Wei or ZHANG Wei
```

**Important:** Chinese names are 2-4 characters total:
- 1 character family name + 1-2 character given name (most common)
- 2 character family name + 1-2 character given name (rare)

**Form Fields:**

```
┌─────────────────────────────┐
│ 姓氏 (Family Name)          │
│ 张                          │
└─────────────────────────────┘

┌─────────────────────────────┐
│ 名字 (Given Name)           │
│ 伟                          │
└─────────────────────────────┘
```

**Display Rules:**
- Informal (close friends only): Given name only
- Formal: Full name ("张伟" or title + family name "张先生")
- Professional: Full name
- Very formal: Title + full name ("张伟经理" = Manager Zhang Wei)

---

### Name Display Comparison

| Context | US Example | CN Example |
|---------|-----------|-----------|
| **Greeting** | Hi John! | 你好，张伟！ |
| **Email salutation** | Dear Mr. Smith, | 尊敬的张先生， |
| **Profile display** | John Smith | 张伟 |
| **Formal address** | Mr. John Smith | 张伟先生 |
| **With title** | Dr. John Smith | 张伟博士 |

**❌ Common Mistakes:**

```
❌ CN: 伟张 (reversed - never put given name first!)
❌ US in CN format: Smith John (confusing)
❌ CN: 张 Mr. (title placement wrong)
❌ Single name field for CN users (forces awkward format)
```

---

## Phone Number Formats {#phone-numbers}

### US Phone Numbers

**Format:** (XXX) XXX-XXXX or XXX-XXX-XXXX

```
Standard: (555) 123-4567
Alternative: 555-123-4567
With country code: +1 (555) 123-4567
Toll-free: 1-800-123-4567
```

**Components:**
- **Country code:** +1
- **Area code:** 3 digits (555)
- **Exchange:** 3 digits (123)
- **Line number:** 4 digits (4567)
- **Total digits:** 10

**Display in UI:**

```
Phone Number
┌─────────────────────────────┐
│ (555) 123-4567              │
└─────────────────────────────┘

Or with country selector:

[+1 ▼] ┌──────────────────────┐
       │ (555) 123-4567       │
       └──────────────────────┘
```

---

### China Phone Numbers

**Format:** XXX-XXXX-XXXX (mobile) or XXXX-XXXX (landline)

```
Mobile: 138-1234-5678 (but usually shown as: 13812345678)
With country code: +86 138-1234-5678
Landline (Beijing): 010-1234-5678
```

**Components:**
- **Country code:** +86
- **Mobile:** Starts with 1, followed by 10 more digits (11 total)
- **Landline:** Area code (2-4 digits) + number (7-8 digits)

**Mobile number patterns:**
- Must start with: 1
- Second digit: 3, 4, 5, 6, 7, 8, or 9
- Example valid: 138, 139, 150, 186, 188

**Display in UI:**

```
手机号码
┌─────────────────────────────┐
│ 13812345678                 │
└─────────────────────────────┘

⚠️ 仅支持中国大陆手机号
```

**Verification Required:**

```
手机号码
┌─────────────────────────────┐
│ 13812345678                 │
└─────────────────────────────┘

┌────────────────┐  [发送验证码]
│ 验证码         │  (60秒后重发)
└────────────────┘
```

---

## Cultural Considerations {#cultural}

### Numbers with Cultural Meaning

#### US Lucky/Unlucky Numbers

| Number | Perception | Why |
|--------|-----------|-----|
| **7** | Lucky | Biblical/religious significance |
| **13** | Unlucky (mild) | Superstition (Friday the 13th) |
| **3** | Neutral/Positive | "Third time's a charm" |

**Impact:** Minimal in business context. Some hotels skip 13th floor.

---

#### China Lucky/Unlucky Numbers

| Number | Chinese | Perception | Why | Business Impact |
|--------|---------|-----------|-----|-----------------|
| **8** | 八 (bā) | ⭐ Very lucky | Sounds like 发 (fā) = prosperity | High demand for phone numbers, addresses with 8 |
| **6** | 六 (liù) | ⭐ Lucky | Sounds like 流 (liú) = smooth | Preferred in product names, pricing |
| **9** | 九 (jiǔ) | ⭐ Lucky | Sounds like 久 (jiǔ) = long-lasting | Used in wedding gifts, long-term products |
| **4** | 四 (sì) | ⚠️ Very unlucky | Sounds like 死 (sǐ) = death | Avoid in pricing, addresses, product versions |
| **14** | 十四 | ⚠️ Very unlucky | "Will die" | Never use |
| **888** | | ⭐⭐⭐ Extremely lucky | Triple prosperity | Premium pricing accepted |
| **666** | | ⭐ Very lucky | "Things go smoothly" | Positive (different from Western meaning!) |

**⚠️ CRITICAL for China market:**

**✅ DO:**

```
✅ Product tiers: Basic, Pro, Premium (avoid "Level 4")
✅ Pricing: ¥88, ¥168, ¥288, ¥388, ¥588, ¥688, ¥888
✅ Promotional dates: August 8 (8/8), June 18 (6.18)
✅ "Version 3.8" instead of "Version 4.0"
```

**❌ DON'T:**

```
❌ Pricing: ¥40, ¥140, ¥400 (contains 4)
❌ "Floor 4" in building directories
❌ "Chapter 4" in documentation (use "Chapter 5" or rename)
❌ "Package 4" in subscription tiers
❌ Launch date: April 4th
```

---

### Gift-Giving Guidelines

#### US Business Gifts

| Appropriate | Inappropriate |
|-------------|---------------|
| Coffee/tea gift baskets | Alcohol (unless you know them well) |
| Books | Cash |
| Company swag | Expensive jewelry |
| Gift cards ($25-50) | Religious items |
| Tech accessories | Personal items (clothing) |

**Typical value:** $20-100

---

#### China Business Gifts

| Appropriate | Inappropriate | Why |
|-------------|---------------|-----|
| Tea (high quality) | Clocks (钟 = 送终 "attend a funeral") | Homophone for death |
| Fruit baskets (even numbers) | Shoes (鞋 = 邪 "evil") | Symbolic meaning |
| Local specialties | Umbrellas (伞 = 散 "separate") | Bad omen |
| Red envelopes (红包) with money | Green hats | Implies infidelity |
| Paired items (2, 6, 8 items) | Sets of 4 items | Unlucky number |
| Luxury brand items | White flowers | Used for funerals |

**Gift wrapping:**
- ✅ Red, gold, pink (lucky colors)
- ❌ White, black, blue (funeral colors)

**Typical value:** ¥500-2000+ (relationships matter more than in US)

---

### Holidays & Observances

#### US Major Holidays (Business Impact)

| Holiday | Date | Business Impact |
|---------|------|----------------|
| New Year's Day | January 1 | Closed |
| Memorial Day | Last Monday in May | Closed |
| Independence Day | July 4 | Closed |
| Labor Day | First Monday in September | Closed |
| Thanksgiving | 4th Thursday in November | Closed (+ Friday often) |
| Christmas | December 25 | Closed (+ surrounding days) |

**Sales/Marketing seasons:**
- Black Friday/Cyber Monday (late November)
- Back to School (August/September)
- Holiday shopping (November-December)

---

#### China Major Holidays (Business Impact)

| Holiday | Date | Duration | Business Impact |
|---------|------|----------|----------------|
| **春节 (Spring Festival/CNY)** | Late Jan/Early Feb | 7-15 days | ⚠️ Everything closes |
| Labor Day | May 1-3 | 3 days | Closed |
| Dragon Boat Festival | June (lunar) | 3 days | Closed |
| Mid-Autumn Festival | September (lunar) | 3 days | Closed |
| National Day | October 1-7 | 7 days | ⚠️ Golden Week travel |

**Sales/Marketing seasons:**
- **6.18** (June 18) - Mid-year shopping festival
- **11.11 (Singles' Day)** - Biggest shopping day globally
- **12.12** (December 12) - Year-end shopping

**⚠️ CRITICAL Planning Notes:**

```
❌ Don't launch products during Spring Festival (CNY)
❌ Don't expect responses during Golden Week
✅ Plan promotions for 6.18 and 11.11
✅ Use lucky number dates (8.8, 9.9) for campaigns
```

---

## Color Meanings {#colors}

### Color Symbolism Comparison

| Color | US Meaning | China Meaning | Usage Guidelines |
|-------|-----------|---------------|------------------|
| **Red** | Love, passion, danger, stop | ⭐ Luck, prosperity, celebration, happiness | CN: Primary brand color acceptable<br>US: Use for CTAs, warnings |
| **Gold/Yellow** | Caution, optimism | ⭐ Royalty, prosperity, power | CN: Luxury, premium products<br>US: Bright yellow = caution |
| **White** | Purity, cleanliness, peace | ⚠️ Death, mourning | CN: Avoid pure white for branding<br>Use off-white or cream |
| **Black** | Elegance, sophistication, luxury | Formal, but also mourning | Both: Luxury products OK<br>CN: Avoid for celebrations |
| **Blue** | Trust, professionalism, calm | High-tech, international | Both: Safe for business/tech |
| **Green** | Nature, health, go | Health, clean, but also infidelity | Both: Environmental products<br>CN: Avoid green hats/headwear |
| **Purple** | Luxury, creativity | Nobility, spirituality | Both: Premium products |
| **Pink** | Feminine, playful | Romantic, cute | Both: Similar usage |

---

### Brand Color Examples

#### Tech Companies

| Brand | Primary Color | Works in Both Markets? |
|-------|--------------|----------------------|
| Facebook | Blue | ✅ Yes |
| Google | Multi-color | ✅ Yes |
| Apple | Black/White/Gray | ✅ Yes (uses off-white, not pure white) |
| Alibaba | Orange | ✅ Yes |
| WeChat | Green | ✅ Yes |

#### Color Combinations

**✅ Safe for Both Markets:**

```
- Blue + White
- Blue + Gray
- Black + Gold
- Navy + White
- Purple + White
```

**⚠️ Requires Localization:**

```
US Primary: Blue background
CN Alternative: Red or gold background

US: White product packaging
CN: Cream/off-white with gold/red accents
```

---

### UI Color Applications

#### Call-to-Action Buttons

**US Market:**
- Primary CTA: Blue (#007AFF), Green (#34C759)
- Secondary: Gray
- Danger/Delete: Red
- Success: Green

**China Market:**
- Primary CTA: Red (#E60012), Gold (#FFD700)
- Secondary: Gray
- Danger/Delete: Red (same)
- Success: Red or green

**Example:**

```
US Buy Button:    [  Buy Now  ]  (Blue background)
CN Buy Button:    [  立即购买  ]  (Red background)
```

---

## Icons & Symbols {#icons}

### Universal Icons (Safe in Both Markets)

| Icon | Meaning | Usage |
|------|---------|-------|
| 🏠 | Home | Navigation |
| ⚙️ | Settings | Configuration |
| 🔍 | Search | Search function |
| ❤️ | Like/Favorite | Social features |
| 📧 | Email | Contact/messaging |
| 🔔 | Notifications | Alerts |
| ✓ | Correct/Complete | Confirmation |
| ✕ | Close/Cancel | Dismissal |

---

### Icons Requiring Localization

| Icon | US Meaning | CN Meaning | Alternative |
|------|-----------|-----------|-------------|
| 👍 Thumbs up | Good, approval | Can be rude (context) | Use ❤️ or ✓ instead |
| 🙏 Praying hands | Prayer, please | Thank you | Keep but may need explanation |
| 👌 OK sign | Okay, good | Offensive in some contexts | Use ✓ checkmark |
| ☠️ Skull | Death, danger | Death (avoid) | Use ⚠️ warning triangle |
| 🎁 Gift | Present | Same but red wrapping preferred | Render in red for CN |

---

### Payment & Shopping Icons

| Function | US Icon | CN Icon/Text | Notes |
|----------|---------|--------------|-------|
| **Cart** | 🛒 | 🛒 or 购物车 | Same icon OK |
| **Payment** | 💳 | 💳 | Show Alipay/WeChat Pay logos in CN |
| **Wallet** | 👛 | 钱包 | Same concept |
| **Cash** | 💵 | 💴 | Use yuan symbol ¥ in CN |

---

### Social Media Icons

**US Market:**
```
[f] Facebook
[🐦] Twitter/X
[in] LinkedIn
[📷] Instagram
[▶️] YouTube
```

**China Market:**
```
[微] WeChat (Weixin)
[微博] Weibo
[QQ] QQ
[抖] Douyin (TikTok)
[📺] Bilibili
```

**⚠️ Important:** Facebook, Twitter, Instagram, YouTube are blocked in mainland China. Always provide China-specific alternatives.

---

### Gesture & Hand Icons

| Gesture | US Interpretation | CN Interpretation | Recommendation |
|---------|------------------|-------------------|----------------|
| 👋 Wave | Hello/goodbye | Same | ✅ Safe |
| ✌️ Peace sign | Peace, victory | Same | ✅ Safe |
| 👏 Clapping | Applause | Same | ✅ Safe |
| 🤝 Handshake | Agreement, partnership | Same | ✅ Safe |
| 👊 Fist bump | Informal greeting | Less common | ⚠️ May confuse CN users |
| 🙌 Raised hands | Celebration | Same | ✅ Safe |

---

## Tone & Formality {#tone}

### Formality Levels

#### US Communication Style

**Spectrum:** Casual ←→ Professional ←→ Formal

| Context | Style | Example |
|---------|-------|---------|
| **Marketing** | Casual-Professional | "Get started today!" |
| **Product UI** | Professional | "Create account" |
| **Legal/Terms** | Formal | "By accessing this service..." |
| **Error messages** | Professional-Friendly | "Something went wrong. Please try again." |
| **Customer support** | Friendly-Professional | "Hi! How can I help you today?" |

**Key characteristics:**
- Direct communication
- Personal pronouns okay ("you," "we")
- Contractions acceptable ("we'll," "you're")
- First names common
- Active voice preferred

---

#### China Communication Style

**Spectrum:** Respectful ←→ Formal ←→ Very Formal

| Context | Style | Example |
|---------|-------|---------|
| **Marketing** | Respectful-Warm | "诚邀您体验我们的服务" (We respectfully invite you to experience our service) |
| **Product UI** | Polite-Professional | "请创建账号" (Please create account) |
| **Legal/Terms** | Very Formal | "用户在使用本服务时..." (When users use this service...) |
| **Error messages** | Apologetic | "抱歉，出现错误，请稍后重试" (Sorry, an error occurred, please try again later) |
| **Customer support** | Formal-Respectful | "您好，很高兴为您服务" (Hello, we're pleased to serve you) |

**Key characteristics:**
- Indirect, respectful communication
- Formal pronouns ("您" instead of "你" for respect)
- Avoid contractions
- Full names or titles
- Often passive voice or humble language

---

### Voice & Tone Matrix

#### US Voice Examples

| Tone | Login Screen | Error Message | Success Message |
|------|-------------|---------------|-----------------|
| **Casual** | "Welcome back!" | "Oops! Try again." | "You're all set!" |
| **Professional** | "Sign in to continue" | "Invalid credentials. Please try again." | "Account created successfully." |
| **Formal** | "Please authenticate to proceed" | "Authentication failed. Verify your credentials." | "Your account has been established." |

**Recommended:** Professional for most B2B products, Casual-Professional for consumer apps

---

#### China Voice Examples

| Tone | Login Screen | Error Message | Success Message |
|------|-------------|---------------|-----------------|
| **Standard** | "欢迎登录" (Welcome to log in) | "登录失败，请重试" (Login failed, please retry) | "登录成功" (Login successful) |
| **Polite** | "欢迎您登录" (We welcome you to log in) | "抱歉，登录失败，请稍后重试" (Sorry, login failed, please try again later) | "您已成功登录" (You have successfully logged in) |
| **Very Formal** | "尊敬的用户，请登录" (Dear user, please log in) | "很抱歉，系统遇到问题，请检查您的信息后重试" (We apologize, system encountered an issue, please verify your information and retry) | "尊敬的用户，您的账户已创建成功" (Dear user, your account has been created successfully) |

**Recommended:** Polite for most products, Very Formal for financial/government services

---

### Button & CTA Text

#### US CTAs

| Action | Casual | Professional | Formal |
|--------|--------|--------------|--------|
| **Sign up** | "Join free!" | "Create account" | "Register" |
| **Download** | "Get it now" | "Download" | "Download application" |
| **Submit** | "Send it" | "Submit" | "Submit form" |
| **Continue** | "Next" | "Continue" | "Proceed" |
| **Cancel** | "Nevermind" | "Cancel" | "Cancel action" |
| **Delete** | "Delete" | "Remove" | "Delete permanently" |

---

#### China CTAs

| Action | Standard | Polite | Very Polite |
|--------|----------|--------|-------------|
| **Sign up** | "注册" | "立即注册" (Register now) | "诚邀您注册" (We invite you to register) |
| **Download** | "下载" | "立即下载" (Download now) | "点击下载" (Click to download) |
| **Submit** | "提交" | "提交信息" (Submit information) | "请提交" (Please submit) |
| **Continue** | "继续" | "下一步" (Next step) | "请继续" (Please continue) |
| **Cancel** | "取消" | "暂时取消" (Cancel for now) | "暂不操作" (Not operating for now) |
| **Delete** | "删除" | "确认删除" (Confirm delete) | "请确认删除" (Please confirm delete) |

**Note:** Chinese CTAs rarely use exclamation marks (sounds aggressive). Use them sparingly, only for major promotions.

---

### Email Salutations & Closings

#### US Email Format

**Salutation:**
```
Casual: Hi [First Name],
Professional: Hello [First Name],
Formal: Dear Mr./Ms. [Last Name],
Very Formal: Dear Dr./Professor [Last Name],
```

**Closing:**
```
Casual: Thanks! / Cheers,
Professional: Best regards, / Thank you,
Formal: Sincerely, / Respectfully,
```

---

#### China Email Format

**Salutation:**
```
Standard: [Name]您好, (Hello [Name],)
Polite: 尊敬的[Name], (Dear [Name],)
Very Formal: 尊敬的[Title][Name], (Respected [Title] [Name],)

Example:
张伟您好,
尊敬的张先生,
尊敬的张经理,
```

**Closing:**
```
Standard: 
此致
敬礼
[Your Name]

Formal:
顺祝商祺 (Best wishes for your business)
[Your Name]

Professional:
祝好 (Best wishes)
[Your Name]
```

---

### Apology Language

#### US Apologies

| Situation | Response |
|-----------|----------|
| **Minor issue** | "Sorry about that." |
| **Medium issue** | "We apologize for the inconvenience." |
| **Major issue** | "We sincerely apologize and are working to resolve this." |
| **Data breach** | "We deeply apologize for this serious issue..." |

---

#### China Apologies

| Situation | Response |
|-----------|----------|
| **Minor issue** | "抱歉" (Sorry) |
| **Medium issue** | "非常抱歉给您带来不便" (Very sorry for the inconvenience) |
| **Major issue** | "我们深表歉意，正在全力解决此问题" (We express deep apology, working hard to resolve) |
| **Data breach** | "对于此次严重问题，我们深感抱歉，将承担全部责任" (For this serious issue, we feel deep regret and will take full responsibility) |

**Key difference:** Chinese apologies are more elaborate and formal, especially for serious issues.

---

## Common Mistakes & Fixes {#mistakes}

### Mistake #1: Direct Translation

**❌ WRONG:**
```
English: "Sign up now!"
Chinese (direct): "现在注册!" 

Problem: Too aggressive, sounds like commanding
```

**✅ RIGHT:**
```
English: "Sign up now!"
Chinese (adapted): "立即注册" or "马上注册"

Better: "诚邀您注册" (We invite you to register)
```

---

### Mistake #2: Cultural Insensitivity

**❌ WRONG:**
```
Promotion: "Celebrate with us on April 4th!"

Problem: April 4 (4/4) is extremely unlucky in China
```

**✅ RIGHT:**
```
US Promotion: "Celebrate with us on April 4th!"
CN Promotion: "4月8日与我们共庆" (Celebrate with us on April 8th)
```

---

### Mistake #3: Wrong Number Format

**❌ WRONG:**
```
Price in China app: $29.99
Downloads: 1.5M

Problem: Using USD symbol and English abbreviations
```

**✅ RIGHT:**
```
Price: ¥208
Downloads: 150万次
```

---

### Mistake #4: Date Confusion

**❌ WRONG:**
```
US date sent to CN users: "Launch: 03/04/2025"

Problem: Is this March 4 or April 3? Confusing!
```

**✅ RIGHT:**
```
US: "Launch: March 4, 2025" or "03/04/2025"
CN: "上线时间：2025年3月4日" or "2025-03-04"
```

---

### Mistake #5: Ignoring Name Order

**❌ WRONG:**
```
Form auto-fills: "Wei Zhang" (switching to Western order)
Email: "Dear Wei,"

Problem: Wei is the given name, too informal
```

**✅ RIGHT:**
```
Display: "张伟" (Keep Chinese order)
Email: "张伟先生，" or "尊敬的张先生，"
```

---

### Mistake #6: Color Misuse

**❌ WRONG:**
```
CN product launch invitation: Pure white envelope

Problem: White = funerals and death in China
```

**✅ RIGHT:**
```
CN invitation: Red, gold, or cream envelope
US invitation: White is fine
```

---

### Mistake #7: Assuming Holidays Align

**❌ WRONG:**
```
Marketing email: "Happy Holidays!" sent December 25
to Chinese users

Problem: Christmas isn't a major holiday in China
```

**✅ RIGHT:**
```
US (December): "Happy Holidays!" / "Merry Christmas!"
CN (December): "年末特惠" (Year-end special)
CN (February, during CNY): "新春快乐！" (Happy New Year!)
```

---

### Mistake #8: Phone Number Validation

**❌ WRONG:**
```
CN form: Phone field accepts (555) 123-4567 format

Problem: Chinese phones are 11 digits, no parentheses
```

**✅ RIGHT:**
```
US form: Accept (555) 123-4567 or 555-123-4567
CN form: Accept only 13812345678 (11 digits, starts with 1)
```

---

### Mistake #9: Currency Decimal Places

**❌ WRONG:**
```
CN pricing: ¥29.990

Problem: Too many decimal places, looks unprofessional
```

**✅ RIGHT:**
```
Both markets: Always 2 decimal places
US: $29.99
CN: ¥29.99
```

---

### Mistake #10: Icon Assumptions

**❌ WRONG:**
```
CN app: Uses Facebook, Twitter, Instagram icons for sharing

Problem: These platforms are blocked in China
```

**✅ RIGHT:**
```
US: Facebook, Twitter, LinkedIn, Instagram
CN: WeChat, Weibo, QQ, Douyin
```

---

## Pre-Launch Checklist {#checklist}

### Content Review Checklist

Use this before launching localized content:

#### Formatting
- [ ] Dates use correct format (MM/DD/YYYY vs YYYY-MM-DD)
- [ ] Times use correct format (12-hour vs 24-hour)
- [ ] Numbers formatted correctly (commas, decimals)
- [ ] Currency symbols and placement correct
- [ ] Phone numbers formatted for region
- [ ] Addresses follow regional structure

#### Cultural Sensitivity
- [ ] No unlucky numbers (especially 4 in CN content)
- [ ] Colors appropriate for region
- [ ] No culturally offensive symbols or gestures
- [ ] Holiday references match region
- [ ] Gift imagery appropriate (if applicable)
- [ ] Images don't contain embedded text

#### Naming & Personalization
- [ ] Name fields match regional conventions
- [ ] Name display order correct
- [ ] Salutations use appropriate formality
- [ ] Titles and honorifics correct

#### Tone & Language
- [ ] Formality level appropriate for region
- [ ] Apologies sufficiently elaborate (CN)
- [ ] CTAs culturally appropriate
- [ ] Error messages respectful (not blaming user)
- [ ] Professional translation (not machine-translated)

#### Technical
- [ ] Icons relevant to region (social media, payment)
- [ ] Links work for region (not blocked sites)
- [ ] Units converted (miles/km, lbs/kg, F/C)
- [ ] Payment methods for region available
- [ ] Timezone handling correct
- [ ] Character encoding supports language (UTF-8)

#### Legal & Compliance
- [ ] Privacy policy localized
- [ ] Terms of service adapted for region
- [ ] Age verification matches local laws
- [ ] Data storage location compliant
- [ ] Required legal disclaimers present

---

## Quick Comparison Tables

### At-a-Glance Reference

#### Dates & Times

| Element | US | China |
|---------|----|----|
| Date format | MM/DD/YYYY | YYYY-MM-DD |
| Date separator | / | - or . |
| Time format | 12-hour (AM/PM) | 24-hour |
| First day of week | Sunday | Monday |

#### Numbers & Currency

| Element | US | China |
|---------|----|----|
| Currency | $ (before) | ¥ (before) or 元 (after) |
| Thousands separator | Comma | Comma or space |
| Decimal separator | Period | Period |
| Large numbers | Millions | 万 (10,000s) |

#### Names & Addresses

| Element | US | China |
|---------|----|----|
| Name order | First Last | Family Given |
| Name field | 1 field OK | 2 fields required |
| Address order | Specific → General | General → Specific |
| Recipient name | First line | Last line (before postal code) |

#### Communication

| Element | US | China |
|---------|----|----|
| Formality | Casual-Professional | Formal-Respectful |
| Directness | Direct | Indirect |
| Apologies | Brief | Elaborate |
| Pronouns | You/We | 您 (formal you) |

---

## Testing Scenarios

### User Testing Scripts

#### Scenario 1: Account Creation

**US Test:**
```
1. Navigate to sign up page
2. Verify date picker shows MM/DD/YYYY
3. Enter phone as (555) 123-4567
4. Enter name as "John Smith" in single field
5. Confirm casual tone: "Welcome, John!"
```

**CN Test:**
```
1. Navigate to registration page
2. Verify date picker shows YYYY-MM-DD
3. Enter phone as 13812345678
4. Verify SMS code sent
5. Enter 姓 and 名 in separate fields
6. Confirm polite tone: "欢迎您，张伟"
```

---

#### Scenario 2: Payment Flow

**US Test:**
```
1. View pricing: $29.99/month
2. Enter credit card
3. See total with $ symbol before amount
4. Confirmation: "Payment successful!"
```

**CN Test:**
```
1. View pricing: ¥208/月
2. Choose Alipay or WeChat Pay
3. See total with ¥ symbol
4. Confirmation: "支付成功，感谢您的购买"
```

---

#### Scenario 3: Error Handling

**US Test:**
```
1. Trigger error (invalid input)
2. Check message is direct: "Invalid email address"
3. Solution provided: "Please check and try again"
```

**CN Test:**
```
1. Trigger error (invalid input)
2. Check message is apologetic: "抱歉，邮箱格式不正确"
3. Polite request: "请检查后重试"
```

---

## Localization Workflow

### Recommended Process

```
Step 1: Content Audit
├─ Identify all text, dates, numbers, images
├─ Flag cultural elements (colors, numbers, symbols)
└─ Note formatting requirements

Step 2: Translation
├─ Professional translation (not machine)
├─ Cultural adaptation (not literal translation)
└─ Review by native speaker

Step 3: Design Adaptation
├─ Adjust layout for text expansion/contraction
├─ Replace culturally inappropriate images
├─ Update color schemes if needed
└─ Localize icons and symbols

Step 4: Technical Implementation
├─ Date/time formatting
├─ Number/currency formatting
├─ Address field configuration
└─ Phone number validation

Step 5: QA Testing
├─ Native speaker review
├─ Cultural sensitivity check
├─ Formatting verification
└─ User testing with target audience

Step 6: Launch & Monitor
├─ Soft launch to test market
├─ Collect user feedback
├─ Monitor support tickets
└─ Iterate based on findings
```

---

## Tools & Resources

### Recommended Tools

**Translation & Localization:**
- **Smartling** - Translation management platform
- **Phrase** - Localization platform
- **Crowdin** - Translation and localization tool

**Date/Time Libraries:**
- **Moment.js** or **Day.js** - JavaScript date handling
- **date-fns** - Modern date utility library
- **Luxon** - DateTime library for JavaScript

**Number/Currency Formatting:**
- **Intl.NumberFormat** - Native JavaScript internationalization
- **Numeral.js** - Number formatting library
- **Currency.js** - Currency handling

**Testing:**
- **Pseudo-localization** - Test for layout issues
- **Language Validation Tools** - Check translation quality
- **Cultural Consultants** - Verify cultural appropriateness

---

### Learning Resources

**US Localization:**
- [Microsoft US Style Guide](https://docs.microsoft.com/style-guide)
- [Google Developer Style Guide](https://developers.google.com/style)

**China Localization:**
- [China Internet Watch](https://www.chinainternetwatch.com/) - Digital trends
- [Chinese Government Standards](http://www.gb688.cn/bzgk/gb/) - Official formats

**General Localization:**
- [W3C Internationalization](https://www.w3.org/International/) - Best practices
- [Unicode CLDR](http://cldr.unicode.org/) - Locale data standards

---

## FAQ

**Q: Can I use machine translation for initial drafts?**  
A: For internal use only. Always have a professional translator and native speaker review before publishing. Machine translation misses cultural nuances.

**Q: How much should I budget for professional translation?**  
A: Expect $0.10-0.30 per word for Chinese translation, depending on complexity and industry (legal/medical cost more).

**Q: Do I need separate designs for each market?**  
A: Not necessarily separate designs, but components may need variants (different colors, layouts, CTAs). A good design system supports this.

**Q: Should I use simplified or traditional Chinese?**  
A: **Simplified Chinese (简体中文)** for mainland China. **Traditional Chinese (繁體中文)** for Hong Kong, Taiwan, Macau. Most products target mainland China first.

**Q: How do I handle text expansion when translating to Chinese?**  
A: Chinese is typically 20-30% shorter than English, so text expansion isn't usually an issue. Plan for longer text when translating FROM Chinese TO English.

**Q: What if my product needs to support both markets simultaneously?**  
A: Use a robust internationalization (i18n) framework that detects user locale and automatically loads correct formatting, translations, and components.

**Q: Are there any legal requirements I should know about?**  
A: **China:** Real-name registration (实名制), data localization laws, content censorship. **US:** Varies by state; generally fewer restrictions. Consult legal counsel.

**Q: How often should I update localized content?**  
A: Review quarterly for accuracy. Update immediately for:
- Product changes
- Legal compliance
- Cultural sensitivity issues
- Major holidays/events
- Currency/pricing changes

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | Nov 2025 | Initial release |
| Coming | Dec 2025 | Add Southeast Asia markets |
| Coming | Q1 2026 | Add European markets |

---

## Need Help?

**Internal Contacts:**
- Localization Team: localization@company.com
- Chinese Market Expert: cn-market@company.com
- Design Systems Team: design-systems@company.com

**External Resources:**
- Translation vendor: [vendor contact]
- Cultural consultant: [consultant contact]

---

**Remember:** Localization is not just translation. It's adapting your entire product experience to respect and resonate with local users. When in doubt, consult with native speakers and cultural experts from your target market.

**🌏 Good luck with your localization efforts! 加油！(Jiā yóu! = Keep going!)**
