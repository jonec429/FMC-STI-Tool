FMC Internal STI Screening Tool
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>STI Clinical Decision Support</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        /* Simple transition for showing/hiding elements */
        .step-section {
            display: none;
            opacity: 0;
            transition: opacity 0.5s ease-in-out, transform 0.3s ease-in-out;
            transform: translateY(10px); /* Start slightly down */
        }
        .step-section.active {
            display: block;
            opacity: 1;
             transform: translateY(0); /* Move to final position */
        }
        /* Custom scrollbar */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #f1f1f1; border-radius: 10px; }
        ::-webkit-scrollbar-thumb { background: #888; border-radius: 10px; }
        ::-webkit-scrollbar-thumb:hover { background: #555; }
        /* Style for clickable options */
        .option-button {
            transition: background-color 0.2s ease, transform 0.1s ease, box-shadow 0.2s ease;
             box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .option-button:hover {
            background-color: #e0f2fe; /* light sky blue */
            transform: translateY(-2px);
             box-shadow: 0 4px 8px rgba(0,0,0,0.15);
        }
        .option-button:active {
            transform: translateY(1px);
             box-shadow: 0 1px 2px rgba(0,0,0,0.1);
        }
        /* Styling for the recommendation box */
        #flow-recommendation ul { margin-left: 1.5rem; list-style-type: disc; margin-bottom: 1rem;}
        #flow-recommendation li { margin-bottom: 0.5rem; }
        #flow-recommendation strong { font-weight: 600; color: #1d4ed8; } /* Bolder blue */
        #flow-recommendation h3 { font-size: 1.125rem; font-weight: 600; margin-bottom: 0.75rem; color: #1f2937; } /* Slightly larger, darker */
        #flow-recommendation h4 { font-size: 1rem; font-weight: 600; margin-top: 1rem; margin-bottom: 0.5rem; color: #374151; }
        #flow-recommendation p { margin-bottom: 0.75rem; line-height: 1.6; }
        #flow-recommendation .text-xs { font-size: 0.75rem; line-height: 1.2; margin-top: 0.25rem; }
        #flow-recommendation .text-red-600 { color: #dc2626; }
        #flow-recommendation .first-line { color: #166534; font-weight: bold; } /* Added style for first-line indication */
        #flow-recommendation .drug-details { margin-left: 1rem; margin-bottom: 0.5rem; } /* Indent drug details */
        #flow-recommendation .drug-details strong { color: #111827; } /* Darker text for drug name/dose */
        #flow-recommendation .fmc-note { background-color: #fefce8; border-left: 4px solid #ca8a04; padding: 0.75rem; margin-top: 1rem; font-size: 0.875rem; } /* Yellow note box */
        #flow-recommendation .fmc-note strong { color: #a16207; } /* Darker yellow */
        #flow-recommendation .fdoh-contact { background-color: #eff6ff; border-left: 4px solid #3b82f6; padding: 0.75rem; margin-top: 1rem; font-size: 0.875rem; } /* Blue note box */
         #flow-recommendation .fdoh-contact strong { color: #1e40af; } /* Darker blue */
         #flow-recommendation .fdoh-contact a { color: #2563eb; text-decoration: underline; }
         #flow-recommendation .fdoh-contact a:hover { color: #1d4ed8; }

    </style>
</head>
<body class="bg-gray-100 min-h-screen flex flex-col items-center p-4 py-8">

    <div class="bg-white rounded-lg shadow-xl p-6 md:p-8 w-full max-w-4xl mx-auto">
        <h1 class="text-2xl md:text-3xl font-bold text-center text-blue-700 mb-6">STI Clinical Decision Support Tool</h1>
        <p class="text-center text-gray-600 mb-8 text-sm">Based on CDC 2021 STI Treatment Guidelines with FMC Reporting Protocols. This tool is for informational purposes and does not replace clinical judgment.</p>

        <!-- Step 1: Select Patient Type -->
        <div id="step-patient-type" class="step-section active">
            <h2 class="text-xl font-semibold mb-4 text-gray-800 text-center">1. Select Patient Type:</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mt-6">
                <button onclick="handlePatientType('pregnant')" class="option-button bg-blue-100 text-blue-800 p-4 rounded-lg font-medium hover:bg-blue-200 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">Pregnant</button>
                <button onclick="handlePatientType('female_not_pregnant')" class="option-button bg-pink-100 text-pink-800 p-4 rounded-lg font-medium hover:bg-pink-200 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-offset-2">Female (Not Pregnant)</button>
                <button onclick="handlePatientType('male')" class="option-button bg-indigo-100 text-indigo-800 p-4 rounded-lg font-medium hover:bg-indigo-200 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2">Male</button>
            </div>
        </div>

        <!-- Step 2: Dynamic Flow Steps -->
        <div id="step-flow" class="step-section">
            <h2 id="flow-title" class="text-xl font-semibold mb-6 text-gray-800 text-center"></h2>

            <!-- Area for Question Options -->
            <div id="flow-options" class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                <!-- Options buttons will be populated here -->
            </div>

            <!-- Area for Recommendation Content -->
            <div id="flow-recommendation" class="prose max-w-none text-gray-700 bg-gray-50 p-4 rounded-lg border border-gray-200 overflow-y-auto max-h-[60vh] " style="display: none;">
                <!-- Recommendation HTML will be populated here -->
            </div>

             <!-- Navigation Buttons -->
            <div class="mt-8 flex justify-between items-center">
                 <button id="back-button" onclick="goBack()" class="inline-flex items-center px-4 py-2 border border-gray-300 shadow-sm text-sm font-medium rounded-md text-gray-700 bg-white hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
                    Back
                </button>
                <button onclick="resetApp()" class="inline-flex items-center px-4 py-2 border border-transparent shadow-sm text-sm font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-500">
                    Start Over
                </button>
            </div>
        </div>
    </div>

    <script>
        // Store the history of steps taken for back navigation
        let historyStack = ['step-patient-type'];

        // --- GUIDELINE DATA STRUCTURE ---
        // Enhanced structure to support multi-step logic
        // type: 'question' or 'recommendation'
        // title: Text displayed above options/recommendation
        // options: Array of {text: button_label, nextStep: id_of_next_node} (only for type: 'question')
        // content: HTML content (only for type: 'recommendation')
        // parentRef: Optional reference to the source guide section for recommendations
        const fdohContactInfo = `
            <div class="fdoh-contact">
                <strong>FDOH Reporting Contact:</strong><br>
                To report communicable diseases in Florida, call <strong>(850) 245-4401</strong> (24/7).<br>
                Website: <a href="https://www.floridahealth.gov/diseases-and-conditions/disease-reporting-and-management/" target="_blank" rel="noopener noreferrer">floridahealth.gov/diseases-and-conditions/disease-reporting-and-management/</a>
            </div>
        `;

        const guidelines = {
            // --- PREGNANT ---
            pregnant: {
                start: {
                     title: "Select Clinical Scenario (Pregnant)",
                     type: 'question',
                     options: [
                        { text: "Initial Screening", nextStep: 'screening_initial' },
                        { text: "Chlamydia Diagnosis", nextStep: 'chlamydia_rec' },
                        { text: "Gonorrhea Diagnosis", nextStep: 'gonorrhea_rec' },
                        { text: "Syphilis Diagnosis", nextStep: 'syphilis_start' },
                        { text: "Trichomoniasis (Symptomatic)", nextStep: 'trich_rec' },
                        { text: "Bacterial Vaginosis (BV) (Symptomatic)", nextStep: 'bv_rec' },
                        { text: "Genital Herpes (HSV)", nextStep: 'hsv_start' },
                     ]
                },
                screening_initial: {
                    title: "Initial Prenatal Screening Summary",
                    type: 'recommendation',
                    parentRef: '"STI Detection Among Special Populations > Pregnant Women" (page 11)',
                    content: `
                        <h3 class="font-semibold text-lg mb-2">Initial Prenatal Visit Screening:</h3>
                        <ul>
                            <li><strong>HIV:</strong> All (opt-out). Retest 3rd trimester if high risk. Rapid test in labor if status unknown.</li>
                            <li><strong>Syphilis:</strong> All. Retest at 28 weeks & delivery if high risk or high community prevalence.</li>
                            <li><strong>Hepatitis B (HBsAg):</strong> All. Vaccinate if susceptible & at risk. Test at delivery if high risk or not screened.</li>
                            <li><strong>Chlamydia:</strong> All <25 yrs, older if increased risk. Retest 3rd trimester if risk persists.</li>
                            <li><strong>Gonorrhea:</strong> All <25 yrs, older if increased risk. Retest 3rd trimester if risk persists.</li>
                            <li><strong>Hepatitis C (HCV):</strong> All during each pregnancy (unless prevalence <0.1%).</li>
                            <li><strong>Cervical Cancer:</strong> Screen same frequency as non-pregnant.</li>
                            <li><strong>BV & Trichomonas:</strong> Screen ONLY if symptomatic.</li>
                            <li><strong>Genital Herpes (HSV):</strong> Routine serologic screening NOT recommended for asymptomatic. Type-specific tests might help identify risk.</li>
                        </ul>
                         <div class="fmc-note">
                             <strong>FMC HIV Reporting Protocol:</strong> Report positive HIV results to patient & health department. Notify triage. Complete Practitioner Disease Report Form within 2 weeks, secure in double envelope marked confidential, mail certified (See Shawna).
                         </div>
                         ${fdohContactInfo}
                    `
                },
                chlamydia_rec: {
                    title: "Chlamydia Treatment (Pregnant)",
                    type: 'recommendation',
                    parentRef: '"Chlamydial Infections > Special Considerations > Pregnancy" (page 68)',
                    content: `
                        <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                        <p class="drug-details"><strong>Azithromycin 1 g orally in a single dose</strong></p>
                        <h3>Alternative Regimen:</h3>
                        <p class="drug-details">Amoxicillin 500 mg orally 3 times/day for 7 days</p>
                        <h3>Notes:</h3>
                        <ul>
                            <li>Doxycycline is contraindicated in 2nd/3rd trimesters. Levofloxacin has limited data/potential risks. Erythromycin not recommended (GI side effects/adverse outcomes).</li>
                            <li><strong>Test of cure</strong> (NAAT) ~4 weeks after treatment is recommended.</li>
                            <li>Retest 3 months after treatment.</li>
                        </ul>
                         <div class="fmc-note">
                            <strong>FMC Reporting Protocol:</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                        </div>
                         ${fdohContactInfo}
                    `
                },
                 gonorrhea_rec: {
                    title: "Gonorrhea Treatment (Pregnant)",
                    type: 'recommendation',
                    parentRef: '"Gonococcal Infections > Special Considerations > Pregnancy" (page 76)',
                    content: `
                        <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                        <p class="drug-details"><strong>Ceftriaxone 500 mg IM in a single dose</strong> (regardless of weight per FMC)</p>
                        <!-- CDC recommends 1g if >=150kg, but FMC doc says 500mg regardless of weight for pregnancy -->
                        <p class="mt-2">PLUS, if Chlamydia infection has not been excluded:</p>
                        <p class="drug-details"><strong>Azithromycin 1 g orally in a single dose</strong></p>
                        <h3>Notes:</h3>
                        <ul>
                            <li>If cephalosporin allergy, consult specialist. Gentamicin cautioned (fetal risks). FMC: Refer to health department for Gentamicin + Azithromycin.</li>
                            <li>Test of cure NOT needed for uncomplicated urogenital/rectal. IS needed for pharyngeal (7-14 days post-treatment).</li>
                            <li>Retest 3 months after treatment.</li>
                        </ul>
                         <div class="fmc-note">
                            <strong>FMC Reporting Protocol:</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                         </div>
                         ${fdohContactInfo}
                    `
                },
                syphilis_start: {
                    title: "Syphilis Diagnosis (Pregnant): Penicillin Allergy?",
                    type: 'question',
                    options: [
                        { text: "No Penicillin Allergy", nextStep: 'syphilis_no_allergy' },
                        { text: "Penicillin Allergy Reported", nextStep: 'syphilis_allergy' }
                    ]
                },
                 syphilis_allergy: {
                    title: "Syphilis Treatment (Pregnant) - PENICILLIN ALLERGY",
                    type: 'recommendation',
                    parentRef: '"Syphilis During Pregnancy > Special Considerations > Penicillin Allergy" (page 51) & FMC Protocol',
                     content: `
                        <p class="text-red-600 font-bold">Parenteral Penicillin G is the ONLY known effective therapy during pregnancy.</p>
                        <ul>
                            <li>Patient MUST be desensitized and treated with Penicillin G.</li>
                            <li>No proven alternatives exist. Doxy/Tetra avoided in 2nd/3rd tri; Erythro/Azithro ineffective for fetus; Ceftriaxone data insufficient.</li>
                            <li>Skin testing or graded challenge may help assess allergy risk prior to desensitization. Consult specialist.</li>
                         </ul>
                         <div class="fmc-note">
                            <strong>FMC Protocol (Allergy):</strong> Refer to health department for management.
                        </div>
                         ${fdohContactInfo}
                         <p class="mt-4">Once desensitized (if not referred), treat with Penicillin regimen appropriate for stage (see 'No Penicillin Allergy' path).</p>

                    `
                 },
                 syphilis_no_allergy: {
                     title: "Syphilis Treatment (Pregnant) - No Allergy",
                    type: 'recommendation',
                    parentRef: '"Syphilis During Pregnancy" (page 49) & FMC Protocol',
                    content: `
                        <h3>General Principle / <span class="first-line">Recommended (First-Line) Therapy:</span></h3>
                        <p>Treat with the Parenteral Penicillin G regimen appropriate for the stage of infection.</p>
                         <h4>FMC Recommended Dosing:</h4>
                        <ul>
                             <li class="drug-details"><strong>Primary, Secondary, Early Latent:</strong> Benzathine Penicillin G 2.4 million units IM in a single dose, AND repeat dose in one week.</li>
                             <li class="drug-details"><strong>Unknown Duration or Late Latent:</strong> Benzathine Penicillin G 2.4 million units IM weekly for 3 doses (total 7.2 million units).</li>
                        </ul>
                         <p class="text-xs italic">(Note: CDC guidelines suggest *considering* a second dose for early stages, while FMC protocol specifies it.)</p>
                        <h3>Specific CDC Considerations:</h3>
                        <ul>
                            <li><strong>Diagnosis in 2nd Half of Pregnancy:</strong> Include sonographic fetal evaluation (but don't delay therapy). Sonographic signs of fetal syphilis may indicate higher risk for fetal treatment failure; consult specialist. A second Penicillin dose may be beneficial (aligns with FMC approach for early stages).</li>
                            <li><strong>Jarisch-Herxheimer Reaction:</strong> Risk of premature labor/fetal distress. Advise patient to seek obstetric care if fever, contractions, or decreased fetal movement occur post-treatment. Do not delay necessary treatment.</li>
                             <li><strong>Dosing Intervals (Late Latent):</strong> Intervals >9 days between weekly doses are NOT acceptable. Repeat the full course if a dose is missed by >9 days. Optimal interval is 7 days.</li>
                            <li><strong>Follow-up Titers:</strong> Check at least at delivery. Details depend on timing of treatment (see guidelines). Most women won't achieve 4-fold decrease before delivery (not failure). A sustained (>2 weeks) 4-fold RISE post-treatment suggests reinfection/failure.</li>
                        </ul>
                        <div class="fmc-note">
                            <strong>FMC Reporting Protocol:</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                         </div>
                         ${fdohContactInfo}
                    `
                 },
                 trich_rec: {
                    title: "Trichomoniasis Treatment (Pregnant)",
                    type: 'recommendation',
                    parentRef: '"Trichomoniasis > Special Considerations > Pregnancy" (page 90)',
                    content: `
                        <h3><span class="first-line">Recommended (First-Line) Regimen (Symptomatic Women):</span></h3>
                        <p class="drug-details"><strong>Metronidazole 500 mg orally 2 times/day for 7 days</strong></p>
                        <h3>Alternative Regimen:</h3>
                        <p class="drug-details">Metronidazole 2 g orally in a single dose</p>
                        <h3>Notes:</h3>
                        <ul>
                            <li>Treat symptomatic women regardless of stage. Metronidazole poses low risk. Tinidazole should be avoided.</li>
                            <li>Routine screening of asymptomatic women not established.</li>
                            <li>Retest within 3 months of treatment.</li>
                            <li>Metronidazole compatible with breastfeeding (low dose regimen); defer 12-24h after 2g dose sometimes advised.</li>
                        </ul>
                    `
                 },
                 bv_rec: {
                    title: "Bacterial Vaginosis (BV) Treatment (Pregnant)",
                    type: 'recommendation',
                     parentRef: '"Bacterial Vaginosis > Special Considerations > Pregnancy" (page 86)',
                     content: `
                         <h3><span class="first-line">Recommended (First-Line) Regimens (Treat symptomatic women):</span></h3>
                         <ul>
                            <li class="drug-details"><strong>Metronidazole 500 mg orally 2 times/day for 7 days</strong></li>
                            <li class="drug-details">OR <strong>Metronidazole 250 mg orally 3 times/day for 7 days</strong></li>
                            <li class="drug-details">OR <strong>Clindamycin 300 mg orally 2 times/day for 7 days</strong></li>
                         </ul>
                         <h3>Alternative Regimens:</h3>
                         <ul>
                            <li class="drug-details">Metronidazole gel 0.75%, one applicator (5 g) intravaginally, once daily for 5 days</li>
                            <li class="drug-details">OR Clindamycin cream 2%, one applicator (5 g) intravaginally at bedtime for 7 days</li>
                            <li class="drug-details">OR Clindamycin ovules 100 mg intravaginally once at bedtime for 3 days*</li>
                         </ul>
                         <p class="text-xs">*Topical clindamycin may weaken latex/rubber.</p>
                         <h3>Notes:</h3>
                         <ul>
                            <li>Routine screening/treatment of asymptomatic women NOT recommended.</li>
                             <li>Metronidazole poses low risk. Tinidazole should be avoided. Insufficient data for secnidazole/other newer regimens.</li>
                            <li>Follow-up unnecessary if symptoms resolve.</li>
                        </ul>
                     `
                 },
                hsv_start: {
                     title: "Genital Herpes (HSV) in Pregnancy: Scenario?",
                     type: 'question',
                     options: [
                         { text: "Management Principles / Prevention", nextStep: 'hsv_principles' },
                         { text: "Suppressive Therapy (Starting 36 weeks)", nextStep: 'hsv_suppression' },
                         { text: "Labor & Delivery Management", nextStep: 'hsv_delivery' },
                         { text: "Treatment of Outbreaks During Pregnancy", nextStep: 'hsv_outbreak_preg' },
                     ]
                },
                hsv_principles: {
                    title: "HSV Management Principles/Prevention (Pregnant)",
                    type: 'recommendation',
                    parentRef: '"Genital Herpes > Special Considerations > Genital Herpes During Pregnancy" (page 35)',
                    content: `
                        <h3>General Principles:</h3>
                        <ul>
                            <li>Goal: Prevent neonatal herpes (prevent acquisition late pregnancy, avoid exposure at delivery).</li>
                            <li>High transmission risk (30-50%) if acquired near delivery; Low (<1%) if history of recurrence or acquired early pregnancy.</li>
                        </ul>
                         <h3>Screening & Prevention:</h3>
                         <ul>
                            <li>Ask all about history. Routine serologic screening NOT recommended.</li>
                            <li>Counsel uninfected women to avoid vaginal/oral sex in 3rd trimester with partners known/suspected to have genital/oral herpes.</li>
                        </ul>
                    `
                },
                hsv_suppression: {
                    title: "HSV Suppressive Therapy (Pregnant - Starting 36 weeks)",
                    type: 'recommendation',
                    parentRef: '"Genital Herpes > Special Considerations > Genital Herpes During Pregnancy" (page 36)',
                    content: `
                        <p>Recommended starting at 36 weeks gestation for women with a <strong>history of recurrent genital herpes</strong> to reduce recurrence at term and decrease C-section frequency.</p>
                        <h3><span class="first-line">Recommended (First-Line) Regimens:</span></h3>
                        <ul>
                            <li class="drug-details"><strong>Acyclovir 400 mg orally 3 times/day</strong></li>
                            <li class="drug-details">OR <strong>Valacyclovir 500 mg orally 2 times/day</strong></li>
                        </ul>
                        <p>Note: Does NOT eliminate risk of neonatal transmission. Not recommended for asymptomatic women without history of outbreaks.</p>
                     `
                },
                 hsv_delivery: {
                    title: "HSV Management at Labor & Delivery",
                    type: 'recommendation',
                    parentRef: '"Genital Herpes > Special Considerations > Genital Herpes During Pregnancy" (page 35)',
                    content: `
                        <ul>
                             <li>At labor onset, carefully question about prodromal symptoms and examine for lesions.</li>
                             <li>Women WITHOUT symptoms/lesions can deliver vaginally.</li>
                             <li>Women WITH active recurrent lesions or prodrome at labor onset should have Cesarean delivery.</li>
                        </ul>
                    `
                 },
                 hsv_outbreak_preg: {
                     title: "HSV Outbreak Treatment During Pregnancy",
                     type: 'recommendation',
                     parentRef: '"Genital Herpes > Special Considerations > Genital Herpes During Pregnancy" (page 36)',
                     content: `
                         <p>Treat first-episode or recurrent outbreaks during pregnancy with standard oral antiviral regimens. Duration may need extension.</p>
                         <p><strong><span class="first-line">Recommended (First-Line) Regimens (Example based on non-pregnant first episode):</span></strong></p>
                         <ul>
                             <li class="drug-details"><strong>Acyclovir 400 mg orally 3 times/day for 7-10 days</strong></li>
                             <li class="drug-details">OR <strong>Valacyclovir 1 g orally 2 times/day for 7-10 days</strong></li>
                             <li class="drug-details">OR <strong>Famciclovir 250 mg orally 3 times/day for 7-10 days</strong></li>
                         </ul>
                         <p>Severe disease requires IV Acyclovir (5-10 mg/kg body weight IV every 8 hours).</p>
                     `
                 },
                 // Add more pregnant conditions as needed
            },
            // --- FEMALE (NON-PREGNANT) ---
             female_not_pregnant: {
                 start: {
                     title: "Select Clinical Scenario (Female, Not Pregnant)",
                     type: 'question',
                     options: [
                        { text: "Routine Screening", nextStep: 'screening_general' },
                        { text: "Cervicitis Signs/Symptoms", nextStep: 'cervicitis_start' },
                        { text: "Vaginal Discharge / Itching / Odor", nextStep: 'vaginal_discharge_eval' },
                        { text: "Genital Ulcers", nextStep: 'genital_ulcers_eval' },
                        { text: "Pelvic/Lower Abdominal Pain (Suspect PID)", nextStep: 'pid_start' },
                        { text: "Chlamydia Diagnosis", nextStep: 'chlamydia_rec' },
                        { text: "Gonorrhea Diagnosis", nextStep: 'gonorrhea_start' }, // Needs branching for site
                        { text: "Syphilis Diagnosis", nextStep: 'syphilis_start' }, // Needs branching for stage
                        { text: "Trichomoniasis Diagnosis", nextStep: 'trich_rec' },
                        { text: "Bacterial Vaginosis (BV) Diagnosis", nextStep: 'bv_rec' },
                        { text: "Vulvovaginal Candidiasis (VVC) Diagnosis", nextStep: 'vvc_start' }, // Needs branching
                        { text: "Genital Herpes (HSV) Diagnosis/Management", nextStep: 'hsv_start' }, // Needs branching
                     ]
                },
                screening_general: { // Keep as recommendation for now
                     title: "STI Screening Summary (Non-Pregnant Females)",
                     type: 'recommendation',
                     parentRef: 'Various sections, consolidated',
                     content: `
                        <h3>Routine Screening Recommendations:</h3>
                        <ul>
                            <li><strong>Chlamydia & Gonorrhea:</strong> Annually if sexually active & <25 yrs. Screen ≥25 yrs if increased risk*. Consider extragenital testing based on exposure/risk.</li>
                            <li><strong>HIV:</strong> At least once (15-65 yrs). More if risk*. Assess PrEP.</li>
                            <li><strong>Syphilis:</strong> Screen if increased risk*.</li>
                             <li><strong>Hepatitis C (HCV):</strong> At least once if ≥18 yrs. Periodically if ongoing risk*.</li>
                            <li><strong>Hepatitis B (HBV):</strong> Screen if risk* and unvaccinated. Vaccinate if susceptible.</li>
                            <li><strong>Trichomonas:</strong> Consider in high prevalence/risk* settings. Screen women with HIV annually.</li>
                            <li><strong>Cervical Cancer:</strong> Follow USPSTF/ACOG/ACS guidelines (start 21/25 yrs).</li>
                             <li><strong>HSV/BV:</strong> Routine screening NOT recommended if asymptomatic.</li>
                         </ul>
                         <p class="text-xs">*Increased risk factors vary but often include: new/multiple partners, partner with STI/multiple partners, inconsistent condoms, history of STI, transactional sex, substance use, incarceration.</p>
                          <div class="fmc-note">
                             <strong>FMC HIV Reporting Protocol:</strong> Report positive HIV results to patient & health department. Notify triage. Complete Practitioner Disease Report Form within 2 weeks, secure in double envelope marked confidential, mail certified (See Shawna).
                         </div>
                         ${fdohContactInfo}
                    `
                },
                cervicitis_start: { // Keep as recommendation for now
                    title: "Cervicitis Management",
                    type: 'recommendation',
                    parentRef: '"Cervicitis" (page 63)',
                    content: `
                         <h3>Diagnosis & Evaluation:</h3>
                        <p>Signs: Mucopurulent exudate or easily induced endocervical bleeding. Often asymptomatic. Assess for PID. Test for GC/CT (NAAT). Evaluate for BV/Trichomonas (NAAT if wet mount neg but symptomatic). Consider M. genitalium testing.</p>
                        <h3>Treatment Decision:</h3>
                         <ul>
                            <li><strong>Presume & Treat (GC/CT):</strong> If increased risk* and follow-up uncertain/NAAT unavailable.</li>
                            <li><strong>Defer & Treat based on results:</strong> If lower risk*.</li>
                         </ul>
                         <p class="text-xs">*Increased risk: <25 yrs, new/>1 partner, partner w/ STI/multiple partners.</p>
                         <h3><span class="first-line">Recommended (First-Line) Regimen (Empiric or CT+):</span></h3>
                         <p class="drug-details"><strong>Doxycycline 100 mg orally 2 times/day for 7 days</strong></p>
                         <p>(Consider concurrent treatment for gonorrhea if patient is at risk or local prevalence is high - see Gonorrhea guidelines).</p>
                         <h3>Alternative:</h3>
                         <p class="drug-details">Azithromycin 1 g orally in a single dose</p>
                         <h3>Follow-Up:</h3>
                         <p>Ensure resolution. Retest GC/CT/Trich at 3 months. Persistent cervicitis: Re-eval, consider M. genitalium, refer if needed.</p>
                         <p>Test for HIV/Syphilis. Treat partners. Abstain from sex until treated.</p>
                     `
                 },
                 vaginal_discharge_eval: { // Keep as recommendation for now
                     title: "Vaginal Discharge Evaluation Summary",
                     type: 'recommendation',
                     parentRef: '"Diseases Characterized by Vulvovaginal Itching, Burning, Irritation, Odor, or Discharge" (page 82)',
                     content: `
                        <h3>Initial Office Evaluation:</h3>
                        <ul>
                            <li>History, Exam, Vaginal pH</li>
                            <li>Wet Mount (Saline): Look for clue cells (BV), motile trichomonads, WBCs.</li>
                            <li>KOH Prep: Whiff test (amine odor -> BV/Trich), look for yeast/hyphae (VVC).</li>
                         </ul>
                         <h3>If Office Tests Suggestive:</h3> Treat accordingly (see specific condition guides).
                         <h3>If Office Tests Negative/Uncertain/Unavailable OR for Confirmation:</h3>
                         <ul>
                             <li><strong>Trichomonas:</strong> NAAT (preferred), culture, rapid antigen.</li>
                             <li><strong>BV:</strong> Amsel criteria, Gram stain (Nugent), molecular tests (NAATs).</li>
                             <li><strong>VVC:</strong> Yeast culture (esp. if microscopy neg or complicated/recurrent), molecular tests.</li>
                             <li><strong>Cervicitis:</strong> Consider GC/CT NAAT if cervicitis suspected.</li>
                         </ul>
                         <p>Treat identified cause. Refer persistent cases without diagnosis.</p>
                     `
                 },
                 genital_ulcers_eval: { // Keep as recommendation for now
                     title: "Genital Ulcer Evaluation Summary",
                     type: 'recommendation',
                     parentRef: '"Diseases Characterized by Genital, Anal, or Perianal Ulcers" (page 27)',
                     content: `
                         <h3>Recommended Evaluation:</h3>
                         <ul>
                            <li><strong>Syphilis:</strong> Serology (non-trep & trep). Lesion test (Darkfield/PCR if available).</li>
                            <li><strong>HSV:</strong> PCR (preferred) or culture from lesion. Type-specific serology may aid if tests neg/no lesion.</li>
                            <li><strong>HIV Testing.</strong></li>
                            <li><strong>Consider Chancroid, LGV, Donovanosis</strong> based on presentation/epidemiology.</li>
                         </ul>
                         <h3>Presumptive Treatment (After collecting tests):</h3>
                         <ul>
                             <li><span class="first-line">Treat for Syphilis if suspected (esp. MSM, high prevalence):</span> Benzathine Penicillin G 2.4 million units IM in a single dose.</li>
                             <li><span class="first-line">Treat for first-episode HSV if suspected (vesicular):</span> e.g., Acyclovir 400 mg PO TID or Valacyclovir 1g PO BID or Famciclovir 250mg PO TID (all for 7-10 days).</li>
                         </ul>
                          <div class="fmc-note">
                             <strong>FMC HIV Reporting Protocol:</strong> Report positive HIV results to patient & health department. Notify triage. Complete Practitioner Disease Report Form within 2 weeks, secure in double envelope marked confidential, mail certified (See Shawna).
                         </div>
                         ${fdohContactInfo}
                     `
                 },
                 pid_start: { // Keep as recommendation for now
                    title: "Pelvic Inflammatory Disease (PID) Summary",
                     type: 'recommendation',
                     parentRef: '"Pelvic Inflammatory Disease" (page 94)',
                    content: `
                         <h3>Diagnosis:</h3> <p>Low threshold. Presume & treat if pelvic/lower abd pain, no other cause, AND ≥1 minimum criterion (CMT, uterine, or adnexal tenderness).</p>
                         <h3>Hospitalize If:</h3> <p>Surgical emergency possible, TOA, pregnant, severe illness/intolerance to PO, no response to outpatient Rx.</p>
                         <h3><span class="first-line">Recommended (First-Line) Treatment Regimens (Empiric, MUST cover GC/CT + Anaerobes):</span></h3>
                         <h4>Parenteral Option 1:</h4>
                         <p class="drug-details"><strong>Ceftriaxone 1 g IV every 24 hours</strong></p>
                         <p class="drug-details">PLUS <strong>Doxycycline 100 mg orally or IV every 12 hours</strong></p>
                         <p class="drug-details">PLUS <strong>Metronidazole 500 mg orally or IV every 12 hours</strong></p>
                         <h4>Parenteral Option 2:</h4>
                         <p class="drug-details"><strong>Cefotetan 2 g IV every 12 hours</strong></p>
                         <p class="drug-details">PLUS <strong>Doxycycline 100 mg orally or IV every 12 hours</strong></p>
                         <h4>Parenteral Option 3:</h4>
                         <p class="drug-details"><strong>Cefoxitin 2 g IV every 6 hours</strong></p>
                         <p class="drug-details">PLUS <strong>Doxycycline 100 mg orally or IV every 12 hours</strong></p>
                         <p class="mt-2">Transition to oral Doxycycline 100mg BID + Metronidazole 500mg BID after clinical improvement to complete 14 days total therapy.</p>
                         <h4>IM/Oral Option (Mild-Moderate PID):</h4>
                         <p class="drug-details"><strong>Ceftriaxone 500 mg IM in a single dose*</strong> (or Cefoxitin 2 g IM + Probenecid 1 g PO x1)</p>
                         <p class="drug-details">PLUS <strong>Doxycycline 100 mg orally 2 times/day for 14 days</strong></p>
                         <p class="drug-details">WITH <strong>Metronidazole 500 mg orally 2 times/day for 14 days</strong></p>
                         <p class="text-xs">(*Use 1g Ceftriaxone if ≥150 kg).</p>
                         <h3>Follow-Up:</h3> <p>Improvement expected in <72h. Retest GC/CT at 3 months. Test HIV/Syphilis. Treat partners (EPT option). Abstain sex.</p>
                     `
                 },
                 chlamydia_rec: { // Same as pregnant rec
                    title: "Chlamydia Treatment (Non-Pregnant)",
                    type: 'recommendation',
                    parentRef: '"Chlamydial Infections" (page 66)',
                    content: `
                        <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                        <p class="drug-details"><strong>Doxycycline 100 mg orally 2 times/day for 7 days</strong></p>
                        <h3>Alternative Regimens:</h3>
                         <p class="drug-details">Azithromycin 1 g orally in a single dose</p>
                         <p class="drug-details">OR Levofloxacin 500 mg orally once daily for 7 days</p>
                         <h3>Notes:</h3>
                         <ul>
                             <li>Doxycycline preferred (higher efficacy vs Azithro, esp. rectal/pharyngeal).</li>
                             <li>Azithro alternative if adherence concern, consider test of cure if rectal infection possible.</li>
                             <li>Abstain sex 7 days post single dose or after 7-day regimen & until partners treated.</li>
                             <li>Test of cure NOT routine. Retest at 3 months (reinfection common).</li>
                             <li>Treat partners (EPT option). Test HIV/GC/Syphilis.</li>
                         </ul>
                          <div class="fmc-note">
                            <strong>FMC Reporting Protocol:</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well. Document reason if alternative therapy used.
                         </div>
                         ${fdohContactInfo}
                     `
                 },
                gonorrhea_start: {
                    title: "Gonorrhea Diagnosis: Site(s) of Infection?",
                     type: 'question',
                     options: [
                         { text: "Cervix / Urethra / Rectum ONLY", nextStep: 'gonorrhea_genrec' },
                         { text: "Pharynx Involved (+/- Other Sites)", nextStep: 'gonorrhea_pharynx' }
                     ]
                },
                gonorrhea_genrec: {
                     title: "Gonorrhea Treatment (Cervix/Urethra/Rectum)",
                     type: 'recommendation',
                     parentRef: '"Uncomplicated Gonococcal Infection of the Cervix, Urethra, or Rectum" (page 73) & FMC Protocol',
                     content: `
                        <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                        <p class="drug-details"><strong>Ceftriaxone 500 mg IM in a single dose</strong> (if patient weight <150 kg)</p>
                        <p class="drug-details">OR <strong>Ceftriaxone 1 g IM in a single dose</strong> (if patient weight ≥150 kg)</p>
                        <p class="mt-2">PLUS (if Chlamydia infection has not been excluded):</p>
                        <p class="drug-details"><strong>Doxycycline 100 mg orally 2 times/day for 7 days</strong></p>
                         <h3>Alternative (If Ceftriaxone unavailable/not feasible per FMC):</h3>
                         <p class="drug-details">Cefixime 800mg orally in a single dose</p>
                         <p>(Add Doxycycline 100mg BID x 7d if Chlamydia not excluded).</p>
                         <h3>Alternative (If Cephalosporin Allergy per FMC):</h3>
                         <p>Refer to health department for: Gentamicin 240mg IM in a single dose PLUS Azithromycin 2 g orally in a single dose.</p>
                         <h3>Notes (CDC):</h3>
                         <p>Test of cure NOT needed. Retest at 3 months. Treat partners (EPT option). Abstain sex 7 days. Test HIV/CT/Syphilis.</p>
                         <div class="fmc-note">
                            <strong>FMC Reporting Protocol:</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                         </div>
                         ${fdohContactInfo}
                     `
                },
                 gonorrhea_pharynx: {
                     title: "Gonorrhea Treatment (Pharynx Involved)",
                     type: 'recommendation',
                     parentRef: '"Uncomplicated Gonococcal Infection of the Pharynx" (page 74) & FMC Protocol',
                     content: `
                        <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                        <p class="drug-details"><strong>Ceftriaxone 500 mg IM in a single dose</strong> (if patient weight <150 kg)</p>
                        <p class="drug-details">OR <strong>Ceftriaxone 1 g IM in a single dose</strong> (if patient weight ≥150 kg)</p>
                         <p class="mt-2">PLUS (if Chlamydia infection not excluded or identified):</p>
                         <p class="drug-details"><strong>Doxycycline 100 mg orally 2 times/day for 7 days</strong></p>
                         <h3>Alternative (If Cephalosporin Allergy per FMC):</h3>
                         <p>Refer to health department for: Gentamicin 240mg IM in a single dose PLUS Azithromycin 2 g orally in a single dose.</p>
                         <h3>Notes (CDC):</h3>
                         <p><strong>Test of cure IS needed</strong> (7-14 days post-treatment, culture if NAAT+). Retest at 3 months. Treat partners (EPT option). Abstain sex 7 days. Test HIV/CT/Syphilis.</p>
                         <div class="fmc-note">
                             <strong>FMC Reporting Protocol:</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                         </div>
                         ${fdohContactInfo}
                     `
                 },
                syphilis_start: { // Needs more branching logic based on stage and allergy
                    title: "Syphilis Treatment Summary",
                    type: 'recommendation', // Simplified for now
                    parentRef: '"Syphilis" sections (page 39+) & FMC Protocol',
                    content: `
                        <p>Treatment depends on stage (Primary, Secondary, Early Latent, Late Latent/Unknown, Tertiary, Neurosyphilis) and Penicillin allergy status.</p>
                         <p><span class="first-line">Recommended (First-Line) Therapy is PENICILLIN G.</span> Dosage/route/duration depend on stage.</p>
                         <h4>FMC Recommended Dosing (Adults):</h4>
                        <ul>
                             <li class="drug-details"><strong>Primary, Secondary, Early Latent:</strong> Benzathine Penicillin G 2.4 million units IM in a single dose.</li>
                             <li class="drug-details"><strong>Unknown Duration or Late Latent:</strong> Benzathine Penicillin G 2.4 million units IM weekly for 3 doses (total 7.2 million units).</li>
                             <li class="drug-details"><strong>Neurosyphilis / Ocular / Otosyphilis:</strong> (Not specified in FMC, use CDC) Aqueous Crystalline Penicillin G IV for 10-14 days.</li>
                        </ul>
                         <p><strong>Penicillin Allergy (FMC Protocol):</strong> Refer to health department for management.</p>
                         <p><strong>Penicillin Allergy (CDC):</strong> Doxycycline is often alternative for early/late latent, but duration varies. Desensitization required for Neuro/Ocular/Otic syphilis and preferred if compliance/follow-up uncertain for other stages.</p>
                         <p>Follow-up (CDC) requires serial quantitative non-treponemal tests (RPR/VDRL) at specific intervals. Consult full guidelines for detailed staging, treatment, allergy management, and follow-up schedules.</p>
                         <p>Test for HIV (CDC). Treat partners based on stage/timing (CDC).</p>
                        <div class="fmc-note">
                            <strong>FMC Reporting Protocol:</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                         </div>
                         ${fdohContactInfo}
                    `
                },
                 trich_rec: { // Same as pregnant rec
                    title: "Trichomoniasis Treatment (Non-Pregnant Females)",
                    type: 'recommendation',
                     parentRef: '"Trichomoniasis" (page 89)',
                    content: `
                        <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                        <p class="drug-details"><strong>Metronidazole 500 mg orally 2 times/day for 7 days</strong></p>
                        <h3>Alternative Regimens:</h3>
                        <p class="drug-details">Tinidazole 2 g orally in a single dose</p>
                        <p class="drug-details">OR Metronidazole 2 g orally in a single dose (Likely less effective)</p>
                        <h3>Notes:</h3>
                        <p>7-day Metronidazole preferred over single dose. Tinidazole equivalent/superior to single dose Metro. Abstain sex until treated. Retest at 3 months. Treat partners (EPT option). Manage resistance per guidelines.</p>
                        <p>Test HIV/other STIs.</p>
                    `
                 },
                 bv_rec: { // Same as pregnant rec
                     title: "Bacterial Vaginosis (BV) Treatment (Non-Pregnant)",
                     type: 'recommendation',
                     parentRef: '"Bacterial Vaginosis" (page 84)',
                     content: `
                        <h3><span class="first-line">Recommended (First-Line) Regimens (Symptomatic women):</span></h3>
                         <ul>
                            <li class="drug-details"><strong>Metronidazole 500 mg orally 2 times/day for 7 days</strong></li>
                            <li class="drug-details">OR <strong>Metronidazole gel 0.75%, one applicator (5 g) intravaginally, once daily for 5 days</strong></li>
                            <li class="drug-details">OR <strong>Clindamycin cream 2%, one applicator (5 g) intravaginally at bedtime for 7 days</strong></li>
                         </ul>
                        <h3>Alternative Regimens:</h3>
                         <ul>
                            <li class="drug-details">Clindamycin 300 mg orally 2 times/day for 7 days</li>
                            <li class="drug-details">OR Clindamycin ovules 100 mg intravaginally once at bedtime for 3 days*</li>
                             <li class="drug-details">OR Secnidazole 2 g oral granules in a single dose†</li>
                            <li class="drug-details">OR Tinidazole 2 g orally once daily for 2 days</li>
                            <li class="drug-details">OR Tinidazole 1 g orally once daily for 5 days</li>
                        </ul>
                        <p class="text-xs">*†Topical clindamycin/secnidazole notes apply (latex/food). </p>
                        <h3>Notes:</h3>
                         <p>Treat symptomatic only. Follow-up unneeded if resolved. Manage recurrence per guidelines. Partner treatment NOT recommended. Test HIV/other STIs.</p>
                    `
                 },
                 vvc_start: { // Needs branching logic based on classification
                     title: "Vulvovaginal Candidiasis (VVC) Treatment Summary",
                     type: 'recommendation', // Simplified for now
                     parentRef: '"Vulvovaginal Candidiasis" (page 91)',
                     content: `
                        <p>Treatment depends on classification (Uncomplicated vs Complicated - Recurrent, Severe, Non-albicans, Compromised Host).</p>
                         <p><span class="first-line">Recommended (First-Line) for Uncomplicated:</span></p>
                        <ul>
                             <li><strong>Topical Azoles (1-3 days):</strong> e.g., Clotrimazole 2% cream x3d, Miconazole 4% cream x3d, Miconazole 200mg supp x3d, Miconazole 1200mg supp x1, Tioconazole 6.5% ointment x1, Butoconazole 2% cream x1, Terconazole 0.8% cream x3d, Terconazole 80mg supp x3d.</li>
                             <li class="drug-details">OR <strong>Fluconazole 150 mg orally in a single dose</strong>.</li>
                        </ul>
                         <p><strong>Complicated:</strong> Requires longer initial therapy +/- maintenance (e.g., weekly Fluconazole for RVVC). Consult guidelines.</p>
                         <p>Diagnosis: Symptoms + Microscopy (KOH/Saline) or Culture. Culture if complicated/microscopy negative. Partner tx generally not needed.</p>
                     `
                 },
                hsv_start: { // Needs more branching logic based on episode type
                    title: "Genital Herpes (HSV) Treatment Summary",
                    type: 'recommendation', // Simplified for now
                    parentRef: '"Genital Herpes" (page 31)',
                    content: `
                         <p>Treatment differs for First Episode vs Recurrent (Episodic vs Suppressive).</p>
                         <p><span class="first-line">Recommended (First-Line) Antivirals:</span> Acyclovir, Valacyclovir, Famciclovir.</p>
                         <h4>First Episode:</h4>
                         <ul>
                            <li class="drug-details"><strong>Acyclovir 400 mg orally 3 times/day for 7-10 days</strong></li>
                            <li class="drug-details">OR <strong>Famciclovir 250 mg orally 3 times/day for 7-10 days</strong></li>
                            <li class="drug-details">OR <strong>Valacyclovir 1 g orally 2 times/day for 7-10 days</strong></li>
                         </ul>
                         <h4>Recurrent (Episodic - examples):</h4>
                         <ul>
                            <li class="drug-details">Acyclovir 800 mg PO BID x 5d OR TID x 2d</li>
                            <li class="drug-details">Famciclovir 1 g PO BID x 1d OR 500mg x1 then 250mg BID x 2d OR 125mg BID x 5d</li>
                            <li class="drug-details">Valacyclovir 500 mg PO BID x 3d OR 1 g PO daily x 5d</li>
                         </ul>
                          <h4>Recurrent (Suppressive):</h4>
                         <ul>
                            <li class="drug-details"><strong>Acyclovir 400 mg orally 2 times/day</strong></li>
                            <li class="drug-details">OR <strong>Valacyclovir 500 mg OR 1 g orally once a day</strong></li>
                            <li class="drug-details">OR <strong>Famciclovir 250 mg orally 2 times/day</strong></li>
                         </ul>
                         <p><strong>Severe:</strong> IV Acyclovir (5-10 mg/kg body weight IV every 8 hours).</p>
                         <p>Counseling is key (natural history, shedding, transmission, partner notification, condoms, suppression). Test for HIV.</p>
                     `
                 },
                // Add more female conditions as needed
            },
            // --- MALE ---
             male: {
                 start: {
                     title: "Select Clinical Scenario (Male)",
                     type: 'question',
                     options: [
                        { text: "Routine Screening", nextStep: 'screening_general' },
                        { text: "Urethritis Signs/Symptoms", nextStep: 'urethritis_start' },
                        { text: "Genital/Anal Ulcers", nextStep: 'genital_ulcers_eval' },
                        { text: "Testicular Pain/Swelling (Suspect Epididymitis)", nextStep: 'epididymitis_start' },
                        { text: "Chlamydia Diagnosis", nextStep: 'chlamydia_rec' },
                        { text: "Gonorrhea Diagnosis", nextStep: 'gonorrhea_start' }, // Needs branching for site
                        { text: "Syphilis Diagnosis", nextStep: 'syphilis_start' }, // Needs branching for stage
                        { text: "Trichomoniasis Diagnosis", nextStep: 'trich_rec' },
                        { text: "Genital Herpes (HSV) Diagnosis/Management", nextStep: 'hsv_start' }, // Needs branching
                     ]
                },
                 screening_general: { // Keep as recommendation for now
                     title: "STI Screening Summary (Males)",
                     type: 'recommendation',
                     parentRef: 'Various sections, consolidated',
                     content: `
                        <h3>Routine Screening Recommendations:</h3>
                        <ul>
                             <li><strong>Chlamydia & Gonorrhea (Urethral - Heterosexual Men):</strong> Not routinely recommended if asymptomatic, but consider in high prevalence/risk* settings.</li>
                             <li><strong>Chlamydia & Gonorrhea (All Sites - MSM):</strong> At least annually (Urethral, Rectal, Pharyngeal-GC only) based on exposure. More frequent (q3-6mo) if higher risk*.</li>
                            <li><strong>HIV:</strong> At least once (15-65 yrs). MSM: At least annually, more frequently (q3-6mo) if higher risk*. Assess PrEP.</li>
                             <li><strong>Syphilis:</strong> MSM: At least annually (more frequently, q3-6mo, if higher risk*). Heterosexual men: Screen if increased risk*.</li>
                             <li><strong>Hepatitis C (HCV):</strong> At least once if ≥18 yrs. MSM with HIV: Annually+. Consider for MSM on PrEP based on risk*. Periodically if ongoing risk (e.g., IVDU).</li>
                            <li><strong>Hepatitis B (HBV):</strong> Screen MSM, IVDU, >1 partner, STI eval, partner w/ HBV, HIV+, chronic liver disease if unvaccinated. Vaccinate if susceptible.</li>
                             <li><strong>Trichomonas/HSV:</strong> Routine screening NOT recommended if asymptomatic.</li>
                         </ul>
                         <p class="text-xs">*Increased risk factors vary but often include: new/multiple/anonymous partners, partner w/ STI/multiple partners, inconsistent condoms, history of STI, transactional sex, substance use (esp. meth), incarceration.</p>
                          <div class="fmc-note">
                             <strong>FMC HIV Reporting Protocol:</strong> Report positive HIV results to patient & health department. Notify triage. Complete Practitioner Disease Report Form within 2 weeks, secure in double envelope marked confidential, mail certified (See Shawna).
                         </div>
                         ${fdohContactInfo}
                     `
                },
                 urethritis_start: { // Nested structure for Urethritis
                     title: "Urethritis: Initial Assessment",
                     type: 'question',
                     options: [
                         { text: "Objective Signs of Inflammation Present?", nextStep: 'urethritis_inflammation_present' },
                         { text: "Symptoms ONLY (No Inflammation Signs)", nextStep: 'urethritis_symptoms_only' }
                     ],
                     urethritis_inflammation_present: {
                         title: "Inflammation Present: Microscopy Available?",
                         type: 'question',
                         options: [
                             { text: "Yes, Gram/MB/GV Stain Available", nextStep: 'urethritis_microscopy_available' },
                             { text: "No Microscopy Available", nextStep: 'urethritis_no_microscopy' }
                         ]
                     },
                     urethritis_microscopy_available: {
                         title: "Microscopy Result?",
                         type: 'question',
                         options: [
                             { text: "GNID Present (Presumed Gonorrhea)", nextStep: 'urethritis_gonorrhea_presumed' },
                             { text: "No GNID (≥2 WBC/OIF) (NGU Diagnosed)", nextStep: 'ngu_diagnosed' }
                         ]
                     },
                     urethritis_gonorrhea_presumed: {
                         title: "Presumed Gonorrhea - Treatment",
                         type: 'recommendation',
                         parentRef: '"Urethritis" (page 61) & "Gonococcal Infections" (page 73) & FMC Protocol',
                         content: `
                             <p>Gram stain shows GNID (or purple intracellular diplococci on MB/GV).</p>
                             <h3>Action:</h3>
                             <ul>
                                 <li>Test for Gonorrhea & Chlamydia (NAAT - urine preferred).</li>
                                 <li><strong>Treat presumptively for BOTH Gonorrhea AND Chlamydia</strong> (unless Chlamydia excluded by reliable, rapid NAAT).</li>
                              </ul>
                              <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                               <p class="drug-details"><strong>Ceftriaxone 500 mg IM in a single dose</strong> (if patient weight <150 kg)</p>
                               <p class="drug-details">OR <strong>Ceftriaxone 1 g IM in a single dose</strong> (if patient weight ≥150 kg)</p>
                              <p class="drug-details">PLUS <strong>Doxycycline 100 mg orally 2 times/day for 7 days</strong></p>
                              <p class="mt-2">See full Gonorrhea guidelines & FMC protocol for alternatives.</p>
                              <div class="fmc-note">
                                 <strong>FMC Reporting Protocol:</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                             </div>
                             ${fdohContactInfo}
                         `
                     },
                     ngu_diagnosed: {
                         title: "NGU Diagnosed - Initial Treatment",
                         type: 'recommendation',
                         parentRef: '"Nongonococcal Urethritis" (page 62) & FMC Protocol',
                         content: `
                             <p>Microscopy shows ≥2 WBC/OIF but NO GNID.</p>
                             <h3>Action:</h3>
                             <ul>
                                 <li>Test for Gonorrhea & Chlamydia (NAAT - urine preferred).</li>
                                 <li>Treat presumptively for NGU (covers Chlamydia).</li>
                              </ul>
                             <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                             <p class="drug-details"><strong>Doxycycline 100 mg orally 2 times/day for 7 days</strong></p>
                             <h3>Alternative Regimens:</h3>
                              <p class="drug-details">Azithromycin 1 g orally in a single dose</p>
                              <p class="drug-details">OR Azithromycin 500 mg orally in a single dose; then 250 mg orally daily for 4 days</p>
                              <p class="text-xs text-red-600 mt-1">Note: Doxycycline preferred over Azithromycin due to M. genitalium resistance & potential rectal Chlamydia in partners.</p>
                               <div class="fmc-note">
                                 <strong>FMC Reporting Protocol (Chlamydia):</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well. Document reason if alternative therapy used.
                             </div>
                             ${fdohContactInfo}
                          `
                     },
                     urethritis_no_microscopy: {
                         title: "Inflammation Present / No Microscopy - Treatment",
                         type: 'recommendation',
                         parentRef: '"Urethritis > Diagnostic Considerations" (page 62) & FMC Protocol',
                         content: `
                             <p>Inflammation confirmed by: Discharge on exam OR +LE on urine OR ≥10 WBC/HPF on urine sediment.</p>
                             <h3>Action:</h3>
                             <ul>
                                 <li>Test for Gonorrhea & Chlamydia (NAAT - urine preferred).</li>
                                 <li><strong>Treat presumptively for BOTH Gonorrhea AND Chlamydia.</strong></li>
                              </ul>
                              <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                               <p class="drug-details"><strong>Ceftriaxone 500 mg IM in a single dose</strong> (if patient weight <150 kg)</p>
                               <p class="drug-details">OR <strong>Ceftriaxone 1 g IM in a single dose</strong> (if patient weight ≥150 kg)</p>
                              <p class="drug-details">PLUS <strong>Doxycycline 100 mg orally 2 times/day for 7 days</strong></p>
                               <div class="fmc-note">
                                 <strong>FMC Reporting Protocol (Gonorrhea & Chlamydia):</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                             </div>
                             ${fdohContactInfo}
                         `
                     },
                     urethritis_symptoms_only: {
                         title: "Symptoms Only (No Inflammation): Follow-up Likely?",
                         type: 'question',
                         options: [
                             { text: "Yes, Follow-up Likely", nextStep: 'urethritis_test_symptoms_only' },
                             { text: "No, High Risk / Follow-up Unlikely", nextStep: 'urethritis_treat_symptoms_only' }
                         ]
                     },
                     urethritis_test_symptoms_only: {
                         title: "Symptoms Only / Follow-up Likely - Action",
                         type: 'recommendation',
                         parentRef: '"Urethritis > Diagnostic Considerations" (page 62)',
                         content: `
                             <p>Symptoms reported but no objective signs of urethral inflammation (no discharge, neg LE/microscopy if done).</p>
                             <h3>Action:</h3>
                             <ul>
                                 <li>Perform NAAT for Gonorrhea & Chlamydia (urine preferred).</li>
                                 <li>Treat based ONLY on test results.</li>
                                 <li>Empiric treatment NOT recommended in this scenario if follow-up is likely.</li>
                              </ul>
                          `
                     },
                      urethritis_treat_symptoms_only: {
                         title: "Symptoms Only / High Risk / Follow-up Unlikely - Treatment",
                         type: 'recommendation',
                          parentRef: '"Urethritis > Diagnostic Considerations" (page 62) & FMC Protocol',
                         content: `
                              <p>Symptoms reported but no objective signs of urethral inflammation. Patient at high risk for infection and unlikely to return for results/follow-up.</p>
                              <h3>Action:</h3>
                             <ul>
                                 <li>Perform NAAT for Gonorrhea & Chlamydia (urine preferred), if possible.</li>
                                  <li><strong>Treat presumptively for BOTH Gonorrhea AND Chlamydia.</strong></li>
                              </ul>
                              <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                               <p class="drug-details"><strong>Ceftriaxone 500 mg IM in a single dose</strong> (if patient weight <150 kg)</p>
                               <p class="drug-details">OR <strong>Ceftriaxone 1 g IM in a single dose</strong> (if patient weight ≥150 kg)</p>
                              <p class="drug-details">PLUS <strong>Doxycycline 100 mg orally 2 times/day for 7 days</strong></p>
                               <div class="fmc-note">
                                 <strong>FMC Reporting Protocol (Gonorrhea & Chlamydia):</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                             </div>
                             ${fdohContactInfo}
                          `
                      }
                 }, // End of urethritis nested structure
                genital_ulcers_eval: { // Same as female non-pregnant rec
                     title: "Genital Ulcer Evaluation Summary",
                     type: 'recommendation',
                     parentRef: '"Diseases Characterized by Genital, Anal, or Perianal Ulcers" (page 27)',
                     content: `
                         <h3>Recommended Evaluation:</h3>
                         <ul>
                            <li><strong>Syphilis:</strong> Serology (non-trep & trep). Lesion test (Darkfield/PCR if available).</li>
                            <li><strong>HSV:</strong> PCR (preferred) or culture from lesion. Type-specific serology may aid if tests neg/no lesion.</li>
                            <li><strong>HIV Testing.</strong></li>
                            <li><strong>Consider Chancroid, LGV, Donovanosis</strong> based on presentation/epidemiology.</li>
                         </ul>
                         <h3>Presumptive Treatment (After collecting tests):</h3>
                         <ul>
                              <li><span class="first-line">Treat for Syphilis if suspected (esp. MSM, high prevalence):</span> Benzathine Penicillin G 2.4 million units IM in a single dose.</li>
                              <li><span class="first-line">Treat for first-episode HSV if suspected (vesicular):</span> e.g., Acyclovir 400 mg PO TID or Valacyclovir 1g PO BID or Famciclovir 250mg PO TID (all for 7-10 days).</li>
                         </ul>
                          <div class="fmc-note">
                             <strong>FMC HIV Reporting Protocol:</strong> Report positive HIV results to patient & health department. Notify triage. Complete Practitioner Disease Report Form within 2 weeks, secure in double envelope marked confidential, mail certified (See Shawna).
                         </div>
                         ${fdohContactInfo}
                     `
                 },
                epididymitis_start: { // Nested structure for Epididymitis
                    title: "Epididymitis: Suspected Cause?",
                    type: 'question',
                    options: [
                         { text: "Likely STI (Chlamydia/Gonorrhea)", nextStep: 'epididymitis_sti' },
                         { text: "Likely STI + Enterics (Insertive Anal Sex)", nextStep: 'epididymitis_sti_enteric' },
                         { text: "Likely Enterics ONLY (Low STI risk)", nextStep: 'epididymitis_enteric' }
                    ],
                    epididymitis_sti: {
                         title: "Epididymitis Tx (Likely GC/CT)",
                         type: 'recommendation',
                         parentRef: '"Epididymitis" (page 99) & FMC Protocol',
                         content: `
                             <p>Acute epididymitis most likely caused by Chlamydia or Gonorrhea (e.g., sexually active men <35 yrs, positive STI test, urethritis signs).</p>
                            <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                             <p class="drug-details"><strong>Ceftriaxone 500 mg IM in a single dose</strong> (if patient weight <150 kg)</p>
                             <p class="drug-details">OR <strong>Ceftriaxone 1 g IM in a single dose</strong> (if patient weight ≥150 kg)</p>
                            <p class="drug-details">PLUS <strong>Doxycycline 100 mg orally 2 times/day for 10 days</strong></p>
                            <h3>Management:</h3> <p>Test GC/CT (urine NAAT) + urine culture. Test HIV/Syphilis. Treat partners. Abstain sex. Follow up if no improvement in 72h.</p>
                             <div class="fmc-note">
                                 <strong>FMC Reporting Protocol (Gonorrhea & Chlamydia):</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                             </div>
                             ${fdohContactInfo}
                         `
                     },
                    epididymitis_sti_enteric: {
                         title: "Epididymitis Tx (Likely GC/CT + Enterics)",
                         type: 'recommendation',
                          parentRef: '"Epididymitis" (page 99) & FMC Protocol',
                         content: `
                            <p>Acute epididymitis most likely caused by Chlamydia, Gonorrhea, OR Enteric organisms (e.g., men who practice insertive anal sex).</p>
                             <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                              <p class="drug-details"><strong>Ceftriaxone 500 mg IM in a single dose</strong> (if patient weight <150 kg)</p>
                              <p class="drug-details">OR <strong>Ceftriaxone 1 g IM in a single dose</strong> (if patient weight ≥150 kg)</p>
                             <p class="drug-details">PLUS <strong>Levofloxacin 500 mg orally once daily for 10 days</strong></p>
                             <h3>Management:</h3> <p>Test GC/CT (urine NAAT) + urine culture. Test HIV/Syphilis. Treat partners if STI confirmed/suspected. Abstain sex. Follow up if no improvement in 72h.</p>
                              <div class="fmc-note">
                                 <strong>FMC Reporting Protocol (Gonorrhea & Chlamydia if positive):</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                             </div>
                             ${fdohContactInfo}
                         `
                    },
                    epididymitis_enteric: {
                         title: "Epididymitis Tx (Likely Enterics ONLY)",
                         type: 'recommendation',
                         parentRef: '"Epididymitis" (page 99)',
                         content: `
                            <p>Acute epididymitis most likely caused by Enteric organisms ONLY (e.g., older men, recent urinary tract instrumentation/surgery, known obstruction, confirmed neg GC/CT).</p>
                             <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                             <p class="drug-details"><strong>Levofloxacin 500 mg orally once daily for 10 days</strong></p>
                             <h3>Management:</h3> <p>Confirm GC negative. Base final treatment on urine culture/susceptibility. Test HIV/Syphilis as appropriate. Partner treatment generally not needed unless STI identified. Follow up if no improvement in 72h.</p>
                         `
                    }
                }, // End of epididymitis nested structure
                 chlamydia_rec: { // Same as female non-pregnant rec
                     title: "Chlamydia Treatment",
                    type: 'recommendation',
                    parentRef: '"Chlamydial Infections" (page 66) & FMC Protocol',
                    content: `
                        <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                        <p class="drug-details"><strong>Doxycycline 100 mg orally 2 times/day for 7 days</strong></p>
                        <h3>Alternative Regimens:</h3>
                         <p class="drug-details">Azithromycin 1 g orally in a single dose</p>
                         <p class="drug-details">OR Levofloxacin 500 mg orally once daily for 7 days</p>
                         <h3>Notes:</h3>
                         <ul>
                             <li>Doxycycline preferred (higher efficacy vs Azithro, esp. rectal/pharyngeal).</li>
                             <li>Azithro alternative if adherence concern, consider test of cure if rectal infection diagnosed.</li>
                             <li>Abstain sex 7 days post single dose or after 7-day regimen & until partners treated.</li>
                             <li>Test of cure NOT routine. Retest at 3 months (reinfection common).</li>
                             <li>Treat partners (EPT option; shared decision-making for MSM). Test HIV/GC/Syphilis.</li>
                         </ul>
                          <div class="fmc-note">
                            <strong>FMC Reporting Protocol:</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well. Document reason if alternative therapy used.
                         </div>
                         ${fdohContactInfo}
                     `
                 },
                gonorrhea_start: { // Same as female non-pregnant path
                    title: "Gonorrhea Diagnosis: Site(s) of Infection?",
                     type: 'question',
                     options: [
                         { text: "Urethra / Rectum ONLY", nextStep: 'gonorrhea_genrec' },
                         { text: "Pharynx Involved (+/- Other Sites)", nextStep: 'gonorrhea_pharynx' }
                     ],
                     gonorrhea_genrec: { // Nested within gonorrhea_start
                        title: "Gonorrhea Treatment (Urethra/Rectum)",
                        type: 'recommendation',
                        parentRef: '"Uncomplicated Gonococcal Infection of the Cervix, Urethra, or Rectum" (page 73) & FMC Protocol',
                        content: `
                           <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                            <p class="drug-details"><strong>Ceftriaxone 500 mg IM in a single dose</strong> (if patient weight <150 kg)</p>
                            <p class="drug-details">OR <strong>Ceftriaxone 1 g IM in a single dose</strong> (if patient weight ≥150 kg)</p>
                           <p class="mt-2">PLUS (if Chlamydia infection has not been excluded):</p>
                           <p class="drug-details"><strong>Doxycycline 100 mg orally 2 times/day for 7 days</strong></p>
                            <h3>Alternative (If Ceftriaxone unavailable/not feasible per FMC):</h3>
                            <p class="drug-details">Cefixime 800mg orally in a single dose</p>
                            <p>(Add Doxycycline 100mg BID x 7d if Chlamydia not excluded).</p>
                            <h3>Alternative (If Cephalosporin Allergy per FMC):</h3>
                            <p>Refer to health department for: Gentamicin 240mg IM in a single dose PLUS Azithromycin 2 g orally in a single dose.</p>
                            <h3>Notes (CDC):</h3>
                            <p>Test of cure NOT needed. Retest at 3 months. Treat partners (EPT option; shared decision-making for MSM). Abstain sex 7 days. Test HIV/CT/Syphilis.</p>
                             <div class="fmc-note">
                                <strong>FMC Reporting Protocol:</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                             </div>
                             ${fdohContactInfo}
                        `
                   },
                   gonorrhea_pharynx: { // Nested within gonorrhea_start
                        title: "Gonorrhea Treatment (Pharynx Involved)",
                        type: 'recommendation',
                        parentRef: '"Uncomplicated Gonococcal Infection of the Pharynx" (page 74) & FMC Protocol',
                        content: `
                           <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                            <p class="drug-details"><strong>Ceftriaxone 500 mg IM in a single dose</strong> (if patient weight <150 kg)</p>
                            <p class="drug-details">OR <strong>Ceftriaxone 1 g IM in a single dose</strong> (if patient weight ≥150 kg)</p>
                            <p class="mt-2">PLUS (if Chlamydia infection not excluded or identified):</p>
                            <p class="drug-details"><strong>Doxycycline 100 mg orally 2 times/day for 7 days</strong></p>
                            <h3>Alternative (If Cephalosporin Allergy per FMC):</h3>
                            <p>Refer to health department for: Gentamicin 240mg IM in a single dose PLUS Azithromycin 2 g orally in a single dose.</p>
                            <h3>Notes (CDC):</h3>
                            <p><strong>Test of cure IS needed</strong> (7-14 days post-treatment, culture if NAAT+). Retest at 3 months. Treat partners (EPT option; shared decision-making for MSM). Abstain sex 7 days. Test HIV/CT/Syphilis.</p>
                             <div class="fmc-note">
                                 <strong>FMC Reporting Protocol:</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                             </div>
                             ${fdohContactInfo}
                        `
                    }
                }, // End of gonorrhea nested structure
                syphilis_start: { // Same as female non-pregnant path
                    title: "Syphilis Treatment Summary",
                    type: 'recommendation', // Simplified for now
                    parentRef: '"Syphilis" sections (page 39+) & FMC Protocol',
                    content: `
                        <p>Treatment depends on stage (Primary, Secondary, Early Latent, Late Latent/Unknown, Tertiary, Neurosyphilis) and Penicillin allergy status.</p>
                         <p><span class="first-line">Recommended (First-Line) Therapy is PENICILLIN G.</span> Dosage/route/duration depend on stage.</p>
                         <h4>FMC Recommended Dosing (Adults):</h4>
                        <ul>
                             <li class="drug-details"><strong>Primary, Secondary, Early Latent:</strong> Benzathine Penicillin G 2.4 million units IM in a single dose.</li>
                             <li class="drug-details"><strong>Unknown Duration or Late Latent:</strong> Benzathine Penicillin G 2.4 million units IM weekly for 3 doses (total 7.2 million units).</li>
                             <li class="drug-details"><strong>Neurosyphilis / Ocular / Otosyphilis:</strong> (Not specified in FMC, use CDC) Aqueous Crystalline Penicillin G IV for 10-14 days.</li>
                        </ul>
                         <p><strong>Penicillin Allergy (FMC Protocol):</strong> Refer to health department for management.</p>
                         <p><strong>Penicillin Allergy (CDC):</strong> Doxycycline is often alternative for early/late latent, but duration varies. Desensitization required for Neuro/Ocular/Otic syphilis and preferred if compliance/follow-up uncertain for other stages.</p>
                         <p>Follow-up (CDC) requires serial quantitative non-treponemal tests (RPR/VDRL) at specific intervals. Consult full guidelines for detailed staging, treatment, allergy management, and follow-up schedules.</p>
                         <p>Test for HIV (CDC). Treat partners based on stage/timing (CDC).</p>
                        <div class="fmc-note">
                            <strong>FMC Reporting Protocol:</strong> Must be reported to all patients and the health department upon receipt of the lab report. Notify triage of results as well.
                         </div>
                         ${fdohContactInfo}
                    `
                },
                 trich_rec: { // Mostly same as female non-pregnant rec, adjusted slightly
                     title: "Trichomoniasis Treatment (Males)",
                     type: 'recommendation',
                     parentRef: '"Trichomoniasis" (page 89)',
                    content: `
                         <h3><span class="first-line">Recommended (First-Line) Regimen:</span></h3>
                         <p class="drug-details"><strong>Metronidazole 2 g orally in a single dose</strong></p>
                         <h3>Alternative Regimens:</h3>
                         <p class="drug-details">Tinidazole 2 g orally in a single dose</p>
                        <p>OR (If single dose fails, no re-exposure): Metronidazole 500mg PO BID x 7 days</p>
                        <h3>Notes:</h3>
                         <p>Tinidazole equivalent/superior to single dose Metro. Abstain sex until treated. Retest generally NOT needed for men. Treat partners (EPT option). Manage resistance per guidelines.</p>
                        <p>Test HIV/other STIs.</p>
                     `
                 },
                 hsv_start: { // Same as female non-pregnant path
                    title: "Genital Herpes (HSV) Treatment Summary",
                    type: 'recommendation', // Simplified for now
                    parentRef: '"Genital Herpes" (page 31)',
                     content: `
                         <p>Treatment differs for First Episode vs Recurrent (Episodic vs Suppressive).</p>
                         <p><span class="first-line">Recommended (First-Line) Antivirals:</span> Acyclovir, Valacyclovir, Famciclovir.</p>
                         <h4>First Episode:</h4>
                         <ul>
                             <li class="drug-details"><strong>Acyclovir 400 mg orally 3 times/day for 7-10 days</strong></li>
                             <li class="drug-details">OR <strong>Famciclovir 250 mg orally 3 times/day for 7-10 days</strong></li>
                             <li class="drug-details">OR <strong>Valacyclovir 1 g orally 2 times/day for 7-10 days</strong></li>
                         </ul>
                          <h4>Recurrent (Episodic - examples):</h4>
                         <ul>
                             <li class="drug-details">Acyclovir 800 mg PO BID x 5d OR TID x 2d</li>
                             <li class="drug-details">Famciclovir 1 g PO BID x 1d OR 500mg x1 then 250mg BID x 2d OR 125mg BID x 5d</li>
                             <li class="drug-details">Valacyclovir 500 mg PO BID x 3d OR 1 g PO daily x 5d</li>
                         </ul>
                          <h4>Recurrent (Suppressive):</h4>
                         <ul>
                             <li class="drug-details"><strong>Acyclovir 400 mg orally 2 times/day</strong></li>
                             <li class="drug-details">OR <strong>Valacyclovir 500 mg OR 1 g orally once a day</strong></li>
                             <li class="drug-details">OR <strong>Famciclovir 250 mg orally 2 times/day</strong></li>
                         </ul>
                          <p><strong>Severe:</strong> IV Acyclovir (5-10 mg/kg body weight IV every 8 hours).</p>
                         <p>Counseling is key (natural history, shedding, transmission, partner notification, condoms, suppression). Test for HIV.</p>
                     `
                 },
                 // Add more male conditions as needed
            }
        };

        // Function to display a specific node in the decision tree
         function displayNode(nodeId) {
             const patientType = historyStack[1]; // Patient type is always the second item
             let node = null;
             let parentNode = null; // Keep track of parent for nested structures

             // Check if the nodeId exists directly under the patient type (e.g., 'start', 'screening_general')
             if (guidelines[patientType]?.[nodeId]) {
                 node = guidelines[patientType][nodeId];
             } else if (historyStack.length > 2) {
                 // Try to find it nested under the condition (historyStack[2])
                 const conditionBranch = historyStack[2];
                 if (guidelines[patientType]?.[conditionBranch]?.[nodeId]) {
                     node = guidelines[patientType][conditionBranch][nodeId];
                 } else {
                     // Try to find it nested deeper (e.g., under a sub-question) - requires traversing
                     // For simplicity in this fix, we'll assume max one level of nesting for now.
                     // A more robust solution might require traversing the object.
                     console.warn("Could not find nested node:", nodeId, "under", conditionBranch);
                 }
             }


             // Fallback if node not found
             if (!node) {
                 console.error("Node not found:", nodeId, " Patient Type:", patientType, "History:", historyStack.join(' -> '));
                 node = { title: "Error", type: 'recommendation', content: "<p>Decision point not found. Please start over.</p>" };
             }

             const titleEl = document.getElementById('flow-title');
             const optionsEl = document.getElementById('flow-options');
             const recommendationEl = document.getElementById('flow-recommendation');

             titleEl.textContent = node.title || "Select Option";
             optionsEl.innerHTML = ''; // Clear previous options
             recommendationEl.innerHTML = ''; // Clear previous recommendation
             recommendationEl.style.display = 'none'; // Hide recommendation area initially

             if (node.type === 'question') {
                 if (node.options && node.options.length > 0) {
                     node.options.forEach(option => {
                         const button = document.createElement('button');
                         button.textContent = option.text;
                         button.className = 'option-button bg-gray-100 text-gray-800 p-4 rounded-lg font-medium hover:bg-gray-200 focus:outline-none focus:ring-2 focus:ring-gray-500 focus:ring-offset-2 text-left';
                         button.onclick = () => handleOption(option.nextStep);
                         optionsEl.appendChild(button);
                     });
                 } else {
                     optionsEl.innerHTML = '<p class="text-center text-gray-500">No further options available for this path.</p>';
                 }
             } else if (node.type === 'recommendation') {
                 let contentHTML = node.content || '<p>No specific recommendation details available for this step.</p>';
                 if (node.parentRef) {
                     contentHTML += `<p class="mt-4 text-sm text-gray-500 italic">Source: ${node.parentRef} in guidelines PDF.</p>`;
                 }
                 recommendationEl.innerHTML = contentHTML;
                 recommendationEl.style.display = 'block';
             }

             // Always show the flow step section if we successfully displayed a node
             if (node.title !== "Error") {
                showStep('step-flow');
             }
         }


        // Function to show a specific step section and hide others
        function showStep(stepId) {
            document.querySelectorAll('.step-section').forEach(section => {
                section.classList.remove('active');
            });
            const nextStepEl = document.getElementById(stepId);
            if (nextStepEl) {
                 // Use setTimeout for transition effect
                 setTimeout(() => {
                    nextStepEl.classList.add('active');
                 }, 50);
            }
             // Manage back button visibility
             const backButton = document.getElementById('back-button');
             if (stepId === 'step-patient-type') {
                 backButton.style.display = 'none'; // Hide back button on first step
             } else {
                 backButton.style.display = 'inline-flex'; // Show back button on subsequent steps
             }
        }

        // Handle patient type selection (Step 1)
        function handlePatientType(type) {
             historyStack = ['step-patient-type', type]; // Reset history with patient type
             displayNode('start'); // Display the starting node for this patient type
        }

         // Handle option selection within the flow (Step 2+)
         function handleOption(nextStepId) {
             if (nextStepId) {
                 // Check if the next step exists before pushing to history
                 const patientType = historyStack[1];
                 let nextNode = null;
                  if (guidelines[patientType]?.[nextStepId]) {
                      nextNode = guidelines[patientType][nextStepId];
                  } else if (historyStack.length > 1) { // Need at least patient type and current node ID
                      const currentNodeId = historyStack[historyStack.length-1];
                      // Check if next step is nested under current node (if current is a question node)
                      if (guidelines[patientType]?.[currentNodeId]?.[nextStepId]) {
                         nextNode = guidelines[patientType][currentNodeId][nextStepId];
                      } else if (historyStack.length > 2) { // Check if nested under condition (historyStack[2])
                          const conditionBranch = historyStack[2];
                          if(guidelines[patientType]?.[conditionBranch]?.[nextStepId]){
                              nextNode = guidelines[patientType][conditionBranch][nextStepId];
                          }
                      }
                  }

                 if (nextNode) {
                     historyStack.push(nextStepId); // Add current step to history
                     displayNode(nextStepId);
                 } else {
                     console.error("Next step ID not found:", nextStepId, " Patient Type:", patientType, "History:", historyStack.join(' -> '));
                     // Optionally display an error message to the user
                 }
             }
         }


         // Go back to the previous step/node
         function goBack() {
             if (historyStack.length > 1) {
                 historyStack.pop(); // Remove the current step/node ID
                 const targetNodeId = historyStack[historyStack.length - 1];

                 if (targetNodeId === 'step-patient-type') {
                     showStep('step-patient-type');
                 } else if (historyStack.length === 2 && targetNodeId !== 'start') {
                      // If only patient type remains after pop, display its 'start' node
                     displayNode('start');
                 } else {
                      // Otherwise, display the node ID now at the end of the stack
                     displayNode(targetNodeId);
                 }
             }
         }


        // Reset the application to the first step
        function resetApp() {
            historyStack = ['step-patient-type'];
            showStep('step-patient-type');
        }

        // Initialize the app view
        document.addEventListener('DOMContentLoaded', () => {
             showStep('step-patient-type'); // Show the first step
        });

    </script>

</body>
</html>

