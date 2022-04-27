# subquery_load_guide
1. run pycharm
2. open subquery_load
3. rename docker-compose.yml
4. rename locust_run.py
5. edit host = "https://api.subquery.network/sq/soramitsu" in locust_run.py
6. change  strings in locust_run.py

def stake_changes(self):
data = json.dumps(stake_changes_by_address(self.address))
        self.client.post('/fearless-wallet-dot', data=data, headers=self.headers)

@tag('history_elements')
@task
def history_elements(self):
data = json.dumps(history_changes_by_address(self.address))
        self.client.post('/fearless-wallet-dot', data=data, headers=self.headers)

7. run services
8. run locust master
9. run locust-worker-1
10. run locust-worker-2
11. view test results
