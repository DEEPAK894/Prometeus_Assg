# Prometeus_Assg
###   1) Export the metrics (like request per second, memory usage, cpu usage etc) in the existing mini project given to Interns<br>
### 2)Install Prometheus and Grafana using Docker (with docker-compose)<br> 
### 3)Configure prometheus (scrape configs) such way that it can scrape the metrics from default metric path of the application job<br> 
### 4)Validate the entire configuration to check if the data is coming or not in Prometheus UI<br> 
### 5)Create the Dashboards in Grafana on top of the metrics exported by adding the Prometheus as a Datasource.<br>
**Ans:-** <br>
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
<br>
