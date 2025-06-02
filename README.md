# Power-Automate-Schedule-Email-with-OneDrive-File-Attachment
Power Automate: Schedule Email with OneDrive File Attachment

# Power Automate: Schedule Email with OneDrive File Attachment

## Objective
This guide outlines the steps to create an automated scheduled email using Power Automate that sends a specific OneDrive file to a designated recipient every hour.

---

## Pre-requisites
- Access to Microsoft Power Automate: [https://make.powerautomate.com](https://make.powerautomate.com)  
- OneDrive for Business with the target file stored  
- Access to Office 365 Outlook  
- Recipient email address  

---

## Step-by-Step Instructions

### 1. Log In to Power Automate
Go to [https://make.powerautomate.com](https://make.powerautomate.com) and sign in with your organizational account.

---

### 2. Create a Scheduled Flow
- Click **+ Create** in the left navigation.
- Select **Scheduled cloud flow**.
- Enter a **Flow name**, e.g., `Hourly Daily Work Update`.
- Set start time:
  - **Date**: 6/2/2025  
  - **Time**: 9:00 AM
- Set the recurrence to **Every 1 hour**.
- Click **Create**.

---

### 3. Configure the Recurrence Trigger
Once the flow is created, a **Recurrence** trigger appears automatically.

---

### 4. Get File Content from OneDrive
- Click **+ New step**.
- Search `Get file content`.
- Choose the **OneDrive for Business** version.
- Select the file using the folder icon.
  - Example path: `/Send Daily Excel Report/Send Daily Excel Report.xlsx`
- Leave **Options** blank under *Advanced Parameters*.
- Set **Infer Content Type** to `Yes`.

---

### 5. Send Email with Attachment
- Click **+ New step**.
- Search `Send an email (V2)` under **Office 365 Outlook**.
- Configure email:
  - **To**: recipient’s email
  - **Subject**: `Hourly Daily Work Update`
  - **Body**: add message text
- Expand **Advanced options**:
  - **Attachment Name**: `Hourly Daily Work Update Excel File.xlsx`
  - **Attachment Content**: dynamic file content from previous step

---

### 6. Save and Test the Flow
- Click **Save**
- Click **Test** → select **Manually** → click **Run Flow**
- Look for **Success** message
- Check recipient email for the message

---

### 7. Completion and Verification
- After success, you’ll see a green **checkmark** next to your flow on the dashboard.

---

## Conclusion
Your Power Automate flow is now live and will send scheduled emails with the desired OneDrive file attached. You can modify the logic as needed.

---

## Next Steps
- Test with different files
- Explore more Power Automate triggers and actions
- Consider approval steps or dynamic conditions

---

**Thank you!**  
*Keep automating to save time and improve efficiency.*
