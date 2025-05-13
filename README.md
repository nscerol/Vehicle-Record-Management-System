# PHPGurukul-Vehicle-Record-Management-System 1.0

Welcome to the PHPGurukul Vehicle Record Management System 1.0 repository. This project aims to provide efficient inventory management.

## Security Vulnerabilities

### CVE-2025-44180

- **Description:** Stored Cross-Site Scripting (XSS) vulnerability via `edit-brand.php`, 'brandname' parameter.
- **Affected Version:** 1.0
- **Affected File:** `/vehiclerecordsystem/admin/edit-brand.php`
- **Vulnerable Parameter:** 'brandname'
- **Impact:** Attackers can inject and execute malicious scripts via the 'brandname' parameter.
- **Solution:** Implement proper input validation and output encoding for the 'brandname' parameter in `/vehiclerecordsystem/admin/edit-brand.php`.

### CVE-2025-44181

- **Description:** Stored Cross-Site Scripting (XSS) vulnerability via `add-brand.php`, 'brandname' parameter.
- **Affected Version:** 1.0
- **Affected File:** `/vehiclerecordsystem/admin/add-brand.php`
- **Vulnerable Parameter:** 'brandname'
- **Impact:** Attackers can inject and execute malicious scripts via the 'brandname' parameter.
- **Solution:** Implement proper input validation and output encoding for the 'brandname' parameter in `/vehiclerecordsystem/admin/add-brand.php`.

### CVE-2025-44182

- **Description:** Stored Cross-Site Scripting (XSS) vulnerability via `edit-vehicle.php`, 'vehiclename, modelnumber, regnumber, vehiclesubtype, chasisnum, enginenumber' parameters.
- **Affected Version:** 1.0
- **Affected File:** `/vehiclerecordsystem/admin/edit-vehicle.php`
- **Vulnerable Parameters:** 'vehiclename, modelnumber, regnumber, vehiclesubtype, chasisnum, enginenumber'
- **Impact:** Attackers can inject and execute malicious scripts via the 'vehiclename, modelnumber, regnumber, vehiclesubtype, chasisnum, enginenumber' parameters.
- **Solution:** Implement proper input validation and output encoding for the 'vehiclename, modelnumber, regnumber, vehiclesubtype, chasisnum, enginenumber' parameters in `/vehiclerecordsystem/admin/edit-vehicle.php`.

### CVE-2025-44183

- **Description:** Stored Cross-Site Scripting (XSS) vulnerability via `profile.php`, 'name, email, and mobile' parameters.
- **Affected Version:** 1.0
- **Affected File:** `/vehiclerecordsystem/admin/profile.php`
- **Vulnerable Parameters:** 'name, email, and mobile'
- **Impact:** Attackers can inject and execute malicious scripts via the 'name, email, and mobile' parameters.
- **Solution:** Implement proper input validation and output encoding for the 'name, email, and mobile' parameters in `/vehiclerecordsystem/admin/profile.php`.

---
