# Senior Fullstack & Blockchain Developer

Passionate about building scalable web applications and innovative blockchain solutions.<br />
I specialize in creating robust, secure, and user-friendly applications that bridge traditional web development with cutting-edge blockchain technology.

# GitHub Analytics
<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=ledgerwave&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=ledgerwave&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false" height="150" alt="languages graph"  />
</div>

<div align="center">
  <img src="https://github-profile-trophy.vercel.app?username=ledgerwave&theme=dracula&column=-1&row=1&margin-w=8&margin-h=8&no-bg=false&no-frame=false&order=4" height="150" alt="trophy graph"  />
</div>

# Rust Smart Contract
```rust
use near_sdk::borsh::{self, BorshDeserialize, BorshSerialize};
use near_sdk::{env, near_bindgen};

#[near_bindgen]
#[derive(BorshDeserialize, BorshSerialize)]
pub struct Counter {
    value: i32,
}

// Default implementation
impl Default for Counter {
    fn default() -> Self {
        Self { value: 0 }
    }
}

#[near_bindgen]
impl Counter {
    // Increment the counter
    pub fn increment(&mut self) {
        self.value += 1;
        env::log_str(&format!("Counter incremented to {}", self.value));
    }

    // Decrement the counter
    pub fn decrement(&mut self) {
        self.value -= 1;
        env::log_str(&format!("Counter decremented to {}", self.value));
    }

    // Get the current value
    pub fn get_value(&self) -> i32 {
        self.value
    }
}
```