**1. Clone wallet sources**

```
git clone https://github.com/ricochetcoin/ricochetwallet.git
```

**2. Modify `CryptoNoteWallet.cmake`**
 
```
set(CN_PROJECT_NAME "ricochet")
set(CN_CURRENCY_DISPLAY_NAME "Ricochet")
set(CN_CURRENCY_TICKER "RIT")
```

**3. Set symbolic link to coin sources at the same level as `src`. For example:**

```
ln -s ../coindicat cryptonote
```

Alternative way is to create git submodule:

```
git submodule add https://github.com/ricochetcoin/ricochet.git cryptonote
```

Replace URL with git remote repository of your coin.

**4. Build**


```
mkdir build && cd build && cmake .. && make
```
On Mac:

```
mkdir build && cd build && cmake .. -DCMAKE_PREFIX_PATH=$(brew --prefix qt5) && make
```
