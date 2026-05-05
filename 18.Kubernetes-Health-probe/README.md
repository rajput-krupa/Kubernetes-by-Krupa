# Health Probes
Something that is monitoring the system and taking some necessary actions to grab status/ recovery/ to make sure system is healthy up and running.
In Kubernetes, 

<img width="618" height="251" alt="Screenshot 2026-05-05 at 12 05 49 PM" src="https://github.com/user-attachments/assets/6b67c080-6902-436b-9dbc-293c6209e1ee" />

The **liveness probe** doesn't fixes the issue by restarting but it gives you some time to look into and check for the actual bug.
First **startup probe**, then **Readiness Probe** and then the **Liveliness probe** starts in loop.

Probes are under containers:
<img width="475" height="212" alt="Screenshot 2026-05-05 at 12 12 53 PM" src="https://github.com/user-attachments/assets/ae5d9f4f-6737-46a1-ae19-83678ddae02f" />

<img width="294" height="162" alt="Screenshot 2026-05-05 at 12 14 30 PM" src="https://github.com/user-attachments/assets/7a375f0c-93eb-4a74-aeda-48d8de015464" />

Initialdelaysec ; timeinterval (secs 0-30 )of first health check.
periodSeconds: Frequency of interval (secs 0-30 )  of healtch checks.

# Steps of Health Check::
1. COntainer starts, **/tmp/healthy** file is created instantly, then  will wait for 30 secs.
2. Probe will continue hitting this endpoint. And as specified the interval, here 30 secs, this health checks will start failing. Bcoz we don't have the file anymore. This will try to cat on the app/ file that doesn't actually exists. End up giving the non-zero Error.
3. This will end up on the Liveprobe and the **Liveprobe** will restart the application. Till next 10 mins as we specified 600s.

ANother Eg: HTTP Probe
<img width="327" height="147" alt="Screenshot 2026-05-05 at 12 37 04 PM" src="https://github.com/user-attachments/assets/e1b1b610-c115-4183-94cf-1deb54400239" />
