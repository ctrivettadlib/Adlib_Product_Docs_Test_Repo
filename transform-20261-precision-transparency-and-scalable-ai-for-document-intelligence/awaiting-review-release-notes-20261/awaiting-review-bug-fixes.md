# AWAITING REVIEW Bug Fixes

Transform 2026.1 resolves issues related to HPE processing, connector visibility, and PDF viewer rendering. These fixes improve processing consistency, reduce configuration confusion, and strengthen the reliability of document review workflows.

This release focuses on ensuring that jobs follow the expected processing path, that validation settings are enforced correctly, that legacy connector options are handled consistently, and that high-resolution documents render reliably in the Human-in-the-Loop viewer.

# **HPE Job Ticket Processing Issue**

### **Why this fix matters**

Jobs using specific job ticket configurations were incorrectly routed to legacy processing.

### **Resolution**

- Corrected handling to ensure jobs are processed using HPE as expected

### **Background**

Jobs with `MERGE="No"` were not processed correctly under HPE and defaulted to legacy routing.

# **Font Validation Handling in HPE**

### **Why this fix matters**

Font validation settings were not respected during processing.

### **Resolution**

- Corrected behavior for `CANCELONMISSINGFONTS` setting

### **Background**

Font validation rules were not properly enforced under HPE processing.

# **Exchange Connector Visibility**

### **Why this fix matters**

Legacy Exchange connector visibility created confusion after the new connector introduction.

### **Resolution**

- Legacy Exchange source hidden by default

### **Background**

The new Exchange Online connector replaces the legacy connector and is now the default.

# **PDF Viewer Rendering Issue**

## **Why this fix matters**

High-resolution images previously rendered incorrectly in the Human-in-the-Loop viewer.

## **Resolution**

- Syncfusion PDF viewer upgraded
- Rendering issues resolved for high-resolution images

## **Background**

This fix improves reliability during document review and data validation.