**1. Clone wallet sources**

```
git clone https://github.com/coindicat/coindicatwallet.git
```

**2. Modify `CryptoNoteWallet.cmake`**
 
```
set(CN_PROJECT_NAME "coindicat")
set(CN_CURRENCY_DISPLAY_NAME "Coindicat")
set(CN_CURRENCY_TICKER "COI")
```

**3. Set symbolic link to coin sources at the same level as `src`. For example:**

```
ln -s ../coindicat cryptonote
```

Alternative way is to create git submodule:

```
git submodule add https://github.com/coindicat/coindicat.git cryptonote
```

Replace URL with git remote repository of your coin.

**4. Build**

```
mkdir build && cd build && cmake .. && make
```
