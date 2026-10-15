# VSMS Digital Releases 

This repository hosts public release APKs for VSMS Digital. The source code is maintained in a separate private repository.

## 📥 Download Latest Release

- 📱 **[VSMS_Digital_v1.4.0_debug.apk](VSMS_Digital_v1.4.0_debug.apk)**: Recommended installation package for Android devices.
- 📱 **[VSMS_Digital_v1.4.0_release.apk](VSMS_Digital_v1.4.0_release.apk)**: Production package for Android devices.

---

## 📝 Release Changelog

### v1.4.0 (Current Release)
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
