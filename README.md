# OWASP Juice Shop Challenges

![JuiceShop_Logo](/img/JuiceShop_Logo_100px.png)

Version 18.0.0

---

Table of Contents
- [OWASP Juice Shop Challenges](#owasp-juice-shop-challenges)
  - [Repository Structure](#repository-structure)
  - [Install JuiceShop](#install-juiceshop)
  - [Challenges](#challenges)
  - [Disclaimer](#disclaimer)

---

## Repository Structure

```bash
OWASP_JuiceShop_Challenges/
├── challenges/
|   ├── bjoerns_favorite_pet/
│   │   ├── bjoerns_favorite_pet_DE.md  # Documentation for bjoerns_favorite_pet_DE
│   │   └── bjoerns_favorite_pet_EN.md  # Documentation for bjoerns_favorite_pet_EN
|   ├── exposed_credentials/
│   │   ├── exposed_credentials_DE.md   # Documentation for exposed_credentials_DE
│   │   └── exposed_credentials_EN.md   # Documentation for exposed_credentials_EN
|   ├── reflected_xss/
│   │   ├── reflected_xss_DE.md         # Documentation for reflected_xss_DE
│   │   └── reflected_xss_EN.md         # Documentation for reflected_xss_EN
|   ├── viewBasket/
│   │   ├── viewBasket_DE.md            # Documentation for viewBasket_DE
│   │   └── viewBasket_EN.md            # Documentation for viewBasket_EN
|   └── web3sandbox/
│       ├── web3sandbox_DE.md           # Documentation for web3sandbox_DE
│       └── web3sandbox_EN.md           # Documentation for web3sandbox_EN
├── img/                                # All Images (Screenshots)
├── .gitignore                          # Ignore rules for Git
├── README.md                           # Project overview and navigation
└── Juice_Shop_Meister_Checkliste.pdf   # Checklist
```

---

## Install JuiceShop

1. Clone Repository from [GitHub/juice-shop](https://github.com/juice-shop/juice-shop)

```bash
git clone https://github.com/juice-shop/juice-shop.git
```

2. Navigate into it the Project folder

```
cd juice-shop
```

3. Install all packages

```
npm install
```

4. Start localserver

```
node start
```

5. Open your Browser [http://localhost:3000](http://localhost:3000)

---

## Challenges

- [Sandbox_EN](/challenges/web3sandbox/sandbox_en.md)
- [View Basked_EN](/challenges/viewBasket/view_basked_en.md)
- [Reflected XSS_EN](/challenges/reflected_xss/reflected_xss_en.md)
- [Exposed Credentials_EN](/challenges/exposed_credentials/exposed_credentials_en.md)
- [Björn's favorite pet_EN](/challenges/bjoerns_favorite_pet/bjoerns_favorite_pet_en.md)

---

## Disclaimer

The vulnerabilities and exploits demonstrated in this repository are intended for learning and practice only. Do not use these techniques against systems you do not have explicit permission to test.

```text

  ██████╗   ███████╗   ███████╗  █████████╗
 ██╔════╝   ██╔════╝  ██╔═════╝  ╚══██╔═══╝
 ██║  ███╗  █████╗    ╚█████╗       ██║
 ██║   ██║  ██╔══╝     ╚═══██╗      ██║
 ██║   ██║  ██║             ██╗     ██║
 ╚██████╔╝  ███████╗   ███████║     ██║
  ╚═════╝   ╚══════╝   ╚══════╝     ╚═╝
```
