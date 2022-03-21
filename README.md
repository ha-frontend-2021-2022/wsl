# WSL (Windows Subsystem for Linux)

Mac och Linux har länge ansets vara överlägsna Windows när det kommer till deras terminal.

I dagens frontend är det mer regel än undantag att man använder sig av någon form av terminalbaserade verktyg. Vanligast är `npm`, som är en pakethanterare (package manager) som installerar och hanterar paket som kan innehålla t.ex. en utvecklingsserver, utvecklingsverktyg, ramverk/bibliotek osv.

Microsoft har dock introducerat något de kallar för Windows Subsystem for Linux, som gör det möjligt att utveckla som om du vore på en Linux-distribution (Ubuntu är den vanligaste att använda).

<br>

## Installera WSL

1. Tryck <kbd>WIN</kbd> + <kbd>Q</kbd>.

1. Skriv `powershell`.

1. Tryck <kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>ENTER</kbd> (för att köra som administrator).

    * _Administrator krävs för att aktivera följande Windows Features: Virtual Machine Platform, Windows Subsystem for Linux._

1. Skriv `wsl --install -d Ubuntu-20.04` för att installera `Ubuntu`.

    * _Starta om datorn om det efterfrågas, och gör sedan om steg 1-4 efter omstart._

    * _Stäng Ubuntu-terminalen när username och password efterfrågas för att använda Ubuntus root-användare som standard-användare._

1. Tryck <kbd>WIN</kbd> + <kbd>Q</kbd>.

1. Skriv `Ubuntu`.

1. Tryck <kbd>ENTER</kbd>.

1. **Klart!**

<br>

## Installera Node.js

1. Tryck <kbd>WIN</kbd> + <kbd>Q</kbd>.

1. Skriv `Ubuntu`.

1. Installera `Node.js` paketlista i `Ubuntu`:

    ```bash
    curl -fsSL https://deb.nodesource.com/setup_lts.x | bash -
    ```

    _Detta installerar LTS (Long Term Support) versionen av Node.js, för övriga Ubuntu-anpassade versioner se: https://github.com/nodesource/distributions/blob/master/README.md#installation-instructions_

1. Installera `Node.js`:

    ```bash
    apt install -y nodejs
    ```

1. Testa:

    ```bash
    node -v
    ```

1. **Klart!**
