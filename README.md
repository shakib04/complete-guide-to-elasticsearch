This repository contains all of the queries used within the [Complete Guide to Elasticsearch course](https://l.codingexplained.com/r/elasticsearch-course?src=github).

<h3>Installation on Linux</h3>
After downloading the Elasticsearch archive, extract it using the following command:
<pre><code>tar -xvf elasticsearch-7.6.2-linux-x86_64.tar.gz</code></pre>

After extracting the archive, you can start Elasticsearch by running the following command:
<pre><code>./elasticsearch-7.6.2/bin/elasticsearch</code></pre>

This will generate a jwt token that you can use to authenticate with the API. You can find the token in the console output, it will look something like this:
<pre><code>
eyJ2ZXIiOiI4LjguMiIsImFkciI6WyIxOTIuMTY4LjAuMTAzOjkyMDAiXSwiZmdyIjoiYzI5MjRmNGY0YTkxOTY2Mzc1ZmVjMzc5NDgyNWUyMzAwMDY0NjA2MGJkNTYxY2ZlZDQ0ZDI3ODdjYzM3ODU2YyIsImtleSI6Ikp6WVpmSWtCaEVtYmt1NHMxTkFfOkktdkI4MmpjUWYtVUNwUWQtQlFPbEEifQ==
</code></pre>

You can use this token to authenticate with the API. Generate a new token by running the following command:
<pre><code>curl -X POST "localhost:9200/_security/oauth2/token" -H 'Content-Type: application/json' -d'
{
  "grant_type": "client_credentials",
  "scope": "kibana"
}'</code></pre>

Ubuntu command:
<pre><code>
bin/elasticsearch-create-enrollment-token --scope kibana
</code></pre>

Login to Kibana using the following URL:
<pre><code>http://localhost:5601</code></pre>

username: elastic
password: the token you generated 
<pre><code>
tjp2nBKbvK2b4JQYNwhh
</code></pre>



Paasoword Reset Command:
<pre><code>
bin/elasticsearch-reset-password -u elastic
</code></pre>



