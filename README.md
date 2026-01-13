# Gmail & Google Sheets Integration System 📧

A robust automation solution designed to streamline email management by seamlessly connecting **Gmail** with **Google Sheets** through **Google Apps Script**. This system enables users to centralize email tracking, organization, and automated response handling within a spreadsheet interface.

---

## **Overview**

This integration tool provides a comprehensive workflow for managing email communications directly from Google Sheets. By leveraging the power of Google Apps Script, it eliminates repetitive manual tasks and creates a unified dashboard for email operations.

### **Key Capabilities**

- **Automated Email Synchronization**: Retrieves and displays the most recent 10 emails from your Gmail inbox, populating structured data fields including message ID, subject line, sender information, and current status
- **Streamlined Response Management**:  Enables direct email replies through the spreadsheet interface by simply filling in the designated response column
- **Intelligent Send Control**: Implements status tracking to prevent duplicate responses and maintain communication integrity
- **Custom Spreadsheet Menu**: Integrates intuitive menu commands directly into Google Sheets: 
  - **Sync Emails**: Refreshes the spreadsheet with latest Gmail data
  - **Send Responses**: Processes and dispatches prepared replies with automatic status updates

---

## **System Workflow**

### **1. Email Synchronization Process**
Access the custom menu and select "Sync Emails" to import your latest Gmail messages.  The system automatically extracts relevant metadata and populates the spreadsheet with organized, actionable information.

### **2. Composing Responses**
Navigate to the **Response** column and enter your reply message for any email that has not been marked as **Responded**. Each row represents an individual email thread ready for engagement.

### **3. Dispatching Replies**
Select "Send Responses" from the custom menu to execute the send operation. The system will:
- Transmit all prepared responses to their respective recipients
- Update the status field to **Responded**
- Record the timestamp of each sent message

---

## **Critical Configuration:  V8 Runtime Requirement**

**⚠️ Important**:  This project requires the V8 JavaScript runtime engine in Google Apps Script for proper execution. 

### **Enabling V8 Runtime**
1. Navigate to your Google Sheet and open the Apps Script editor:  **Extensions → Apps Script**
2. In the left sidebar, select **Project Settings**
3. Locate the **Google Apps Script runtime** section
4. Enable **Chrome V8 runtime**
5. Save your configuration before running any scripts

> **Note**: The V8 engine is necessary to support modern JavaScript (ES6+) features used throughout this codebase.  Without it, the script will not execute correctly.

---

## **Technology Stack**

- **Google Workspace APIs**:  Provides native integration between Gmail and Sheets platforms
- **Google Apps Script**: Server-side JavaScript runtime environment for automation logic
- **Modern JavaScript (ES6+)**: Implements object-oriented programming patterns for maintainable, scalable code architecture

---

## **Spreadsheet Schema**

The automated system generates a structured data table with the following columns: 

| Column | Description |
|--------|-------------|
| **ID** | Unique message identifier from Gmail |
| **Subject** | Email subject line |
| **Sender** | Original sender's email address |
| **Recipient** | Destination email address |
| **Snippet** | Preview excerpt from email body |
| **Response** | User-inputted reply message |
| **Date** | Timestamp of email receipt |
| **Status** | Current state (Read/Responded) |
| **Response Date** | Timestamp of reply transmission |

---

## **Implementation Guide**

### **Step-by-Step Setup**

1. Create or open a Google Sheets document
2. Access the script editor: **Extensions → Apps Script**
3. Verify V8 runtime is enabled (see Configuration section above)
4. Paste the provided source code into the editor
5. Save the project with a descriptive name
6. Refresh your spreadsheet to activate the custom menu
7. Grant necessary permissions when prompted
8. Begin using the automation features via the custom menu

---

## **Quick Start Template**

To accelerate your setup process, a pre-configured spreadsheet template is available for immediate use. 

📥 **[Access Template Spreadsheet](https://bit.ly/planilhaemailresponder)**

This template includes pre-formatted columns and is optimized for seamless integration with the automation script.

---

## **Best Practices**

- **Review before sending**: Always verify response content before executing the send command
- **Regular synchronization**: Periodically sync emails to maintain up-to-date information
- **Status monitoring**: Check the status column to track communication history
- **Backup data**: Maintain periodic backups of your spreadsheet for data safety

---

## **Support & Contributions**

For questions, issues, or enhancement suggestions, please engage through the appropriate channels.  Contributions that improve functionality, documentation, or user experience are welcomed. 

---

**Built with ❤️ using Google Workspace automation tools**
