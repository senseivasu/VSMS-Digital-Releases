# VSMS Digital Releases 

This repository hosts public release APKs for VSMS Digital. The source code is maintained in a separate private repository.

## 📥 Download Latest Release

- 📱 **[VSMS_Digital_v1.3.1_release.apk](VSMS_Digital_v1.3.1_release.apk)**: Production package optimized for Android devices.

---

## 📝 Release Changelog

### v1.3.1 (Current Release)
- **Custom DOB Change Confirmation Modal**: Replaced standard browser confirm boxes with a custom React modal when patient DOB is updated. Offers a clear three-way decision:
  1. *Keep Existing Data & Recalculate*: Updates DOB/Age but retains patient name, demographics, and checked items.
  2. *Clear Data & Start Fresh*: Resets demographics and clears checklist scores.
  3. *Cancel Change*: Reverts the DOB change to the original date.
- **Clinical Disability Reference Table**: Added a high-density disability classification chart (Borderline, Mild, Moderate, Severe, Profound) on the Reports page.
  * Sticky on the desktop report sidebar.
  * Hidden behind a mobile draggable Floating Action Button (FAB) and revealed via a bottom-sheet modal.
  * Completely excluded from PDF exports and print layouts.
- **WebView Selection Handle Outline Suppressed**: Added a global CSS reset to eliminate the square focus outline artifact around native Android WebView text selection handle teardrops.
- **Design Synchronization (RorschachPro)**: Synchronized header card size (`h-20`), logo positioning, and centered tabs menu alignments.

### v1.3.0
- Intermediate local development updates and clinical metrics syncing.

### v1.2.2
- Initial clinical reference manual integration and UI refinements.
