# MERN_Application_with_Grafana_and_Prometheus
## 1. MERN Application Setup:

   - Deploy a travel memory application in your local machine.
     Assuming the same configuration like all other Travel Memory projects,
![Screenshot 2024-02-27 215829](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/26fece54-f352-4697-8c3e-ab13d03aade4)

## 2. Integrate Prometheus:

   - Integrate Prometheus metrics into the Node.js backend. Use client libraries to expose custom metrics like API response times, request counts, and error rates.

   - Set up MongoDB monitoring using an exporter, such as MongoDB Exporter, to track database performance.
Downloaded the Mongo DB exporter and extracted it before configuring.
![Screenshot 2024-02-28 161124](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/c339ed65-0ab4-403f-9771-7fba28c7098d)

![Screenshot 2024-02-28 160405](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/946f1c8c-ac76-434e-9b9a-ad5596ade297)
Prometheus Yaml file is given the scrape points to collect the metrics from as jobs(Prometheus,Mongodb and backend)
![Screenshot 2024-02-29 161501](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/578ad9c9-f697-4704-8bb4-535e57aef01e)
### Started Mongo db Exporter at 9216,while backend is already running at port 3001
![Screenshot 2024-03-01 150750](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/1afd9d58-723c-4d72-8a41-b4ed4b361dc2)

 ![Screenshot 2024-03-01 004330](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/bdb60322-2dd6-41e8-8309-e38c4a36c93f)
 ### Started prometheus at 9090
![Screenshot 2024-02-28 162917](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/cf8069b3-315f-49c1-bc90-c0e170b92065)
![Screenshot 2024-03-01 003229](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/3c54aa52-9582-4a60-bbac-d16243da91d5)


## 3. Enhance Grafana Dashboards:
### Install and start grafana at 3000 while restarting the front end server at 3002 or directly grafana at a unused port.
![Screenshot 2024-03-01 020506](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/32833063-1e87-4292-bbda-fda10ea7c67b)
- login to grafana runnng locally
![Screenshot 2024-03-01 020519](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/95bcc7af-06d0-4ce5-beb6-98513563391c)
- Add datasource as Prometheus
- ![Screenshot 2024-03-01 020737](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/c8610034-0663-4720-ba94-b348871a0fbe)
- Added the url of the prometheus
- ![Screenshot 2024-03-01 020903](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/58519d3c-dab2-4894-9d2d-59d84d424900)

   - Created advanced Grafana dashboards to display both the default and custom metrics from the MERN application.
![Screenshot 2024-03-01 021411](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/4655b525-dd28-49aa-917e-44c48fbc9117)
![Screenshot 2024-03-01 021500](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/6898d29d-f5cc-4ce1-b9bb-e6cc14ef9080)


   - Included detailed visualizations for backend performance, database health, and frontend performance (if possible).

## 4. Log Aggregation:

   - Integrated a log aggregation system (such as Loki, ELK Stack, or Fluentd) to collect and visualize logs from the MERN application.

   - Created a dashboard in Grafana to explore and analyze these logs.
![Screenshot 2024-03-01 022649](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/610e1f0e-e5c2-4d2d-a80d-cc8ea8a289e0)

## 5. Alerting and Anomaly Detection:

   - Developed sophisticated alerting rules in Grafana based on application-specific metrics and log patterns.
 ![Screenshot 2024-03-01 152533](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/09cedfd8-a52b-49f0-9d8b-f9802af7f9ff)

![image](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/dc7614db-cf21-4802-ae58-11a3253b1546)
![image](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/64fbf3af-3314-40db-b72f-27d55f6c50d8)
![image](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/cb3cd15f-fffe-4c72-8b23-2cad436c4914)
![image](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/a9ebc4d2-a516-4562-a969-d999a155a226)
Now the alert is created ,it will alert when the define threshhold is reached.
![image](https://github.com/rk630/MERN_Application_with_Grafana_and_Prometheus/assets/139606316/e2416fc3-1ef3-44cc-b017-e7fd732ad823)



   - Explored anomaly detection with Grafana, using the gathered metrics and logs.
