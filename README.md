# teams-league-airflow-elt

This project shows a real world use case with ELT pipeline using Cloud Storage, BigQuery, Airflow and Cloud Composer

The link to the video : 

https://youtu.be/XT-xdEtN0dA

The link to the article :

https://medium.com/@mazlum.tosun/elt-batch-pipeline-with-cloud-storage-bigquery-orchestrated-by-airflow-composer-8bbfc80bf171

### Deploy the Airflow DAG in Composer with Cloud Build from the local machine

```shell
gcloud builds submit \
    --project=$PROJECT_ID \
    --region=$LOCATION \
    --config deploy-dag.yaml \
    --substitutions _FEATURE_NAME="team_league_elt",_COMPOSER_ENVIRONMENT="dev-composer-env",_CONFIG_FOLDER_NAME="config",_ENV="dev" \
    --verbosity="debug" .
```
