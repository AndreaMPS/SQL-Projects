# Andrea Smith | MIMIC-IV Hospital Stay Data - Relational Database Analysis & Tabling | 6160

# 6.0 Creating table with health factors ***************************************************
CREATE TABLE predictive_model_data (
    age_at_admission DECIMAL(5, 2),
    gender ENUM('Female', 'Male'),
    race ENUM('White/Cauc', 'Black/AfrAm', 'Other'),
    cci_score INT,

    -- Binary indicators for past diagnoses
    mi_indicator BOOLEAN,
    chf_indicator BOOLEAN,
    pad_indicator BOOLEAN,
    cerebrovascular_indicator BOOLEAN,
    dementia_indicator BOOLEAN,
    copd_indicator BOOLEAN,
    connective_tissue_disorder_indicator BOOLEAN,
    ulcer_disease_indicator BOOLEAN,
    mild_liver_disease_indicator BOOLEAN,
    diabetes_no_complications_indicator BOOLEAN,
    diabetes_with_complications_indicator BOOLEAN,
    hemiplegia_indicator BOOLEAN,
    renal_disease_indicator BOOLEAN,
    malignancy_indicator BOOLEAN,
    moderate_liver_disease_indicator BOOLEAN,
    metastatic_solid_indicator BOOLEAN,
    hiv_aids_indicator BOOLEAN,

    -- Lab results within past 6 months or 6 hours from ED
    max_cholesterol ENUM('>200 mg/dL', '<=200 mg/dL', 'Missing'),
    max_triglycerides ENUM('>150 mg/dL', '<=150 mg/dL', 'Missing'),
    min_hdl ENUM('>=60 mg/dL', '<60 mg/dL', 'Missing'),
    max_ldl ENUM('>100 mg/dL', '<=100 mg/dL', 'Missing'),
    min_albumin ENUM('>=3.5 g/dL', '<3.5 g/dL', 'Missing'),
    min_albumin_ed ENUM('>=3.5 g/dL', '<3.5 g/dL', 'Missing'),
    max_sodium_ed ENUM('>143 mmol/L', '<134 mmol/L', '134-143 mmol/L', 'Missing'),
    min_sodium_ed ENUM('>143 mmol/L', '<134 mmol/L', '134-143 mmol/L', 'Missing'),
    max_potassium_ed ENUM('>5.1 mmol/L', '<3.5 mmol/L', '3.5-5.1 mmol/L', 'Missing'),
    min_potassium_ed ENUM('>5.1 mmol/L', '<3.5 mmol/L', '3.5-5.1 mmol/L', 'Missing'),
    max_chloride_ed ENUM('>107 mmol/L', '<98 mmol/L', '98-107 mmol/L', 'Missing'),
    min_chloride_ed ENUM('>107 mmol/L', '<98 mmol/L', '98-107 mmol/L', 'Missing'),
    max_co2_ed ENUM('>31 mmol/L', '<21 mmol/L', '21-31 mmol/L', 'Missing'),
    min_co2_ed ENUM('>31 mmol/L', '<21 mmol/L', '21-31 mmol/L', 'Missing'),
    max_glucose_ed ENUM('>125 mg/dL', '<70 mg/dL', '70-125 mg/dL', 'Missing'),
    min_glucose_ed ENUM('>125 mg/dL', '<70 mg/dL', '70-125 mg/dL', 'Missing'),
    max_bun_ed ENUM('>30 mg/dL', '<=30 mg/dL', 'Missing'),
    max_creatinine_ed ENUM('>0.95 mg/dL', '<=0.95 mg/dL', 'Missing'),
    min_egfr_ed ENUM('>=60 mL/min/1.73m2', '<60 mL/min/1.73m2', 'Missing'),
    max_total_protein_ed ENUM('>8.3 g/dL', '<6.3 g/dL', '6.3-8.3 g/dL', 'Missing'),
    min_total_protein_ed ENUM('>8.3 g/dL', '<6.3 g/dL', '6.3-8.3 g/dL', 'Missing'),
    max_total_bilirubin_ed ENUM('>1 mg/dL', '<=1 mg/dL', 'Missing'),
    max_calcium_ed ENUM('>10.3 mg/dL', '<8.6 mg/dL', '8.6-10.3 mg/dL', 'Missing'),
    min_calcium_ed ENUM('>10.3 mg/dL', '<8.6 mg/dL', '8.6-10.3 mg/dL', 'Missing'),
    max_wbc_ed ENUM('>10.7 x10^3/uL', '<4.1 x10^3/uL', '4.1-10.7 x10^3/uL', 'Missing'),
    min_wbc_ed ENUM('>10.7 x10^3/uL', '<4.1 x10^3/uL', '4.1-10.7 x10^3/uL', 'Missing'),
    max_rbc_ed ENUM('>4.9 x10^6/uL', '<3.7 x10^6/uL', '3.7-4.9 x10^6/uL', 'Missing'),
    min_rbc_ed ENUM('>4.9 x10^6/uL', '<3.7 x10^6/uL', '3.7-4.9 x10^6/uL', 'Missing'),
    max_rdW_ed ENUM('>16.3%', '<12.2%', '12.2-16.3%', 'Missing'),
    min_rdW_ed ENUM('>16.3%', '<12.2%', '12.2-16.3%', 'Missing'),
    max_hemoglobin_ed ENUM('>15 g/dL', '<11.5 g/dL', '11.5-15 g/dL', 'Missing'),
    min_hemoglobin_ed ENUM('>15 g/dL', '<11.5 g/dL', '11.5-15 g/dL', 'Missing'),
    max_hematocrit_ed ENUM('>44%', '<34%', '34-44%', 'Missing'),
    min_hematocrit_ed ENUM('>44%', '<34%', '34-44%', 'Missing'),
    max_platelets_ed ENUM('>376 x10^3/uL', '<153 x10^3/uL', '153-376 x10^3/uL', 'Missing'),
    min_platelets_ed ENUM('>376 x10^3/uL', '<153 x10^3/uL', '153-376 x10^3/uL', 'Missing'),
    max_neutrophils_ed ENUM('>7.4 x10^3/uL', '<2 x10^3/uL', '2-7.4 x10^3/uL', 'Missing'),
    min_neutrophils_ed ENUM('>7.4 x10^3/uL', '<2 x10^3/uL', '2-7.4 x10^3/uL', 'Missing'),
    max_lymph_ed ENUM('>3.5 x10^3/uL', '<1.1 x10^3/uL', '1.1-3.5 x10^3/uL', 'Missing'),
    min_lymph_ed ENUM('>3.5 x10^3/uL', '<1.1 x10^3/uL', '1.1-3.5 x10^3/uL', 'Missing'),
    max_lactate_ed ENUM('>2 mmol/L', '<=2 mmol/L', 'Missing'),
    max_troponin_ed ENUM('>0.08 ng/mL', '<=0.08 ng/mL', 'Missing'),
    min_map_ed ENUM('>=60 mmHg', '<60 mmHg', 'Missing'),
    max_fio2_ed ENUM('>0.21%', '<=0.21%', 'Missing'),
    max_o2_flow_rate_ed ENUM('>0 L/min', 'Missing or 0 L/min'),
    min_gcs_ed ENUM('>=14', '<14', 'Missing'),
    max_po2_ed ENUM('>100 mmHg', '<75 mmHg', '75-100 mmHg', 'Missing'),
    min_po2_ed ENUM('>100 mmHg', '<75 mmHg', '75-100 mmHg', 'Missing'),
    max_pco2_ed ENUM('>45 mmHg', '<35 mmHg', '35-45 mmHg', 'Missing'),
    min_pco2_ed ENUM('>45 mmHg', '<35 mmHg', '35-45 mmHg', 'Missing'),

    /* Vitals within 6 hours from ED */
    max_heart_rate_ed INT,
    max_respiratory_rate_ed INT,
    min_respiratory_rate_ed INT,
    min_dbp_ed INT,
    min_sbp_ed INT,
    max_temperature_ed DECIMAL(4, 2),
    min_o2_saturation_ed INT
);

# ***************************************************************************

/* 7.0 MySQL: Identify Patients with Sepsis-3 and Diagnosed with Sepsis at Discharge */
WITH sepsis_patients AS (
    SELECT
        p.subject_id,
        p.hadm_id,
        p.stay_id,
        d.icd_code,
        d.icd_version
    FROM
        icustays p
    INNER JOIN diagnoses_icd d ON p.hadm_id = d.hadm_id
    WHERE
        d.icd_code IN ('A419', 'R6521', 'R6520') /* Example ICD codes for Sepsis, replace as needed */
        AND d.icd_version = 10 /* Assuming ICD-10 codes, change as needed  */
),
sofa_scores AS (
    SELECT
        p.subject_id,
        p.hadm_id,
        p.stay_id,
        MIN(s.charttime) AS sepsis_onset_time
    FROM
        chartevents s
    INNER JOIN sepsis_patients p ON s.subject_id = p.subject_id AND s.hadm_id = p.hadm_id
    WHERE
        s.itemid IN (220739, 223900, 220045) /* Example SOFA-related item IDs */
        AND s.value IS NOT NULL
        AND s.value > 2 /* Example threshold for SOFA */
    GROUP BY
        p.subject_id, p.hadm_id, p.stay_id
)
SELECT
    DISTINCT p.subject_id,
    p.hadm_id,
    p.stay_id,
    r.text AS radiology_report
FROM
    sofa_scores p
INNER JOIN radiology_reports r ON p.subject_id = r.subject_id
ORDER BY RAND()
LIMIT 10;


# Upload Data to Snowflake
# Export the Results: Save the query results into a CSV file.
# Load Data into Snowflake: Use the Snowflake PUT and COPY INTO commands to upload 

# **************************
/* 7.2 Snowflake: Create a table in Snowflake */
CREATE OR REPLACE TABLE sepsis_patients_radiology (
    subject_id INT,
    hadm_id INT,
    stay_id INT,
    radiology_report TEXT
);

-- Load the data into Snowflake
PUT file://path/to/exported.csv @mystage;
COPY INTO sepsis_patients_radiology
FROM @mystage/exported.csv
FILE_FORMAT = (TYPE = 'CSV' FIELD_OPTIONALLY_ENCLOSED_BY = '"');

# Integrate LLM with Snowflake: Set up an LLM-enabled SQL tool like Snowflake's Snowpark with Python to summarize similarities.
# Python Code for LLM Processing:
from snowflake.snowpark.session import Session
from openai import ChatCompletion

# Snowflake connection
session = Session.builder.configs({
    "account": "your_account",
    "user": "your_user",
    "password": "your_password",
    "database": "your_database",
    "schema": "your_schema"
}).create()

# Query the data
df = session.sql("SELECT radiology_report FROM sepsis_patients_radiology").to_pandas()

# Use OpenAI API to summarize
openai.api_key = "your_openai_api_key"
responses = []
for report in df['radiology_report']:
    response = ChatCompletion.create(
        model="gpt-4",
        messages=[
            {"role": "system", "content": "Summarize the similarities between radiology reports."},
            {"role": "user", "content": report}
        ]
    )
    responses.append(response['choices'][0]['message']['content'])

# Print summarized similarities
for idx, summary in enumerate(responses):
    print(f"Report {idx + 1} Summary: {summary}")



