# originalityAI-Config
## Introduction
1. A config file that demonstrates the vulnerability of user accounts on originality.ai
2. Originality.ai is a software tool that provides highly accurate AI Detection and Plagiarism checks for text. 
3. However, due to the lack of a csrf-token and very high rate-limit values, there is a great chance of DDos attacks. 
4. This config explores the vulnerability that can be exploited for this attack.
\n

## Working

1. While originalityAI's login site has mentioned a recaptcha, the POST Login request payload shows captcha as null.

<img width="200" alt="Screenshot 2023-10-30 at 11 25 56" src="https://github.com/AdithyahNair/originalityAI-Config/assets/74417984/a24a41c0-0cbd-4eae-9c97-eee2e984a8c2">  <img width="600" alt="Screenshot 2023-10-30 at 11 28 25" src="https://github.com/AdithyahNair/originalityAI-Config/assets/74417984/ae30a087-86be-4a1d-922f-d88c1208a5b5">

2. The config captuers the access_token for the successive login response. After which, it is used to check if the account has a subscription or not. If yes, then we can capture the API key through the developer's tab, within the **network** section.

3. This is demonstrated in the code written in the config.

4. The config can be used on automated pentesting software like SilverBullet for performing bruteforce checks on wordlists. However, this issue can be mitigated by enabling Google's V3 Recaptcha along with strict rate limits.

## The config provided is strictly to be used for educational purposes only.



