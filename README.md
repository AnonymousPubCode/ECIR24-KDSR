# KDSR: Knowledge Distillation for Modality-enriched Sequential Recommendation

This is a temporary repository space for our ECIR24 submission code, anonymized to keep specific details, including personal and institutional identifiers, concealed. Upon acceptance of our paper, we will release the full repository, which will encompass baseline implementations and other supplementary details.

## Preprocessing Steps

1. **Download Raw Data**:
   - Retrieve the dataset from [Amazon Reviews](http://jmcauley.ucsd.edu/data/amazon/links.html).

2. **Image Collection**:
   - Create an `image` directory within the downloaded dataset folder.
   - Crawl and store the images in the `image` directory.

3. **Set Configuration**:
   - Refer to `config/preprocess.yaml` for initiating dataset preparation.

4. **Data Extraction and Processing**:
   - Navigate to the `preprocess/dataset_name/` directory.
   - Sequentially execute the following scripts:
     ```python
     sh preprocess.sh
     ```

_Note_: The preprocessing stage offers various options. You can generate datasets for:
- Collaborative Filtering (`dataset_cf`)
- Sequential Recommendation (`dataset_sr`)
- Multimodal Sequential Recommendation (`dataset_mmsr`)

## Execution Guide

**Before You Start**:
- Inspect the `config/model.yaml` to confirm your configuration settings.
- Ensure you're pointing to the appropriate preprocessed dataset directory.

**Running the Model**:
Simply use the following command:

```python
python main.py dataset_name
```

For instance, to run the model on the 'beauty' dataset:

```python
python main.py beauty
```

Results will be directed to the `log/` directory.

## Additional Information

An illustrative execution log is available in `running_records.log`. It showcases the model's runtime records and outcomes on the beauty dataset.
