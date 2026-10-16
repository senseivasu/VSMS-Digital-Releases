# VSMS Digital Releases 

This repository hosts public release APKs for VSMS Digital. The source code is maintained in a separate private repository.

## 📥 Download Latest Release

- 📱 **[VSMS_Digital_v1.5.2_debug.apk](VSMS_Digital_v1.5.2_debug.apk)**: Recommended installation package for Android devices.
- 📱 **[VSMS_Digital_v1.5.2_release.apk](VSMS_Digital_v1.5.2_release.apk)**: Production package for Android devices.

---

## 📝 Release Changelog

### v1.5.2 (Current Release)
- **Eliminated Duplicate Assessment Saves**: Serialized file storage operations via an atomic sequential execution queue (`runExclusive`) to eliminate race conditions between concurrent saves and disk I/O.
- **Smart Patient Identity Matching & Idempotency**: Automatically matches existing records by MRD or Name + DOB + DOA to update records in place rather than creating duplicates, treating identical re-saves as idempotent no-ops.
- **Session Persistence**: Stored `activeRecordId` in local storage (`vsms_active_record_id`) ensuring patient sessions remain linked across browser refreshes and app reloads.
- **Controlled Action-Driven Page Navigation**: Restricted progression between Demographics, Checklist, and Report strictly to on-page buttons (Next, Generate Report, Back), converting top step tabs to visual-only progress indicators and disabling swipe/arrow jumping.
- **Deterministic Save Triggers**: Automatically saves demographic drafts on "Next: Checklist" and full assessment scores on "Generate Report".
- **Interactive Unsaved Edits Toast**: Prompts clinicians when "Generate Report" is clicked on a modified record with options to "Save & View Report" or "View Report Only".
- **Export & PDF Debouncing**: Added in-flight locks to PDF generation and JSON export buttons to eliminate duplicate file downloads on rapid multi-clicks.

### v1.5.0
- **Native Google Authentication**: Integrated `@capawesome/capacitor-google-sign-in` utilizing Android Credential Manager for 1-tap Google login.
- **Mandatory Clinician Sign-In Gate**: Implemented `LoginGate.jsx` clinician authentication gate while keeping the existing hardware `ALLOWED_DEVICE_IDS` check fully enforced.
- **Access Restriction via Test Users**: Enforced access control via Google Cloud Console OAuth Test Users whitelist with dedicated in-app authorization dialogs.
- **Automated Google Drive Sync**: Patient assessments are automatically backed up and synchronized to each clinician's private Google Drive `appDataFolder` (`vsms_assessments_data.json`) with silent background token refresh.
- **Clinician Identity Synchronization**: Automatically pre-populates default practitioner name from the signed-in Google account profile.

### v1.4.1
- **Manual Referral Entry & Search**: Added a searchable dropdown with custom referral source entry to Demographics, allowing clinicians to select presets or add custom doctors/sources with local and Google Drive cloud persistence.
- **Dynamic Assessment Locations**: Purged prefilled default locations, retaining only custom entered clinics/centres with native device file storage and Google Drive cloud synchronization.
- **Terminology Standardization**: Replaced clinician designations with "Clinical Psychologist" across Demographics, Saved Assessments table, and Clinical Reports.
- **Report Signature**: Standardized the signature field on reports to "Clinician's Signature".

### v1.4.0
- **Tabulated Database View**: Replaced card grid on the Saved Assessments page with a full-width responsive clinical data table.
- **Direct Record Editing**: Introduced per-row Edit action that loads assessment data into the active Demographics and Checklist workflow, recalculates results automatically, and updates the saved record upon Save.
- **Interactive Table Sorting**: Added interactive sorting across all data columns (MRD ID, Patient Name, Age, Sex, Date of Assessment, Clinical Psychologist, SQ Score) with visual direction indicators.
- **Inline Delete Confirmation**: Embedded warning and confirmation controls directly within table rows to avoid modal interruptions.
- **Age Presentation**: Displayed age in years only (`X yrs`) for clean clinical scannability while preserving accurate chronological total-month numerical sorting.
- **Simplified Database Header**: Replaced the 3-tier dark-gradient hero banner with a clean, clinical header card containing quick-action buttons and live counter badges.
- **Separated Age & Sex**: De-coupled combined age/sex data into individual dedicated columns for clearer tabulation.

### v1.3.1
- **Custom DOB Change Confirmation Modal**: Replaced standard browser confirm boxes with a custom React modal when patient DOB is updated. Offers a clear three-way decision:
  1. *Keep Existing Data & Recalculate*: Updates DOB/Age but retains patient name, demographics, and checked items.
  2. *Clear Data & Start Fresh*: Resets demographics and clears checklist scores.
  3. *Cancel Change*: Reverts the DOB change to the original date.
- **Clinical Disability Reference Table**: Added a high-density disability classification chart on the Reports page.
- **WebView Selection Handle Outline Suppressed**: Added a global CSS reset to eliminate the square focus outline artifact around native Android WebView text selection handle teardrops.
- **Design Synchronization (RorschachPro)**: Synchronized header card size (`h-20`), logo positioning, and centered tabs menu alignments.

### v1.3.0
- Intermediate local development updates and clinical metrics syncing.

### v1.2.2
- Initial clinical reference manual integration and UI refinements.
