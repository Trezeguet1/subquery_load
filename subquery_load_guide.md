# subquery_load_guide
1.Run IDE PyCharm CE
2. Clone and open subquery_load project GitHub - stepanLav/subquery_load
3. Run services in docker-compose.yml
4. Edit host = "https://api.subquery.network/sq/soramitsu" in locust_run.py

class QuickstartUser(HttpUser):
    wait_time = constant(float(os.environ.get('WAIT_TIME', 1)))
    host = "https://api.subquery.network/sq/soramitsu"

5. Replace '/fearless-wallet-dot' for 22&28 strings in locust_run.py
   
self.client.post('/fearless-wallet-dot', data=data, headers=self.headers)

6. Run services in docker-compose.yml again
7. Expand Docker Compose and run locust master
8. Run locust-worker-1
9. Run locust-worker-2
10. Check test results
