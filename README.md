# Prometeus_Assg
 ###  1) Export the metrics (like request per second, memory usage, cpu usage etc) in the existing mini project given to Interns<br>
### 2)Install Prometheus and Grafana using Docker (with docker-compose)<br> 
### 3)Configure prometheus (scrape configs) such way that it can scrape the metrics from default metric path of the application job<br> 
### 4)Validate the entire configuration to check if the data is coming or not in Prometheus UI<br>
### 5)Create the Dashboards in Grafana on top of the metrics exported by adding the Prometheus as a Datasource.<br>
**Ans:-** <br><br>
**Step 1:** Install Docker in our Linux machine <br><br>
**Step 2:** Create Flask Application.<br>
  + Create a Flask application with metrics instrumentation. Create app.py file and add the python code into that file.<br>
  + Make sure that existing  project is instrumented with Prometheus metrics. Need to use a Prometheus client library in the code to expose the desired metrics.<br>
  
**Step 3:** Set Up Docker-Compose for Prometheus and Grafana.<br>
  + Create a docker-compose.yml file to define the services.Pull the images of Prometheus and Grafana from DockerHub. <br>
  
**Step 4:** Configure Prometheus Scraping.<br>
  + Create a prometheus.yml file in the project directory. <br>

**Step 5:** Run Docker Compose.<br>
  + Run the following command to build and start the Docker containers.
     >       docker-compose up -d
  + This will start Prometheus and Grafana in the background.  
<br>

**Step 6:** Verify Prometheus Configuration.<br>
  + Visit http://localhost:9090 in the browser to access the Prometheus UI.
  + Check the "Targets" tab to verify if the application is being scraped successfully. <br>

**Step 7:** Set Up Grafana Datasource.<br>
  + Open http://localhost:3000 in your browser.
  + Log in using the default credentials (admin/admin).
  + Add Prometheus as a datasource:
     - Go to "Settings" -> "Data Sources".
     - Add a new data source, select Prometheus, and set the URL to http://prometheus:9090.
     - Click "Save & Test" to verify the connection.<br>

   **Step 8:** Create Grafana Dashboards.<br>
  + In Grafana, go to the "+" menu on the left sidebar and select "Dashboard."
  +  Click on "Add new panel."
  +  In the "Query" section, select your Prometheus data source and start building your queries based on the metrics your application exposes.<br>

  # ScreenShots<br>
 +   Prometheus Targets Page: Overview of Monitored Targets<br><br>
![Prometeus Dashboard](https://github.com/DEEPAK894/Prometeus_Assg/blob/main/Screenshot%20from%202023-11-28%2014-34-17.png)<br><br>
 +   Dashboard in Grafana: Visualizing Flask Application Metrics<br>

1. flask_cpu_usage_percentage <br><br>
![Grafana Dashboard](https://github.com/DEEPAK894/Prometeus_Assg/blob/main/Screenshot%20from%202023-11-28%2014-31-57.png)<br><br>
2. process_cpu_seconds_total <br><br>
![Grafana Dashboard](https://github.com/DEEPAK894/Prometeus_Assg/blob/main/Screenshot%20from%202023-11-28%2014-32-34.png)


