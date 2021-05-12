This guide explains how to serverlessly perform scheduled data load from [Cloud Storage](https://cloud.google.com/storage) and transform in [BigQuery](https://cloud.google.com/bigquery) using [Cloud Workflows](https://cloud.google.com/workflows), [Cloud Functions](https://cloud.google.com/functions) and [Firestore](https://cloud.google.com/firestore)

Please refer to the related article for all the steps to follow in this tutorial: [Serverless orchestration: Loading data from Cloud Storage to BigQuery using Workflows](https://cloud.google.com/architecture/serverless-orchestration-loading-data-from-cloud-storage-to-biquery-using-workflows)

Contents of this repository:

* `main.tf`: Terraform template to set up the demo
* `file_change_handler`: Cloud Function trigger (Python 3.7) to handle [object finalize](https://cloud.google.com/functions/docs/calling/storage#object_finalize) events from Cloud Storage.
* `workflow_handlers`: Cloud Functions to handle BigQuery jobs and the workflow YAML.
* `generator`: Script (Python 3.7) to generate AVRO files and upload to a Cloud Storage bucket.
