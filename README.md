**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation

*TODO:* run `kubectl` command to show the running pods and services for all components. Take a screenshot of the output and include it here to verify the installation

![Successfully install Grafana, Prometheus, and Jaeger](https://user-images.githubusercontent.com/61376012/208572701-fded96a7-64a5-40a1-90df-d611585bc25e.png)

## Setup the Jaeger and Prometheus source
*TODO:* Expose Grafana to the internet and then setup Prometheus as a data source. Provide a screenshot of the home page after logging into Grafana.
![Successfully access Grafana’s web UI](https://user-images.githubusercontent.com/61376012/208572812-79c2258b-7be7-4c40-ac54-54f069b9bea4.png)

## Create a Basic Dashboard
*TODO:* Create a dashboard in Grafana that shows Prometheus as a source. Take a screenshot and include it here.
![image](https://user-images.githubusercontent.com/61376012/208578838-222171e6-1adc-4f21-954a-4dc520f47ea1.png)

## Describe SLO/SLI
*TODO:* Describe, in your own words, what the SLIs are, based on an SLO of *monthly uptime* and *request response time*.  
A Service-Level Objective (SLO) is a measurable goal set by the SRE team to ensure a standard level of performance during a specified period of time.  
A Service-Level Indicator (SLI) is a specific metric used to measure the performance of a service.  
For example, suppose that your team has the following SLO:  
The application will have an uptime of 99.9% during the next year.  
In this case, your SLI would be the actual measurement of the uptime. Perhaps during that year, you actually achieved 99.5% uptime or 97.3% uptime. These measurements are your SLIs—they indicate the level of performance your service actually exhibited, and show you whether you achieved your SLO (in this case, the SLIs show that performance fell short of your objective).  

## Creating SLI metrics.
*TODO:* It is important to know why we want to measure certain metrics for our customer. Describe in detail 5 metrics to measure these SLIs. 
The average 20x responses of the web application is 97.99%.  
Incoming request that are had 40x are 1%
The average of incoming requests is 600ms  
The average of CPUs is 50%  
The avarage of Ram is 300Mib  

## Create a Dashboard to measure our SLIs
*TODO:* Create a dashboard to measure the uptime of the frontend and backend services We will also want to measure to measure 40x and 50x errors. Create a dashboard that show these values over a 24 hour period and take a screenshot.  
![image](https://user-images.githubusercontent.com/61376012/208604422-ef480a52-7baa-4651-8a6f-91959c359b83.png)

## Creating SLIs and SLOs  
SLOs:
99.95% of uptime per month  
0.5% of 40x/50x responses per month.  
Application responses should be served within 1500 ms per month.  
Monthly average CPU usage should be 60% or less.  
Monthly average memory usage should not exceed 600Mib.  
SLIs:
The average 20x responses of the web is 97.99%.  
1% of the total incoming requests had 50x responses.  
It took an average of 600 ms for incoming requests to be served.  
The average of CPUs is 50%.  
The avarage of Ram is 300Mib.  

## Craft KPIs based on SLIs and SLOs.
* The average 20x or 30x responses of the web is 97.99%.  
Monthly uptime - this KPI indicates the total usability of the application.  
20x code responses per month - this KPI indicates availability of the pages of the application.  
Monthly traffic - this KPI will indicate the number of requests served by the application.  
* 1% of the total incoming requests had 50x responses.  
Monthly downtime - this KPI indicates the number of times the application was down  
Errors per month - this KPI will indicate the monthly errors encountered in the application.  
Monthly traffic - this KPI will indicate the number of requests served by the application.  
* It took an average of 600 ms for incoming requests to be served.  
Average monthly latency - this KPI will indicate the time it took for the application to respond to requests.  
Monthly uptime - this KPI indicates the total usability of the application.  
Monthly traffic - this KPI will indicate the number of requests served by the application.  
* The average of CPUs is 50%.  
Average monthly CPU usage of pod used by the application - this KPI will indicate how much CPU is used by the source pod of the application.  
Average monthly CPU usage of all the pods - this KPI will indicate how much CPU is used by all the pods required to run the application.  
Monthly quota limit - this KPI will indicate whether the application is exceeding its usage of the CPU quota.  
* The avarage of Ram is 300Mib.  
Average monthly memory usage of pod used by the application - this KPI will indicate how much memory is used by the source pod of the application.  
Average monthly memory usage of all the pods - this KPI will indicate how much memory is used by all the pods required to run the application.  
Monthly quota limit - this KPI will indicate whether the application is exceeding its usage of the memory quota.  

## Final Dashboard
![image](https://user-images.githubusercontent.com/61376012/209266637-e0915b97-aa32-44db-bcf9-17f2a7e94604.png)

