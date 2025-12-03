# Postman API automation using github action # 

This repo contains postman scripts for phoenix inwarranty flow which uses newman and html-extra and test will be triggered on push against the branch 

The generated report is available in artifact path and also deployed in github pages


## project structure ##


```
postman inwarranty collections
├─ In Warranty flow.postman_collection.json  # collection file
├─ QA.postman_environment.json  # environment file


```

## Tech stack ##

1. Postman
2. node js - 22v
3. newman
4. newman reporter-html-extra
5. git hub actions
6. git hub pages


## Git hub pages ##

you can view the latest test report using : https://sharath883.github.io/phoenix-inwarranty-flow-collection/


## How to run this project ##

1. clone this repo to local using https://github.com/sharath883/phoenix-inwarranty-flow-collection.git
2. Install node js and NPM
3. Install newman using  ``` npm install -g newman ```
4. Instal html reporter using ``` npm install -g newman-reporter-htmlextra ```
5. Run the newman command :
   ```
   newman run 'In Warranty flow.postman_collection.json' \
         -e QA.postman_environment.json \
         -r cli,htmlextra \
         --reporter-htmlextra-export  ./newman/index.html
   ```

## html report ## 

The report will be created in newman folder and report looks like 

![newman report](https://github.com/sharath883/phoenix-inwarranty-flow-collection/blob/report_example/newman%20html%20report.png)




