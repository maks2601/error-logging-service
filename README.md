# error-logging-service
<p align="center"><b>Stack</b></p>
<ol>
<li>For client SDK I prefer OpenTelemetry because it will be easier to connect it to our backend then other popular solutions like Sentry</li>
<li>For the Backend API I would use Nest.js as a reliable solution in case of project expansion. Then JWT for control authorization and limiting the count of events from specific client. After auth data will be transferred through Kafka to processing services where it will be stored in our DB. As a DB provider I would choose ClickHouse because it’s columnar db so it is more optimized for working with such data types for example sort, count and insert errors much faster.</li>
<li>For the dashboard I would use React or React Native depending on whether it will be used as a mobile app. Tailwind and shadcn for fast prototyping and Recharts as good lib for displaying charts</li>
<li>For email notifications I’d prefer Postmark because it’s easy to implement and it saves us from getting important messages about critical errors into spam</li>
<li>For scalable deployment I will use Docker for containerization of API, dashboard and ClickHouse. Kubernetes to manage scale and Fly.io for easy MVP deployment or AWS if we’re planning to scale fast. Grafana will be used for monitoring</li>
</ol>
<p align="center"><b>Questions</b></p>
<ul>
<li>Will we have a mobile app for the dashboard?</li>
<li>At the moment, are we focusing on the speed of MVP development or on working with a large number of simultaneous users?</li>
<li>What competitive advantages will our service provide? (to understand the complexity of development)</li>
</ul>
