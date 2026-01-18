# PVA2 - Programování a vývoj aplikací
## Cvičení 13: Logování

**Příklad výstupu logu:**
```
2026-01-18 14:30:15 - INFO - Kalkulačka spuštěna
2026-01-18 14:30:22 - INFO - Operace: 10.0 + 5.0 = 15.0
2026-01-18 14:30:30 - WARNING - Pokus o dělení nulou
```


### 1 Kalkulačka
Vytvořte program `calculator_log.py`, který:

1. Implementuje jednoduchou kalkulačku se čtyřmi základními operacemi (+, -, *, /)
2. Používá výjimky pro ošetření chyb
3. Loguje průběh výpočtů:
   - `INFO` - zahájení programu
   - `INFO` - úspěšně provedený výpočet a výsledek
   - `WARNING` - pokus o dělení nulou
   - `ERROR` - neplatný vstup (nelze převést na číslo)
   - `ERROR` - neplatná operace
   - `INFO` - ukončení programu
  
**Příklad běhu programu:**
```
INFO:root:Kalkulačka spuštěna
Zadejte první číslo: 10
Zadejte operaci (+, -, *, /): +
Zadejte druhé číslo: 5
INFO:root:Operace: 10.0 + 5.0 = 15.0
Výsledek: 15.0
```

**Požadavky:**
- Použijte úroveň logování `DEBUG`
- Program běží v cyklu, dokud uživatel nezadá 'konec' jako první číslo
- Ošetřete všechny možné chyby pomocí výjimek

### 2 Správce úkolů s logováním
Vytvořte program `todo_list.py` - jednoduchý správce úkolů, který:

1. Používá seznam pro ukládání úkolů
2. Nabízí menu s možnostmi:
   - Přidat úkol
   - Zobrazit všechny úkoly
   - Označit úkol jako hotový (odstranit ze seznamu)
   - Ukončit program
3. Loguje všechny akce:
   - `INFO` - spuštění programu
   - `INFO` - přidání nového úkolu
   - `INFO` - zobrazení seznamu úkolů
   - `INFO` - dokončení úkolu
   - `WARNING` - pokus o dokončení neexistujícího úkolu
   - `ERROR` - neplatná volba v menu
   - `INFO` - ukončení programu

**Příklad běhu:**
```
INFO:root:Správce úkolů spuštěn

=== TODO LIST ===
1. Přidat úkol
2. Zobrazit úkoly
3. Dokončit úkol
4. Ukončit
Vaše volba: 1
Zadejte úkol: Nakoupit mléko
INFO:root:Přidán úkol: Nakoupit mléko
```

**Požadavky:**
- Použijte seznam pro ukládání úkolů
- Program běží v cyklu dokud uživatel nezvolí ukončení
- Při zobrazení úkolů vypište každý úkol s číslováním



### 3 Hra s logováním
Vytvořte hru **"Hádej číslo"** (`guess_number.py`), která:

1. Vygeneruje náhodné číslo od 1 do 100
2. Hráč má neomezený počet pokusů číslo uhodnout
3. Po každém pokusu program řekne, zda je hledané číslo větší nebo menší
4. Loguje průběh hry:
   - `INFO` - spuštění hry, rozsah čísel
   - `DEBUG` - každý pokus hráče (ale nezobrazuje správné číslo!)
   - `WARNING` - vstup mimo rozsah 1-100
   - `ERROR` - neplatný vstup (ne číslo)
   - `INFO` - úspěšné uhodnutí, počet pokusů
   - `INFO` - ukončení hry

**Příklad běhu:**
```
INFO:root:Hra spuštěna. Hádej číslo od 1 do 100.
Tvůj tip: 50
DEBUG:root:Hráč tipoval: 50
Hledané číslo je větší!
Tvůj tip: 75
DEBUG:root:Hráč tipoval: 75
Hledané číslo je menší!
Tvůj tip: 60
DEBUG:root:Hráč tipoval: 60
INFO:root:Správně! Číslo bylo 60. Počet pokusů: 3
```

**Požadavky:**

- Použijte import random pro generování náhodného čísla
- Počítejte pokusy hráče
- Ošetřete neplatné vstupy pomocí výjimek

