# Activity: File Management & Git

## Part A: Managing Files and Folders

1. Create a folder in your home directory using your name as the name of the folder:
    ```bash
    mkdir Hayri-Olcay
    ```
    _Output:_
    No output

2. Move into the folder:
    ```bash
    cd Hayri_olcay
    ```
    _Output:_
    No output

3. Create an empty file:
    ```bash
    touch test.txt
    ```
    _Output:_
    No output

4. Create a new folder in this folder called `myfolder`:
    ```bash
    mkdir myfolder
    ```
    _Output:_
    No output

5. Move the empty file you created into `myfolder`:
    ```bash
    mv test.txt myfolder
    ```
    _Output:_
    No output

6. Create a backup of the file:
    ```bash
    cp myfolder/test.txt myfolder/test.bkp
    ```
    _Output:_
    No output

7. Remove the backup file:
    ```bash
    rm myfolder/test.bkp
    ```
    _Output:_
    No output

8. Go back to your home directory:
    ```bash
    cd ~
    ```
    _Output:_
    No output

## Part B: Working with Git

1. Clone the repository:
    ```bash
    git clone https://github.com/TheAcademy/pss-orderbook-deploy/
    ```
    _Output:_
    ```
    Cloning into 'pss-orderbook-deploy'...
    Username for 'https://github.com': Hayri-Olcay
    Password for 'https://Hayri-Olcay@github.com': 
    remote: Enumerating objects: 5052, done.
    remote: Counting objects: 100% (808/808), done.
    remote: Compressing objects: 100% (96/96), done.
    remote: Total 5052 (delta 759), reused 724 (delta 712), pack-reused 4244
    Receiving objects: 100% (5052/5052), 8.10 MiB | 3.45 MiB/s, done.
    Resolving deltas: 100% (2836/2836), done.
    ```

2. Go to the newly created `pss-orderbook-deploy` directory:
    ```bash
    cd pss-orderbook-deploy
    ```
    _Output:_
    No output

3. Navigate to the folder `src/linux_activities/Activity2`:
    ```bash
    cd src/linux_activities/Activity2
    ```
    _Output:_
    No output

## Searching Files

1. Display the contents of the file `stock_investments.txt`:
    ```bash
    cat stock_investments.txt
    ```
    _Output:_
    ```
    Stock Ticker,Number of Shares,Purchase Price,Current Price
    AAPL,100,200,250
    GOOG,50,300,350
    MSFT,75,100,125
    AMZN,25,600,650
    FB,100,150,175
    TSLA,50,400,450
    INTC,75,75,87.5
    CSCO,25,200,225
    NVDA,100,300,350
    PYPL,50,250,275
    IBM,75,100,112.5
    ORCL,25,400,450
    MCD,100,150,162.5
    WMT,50,200,225
    XOM,75,100,112.5
    CVX,25,300,325
    PG,100,100,112.5
    KO,50,100,112.5
    JNJ,75,100,112.5
    PFE,25,100,112.5
    MRK,100,100,112.5
    UNH,50,100,112.5
    HD,75,100,112.5
    LOW,25,100,112.5
    MOR,100,100,112.5
    BBY,50,100,112.5
    DIS,75,100,112.5
    CMCSA,25,100,112.5
    TWX,100,100,112.5
    T,50,100,112.5
    VZ,75,100,112.5
    CVS,25,100,112.5
    WBA,100,100,112.5
    NKE,50,100,112.5
    MMM,75,100,112.5
    JPM,25,100,112.5
    BAC,100,100,112.5
    C,50,100,112.5
    GS,75,100,112.5
    MS,25,100,112.5
    WFC,100,100,112.5
    USB,50,100,112.5
    PNC,75,100,112.5
    BMO,25,100,112.5
    TD,100,100,112.5
    BNS,50,100,112.5
    RY,75,100,112.5
    AXP,25,100,112.5
    DAL,100,100,112.5
    LUV,50,100,112.5
    AAL,75,100,112.5
    DAL,25,100,112.5
    UPS,100,100,112.5
    FDX,50,100,112.5
    DAL,75,100,112.5
    AAL,25,100,112.5
    DAL,100,100,112.5
    LUV,50,100,112.5
    AAL,75,100,112.5
    DAL,25,100,112.5
    UPS,100,100,112.5
    FDX,50,100,112.5
    ```

2. Display the first five lines of the file:
    ```bash
    head -5 stock_investments.txt
    ```
    _Output:_
    ```
    Stock Ticker,Number of Shares,Purchase Price,Current Price
    AAPL,100,200,250
    GOOG,50,300,350
    MSFT,75,100,125
    AMZN,25,600,650
    ```

3. Display the five last lines of the file:
    ```bash
    tail -5 stock_investments.txt
    ```
    _Output:_
    ```
    LUV,50,100,112.5
    AAL,75,100,112.5
    DAL,25,100,112.5
    UPS,100,100,112.5
    FDX,50,100,112.5
    ```

4. Display how many times the word GOOG is used:
    ```bash
    grep GOOG stock_investments.txt | wc -l
    ```
    _Output:_
    ```
    1
    ```

5. Display how many lines contain the word T:
    ```bash
    grep -wc T stock_investments.txt
    ```
    _Output:_
    ```
    1
    ```

6. List the files that contain the word SPY in any letter case:
    ```bash
    grep -i SPY *
    ```
    _Output:_
    ```
    grep: AAL: Is a directory
    grep: AAPL: Is a directory
    grep: AMZN: Is a directory
    grep: AXP: Is a directory
    grep: BAC: Is a directory
    grep: BBY: Is a directory
    grep: BMO: Is a directory
    grep: BNS: Is a directory
    grep: C: Is a directory
    grep: CMCSA: Is a directory
    grep: CSCO: Is a directory
    grep: CVS: Is a directory
    grep: CVX: Is a directory
    grep: DAL: Is a directory
    grep: DIS: Is a directory
    grep: FB: Is a directory
    grep: FDX: Is a directory
    grep: GOOG: Is a directory
    grep: GS: Is a directory
    grep: HD: Is a directory
    grep: IBM: Is a directory
    grep: INTC: Is a directory
    grep: JNJ: Is a directory
    grep: JPM: Is a directory
    grep: KO: Is a directory
    grep: LOW: Is a directory
    grep: LUV: Is a directory
    grep: MCD: Is a directory
    grep: MMM: Is a directory
    grep: MOR: Is a directory
    grep: MRK: Is a directory
    grep: MS: Is a directory
    grep: MSFT: Is a directory
    grep: NKE: Is a directory
    grep: NVDA: Is a directory
    grep: ORCL: Is a directory
    grep: PFE: Is a directory
    grep: PG: Is a directory
    grep: PNC: Is a directory
    grep: PYPL: Is a directory
    grep: RY: Is a directory
    grep: T: Is a directory
    grep: TD: Is a directory
    grep: TSLA: Is a directory
    grep: TWX: Is a directory
    grep: UNH: Is a directory
    grep: UPS: Is a directory
    grep: USB: Is a directory
    grep: VZ: Is a directory
    grep: WBA: Is a directory
    grep: WFC: Is a directory
    grep: WMT: Is a directory
    grep: XOM: Is a directory
    ```

7. List the files that do not contain the word SPY:
    ```bash
    grep -L SPY *
    ```
    _Output:_
    ```
    grep: AAL: Is a directory
    AAL
    grep: AAPL: Is a directory
    AAPL
    grep: AMZN: Is a directory
    AMZN
    grep: AXP: Is a directory
    AXP
    grep: BAC: Is a directory
    BAC
    grep: BBY: Is a directory
    BBY
    grep: BMO: Is a directory
    BMO
    grep: BNS: Is a directory
    BNS
    grep: C: Is a directory
    C
    grep: CMCSA: Is a directory
    CMCSA
    grep: CSCO: Is a directory
    CSCO
    grep: CVS: Is a directory
    CVS
    grep: CVX: Is a directory
    CVX
    grep: DAL: Is a directory
    DAL
    grep: DIS: Is a directory
    DIS
    grep: FB: Is a directory
    FB
    grep: FDX: Is a directory
    FDX
    grep: GOOG: Is a directory
    GOOG
    grep: GS: Is a directory
    GS
    grep: HD: Is a directory
    HD
    grep: IBM: Is a directory
    IBM
    grep: INTC: Is a directory
    INTC
    grep: JNJ: Is a directory
    JNJ
    grep: JPM: Is a directory
    JPM
    grep: KO: Is a directory
    KO
    grep: LOW: Is a directory
    LOW
    grep: LUV: Is a directory
    LUV
    grep: MCD: Is a directory
    MCD
    grep: MMM: Is a directory
    MMM
    grep: MOR: Is a directory
    MOR
    grep: MRK: Is a directory
    MRK
    grep: MS: Is a directory
    MS
    grep: MSFT: Is a directory
    MSFT
    grep: NKE: Is a directory
    NKE
    grep: NVDA: Is a directory
    NVDA
    grep: ORCL: Is a directory
    ORCL
    grep: PFE: Is a directory
    PFE
    grep: PG: Is a directory
    PG
    grep: PNC: Is a directory
    PNC
    grep: PYPL: Is a directory
    PYPL
    grep: RY: Is a directory
    RY
    stock_investments.txt
    grep: T: Is a directory
    T
    grep: TD: Is a directory
    TD
    grep: TSLA: Is a directory
    TSLA
    grep: TWX: Is a directory
    TWX
    grep: UNH: Is a directory
    UNH
    grep: UPS: Is a directory
    UPS
    grep: USB: Is a directory
    USB
    grep: VZ: Is a directory
    VZ
    grep: WBA: Is a directory
    WBA
    grep: WFC: Is a directory
    WFC
    grep: WMT: Is a directory
    WMT
    grep: XOM: Is a directory
    XOM
    ```

8. Find all files containing the word “data” in their name:
    ```bash
    find . -type f -name "*data*"
    ```
    _Output:_
    ```
    ./GOOG/data.txt
    ./AAL/data.txt
    ./TWX/data.txt
    ./PYPL/data.txt
    ./MMM/data.txt
    ./MSFT/data.txt
    ./T/data.txt
    ./TD/data.txt
    ./NVDA/data.txt
    ./FDX/data.txt
    ./CSCO/data.txt
    ./CVX/data.txt
    ./MS/data.txt
    ./KO/data.txt
    ./UPS/data.txt
    ./TSLA/data.txt
    ./BBY/data.txt
    ./INTC/data.txt
    ./BMO/data.txt
    ./LUV/data.txt
    ./BAC/data.txt
    ./GS/data.txt
    ./BNS/data.txt
    ./USB/data.txt
    ./FB/data.txt
    ./JPM/data.txt
    ./PFE/data.txt
    ./LOW/data.txt
    ./PNC/data.txt
    ./DIS/data.txt
    ./DAL/data.txt
    ./MCD/data.txt
    ./RY/data.txt
    ./HD/data.txt
    ./UNH/data.txt
    ./PG/data.txt
    ./MRK/data.txt
    ./ORCL/data.txt
    ./JNJ/data.txt
    ./C/data.txt
    ./AAPL/data.txt
    ./CMCSA/data.txt
    ./WMT/data.txt
    ./WBA/data.txt
    ./VZ/data.txt
    ./IBM/data.txt
    ./WFC/data.txt
    ./MOR/data.txt
    ./XOM/data.txt
    ./AXP/data.txt
    ./AMZN/data.txt
    ./CVS/data.txt
    ./NKE/data.txt
    ```

9. Find folders named error:
    ```bash
    find . -type d -name error
    ```
    _Output:_
    ```
    ./WFC/error
    ```

10. Change permissions on all files that contain the word "data" so that the files are read-only for group and other:
    ```bash
    sudo find . -type f -name "*data*" -exec chmod 744 {} \;
    ```
    _Output:_
    No output

11. Locate and remove write permission for all users on the file named `WFC/data.txt`:
    ```bash
    chmod a-w WFC/data.txt
    ```
    _Output:_
    No output

