# Detection-of-Heart-Murmur-from-Phonocardiogram-Signals

DEEP MURMUR: AI DRIVEN PHONOCARDIOGRAM ANALYSIS FOR HEART MURMUR DETECTION

MODEL: STACKED ENSEMBLE MODEL

PREPROCESSING:
1. FILTERING OF THE AUDIO FILES USING BUTTER WORTH BAND PASS FILTER OF RANGE 25Hz TO 400Hz
2. TEMPORAL SLIDING WINDOW BASED SEGMENTATION:1 SECOND WINDOW WITH 50% OVERLAP
3. EXTRACT MFCC FEATURES FOR EACH SEGMENT.

THERE ARE 4 VALVE RECORDINGS FOR A PERSON SO EACH VALVE HAS 13 MFCC COEFFICIENTS
TOTALLY: 13*4=52 MFCC COEFFICIENTS PER PATIENT

AND 92- SEGMENTS OF WINDOW(FIXED FOR ALL PATIENTS BY PADDING)

AFTER PREPROCESSING WE GET 92*52 FEATURE MATRIX AS OUTPUT.

BASE LEARNER 1:MULTI HEAD SELF ATTENTION TRANSFORMER

BASE LEARNER 2:PATCH TST(HUGGING FACE)

META LEARNER:XGBOOST
