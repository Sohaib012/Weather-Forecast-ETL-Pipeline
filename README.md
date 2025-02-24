
# Introduction:


<h3 align="center">Weather Forecast ETL Pipeline</h3>

  <p align="center">
    The project includes a Bash script to extract, transform, and load weather data, schedule it to run daily, and write a script to measure forecast accuracy i.e fc_accuracy.
rx_poc.log this is your POC weather report log file, or a text file which contains a growing history of the daily weather data you will scrape.
</div>


<!-- ABOUT THE PROJECT -->
## About The Project

### Technologies
```sh
Bash Scripting
Cron jobs
  ```

### Projet in Action

### Raw data source
```sh
$ curl https://wttr.in/rawalpindi
  ```
![image](https://github.com/user-attachments/assets/e57fff3c-3050-479c-8d36-4e0ee0493dea)

## Extract
### Extract data to a weather report
```sh
$ curl wttr.in/rawalpindi --output weather_report
  ```

### Extract current temp and tomorrow's noon temp and store in log file
```sh
$ ./rx_poc.sh
  ```

### Schedule cron job to run daily
```sh
crontab -e
0 8 * * * rx_poc.sh
  ```
## Transforn & Load
### Run script to report historical forecasting accuracy 
### This will also load the data to historical_forecast_accuracy.tsv
```sh
$ ./fc_accuracy.sh
  ```
### Basis for transformation
![image](https://github.com/user-attachments/assets/6d498220-bf46-4fe5-b5b0-f2718f6d305a)


### Requirements
```sh
Linux OS
  ```



