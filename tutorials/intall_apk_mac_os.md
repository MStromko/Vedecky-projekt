# AKO INŠTALOVAŤ APLIKÁCIE NA MAC OS S PROCESOROM M1

  - pre lepšie inštalovanie aplikácii na operačnom systéme MAC OS sa používa nástroj **BREW**
  - v tomto Tutoriály Vám ukážem ako sa dá nainštalovať 
  - a ukážem Vám aj to ako sa potom inštalujú jednotlivé aplikácie
  
## Inštalácia nástroja BREW
1. Z oficiálnej stránky si skopírujeme príkaz, ktorý použijeme na inštalovanie. Tento príkaz nájdete aj tu nižšie pokiaľ by nefungoval, tak si ho skopírujte z nasledujúceho odkazu. [OFFICIAL WEBSIDE](https://brew.sh/)

          /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
2. Pre správne nastavenie nástroja **BREW** zadáme do príkazového riadka nasledujúci príkaz

          export PATH="/opt/homebrew/bin:$PATH"
          
 ## Inštalácia aplikácie
 
 - pokiaľ chcete najnštaloavť aplikáciu, ktorá je _natívna_ pre systém MAC OS tak Vám stačí zadať príkaz 
 
            brew install git
  - avšak keď tento príkaz nefunguje, tak použite ho s trošku zmenením znením
      
        arch -arm64 brew install git
    
 ## Nové info o používaní flask a docker na procesore M1 
 - apple spušťa aplikáciu AIR DROP na porte číslo 5000 v počítači to beží na localhoste čo pri spôšťaní flask APK robí problémy hlavne v kombinácii s dockerom
 - riešenie je jednoduché:
    - treba ísť do nastavení a vypnút zdielanie AIR play príjímač 
    - cesta: SETTINGS->SHARE->odskrtnúť poslednú položku AIR play prijímač
    - stránka z ktorej som čerpal: [WEBSIDE](https://progressstory.com/tech/port-5000-already-in-use-macos-monterey-issue/)  
