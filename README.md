# ena-testing-example-data
This contains example submissions for ENA

Submit using:

```bash
curl -X POST 'https://www.ebi.ac.uk/ena/submit/drop-box/submit' -u "$ena_submission_password:$ena_submission_password" -F "SUBMISSION=@project_test/submission.xml" -F "PROJECT=@project_test/project.xml" --max-time 10
curl -X POST 'https://www.ebi.ac.uk/ena/submit/drop-box/submit' -u "$ena_submission_password:$ena_submission_password" -F "SUBMISSION=@sample_test/submission.xml" -F "SAMPLE=@sample_test/sample.xml" --max-time 10
java -jar webin-cli.jar -username '$ena_submission_password' -password '$ena_submission_password' -context genome -manifest assembly_test/manifest.tsv -submit -test
```

to the test environment or to production:

```bash
curl -X POST 'https://www.ebi.ac.uk/ena/submit/drop-box/submit' -u "$ena_submission_password:$ena_submission_password" -F "SUBMISSION=@project_test/submission.xml" -F "PROJECT=@project_test/project.xml" --max-time 10
curl -X POST 'https://www.ebi.ac.uk/ena/submit/drop-box/submit' -u "$ena_submission_password:$ena_submission_password" -F "SUBMISSION=@sample_test/submission.xml" -F "SAMPLE=@sample_test/sample.xml" --max-time 10
java -jar webin-cli.jar -username '$ena_submission_password' -password '$ena_submission_password' -context genome -manifest assembly_test/manifest.tsv -submit
```

You should receive a response if not check that your password is accurate - it must be enclosed in `'` and you will not be notified if there was an error. 