# রিলস মেকার

ছবি আর নিজের লেখা দিয়ে শর্ট ভিডিও বানানোর অ্যাপ। সবকিছু ব্রাউজারেই চলে, কোনো সার্ভার বা API Key লাগে না।

## রিপোজিটরির গঠন (এভাবেই GitHub-এ থাকতে হবে)
```
wrangler.jsonc
README.md
public/
  index.html
```

## Cloudflare-এ পাবলিশ
1. GitHub-এ এই তিনটি ফাইল ওপরের গঠন ঠিক রেখে আপলোড করুন (`index.html` অবশ্যই `public` ফোল্ডারের ভেতরে)।
2. Cloudflare Dashboard → **Workers & Pages** → **Create** → **Import a repository** দিয়ে রিপোজিটরিটা কানেক্ট করুন।
3. Build command খালি রাখুন। Deploy command থাকবে `npx wrangler deploy`।
4. `wrangler.jsonc` ফাইলের `name` (এখন `reels-maker`) আর Cloudflare-এ আপনার প্রজেক্টের নাম একই হতে হবে। না মিললে একটা বদলে অন্যটার সাথে মিলিয়ে নিন।
5. Deploy হলে `https://নাম.workers.dev` লিংক পাবেন।

## নিরাপত্তা
কোনো API Key এই ফাইলে বা GitHub-এ রাখবেন না।
