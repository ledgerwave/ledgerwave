# Senior Fullstack & Blockchain Developer

Passionate about building scalable web applications and innovative blockchain solutions.<br />
I specialize in creating robust, secure, and user-friendly applications that bridge traditional web development with cutting-edge blockchain technology.

## 📊 GitHub Stats
<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=ledgerwave&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=ledgerwave&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false" height="150" alt="languages graph"  />
</div>

<div align="center" style="margin-top: -35px;">
  <img src="https://github-profile-trophy.vercel.app?username=ledgerwave&theme=dracula&column=-1&row=1&margin-w=8&margin-h=8&no-bg=false&no-frame=false&order=4" height="150" alt="trophy graph"  />
</div>

<div style="margin-top: -35px;">

## 🛠 Haskell Smart Contract
```haskell
```haskell
{-# LANGUAGE DataKinds           #-}
{-# LANGUAGE NoImplicitPrelude   #-}
{-# LANGUAGE TemplateHaskell     #-}
{-# LANGUAGE ScopedTypeVariables #-}
{-# LANGUAGE OverloadedStrings   #-}

module SimpleSecret where

import PlutusTx
import PlutusTx.Prelude
import Plutus.V2.Ledger.Api
import Plutus.V2.Ledger.Contexts
import Prelude (IO, putStrLn)

-- 🎁 Simple Secret Validator
-- The transaction succeeds only if the provided guess equals the secret.
{-# INLINABLE mkValidator #-}
mkValidator :: BuiltinByteString -> BuiltinByteString -> ScriptContext -> Bool
mkValidator secret guess _ = traceIfFalse "❌ Wrong secret!" (guess == secret)

-- 🔧 Compile the validator
validator :: Validator
validator = mkValidatorScript $$(PlutusTx.compile [|| mkValidator ||])

-- 🔢 Get the validator hash
valHash :: ValidatorHash
valHash = validatorHash validator

-- 🏦 Get the contract address
valAddress :: Address
valAddress = scriptHashAddress valHash

-- ✅ Build confirmation
main :: IO ()
main = putStrLn "✅ Simple Plutus smart contract compiled successfully!"
```
</div>

---

🔗 Connect with Me
<div align="center"> 

![Follow](https://img.shields.io/github/followers/ledgerwave?label=Follow&style=for-the-badge&color=blue) ![Profile Views](https://komarev.com/ghpvc/?username=ledgerwave&color=green&style=for-the-badge) 

</div>

---

### 🎯 Hobbies & Interests

* 💻 **Coding & Tech** - Exploring new programming languages, building projects, and contributing to open source.
* ⚽ **Football** - Playing and following matches passionately.
* 🎾 **Tennis** - Hitting the court whenever possible to stay active.
* 📚 **Reading & Learning** - Always curious about tech trends, science, and self-improvement.
* 🎮 **Gaming** - Relaxing with strategy and adventure games in free time.

---