# run pycharm
# open subquery_load
# rename docker-compose.yml
# reanme docker-compose.yml
# edit host = "https://api.subquery.network/sq/soramitsu" in locust_run.py
# change  strings

{
def stake_changes(self):
        data = json.dumps(stake_changes_by_address(self.address))
        self.client.post('/fearless-wallet-dot', data=data, headers=self.headers)

    @tag('history_elements')
    @task
    def history_elements(self):
        data = json.dumps(history_changes_by_address(self.address))
        self.client.post('/fearless-wallet-dot', data=data, headers=self.headers)
}
# run services
# run locust master
# run locust-worker-1
# run locust-worker-2
