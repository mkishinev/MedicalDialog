# Imaging and Procedures Summary (Append-Only)

**Purpose:** A structured, AI tools friendly, human-editable summary of imaging and procedure reports.
Add new studies by **appending** a new block (do not overwrite prior ones). 
Use the same AI tool to generate a new entry from a new imaging or procedure summary in pdf or other format.

---

## Schema for new entries (copy/paste)

```yaml
- study_type: ""
  body_region: ""
  exam_date: "YYYY-MM-DD"   # if unknown: "Not found in report"
  facility: ""
  indication: ""
  technique: ""
  key_findings:
    - ""
  quantitative_results:
    - name: ""
      value: ""
      units: ""
      reference_or_interpretation: ""
  impression: ""
  recommendations: ""
  source_file: ""
```

---

# Studies

---

## Colonoscopy

```yaml
- study_type: "Colonoscopy with Polypectomy"
  body_region: "Colon and Rectum"
  exam_date: "2024-08-03"
  facility: "Digestive Health Associates"
  indication: "Routine colorectal cancer screening; age 57 at time of procedure"
  technique: "Standard colonoscopy under moderate sedation (midazolam + fentanyl); Boston Bowel Preparation Scale score 8/9"
  key_findings:
    - "Complete examination to cecum achieved"
    - "One 6mm sessile polyp identified in the sigmoid colon"
    - "Polyp removed by cold snare polypectomy; specimen sent to pathology"
    - "Pathology result: tubular adenoma, low-grade dysplasia, completely excised"
    - "No other polyps, masses, or mucosal abnormalities identified"
    - "No diverticula, no hemorrhoids, no signs of colitis"
  quantitative_results:
    - name: "Number of polyps"
      value: "1"
      units: "count"
      reference_or_interpretation: "Single low-risk adenoma"
    - name: "Polyp size"
      value: "6"
      units: "mm"
      reference_or_interpretation: "Small; <10mm is lower risk category"
  impression: "Single 6mm tubular adenoma, low-grade dysplasia, completely resected. No high-risk features. Overall low-risk adenoma finding."
  recommendations: "Repeat colonoscopy in 3 years (2027-08) per standard surveillance guidelines for low-risk adenoma."
  source_file: "colonoscopy_report_2022-08-03.pdf"
```

---

## Right Knee X-Ray

```yaml
- study_type: "X-Ray, Right Knee, 3 Views"
  body_region: "Right Knee"
  exam_date: "2024-04-22"
  facility: "Orthopedic & Sports Medicine Imaging"
  indication: "Right knee pain with activity; pain worsening over 6 months; evaluate for structural pathology"
  technique: "Weight-bearing AP, lateral, and sunrise (merchant) views"
  key_findings:
    - "Moderate joint space narrowing in the medial tibiofemoral compartment"
    - "Marginal osteophyte formation at medial femoral condyle and tibial plateau"
    - "Mild subchondral sclerosis medial compartment"
    - "Lateral compartment preserved"
    - "Patellofemoral compartment shows mild lateral facet osteophytes"
    - "No acute fracture or dislocation"
    - "Soft tissue structures not assessable on plain film"
  quantitative_results:
    - name: "Kellgren-Lawrence Grade (medial compartment)"
      value: "2"
      units: "grade (0-4)"
      reference_or_interpretation: "Grade 2 = mild-moderate osteoarthritis; definite osteophytes, possible joint space narrowing"
    - name: "Medial joint space"
      value: "3.2"
      units: "mm"
      reference_or_interpretation: "Mildly reduced; normal >4mm weight-bearing"
  impression: "Grade 2 osteoarthritis right knee, predominantly medial compartment. Findings consistent with age-related degenerative change accelerated by high activity level. No acute pathology."
  recommendations: "Physical therapy referral for quadriceps strengthening and gait optimization. Activity modification as tolerated — cycling preferred over running for joint loading. NSAIDs contraindicated given intolerance; consider topical diclofenac or acetaminophen for pain management. Repeat imaging if symptoms progress. MRI if mechanical symptoms (locking, catching) develop."
  source_file: "right_knee_xray_2024-04-22.pdf"
```

---

## Lumbar Spine MRI

```yaml
- study_type: "MRI Lumbar Spine without Contrast"
  body_region: "Lumbar Spine"
  exam_date: "2020-01-08"
  facility: "Advanced Spine Imaging Center"
  indication: "Low back pain with left leg radiculopathy; pain radiating to left foot; evaluate for disc pathology"
  technique: "1.5T MRI; sagittal and axial T1 and T2 sequences; no contrast administered"
  key_findings:
    - "L4-L5: moderate disc space narrowing, posterior disc bulge with annular fissure, mild bilateral foraminal stenosis, left greater than right"
    - "L5-S1: mild disc space narrowing, small central and left paracentral disc protrusion, contact with left S1 nerve root without significant compression"
    - "L3-L4: mild facet arthropathy, no significant stenosis"
    - "No high-grade spinal canal stenosis at any level"
    - "Conus medullaris normal in position and signal"
    - "Vertebral body heights and alignment maintained"
  quantitative_results:
    - name: "L4-L5 disc height"
      value: "Moderately reduced"
      units: "qualitative"
      reference_or_interpretation: "Consistent with degenerative disc disease"
    - name: "Spinal canal diameter L4-L5"
      value: "12"
      units: "mm"
      reference_or_interpretation: "Low normal; >10mm generally adequate"
  impression: "Multilevel lumbar degenerative disc disease, most significant at L4-L5 with posterior bulge and mild bilateral foraminal stenosis. L5-S1 small disc protrusion with left S1 nerve root contact — likely source of left leg radiculopathy. No surgical emergency."
  recommendations: "Conservative management: physical therapy, core stabilization, epidural steroid injection if radiculopathy does not resolve. Neurosurgical referral only if progressive neurological deficit or bowel/bladder involvement. Avoid heavy axial spinal loading."
  source_file: "lumbar_MRI_2020-01-08.pdf"
```

---

## Stress Echocardiogram

```yaml
- study_type: "Exercise Stress Echocardiogram"
  body_region: "Heart"
  exam_date: "2023-03-18"
  facility: "Regional Cardiovascular Imaging Center"
  indication: "Post-NSTEMI cardiac function assessment; 2-year post-PCI evaluation; exercise tolerance assessment"
  technique: "Standard Bruce protocol treadmill exercise; 2D echocardiography at rest and peak stress; no contrast"
  key_findings:
    - "Resting LV function normal; EF estimated 58%"
    - "No resting wall motion abnormalities"
    - "Achieved 10.2 METS — excellent functional capacity for age"
    - "No exercise-induced wall motion abnormalities"
    - "No significant ST changes during exercise"
    - "Normal blood pressure response to exercise"
    - "Mild diastolic dysfunction grade 1 at rest — age-appropriate"
    - "No significant valvular abnormalities"
  quantitative_results:
    - name: "Resting Ejection Fraction (EF)"
      value: "58"
      units: "%"
      reference_or_interpretation: "Normal (>55%); preserved systolic function post-NSTEMI"
    - name: "Exercise capacity"
      value: "10.2"
      units: "METS"
      reference_or_interpretation: "Excellent; >10 METS associated with very low cardiac mortality"
    - name: "Peak heart rate achieved"
      value: "158"
      units: "bpm"
      reference_or_interpretation: "94% of age-predicted maximum; adequate stress achieved"
    - name: "Peak systolic BP"
      value: "194"
      units: "mmHg"
      reference_or_interpretation: "Normal exercise BP response"
  impression: "Excellent functional capacity at 10.2 METS. Normal LV systolic function with EF 58%. No inducible ischemia. No exercise-induced wall motion abnormalities. Reassuring post-NSTEMI stress test. Mild grade 1 diastolic dysfunction — age-appropriate, not clinically significant at this time."
  recommendations: "Continue current cardiac medications. No exercise restrictions — high activity level supported by results. Repeat stress echo in 3 years or sooner if new symptoms (chest pain, dyspnea, palpitations) develop. Annual cardiology follow-up."
  source_file: "stress_echo_2023-03-18.pdf"
```

---

## DEXA Scan (Bone Density)

```yaml
- study_type: "Dual-Energy X-Ray Absorptiometry (DEXA)"
  body_region: "Lumbar Spine and Left Hip"
  exam_date: "2024-11-05"
  facility: "Regional Bone Health Center"
  indication: "Baseline bone density assessment; age 59; family history of osteoporosis (mother); long-term statin use"
  technique: "Standard DEXA protocol; lumbar spine L1-L4 and left hip (femoral neck and total hip)"
  key_findings:
    - "Lumbar spine BMD mildly reduced for age"
    - "Femoral neck BMD within normal range"
    - "Total hip BMD within normal range"
    - "No vertebral fractures identified on lateral spine imaging"
  quantitative_results:
    - name: "Lumbar Spine L1-L4 BMD"
      value: "1.08"
      units: "g/cm²"
      reference_or_interpretation: "T-score -1.2; low normal; osteopenia threshold is T-score < -1.0"
    - name: "Lumbar Spine T-score"
      value: "-1.2"
      units: "SD"
      reference_or_interpretation: "Osteopenia range (-1.0 to -2.5); monitor"
    - name: "Femoral Neck BMD"
      value: "0.94"
      units: "g/cm²"
      reference_or_interpretation: "T-score -0.6; normal"
    - name: "Femoral Neck T-score"
      value: "-0.6"
      units: "SD"
      reference_or_interpretation: "Normal range (> -1.0)"
    - name: "Total Hip T-score"
      value: "-0.4"
      units: "SD"
      reference_or_interpretation: "Normal range"
  impression: "Mild osteopenia at lumbar spine (T-score -1.2). Normal femoral neck and total hip density. High activity level is protective. Maternal family history of osteoporosis warrants monitoring."
  recommendations: "Ensure adequate calcium (1200mg/day dietary preferred) and Vitamin D (maintain 25-OH-D 40-60 ng/mL). Continue weight-bearing exercise. Repeat DEXA in 2 years. No pharmacological treatment indicated at this time. Reassess if T-score worsens or fragility fracture occurs."
  source_file: "DEXA_2024-11-05.pdf"
```

---

## Physical Therapy — Right Knee

```yaml
- study_type: "Physical Therapy Course"
  body_region: "Right Knee"
  exam_date: "2026-02-06"
  facility: "ActiveCare Physical Therapy"
  indication: "Right knee osteoarthritis Grade 2; pain with stairs, prolonged walking, and heavy leg press"
  technique: "12-session course over 8 weeks; quadriceps strengthening, VMO activation, gait retraining, activity modification counseling"
  key_findings:
    - "Initial presentation: pain rated 6/10 with descending stairs, 4/10 with cycling"
    - "Significant quadriceps weakness identified, particularly VMO"
    - "Mild gait deviation with knee valgus under load"
    - "Discharge assessment: pain 2/10 with stairs, 1/10 with cycling"
    - "Strength improved approximately 35% by dynamometry"
  quantitative_results:
    - name: "Initial pain (NRS, stairs)"
      value: "6"
      units: "out of 10"
      reference_or_interpretation: "Moderate pain at intake"
    - name: "Discharge pain (NRS, stairs)"
      value: "2"
      units: "out of 10"
      reference_or_interpretation: "Significant improvement; functional"
    - name: "Sessions completed"
      value: "12"
      units: "sessions"
      reference_or_interpretation: "Full course completed"
  impression: "Good response to PT. Functional improvement achieved. Patient counseled to continue home exercise program and avoid high-impact axial loading (running, heavy leg press). Cycling and swimming preferred."
  recommendations: "Continue home exercise program. Return to PT if symptoms recur or worsen. Orthopedic consultation if pain returns to baseline despite PT. Avoid running as primary cardio."
  source_file: "PT_discharge_summary_2024-06-28.pdf"
```

---

