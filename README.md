aa>**NOTE:**
  * aa
  * bb

Breaking Changes:
- Change the Azure CPI job name from `cpi` to `azure_cpi`. You should update your `bosh.yml`.
  From

  ```
  jobs:
  - name: bosh
    templates:
    - {name: cpi, release: bosh-azure-cpi}

    properties:
      director:
        cpi_job: cpi

  cloud_provider:
    template: {name: cpi, release: bosh-azure-cpi}
  ```

  to

  ```
  jobs:
  - name: bosh
    templates:
    - {name: azure_cpi, release: bosh-azure-cpi}

    properties:
      director:
        cpi_job: azure_cpi

  cloud_provider:
    template: {name: azure_cpi, release: bosh-azure-cpi}
  ```
