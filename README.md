<br />
<div align="center">

  <h3 align="center">Disk Prices Scraper</h3>

  <p align="center">
    Scrape data into CSV and JSON files from <a href="https://diskprices.com">diskprices.com</a>
    <br />
    <a href="https://github.com/badster-git/disk-prices-scraper/issues">Report Bug</a>
  </p>
</div>

## About
I made this little scraper because I wanted more flexibility to filter out certain drives from [diskprices.com](https://diskprices.com]). Things like filtering out by brandnames and so on. 

This scraper does have the ability to attach a brandname value to each drive, but not all brands are covered so some will output with 'Unknown Brand' in the end.


## Usage

### Data Type (-t | --type)

This sets whether to use GB or TB if using min or max arguments.
```sh
python main.py (-t | --type) gb
python main.py (-t | --type) tb
```

### Minimum Drive Capacity (-mi | --min)
This sets the minimum amount of storage space a drive can have. The number used here is dependent on data type being used.
```sh
python main.py (-mi | --min) {1-9999999}
```


### Maximum Drive Capacity (-ma | --max)
This sets the maximum amount of storage space a drive can have. The number used here is dependent on data type being used.
```sh
python main.py (-ma | --max) {1-9999999}
```

### Condition (-c | --condition)

This determines whether to show new drives, used drives or both.
```sh
python main.py (-c | --condition) {new,used,all}
```

### Disk Types (-dt | --disk-types)

This sets which disk types to scrape. To view the list of all the available disk types, run the help command.
```sh
python main.py (-dt | --disk-types) disk01 disk02 disk03
```

### Help (-h | --help)
Displays the basic functionality of arguments in the terminal
```
python main.py  -h
```

## Packages Used
* [BeautifulSoup4](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
* [lxml](https://lxml.de/)
* [chromedriver-binary-auto](https://pypi.org/project/chromedriver-binary-auto/)
* [Selenium](https://www.selenium.dev/)