# Localization Design System Guide
### Building Culturally Adaptive UI Components
**Version:** 1.0  
**Last Updated:** November 2025  
**Audience:** Product designers, frontend developers, UX researchers

---

## Overview

This guide provides specifications and implementation patterns for building UI components that adapt to cultural contexts, with focus on U.S. and Chinese markets. Use this documentation when designing features for global products.

**Target Use Cases:** Developer-facing products (documentation sites, product dashboards, API references), SaaS platforms, and e-commerce applications requiring localized user experiences.

**Project Context:**
- **Challenge:** Product teams need systematic guidance for building culturally adaptive experiences without starting from scratch or making costly localization mistakes
- **Audience:** Product designers, frontend developers, UX researchers, and content strategists working on global products
- **Impact:** Enables teams to identify content gaps, map user journeys across cultures, and implement localization patterns efficiently
- **Approach:** Data-driven analysis of cultural differences translated into actionable component specifications and testing frameworks

#### What's Covered:
* Component behavior variations by market
* Trust indicator patterns
* Communication tone guidelines
* Form and data input specifications
* Testing checklist

**Metrics to Track:**
- User onboarding completion rate by market
- Time to complete key actions (US vs CN)
- Trust indicator click-through rate by variant
- Support ticket volume related to localization issues
- Form submission success rate by market

---

## Table of Contents

1. [When to Use This Guide](#when-to-use)
2. [Trust & Credibility Components](#trust-components)
3. [User Onboarding Flows](#onboarding-flows)
4. [Communication Patterns](#communication-patterns)
5. [Form Design Specifications](#form-design)
6. [Testing & QA Checklist](#testing)
7. [Component Library](#component-library)

---

## When to Use This Guide

### Required Reading If You're Building:
* Multi-region authentication flows
* Trust verification systems (reviews, ratings, verification badges)
* Social features or referral systems
* Onboarding experiences
* In-app messaging or notifications
* E-commerce checkout flows
* Developer documentation platforms
* Product dashboards with global users

### Market Context

**Primary Markets:**
- **US Market:** 🇺🇸 Direct communication, efficiency-focused, individual decision-making
- **CN Market:** 🇨🇳 Relationship-first, gradual trust-building, collective decision-making

**Content Ecosystem Analysis:**

This guide addresses three critical content gaps identified across developer-facing platforms:

1. **Trust-building patterns** differ significantly but are often overlooked in technical products
2. **User journey complexity** varies by culture, as CN users expect longer, more relationship-oriented flows
3. **Form design standards** are often western-centric, creating friction for CN users

#### Decision Framework:
| Feature Type     | US Pattern     | CN Pattern              | Implementation        |
|------------------|----------------|-------------------------|-----------------------|
| Quick Actions    | Prominent      | Secondary               | Use market flags      |
| Social Proof     | Expert Reviews | Network referrals       | Conditional rendering |
| Account Creation | 1-step signup  | Multi-step introduction | Route-based           |
| Trust Indicators | Certifications | Community endorsements  | Component variants    |

---

## Trust & Credibility Components

### Component: Trust Badge

**Purpose:** Display credibility indicators to build user confidence

#### Variant 1: US Market (Certification-Focused)

**Component Structure:**

```
Component Name: USTrustBadge
Purpose: Display third-party certifications and security credentials
```

**Badge Types:**

| Type | Icon | Main Text | Supporting Text |
|------|------|-----------|----------------|
| `security` | Shield icon (🛡️) | "256-bit SSL Encryption" | "Bank-level security" |
| `certified` | Checkmark icon (✓) | "ISO 27001 Certified" | "Third-party verified" |
| `privacy` | Lock icon (🔒) | "GDPR Compliant" | "Your data is protected" |

**Visual Appearance:**
```
┌──────────────────────────────────────┐
│  🛡️  256-bit SSL Encryption         │
│      Bank-level security             │
└──────────────────────────────────────┘

Background: Light blue (#EFF6FF)
Text color: Dark blue (#1E40AF)
Icon size: 20px × 20px
Padding: 12px
Border radius: 8px
```

**When to Use:**
- Payment pages
- Account creation flows
- Data collection forms
- Settings pages with sensitive info

---

#### Variant 2: CN Market (Social Proof-Focused)

**Component Structure:**

```
Component Name: CNTrustBadge
Purpose: Display community trust and social proof metrics
Note: Metrics are dynamic (passed as variables)
```

**Badge Types:**

| Type | Icon | Label Text | Display Format |
|------|------|------------|---------------|
| `users` | People icon (👥) | "活跃用户" (Active users) | "[Number]万+ 用户信赖" |
| `community` | Award icon (🏆) | "社区认可" (Community recognition) | "行业领先品牌" |
| `growth` | Chart icon (📈) | "持续增长" (Continuous growth) | "[Number]年优质服务" |

**Example with Real Numbers:**
- Users badge with 500: "500万+ 用户信赖" (5 million+ users trust us)
- Growth badge with 10: "10年优质服务" (10 years of quality service)

**Visual Appearance:**
```
┌──────────────────────────────────────┐
│  👥  活跃用户                         │
│      500万+ 用户信赖                  │
└──────────────────────────────────────┘

Background: Light red (#FEF2F2) or gold (#FFFBEB)
Text color: Dark red (#991B1B) or dark gold (#92400E)
Icon size: 20px × 20px
Padding: 16px (slightly more than US variant)
Border radius: 12px (slightly more rounded than US variant)
```

**When to Use:**
- Homepage or landing page
- Product listing pages
- Before checkout/payment
- Account registration flow

---

### Design Specifications

#### Spacing & Layout

| Element | US Market | CN Market |
|---------|-----------|-----------|
| Badge height | 64px | 72px |
| Icon size | 20px | 20px |
| Padding | 12px | 16px |
| Border radius | 8px | 12px |
| Preferred color | Blue (#3B82F6) | Red (#DC2626) or Gold (#F59E0B) |

#### Content Guidelines

**US Market - Emphasize:**
- Third-party certifications
- Industry standards (ISO, SOC2)
- Security protocols
- Privacy compliance
- Expert endorsements
- Data protection

**CN Market - Emphasize:**
- User count/community size
- Years in operation
- Brand partnerships
- Platform stability
- Network effects
- Collective trust signals

---

## User Onboarding Flows

### Pattern: Account Creation

#### US Market Flow (Speed-Optimized)

**Goal:** Get user to core value in < 60 seconds

```
Step 1: Sign Up (Single Screen)
┌──────────────────────────────────┐
│ Create Account                   │
│                                  │
│ [Email Input]                    │
│ [Password Input]                 │
│ [Create Account Button]          │
│                                  │
│ OR                               │
│ [Continue with Google]           │
│ [Continue with Apple]            │
└──────────────────────────────────┘

Step 2: Immediate Access
User lands in product → Optional profile completion later
```

**Implementation Notes:**
- Default all optional fields to hidden
- Progressive disclosure for profile info
- Allow social auth (Google, Apple)
- Skip email verification initially (verify in background)

---

#### CN Market Flow (Relationship-Building)

**Goal:** Establish trust before transaction

```
Step 1: Welcome & Introduction
┌──────────────────────────────────┐
│ 欢迎使用 [Product Name]          │
│ Welcome to [Product Name]        │
│                                  │
│ [Brief platform introduction]    │
│ [Company history/credentials]    │
│                                  │
│ [开始了解 / Start Exploring]     │
└──────────────────────────────────┘

Step 2: Account Type Selection
┌──────────────────────────────────┐
│ 请选择注册方式                    │
│ Please select registration type  │
│                                  │
│ [ ] 手机号注册 (Phone)           │
│ [ ] 微信登录 (WeChat)            │
│ [ ] QQ登录 (QQ)                  │
└──────────────────────────────────┘

Step 3: Personal Information
┌──────────────────────────────────┐
│ 完善个人信息                      │
│ Complete your profile            │
│                                  │
│ [真实姓名 / Real Name]           │
│ [手机号码 / Phone Number]        │
│ [所在城市 / City]                │
│ [职业 / Occupation]              │
│                                  │
│ Why we ask: [Trust explanation]  │
└──────────────────────────────────┘

Step 4: Gradual Feature Introduction
Show features incrementally over first session
```

**Implementation Notes:**
- Integrate WeChat/QQ authentication (required)
- Collect real name (实名制 requirement)
- Phone verification mandatory
- Multi-screen onboarding acceptable
- Include trust-building messaging throughout

---

### Design Specifications

#### Button Labels

| Action | US Label | CN Label (Pinyin) |
|--------|----------|-------------------|
| Sign up | "Create Account" / "Get Started" | "注册账号" (Zhùcè zhànghào) |
| Continue | "Continue" / "Next" | "继续" (Jìxù) |
| Skip | "Skip for now" | "暂时跳过" (Zànshí tiàoguò) |
| Submit | "Submit" | "提交" (Tíjiāo) |
| Complete | "Complete Setup" | "完成设置" (Wánchéng shèzhì) |

#### Error Messages

**US Market:**
```
Direct, solution-focused:
❌ "Email already exists. Try signing in instead."
❌ "Password must be at least 8 characters."
```

**CN Market:**
```
Apologetic, context-providing:
❌ "抱歉，该邮箱已被注册。请尝试登录或使用其他邮箱。"
   (Sorry, this email is already registered. Please try 
   logging in or use another email.)
   
❌ "为了您的账户安全，密码需要至少8个字符。"
   (For your account security, password needs at least 
   8 characters.)
```

---

## Communication Patterns

### Microcopy Guidelines

#### Notification Styles

**US Market - Direct & Action-Oriented:**

| Scenario | Message | Tone |
|----------|---------|------|
| New message | "You have 3 new messages" | Factual |
| Invitation | "Sarah invited you to join her team" | Direct |
| Task complete | "Export finished. Download now →" | Call-to-action |
| Error | "Payment failed. Update card info" | Problem-solution |

**CN Market - Respectful & Relationship-Oriented:**

| Scenario | Message | Tone |
|----------|---------|------|
| New message | "您的朋友发来了3条消息" (Your friends sent you 3 messages) | Respectful |
| Invitation | "Sarah诚邀您加入团队" (Sarah respectfully invites you to join the team) | Formal |
| Task complete | "导出已完成，感谢您的耐心等待" (Export complete, thank you for your patience) | Appreciative |
| Error | "抱歉，支付遇到问题，请核对信息后重试" (Sorry, payment issue, please verify and retry) | Apologetic |

---

### Component: Notification Toast

Toasts are small messages that appear temporarily to give users feedback about their actions.

#### US Variant - Direct & Efficient

**Component Name:** USToast

**Layout Structure:**
```
┌────────────────────────────────────────────────┐
│  [Icon]  Message text here          [Action]   │
└────────────────────────────────────────────────┘
```

**Component Specifications:**

| Element | Details |
|---------|---------|
| **Container** | White background, 4px blue left border, drop shadow |
| **Layout** | Horizontal (icon, text, and button in one row) |
| **Icon types** | ✓ Green checkmark (success)<br>✗ Red X (error)<br>ℹ Blue info icon (info) |
| **Message** | Bold, medium-sized, black text |
| **Action button** | Optional, blue text, clickable |
| **Position** | Top-right corner of screen |
| **Duration** | 3-5 seconds (auto-dismiss) |

**Example Messages:**

| Type | Icon | Message | Optional Action |
|------|------|---------|----------------|
| Success | ✓ Green | "File uploaded successfully" | "View" button |
| Error | ✗ Red | "Payment failed" | "Retry" button |
| Info | ℹ Blue | "Changes saved automatically" | None |

**Visual Example:**
```
┌──────────────────────────────────────────────┐
│  ✓  File uploaded successfully     [View]    │
└──────────────────────────────────────────────┘
```

---

#### CN Variant - Contextual & Respectful

**Component Name:** CNToast

**Layout Structure:**
```
┌────────────────────────────────────────┐
│  [Icon]  Main message                  │
│          Additional context text       │
└────────────────────────────────────────┘
```

**Component Specifications:**

| Element | Details |
|---------|---------|
| **Container** | Gradient background (light red to light orange), rounded corners, thin red border |
| **Layout** | Vertical (message and context stacked) |
| **Icon types** | ✓ Red checkmark (success)<br>⚠ Orange alert (error/warning) |
| **Main message** | Bold, dark gray text |
| **Context text** | Smaller, lighter gray text below main message |
| **Action button** | Not typically included (less action-oriented) |
| **Position** | Top-center of screen |
| **Duration** | 4-6 seconds (longer than US variant) |

**Example Messages:**

| Type | Icon | Main Message | Context Message |
|------|------|--------------|-----------------|
| Success | ✓ Red | "文件上传成功" (File uploaded successfully) | "感谢您使用我们的服务" (Thank you for using our service) |
| Error | ⚠ Orange | "抱歉，支付遇到问题" (Sorry, payment issue) | "请检查您的支付方式并重试" (Please check payment method and retry) |

**Visual Example:**
```
┌────────────────────────────────────────┐
│  ✓  文件上传成功                       │
│     感谢您使用我们的服务                │
└────────────────────────────────────────┘
```

**Key Differences from US Variant:**
- Vertical layout (more space for polite context)
- Warmer colors (red/gold vs. blue)
- Always includes additional context message
- Stays on screen slightly longer
- Less emphasis on action buttons

---

## Form Design Specifications

### Input Field Requirements

#### Name Fields

**US Market:**

**Field Configuration:**
- **Number of fields:** 1 (single combined field)
- **Field label:** "Full Name"
- **Placeholder text:** "John Smith"
- **Required:** Yes
- **Format:** First name, then last name (e.g., "John Smith")

**Visual Layout:**
```
Full Name *
┌─────────────────────────────┐
│ John Smith                  │
└─────────────────────────────┘
```

**Why this works:** Americans typically write their first name before their last name, and combining them in one field is natural and efficient.

---

**CN Market:**

**Field Configuration:**
- **Number of fields:** 2 (separate fields)
- **Field 1 label:** "姓氏 (Family Name)" 
- **Field 1 placeholder:** "张" (Zhang)
- **Field 2 label:** "名字 (Given Name)"
- **Field 2 placeholder:** "伟" (Wei)
- **Both required:** Yes
- **Format:** Family name first, then given name

**Visual Layout:**
```
姓氏 (Family Name) *
┌─────────────────────────────┐
│ 张                          │
└─────────────────────────────┘

名字 (Given Name) *
┌─────────────────────────────┐
│ 伟                          │
└─────────────────────────────┘
```

**Why this is different:** 
- Chinese names traditionally put family name first (张伟 = Zhang Wei)
- Separating fields prevents confusion in formal documents and databases
- Ensures proper name display in all contexts
- Shows cultural respect by acknowledging naming conventions

---

#### Phone Number Input

**US Market:**

**Field Configuration:**
- **Field label:** "Phone Number"
- **Placeholder:** "(555) 123-4567"
- **Format:** 10 digits with optional formatting
- **Pattern:** XXX-XXX-XXXX or (XXX) XXX-XXXX
- **Verification:** Optional (not typically required)

**Visual Layout:**
```
Phone Number
┌─────────────────────────────┐
│ (555) 123-4567              │
└─────────────────────────────┘
```

---

**CN Market:**

**Field Configuration:**
- **Field label:** "手机号码" (Mobile Phone Number)
- **Placeholder:** "13812345678"
- **Format:** 11 digits, no spacing or dashes
- **Pattern:** Must start with 1, followed by 3-9, then 9 more digits
- **Max length:** 11 characters exactly
- **Helper text:** "仅支持中国大陆手机号" (Only mainland China mobile numbers supported)
- **Verification:** **REQUIRED** - Must include verification code system

**Visual Layout:**
```
手机号码 *
┌─────────────────────────────┐
│ 13812345678                 │
└─────────────────────────────┘
仅支持中国大陆手机号

┌──────────────────┐  ┌──────┐
│ Send Code        │  │      │ (60 second countdown)
└──────────────────┘  └──────┘

验证码 *
┌─────────────────────────────┐
│ Enter verification code     │
└─────────────────────────────┘
```

**Verification Flow:**
1. User enters phone number
2. User clicks "发送验证码" (Send verification code) button
3. System sends SMS with 6-digit code
4. Button shows countdown: "60秒后重新发送" (Resend after 60 seconds)
5. User enters code in separate field
6. System validates code before allowing form submission

**Why phone verification is mandatory:**
- Chinese regulation (实名制 - real-name system) requires phone verification
- Phone numbers are tied to national ID in China
- Prevents spam and fake accounts
- Standard expectation for all apps/services in China

---

### Form Validation Messages

| Validation | US Message | CN Message |
|------------|-----------|-----------|
| Required field | "This field is required" | "此项为必填项" |
| Invalid email | "Please enter a valid email" | "请输入有效的电子邮箱" |
| Password too short | "Min 8 characters" | "密码至少需要8个字符" |
| Phone invalid | "Invalid phone number" | "手机号码格式不正确" |
| Success | "Saved successfully" | "保存成功，感谢您的配置" |

---

## Testing & QA Checklist

### Pre-Launch Checklist

**Cultural Adaptation:**
- [ ] Trust indicators appropriate for target market
- [ ] Communication tone matches cultural expectations  
- [ ] Onboarding flow length appropriate (fast vs. gradual)
- [ ] Form fields match local requirements (name format, phone validation)
- [ ] Color scheme culturally appropriate (blue vs. red/gold)

**Technical:**
- [ ] Language switching works without page reload
- [ ] Content doesn't overflow in target language
- [ ] Right-to-left (RTL) support if needed
- [ ] Date/time formats localized
- [ ] Currency formatting correct

**Content:**
- [ ] All text professionally translated (not machine translation)
- [ ] Microcopy reviewed by native speaker
- [ ] Cultural references adapted or removed
- [ ] Images don't contain text that needs translation
- [ ] Legal compliance for region (privacy policies, terms)

---

## Component Library

### Available Components

| Component | US Variant | CN Variant | Documentation |
|-----------|-----------|-----------|---------------|
| TrustBadge | ✅ | ✅ | [View](#trust-components) |
| Toast Notification | ✅ | ✅ | [View](#communication-patterns) |
| OnboardingFlow | ✅ | ✅ | [View](#onboarding-flows) |
| ReviewCard | ✅ | ✅ | Coming soon |
| SocialShare | ✅ | ✅ | Coming soon |
| AuthModal | ✅ | ✅ | Coming soon |

### How Developers Use These Components

**Implementation Note for Designers:**  
Developers will implement these components using the specifications provided in this guide. Each component has two versions:
- One optimized for US market patterns
- One optimized for Chinese market patterns

The system automatically shows the correct version based on:
- User's language setting
- User's location
- Manual market selection in admin settings

**Example:** When a user from the US visits the site, they see the US TrustBadge (blue, certification-focused). When a user from China visits, they see the CN TrustBadge (red/gold, community-focused).

---

## Additional Resources

**External Research:**
- Cross Cultural Communication Essay (internal document)

**Questions?**  
Contact: design-systems-team@company.com

---

**Version History:**
- v1.0 (Nov 2025): Initial release
